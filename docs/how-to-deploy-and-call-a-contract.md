---
sidebar_position: 5
---

# How to Deploy & Call a Contract


## Introduction

After you've finished writing a contract, you want to deploy and call it. But first, you should learn how the a smart contract interacts with the blockchain.

As explained in the [Overview section](./overview.md), a `scryptTS` contract is based on the Bitcoin UTXO model. A **constract instance** is an abstraction that represents a specific contract deployed on-chain, so you can use it to interact with the contract like a normal TypeScript object. In this section, we will go over some fundamental concepts in details.


### Tx Builders

To deploy or interact with contracts, we must build transactions and broadcast them to Bitcoin.
We have some built-in tx builders for the most common way to interact with contracts, so usually you don't have to implement them. If the default tx builder does not meet your specific requirements, such as having extra inputs or outputs in your tx, you can [customize it](./how-to-customize-a-contract-tx.md).


#### Contract Deployment Transaction

A Bitcoin transaction is required when deploying a contract to the blockchain. The transaction should have an output, whose script is compiled from the contract. This output is known as a contract UTXO and we regard the contract instance comes `from` this UTXO.

An instance's `from` can be accessed.
```ts
// the tx that contains the instance
instance.from.tx
// the index of the tx output that contains the instance
instance.from.outputIndex
```

#### Contract Call Transaction

When you call a public method of a contract instance in a UTXO, a call transaction is needed. The transaction has an input that references to the UTXO and contains the script consisted of the method's arguments. We regard the contract instance goes `to` this transaction input.

An instance's `to` can be accessed.
```ts
// the tx that spends the instance
instance.to.tx
// the index of the tx input that spends the UTXO the instance is in
instance.to.inputIndex
```


This section could be summarized as the diagram below:

![](../static/img/contract_tx.svg)


## Prepare a Signer and Provider

As we mentioned in the [testing section](./how-to-test-a-contract.md), a signer and a provider should be connected to a contract before deployment and call. 


For local testing, we can use the `TestWallet` introduced [before](./how-to-test-a-contract#testwallet), with a mock provider. When we are ready to deploy the contract to the testnet/mainnet, we need a real provider like [DefaultProvider](./how-to-test-a-contract.md#provider).

```ts
const network = bsv.Networks.testnet; // or bsv.Networks.mainnet
const signer = new TestWallet(privateKey, new DefaultProvider(network));
```

Don't forget to connect the signer to the contract instance as well:

```ts
await instance.connect(signer);
```

## Contract Deployment

To deploy a smart contract, simply call its `deploy` method:


```ts
// construct a new instance of `MyContract`
let instance = new MyContract(...initArgs);

// connect the signer to the instance
await instance.connect(signer);

// the contract UTXO’s satoshis
const initBalance = 1234;

// build and send tx for deployment
const deployTx = await instance.deploy(initBalance);
console.log(`Smart contract successfully deployed with txid ${tx.id}`);
```

## Contract Call

Similar to what we described in [this section](./how-to-test-a-contract#call-a-public-method), you can call a contract's public `@method` on the blockchain as follows:

```ts
// build and send tx for calling `foo`
const { tx, atInputIndex } = await instance.methods.foo(arg1, arg2, opts);
console.log(`Smart contract method successfully called with txid ${tx.id}`);
```

The major differences between here and local tests are:
1. the contract needs to be depoyed first;
2. the contract instance is connected to a real provider, which broadcasts transactions to the blockchain.

### Create a smart contract instance from a transaction
To interact with a deployed smart contract (i.e., calling its public methods), we need its contract instance corresponding to its latest state on chain, stateful or not. When testing on testnet, we usually put a contract's deployment and its calling (note there could be multiple calls if the contract is stateful) in the same process for convenience, so that we don't need to manage the internal state of the instance manually, because it's always consistent with the transactions on chain.

The [following code](https://github.com/sCrypt-Inc/scryptTS-examples/blob/master/tests/testnet/counter.ts) tests the stateful contract [Counter](./how-to-write-a-contract/stateful-contract.md#create-a-stateful-contract). `currentInstance` always points to the latest instance.
```ts
const counter = new Counter(0n)

await counter.connect(getDefaultSigner())

// deploy the contract first
const deployTx = await counter.deploy(1)
console.log('Counter deploy tx:', deployTx.id)

// then call the contract by reusing the same instance `counter`
let currentInstance = counter

// call the method of current instance to apply the updates on chain
for (let i = 0; i < 3; ++i) {
    // avoid mempool conflicts, sleep to allow previous tx "sink-into" the network
    await sleep(2)

    // create the next instance from the current
    const nextInstance = currentInstance.next()

    // apply updates on the next instance off chain
    nextInstance.increment()

    // call the method of current instance to apply the updates on chain
    const { tx: tx_i } = await currentInstance.methods.incrementOnChain({
        next: {
            instance: nextInstance,
            balance,
        },
    } as MethodCallOptions<Counter>)

    console.log(
        `Counter call tx: ${tx_i.id}, count updated to: ${nextInstance.count}`
    )

    // update the current instance reference
    currentInstance = nextInstance
}

```

In reality, a contract's deployment and its call, and its different calls in the case of a stateful contract, may well be in separate processes. For example, the deployment party is different from the calling party, or multiple parties call it. If so, we need to create a contract instance from an on-chain transaction that represents its latest state, before we can call its method.

We can do so in two steps:
1. `new` an instance using the same constructor arguments as when deploying the contract
2. call `syncState()` to synchronize the state of the contract instance from the transaction.

```ts
// step 1
const counter = new Counter(0n)
// step 2: the latest counter is at the given output of `tx`
instance.syncState(tx, atOutputIndex)

// we're good here, the `instance` is now in sync with the on-chain transaction
```

Let's look at a more complex example.

### Method with Signatures

A contract public `@method` often needs a signature argument for authentication. Take this [Pay To Pubkey Hash (P2PKH)](https://learnmeabitcoin.com/technical/p2pkh) contract for example:

```ts
export class P2PKH extends SmartContract {
    @prop()
    readonly pubKeyHash: PubKeyHash;

    constructor(pubKeyHash: PubKeyHash) {
        super(pubKeyHash);
        this.pubKeyHash = pubKeyHash;
    }

    @method()
    public unlock(sig: Sig, pubkey: PubKey) {
        // make sure the `pubkey` is the one locked with its hash value in the constructor
        assert(hash160(pubkey) == this.pubKeyHash, 'pubKeyHash check failed');

	   // make sure the `sig` is signed by the private key corresponding to the `pubkey`
        assert(this.checkSig(sig, pubkey), 'signature check failed');
    }
}
```

We can call the `unlock` method like this:

```ts
// call
const { tx: callTx } = await p2pkh.methods.unlock(
    // the first argument `sig` is replaced by a callback function which will return the needed signature
    (sigResps) => findSig(sigResps, publicKey),

    // the second argument is still the value of `pubkey`
    PubKey(toHex(publicKey)),

    // method call options
    {
        // A request for signer to sign with the private key corresponding to a public key
        pubKeyOrAddrToSign: publicKey
    } as MethodCallOptions<P2PKH>
);

console.log('contract called: ', callTx.id);

```

When `p2phk.method.unlock` is called, the option contains `pubKeyOrAddrToSign`, requesting a signature against `publicKey`.

The first argument is a signature, which can be obtained in a callback function. The function takes a list of signatures requested in `pubKeyOrAddrToSign` and find the one signature to the right public key/address.

In general, if your `@method` needs `Sig`-typed arguments, you could obtain them as follows:

1. Ensure that the `pubKeyOrAddrToSign` contains all public keys/addresses corresponding to these `Sig`s;

2. Replace each `Sig` argument with a callback function that filters to the right `Sig` from the full list of signature in `sigResps`.


## Example

Here is the complete sample code for the deployment and call of a P2PKH contract.

```ts
import { privateKey } from '../../utils/privateKey';

// compile contract
await P2PKH.compile()

// public key of the `privateKey`
const publicKey = privateKey.publicKey
// hash of the `publicKey`
const pkh = bsv.crypto.Hash.sha256ripemd160(publicKey.toBuffer())

// setup signer
const signer = new TestWallet(privateKey, new DefaultProvider());

// initialize an instance with `pkh`
let p2pkh = new P2PKH(PubKeyHash(toHex(pkh)))

// connect the signer
await p2pkh.connect(signer);

// deploy the contract, with 1 satoshi locked in
const deployTx = await p2pkh.deploy(1);
console.log('contract deployed: ', deployTx.id);

// call
const { tx: callTx } = await p2pkh.methods.unlock(
    (sigResps) => findSig(sigResps, publicKey),
    PubKey(toHex(publicKey)),
    {
        pubKeyOrAddrToSign: publicKey
    } as MethodCallOptions<P2PKH>
);

console.log('contract called: ', callTx.id);

```

More examples can be found [here](https://github.com/sCrypt-Inc/scryptTS-examples/tree/master/tests/testnet).


### Running the code

The deployment and call code is wrapped into a simple NPM command:

```sh
npm run testnet
```

Make sure you fund your address before running this command.
After a successful run you should see something like the following:

```
Demo contract deployed:  f3f372aa25f159efa93db8c51a4eabbb15935358417ffbe91bfb78f4f0b1d2a3
Demo contract called:  dc53da3e80aadcdefdedbeb6367bb8552e381e92b226ab1dc3dc9b3325d8a8ee
```

These are the TXIDs of the transaction which deployed the smart contract and then the one which called its method. You can see the transactions using a [block explorer](https://test.whatsonchain.com/tx/f3f372aa25f159efa93db8c51a4eabbb15935358417ffbe91bfb78f4f0b1d2a3).


### Customize Transactions
Deploying and calling a contract builds transactions with a certain format, which suffices for many cases. In cases where the tx format does not work for you and you need to customize it, please refer to [this section](./how-to-customize-a-contract-tx.md).