scrypt-ts

# scrypt-ts

## Table of contents

### Namespaces

- [bsv](modules/bsv.md)

### Enumerations

- [ProviderEvent](enums/ProviderEvent.md)

### Other Classes

- [FunctionCall](classes/FunctionCall.md)
- [HashedMap](classes/HashedMap.md)
- [HashedSet](classes/HashedSet.md)
- [Provider](classes/Provider.md)
- [SensiletSigner](classes/SensiletSigner.md)
- [Signer](classes/Signer.md)
- [TestWallet](classes/TestWallet.md)
- [WhatsonchainProvider](classes/WhatsonchainProvider.md)

### SmartContract Classes

- [SmartContract](classes/SmartContract.md)
- [SmartContractLib](classes/SmartContractLib.md)

### Standard Contracts Classes

- [Constants](classes/Constants.md)
- [OpCode](classes/OpCode.md)
- [SigHash](classes/SigHash.md)
- [Tx](classes/Tx.md)
- [Utils](classes/Utils.md)
- [VarIntReader](classes/VarIntReader.md)
- [VarIntWriter](classes/VarIntWriter.md)

### Interfaces

- [ContractArtifact](interfaces/ContractArtifact.md)
- [Range](interfaces/Range.md)
- [SignTransactionOptions](interfaces/SignTransactionOptions.md)
- [SignatureRequest](interfaces/SignatureRequest.md)
- [SignatureResponse](interfaces/SignatureResponse.md)
- [TransactionResponse](interfaces/TransactionResponse.md)
- [TxContext](interfaces/TxContext.md)
- [TxInputRef](interfaces/TxInputRef.md)
- [TxOutputRef](interfaces/TxOutputRef.md)
- [VerifyResult](interfaces/VerifyResult.md)

### Array Type Aliases

- [FixedArray](README.md#fixedarray)

### Other Type Aliases

- [AddressOption](README.md#addressoption)
- [AddressesOption](README.md#addressesoption)
- [ByteString](README.md#bytestring)
- [Network](README.md#network)
- [OpCodeType](README.md#opcodetype)
- [PrivKey](README.md#privkey)
- [PubKey](README.md#pubkey)
- [PubKeyHash](README.md#pubkeyhash)
- [Ripemd160](README.md#ripemd160)
- [Sha1](README.md#sha1)
- [Sha256](README.md#sha256)
- [Sig](README.md#sig)
- [SigHashPreimage](README.md#sighashpreimage)
- [SigHashType](README.md#sighashtype)
- [SignerError](README.md#signererror)
- [SortedItem](README.md#sorteditem)
- [SubBytes](README.md#subbytes)
- [TxHash](README.md#txhash)
- [UTXO](README.md#utxo)

### Types Type Aliases

- [auto](README.md#auto)

### Bytes Operations Functions

- [byteString2Int](README.md#bytestring2int)
- [int2ByteString](README.md#int2bytestring)
- [len](README.md#len)
- [reverseByteString](README.md#reversebytestring)

### Hashing Functions

- [hash160](README.md#hash160)
- [hash256](README.md#hash256)
- [ripemd160](README.md#ripemd160-2)
- [sha1](README.md#sha1-2)
- [sha256](README.md#sha256-2)

### Math Functions

- [abs](README.md#abs)
- [max](README.md#max)
- [min](README.md#min)
- [within](README.md#within)

### Other Functions

- [OpCodeType](README.md#opcodetype-1)
- [PrivKey](README.md#privkey-1)
- [PubKey](README.md#pubkey-1)
- [PubKeyHash](README.md#pubkeyhash-1)
- [Ripemd160](README.md#ripemd160-1)
- [Sha1](README.md#sha1-1)
- [Sha256](README.md#sha256-1)
- [Sig](README.md#sig-1)
- [SigHashPreimage](README.md#sighashpreimage-1)
- [SigHashType](README.md#sighashtype-1)
- [addressesToList](README.md#addressestolist)
- [and](README.md#and)
- [buildOpreturnScript](README.md#buildopreturnscript)
- [buildPublicKeyHashScript](README.md#buildpublickeyhashscript)
- [equals](README.md#equals)
- [getBuildInType](README.md#getbuildintype)
- [getDummyP2pkhUTXOs](README.md#getdummyp2pkhutxos)
- [getPreimage](README.md#getpreimage)
- [getRandomAddress](README.md#getrandomaddress)
- [getSortedItem](README.md#getsorteditem)
- [hasModifier](README.md#hasmodifier)
- [invert](README.md#invert)
- [isNumberLiteralExpr](README.md#isnumberliteralexpr)
- [number2hex](README.md#number2hex)
- [or](README.md#or)
- [signTx](README.md#signtx)
- [toByteString](README.md#tobytestring)
- [toHex](README.md#tohex)
- [utxoFromOutput](README.md#utxofromoutput)
- [xor](README.md#xor)

### Signature Verification Functions

- [checkMultiSig](README.md#checkmultisig)

### assert Functions

- [assert](README.md#assert)

### bitshift Functions

- [lshift](README.md#lshift)
- [pow2](README.md#pow2)
- [rshift](README.md#rshift)

### decorator Functions

- [method](README.md#method)
- [prop](README.md#prop)

### exit() Functions

- [exit](README.md#exit)

## Array Type Aliases

### FixedArray

Ƭ **FixedArray**<`T`, `N`\>: `N` extends `N` ? `number` extends `N` ? `T`[] : `_TupleOf`<`T`, `N`, []\> : `never`

An array is a fixed-size list of values of the same basic type.
When you declare an array you have to declare it like this:

**`Example`**

```ts
let aaa: FixedArray<bigint, 3> = [1n, 3n, 3n];

let abb: FixedArray<FixedArray<bigint, 2>, 3> = [[1n, 3n], [1n, 3n], [1n, 3n]];

let bbb: FixedArray<FixedArray<FixedArray<bigint, 1>, 2>, 3> = [[[1n], [1n]], [[1n], [1n]], [[1n], [1n]]];
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `T` |
| `N` | extends `number` |

#### Defined in

[src/smart-contract/builtins/types.ts:69](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/types.ts#L69)

___

## Other Type Aliases

### AddressOption

Ƭ **AddressOption**: [`Address`](classes/bsv.Address.md) \| `string`

#### Defined in

[src/bsv/types.ts:7](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/types.ts#L7)

___

### AddressesOption

Ƭ **AddressesOption**: [`AddressOption`](README.md#addressoption) \| [`AddressOption`](README.md#addressoption)[]

#### Defined in

[src/bsv/types.ts:9](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/types.ts#L9)

___

### ByteString

Ƭ **ByteString**: `Bytes`

#### Defined in

[src/smart-contract/builtins/types.ts:31](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/types.ts#L31)

___

### Network

Ƭ **Network**: [`Network`](interfaces/bsv.Networks.Network.md)

#### Defined in

[src/bsv/types.ts:5](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/types.ts#L5)

___

### OpCodeType

Ƭ **OpCodeType**: `Bytes` & { `__type`: ``"OpCodeType"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:88

node_modules/scryptlib/dist/scryptTypes.d.ts:61

___

### PrivKey

Ƭ **PrivKey**: `Int` & { `__type`: ``"PrivKey"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:69

node_modules/scryptlib/dist/scryptTypes.d.ts:36

___

### PubKey

Ƭ **PubKey**: `Bytes` & { `__type`: ``"PubKey"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:70

node_modules/scryptlib/dist/scryptTypes.d.ts:39

___

### PubKeyHash

Ƭ **PubKeyHash**: [`Ripemd160`](README.md#ripemd160)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:73

node_modules/scryptlib/dist/scryptTypes.d.ts:48

___

### Ripemd160

Ƭ **Ripemd160**: `Bytes` & { `__type`: ``"Ripemd160"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:72

node_modules/scryptlib/dist/scryptTypes.d.ts:45

___

### Sha1

Ƭ **Sha1**: `Bytes` & { `__type`: ``"Sha1"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:74

node_modules/scryptlib/dist/scryptTypes.d.ts:49

___

### Sha256

Ƭ **Sha256**: `Bytes` & { `__type`: ``"Sha256"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:75

node_modules/scryptlib/dist/scryptTypes.d.ts:52

___

### Sig

Ƭ **Sig**: `Bytes` & { `__type`: ``"Sig"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:71

node_modules/scryptlib/dist/scryptTypes.d.ts:42

___

### SigHashPreimage

Ƭ **SigHashPreimage**: `Bytes` & { `__type`: ``"SigHashPreimage"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:87

node_modules/scryptlib/dist/scryptTypes.d.ts:58

___

### SigHashType

Ƭ **SigHashType**: `Bytes` & { `__type`: ``"SigHashType"``  }

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:86

node_modules/scryptlib/dist/scryptTypes.d.ts:55

___

### SignerError

Ƭ **SignerError**: `ProviderError`

#### Defined in

[src/bsv/abstract-signer.ts:47](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/abstract-signer.ts#L47)

___

### SortedItem

Ƭ **SortedItem**<`T`\>: `Object`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Type declaration

| Name | Type |
| :------ | :------ |
| `idx` | `bigint` |
| `item` | `T` |

#### Defined in

[src/smart-contract/builtins/types.ts:468](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/types.ts#L468)

___

### SubBytes

Ƭ **SubBytes**: [`PubKey`](README.md#pubkey) \| [`Sig`](README.md#sig) \| [`Sha256`](README.md#sha256) \| [`Sha1`](README.md#sha1) \| [`SigHashType`](README.md#sighashtype) \| [`Ripemd160`](README.md#ripemd160) \| [`OpCodeType`](README.md#opcodetype)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:95

___

### TxHash

Ƭ **TxHash**: `string`

#### Defined in

[src/bsv/abstract-provider.ts:7](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/abstract-provider.ts#L7)

___

### UTXO

Ƭ **UTXO**: [`IUnspentOutput`](interfaces/bsv.Transaction.IUnspentOutput.md)

#### Defined in

[src/bsv/types.ts:3](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/types.ts#L3)

___

## Types Type Aliases

### auto

Ƭ **auto**: `any`

The auto keyword specifies that the type of the variable, of basic type, declared will be automatically deducted from its initializer.

#### Defined in

[src/smart-contract/builtins/types.ts:52](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/types.ts#L52)

## Bytes Operations Functions

### byteString2Int

▸ **byteString2Int**(`a`): `bigint`

ByteString can be converted to bigint using function byteString2Int.

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `Bytes` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:30](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L30)

___

### int2ByteString

▸ **int2ByteString**(`n`, `size?`): [`ByteString`](README.md#bytestring)

bigint can be converted to string with int2ByteString.
If `size` is not passed, the number `n` is converted to a ByteString with as few bytes as possible.
Otherwise, converts the number `n` to a ByteString of the specified size, including the sign bit. Fails if the number cannot be accommodated.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `n` | `bigint` | a number being converts |
| `size?` | `bigint` | the size of the ByteString |

#### Returns

[`ByteString`](README.md#bytestring)

#### Defined in

[src/smart-contract/builtins/functions.ts:18](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L18)

___

### len

▸ **len**(`a`): `number`

Returns the length of the ByteString. Not the length of the string.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `a` | `Bytes` | a ByteString |

#### Returns

`number`

The length of the ByteString.

#### Defined in

[src/smart-contract/builtins/functions.ts:42](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L42)

___

### reverseByteString

▸ **reverseByteString**(`b`, `size`): [`ByteString`](README.md#bytestring)

Returns reversed bytes of b, which is of size bytes. Note size must be a compiled-time constant.
It is often useful when converting a number between little-endian and big-endian.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `b` | `Bytes` | a ByteString to be reversed |
| `size` | `number` | the size of the ByteString. |

#### Returns

[`ByteString`](README.md#bytestring)

reversed ByteString.

#### Defined in

[src/smart-contract/builtins/functions.ts:53](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L53)

___

## Hashing Functions

### hash160

▸ **hash160**(`a`): [`Ripemd160`](README.md#ripemd160)

A RIPEMD160 hash of a SHA256 hash, which is always 160 bits or 20 bytes long.
This value is commonly used inside Bitcoin, particularly for Bitcoin
addresses.

See:
https://en.wikipedia.org/wiki/RIPEMD

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `a` | `Bytes` | ByteString Data, a.k.a. pre-image, which can be any size. |

#### Returns

[`Ripemd160`](README.md#ripemd160)

The hash in the form of a string.

#### Defined in

[src/smart-contract/builtins/functions.ts:169](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L169)

___

### hash256

▸ **hash256**(`a`): [`Sha256`](README.md#sha256)

A double SHA256 hash, which is always 256 bits or 32 bytes bytes long. This
hash function is commonly used inside Bitcoin, particularly for the hash of a
block and the hash of a transaction.

See:
https://www.movable-type.co.uk/scripts/sha256.html

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `a` | `Bytes` | ByteString data, a.k.a. pre-image, which can be any size. |

#### Returns

[`Sha256`](README.md#sha256)

The hash in the form of a string.

#### Defined in

[src/smart-contract/builtins/functions.ts:184](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L184)

___

### ripemd160

▸ **ripemd160**(`a`): [`Ripemd160`](README.md#ripemd160)

A RIPEMD160 hash, which is always 160 bits or 20 bytes long.
See:
https://en.wikipedia.org/wiki/RIPEMD

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `a` | `Bytes` | ByteString Data, a.k.a. pre-image, which can be any size. |

#### Returns

[`Ripemd160`](README.md#ripemd160)

The hash in the form of a ByteString.

#### Defined in

[src/smart-contract/builtins/functions.ts:127](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L127)

___

### sha1

▸ **sha1**(`a`): [`Sha1`](README.md#sha1)

A SHA or SHA1 hash, which is always 160 bits or 20 bytes long.

See:
https://en.wikipedia.org/wiki/SHA-1

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `a` | `Bytes` | ByteString Data, a.k.a. pre-image, which can be any size. |

#### Returns

[`Sha1`](README.md#sha1)

The hash in the form of a string.

#### Defined in

[src/smart-contract/builtins/functions.ts:140](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L140)

___

### sha256

▸ **sha256**(`a`): [`Sha256`](README.md#sha256)

A SHA256 hash, which is always 256 bits or 32 bytes long.

See:
https://www.movable-type.co.uk/scripts/sha256.html

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `a` | `Bytes` | ByteString Data, a.k.a. pre-image, which can be any size. |

#### Returns

[`Sha256`](README.md#sha256)

The hash in the form of a string.

#### Defined in

[src/smart-contract/builtins/functions.ts:154](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L154)

___

## Math Functions

### abs

▸ **abs**(`a`): `bigint`

The input `a` is made positive.

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `bigint` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:88](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L88)

___

### max

▸ **max**(`a`, `b`): `bigint`

Returns the largest of `a` and `b`.

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `bigint` |
| `b` | `bigint` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:107](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L107)

___

### min

▸ **min**(`a`, `b`): `bigint`

Returns the smallest of `a` and `b`.

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `bigint` |
| `b` | `bigint` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:99](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L99)

___

### within

▸ **within**(`x`, `min`, `max`): `boolean`

Returns true if `x` is within the specified range (left-inclusive), false otherwise.

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `bigint` |
| `min` | `bigint` |
| `max` | `bigint` |

#### Returns

`boolean`

#### Defined in

[src/smart-contract/builtins/functions.ts:115](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L115)

___

## Other Functions

### OpCodeType

▸ **OpCodeType**(`b`): [`OpCodeType`](README.md#opcodetype)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`OpCodeType`](README.md#opcodetype)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:88

___

### PrivKey

▸ **PrivKey**(`n`): [`PrivKey`](README.md#privkey)

#### Parameters

| Name | Type |
| :------ | :------ |
| `n` | `Int` |

#### Returns

[`PrivKey`](README.md#privkey)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:69

___

### PubKey

▸ **PubKey**(`b`): [`PubKey`](README.md#pubkey)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`PubKey`](README.md#pubkey)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:70

___

### PubKeyHash

▸ **PubKeyHash**(`b`): [`PubKeyHash`](README.md#pubkeyhash)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`PubKeyHash`](README.md#pubkeyhash)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:73

___

### Ripemd160

▸ **Ripemd160**(`b`): [`Ripemd160`](README.md#ripemd160)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`Ripemd160`](README.md#ripemd160)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:72

___

### Sha1

▸ **Sha1**(`b`): [`Sha1`](README.md#sha1)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`Sha1`](README.md#sha1)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:74

___

### Sha256

▸ **Sha256**(`b`): [`Sha256`](README.md#sha256)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`Sha256`](README.md#sha256)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:75

___

### Sig

▸ **Sig**(`b`): [`Sig`](README.md#sig)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`Sig`](README.md#sig)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:71

___

### SigHashPreimage

▸ **SigHashPreimage**(`b`): [`SigHashPreimage`](README.md#sighashpreimage)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `Bytes` |

#### Returns

[`SigHashPreimage`](README.md#sighashpreimage)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:87

___

### SigHashType

▸ **SigHashType**(`s`): [`SigHashType`](README.md#sighashtype)

#### Parameters

| Name | Type |
| :------ | :------ |
| `s` | ``0`` \| `SigHash` |

#### Returns

[`SigHashType`](README.md#sighashtype)

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:86

___

### addressesToList

▸ **addressesToList**(`addresses`): `string`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `addresses` | [`AddressesOption`](README.md#addressesoption) |

#### Returns

`string`[]

#### Defined in

[src/bsv/utils.ts:34](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/utils.ts#L34)

___

### and

▸ **and**(`a`, `b`): `Int`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `Int` |
| `b` | `Int` |

#### Returns

`Int`

#### Defined in

node_modules/scryptlib/dist/builtins.d.ts:15

___

### buildOpreturnScript

▸ **buildOpreturnScript**(`data`): [`Script`](classes/bsv.Script-1.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `string` |

#### Returns

[`Script`](classes/bsv.Script-1.md)

#### Defined in

node_modules/scryptlib/dist/builtins.d.ts:22

___

### buildPublicKeyHashScript

▸ **buildPublicKeyHashScript**(`pubKeyHash`): [`Script`](classes/bsv.Script-1.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `pubKeyHash` | [`Ripemd160`](README.md#ripemd160) |

#### Returns

[`Script`](classes/bsv.Script-1.md)

#### Defined in

node_modules/scryptlib/dist/builtins.d.ts:23

___

### equals

▸ **equals**<`T`\>(`a`, `b`): `boolean`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `T` |
| `b` | `T` |

#### Returns

`boolean`

#### Defined in

[src/smart-contract/builtins/types.ts:129](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/types.ts#L129)

___

### getBuildInType

▸ **getBuildInType**(`type`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `type` | `string` |

#### Returns

`string`

#### Defined in

[src/transformation/utils.ts:11](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/transformation/utils.ts#L11)

___

### getDummyP2pkhUTXOs

▸ **getDummyP2pkhUTXOs**(`count?`): [`UTXO`](README.md#utxo)[]

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `count` | `number` | `1` |

#### Returns

[`UTXO`](README.md#utxo)[]

#### Defined in

[src/bsv/utils.ts:6](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/utils.ts#L6)

___

### getPreimage

▸ **getPreimage**(`tx`, `lockingScript`, `inputAmount`, `inputIndex?`, `sighashType?`, `flags?`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `tx` | [`Transaction`](classes/bsv.Transaction-1.md) |
| `lockingScript` | [`Script`](classes/bsv.Script-1.md) |
| `inputAmount` | `number` |
| `inputIndex?` | `number` |
| `sighashType?` | `number` |
| `flags?` | `number` |

#### Returns

`string`

#### Defined in

node_modules/scryptlib/dist/utils.d.ts:26

___

### getRandomAddress

▸ **getRandomAddress**(`network?`): [`Address`](classes/bsv.Address.md)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `network` | [`Network`](interfaces/bsv.Networks.Network.md) | `bsv.Networks.testnet` |

#### Returns

[`Address`](classes/bsv.Address.md)

#### Defined in

[src/bsv/utils.ts:17](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/utils.ts#L17)

___

### getSortedItem

▸ **getSortedItem**<`K`, `V`\>(`collection`, `k`): `SortedItem`<`K`\>

#### Type parameters

| Name |
| :------ |
| `K` |
| `V` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `Map`<`K`, `V`\> \| `Set`<`K`\> |
| `k` | `K` |

#### Returns

`SortedItem`<`K`\>

#### Defined in

node_modules/scryptlib/dist/scryptTypes.d.ts:93

___

### hasModifier

▸ **hasModifier**(`node`, `...kinds`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `node` | `Node` |
| `...kinds` | (`ConstKeyword` \| `DefaultKeyword` \| `ExportKeyword` \| `InKeyword` \| `PrivateKeyword` \| `ProtectedKeyword` \| `PublicKeyword` \| `StaticKeyword` \| `AbstractKeyword` \| `AsyncKeyword` \| `DeclareKeyword` \| `OutKeyword` \| `ReadonlyKeyword` \| `OverrideKeyword`)[] |

#### Returns

`boolean`

#### Defined in

[src/transformation/utils.ts:48](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/transformation/utils.ts#L48)

___

### invert

▸ **invert**(`a`): `Int`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `Int` |

#### Returns

`Int`

#### Defined in

node_modules/scryptlib/dist/builtins.d.ts:18

___

### isNumberLiteralExpr

▸ **isNumberLiteralExpr**(`expr`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `expr` | `Node` |

#### Returns

`boolean`

#### Defined in

[src/transformation/utils.ts:64](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/transformation/utils.ts#L64)

___

### number2hex

▸ **number2hex**(`val`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `val` | `number` \| `bigint` |

#### Returns

`string`

#### Defined in

[src/transformation/utils.ts:40](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/transformation/utils.ts#L40)

___

### or

▸ **or**(`a`, `b`): `Int`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `Int` |
| `b` | `Int` |

#### Returns

`Int`

#### Defined in

node_modules/scryptlib/dist/builtins.d.ts:16

___

### signTx

▸ **signTx**(`tx`, `privateKey`, `lockingScript`, `inputAmount`, `inputIndex?`, `sighashType?`, `flags?`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `tx` | [`Transaction`](classes/bsv.Transaction-1.md) |
| `privateKey` | [`PrivateKey`](classes/bsv.PrivateKey.md) |
| `lockingScript` | [`Script`](classes/bsv.Script-1.md) |
| `inputAmount` | `number` |
| `inputIndex?` | `number` |
| `sighashType?` | `number` |
| `flags?` | `number` |

#### Returns

`string`

#### Defined in

node_modules/scryptlib/dist/utils.d.ts:25

___

### toByteString

▸ **toByteString**<`T`\>(`str`, `isUtf8?`): [`ByteString`](README.md#bytestring)

Converts a literal to ByteString.
If not passing `isUtf8`, then `str` should be in the format of hex literal, i.e. `/^([0-9a-fA-F]{2})*$/`
Otherwise, `str` should be in the format of utf8 literal, i.e. `hello world`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends `string` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `str` | `string` \| `HexType`<`T`\> | literal string, can be hex literal or utf8 literal, depends on isUtf8 marker |
| `isUtf8?` | ``true`` | marker indicating whether `str` is utf8 or hex |

#### Returns

[`ByteString`](README.md#bytestring)

#### Defined in

[src/smart-contract/builtins/types.ts:40](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/types.ts#L40)

___

### toHex

▸ **toHex**(`x`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `Object` |
| `x.toString` | (`format`: ``"hex"``) => `string` |

#### Returns

`string`

#### Defined in

node_modules/scryptlib/dist/utils.d.ts:18

___

### utxoFromOutput

▸ **utxoFromOutput**(`tx`, `outputIndex`): [`UTXO`](README.md#utxo)

#### Parameters

| Name | Type |
| :------ | :------ |
| `tx` | [`Transaction`](classes/bsv.Transaction-1.md) |
| `outputIndex` | `number` |

#### Returns

[`UTXO`](README.md#utxo)

#### Defined in

[src/bsv/utils.ts:21](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/bsv/utils.ts#L21)

___

### xor

▸ **xor**(`a`, `b`): `Int`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `Int` |
| `b` | `Int` |

#### Returns

`Int`

#### Defined in

node_modules/scryptlib/dist/builtins.d.ts:17

___

## Signature Verification Functions

### checkMultiSig

▸ **checkMultiSig**(`signatures`, `publickeys`): `boolean`

Compares the first signature against each public key until it finds an ECDSA match. Starting with the subsequent public key, it compares the second signature against each remaining public key until it finds an ECDSA match. The process is repeated until all signatures have been checked or not enough public keys remain to produce a successful result. All signatures need to match a public key. Because public keys are not checked again if they fail any signature comparison, signatures must be placed in the scriptSig using the same order as their corresponding public keys were placed in the scriptPubKey or redeemScript. If all signatures are valid, 1 is returned, 0 otherwise. Due to a bug, one extra unused value is removed from the stack.

**`See`**

https://wiki.bitcoinsv.io/index.php/Opcodes_used_in_Bitcoin_Script

#### Parameters

| Name | Type |
| :------ | :------ |
| `signatures` | [`Sig`](README.md#sig)[] |
| `publickeys` | [`PubKey`](README.md#pubkey)[] |

#### Returns

`boolean`

#### Defined in

[src/smart-contract/builtins/functions.ts:70](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L70)

___

## assert Functions

### assert

▸ **assert**(`condition`, `msg?`): asserts condition

#### Parameters

| Name | Type |
| :------ | :------ |
| `condition` | `boolean` |
| `msg?` | `string` |

#### Returns

asserts condition

#### Defined in

[src/smart-contract/builtins/functions.ts:191](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L191)

___

## bitshift Functions

### lshift

▸ **lshift**(`x`, `n`): `bigint`

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `bigint` |
| `n` | `bigint` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:240](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L240)

___

### pow2

▸ **pow2**(`n`): `bigint`

#### Parameters

| Name | Type |
| :------ | :------ |
| `n` | `bigint` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:232](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L232)

___

### rshift

▸ **rshift**(`x`, `n`): `bigint`

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `bigint` |
| `n` | `bigint` |

#### Returns

`bigint`

#### Defined in

[src/smart-contract/builtins/functions.ts:248](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L248)

___

## decorator Functions

### method

▸ **method**(`sigHashType?`): (`target`: `any`, `methodName`: `string`, `descriptor`: `PropertyDescriptor`) => `PropertyDescriptor`

Indicates whether the method is a contract method, and ordinary methods do not affect the execution of the contract

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `sigHashType` | [`SigHashType`](README.md#sighashtype) | `SigHash.ALL` |

#### Returns

`fn`

▸ (`target`, `methodName`, `descriptor`): `PropertyDescriptor`

##### Parameters

| Name | Type |
| :------ | :------ |
| `target` | `any` |
| `methodName` | `string` |
| `descriptor` | `PropertyDescriptor` |

##### Returns

`PropertyDescriptor`

#### Defined in

[src/smart-contract/decorators.ts:8](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/decorators.ts#L8)

___

### prop

▸ **prop**(`state?`): (`target`: `any`, `propertyName`: `string`) => `void`

Indicates whether the property is an property of a contract, and ordinary class properties cannot be accessed in contract methods

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `state` | `boolean` | `false` | Whether the property is a property of a stateful contract |

#### Returns

`fn`

▸ (`target`, `propertyName`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `target` | `any` |
| `propertyName` | `string` |

##### Returns

`void`

#### Defined in

[src/smart-contract/decorators.ts:80](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/decorators.ts#L80)

___

## exit() Functions

### exit

▸ **exit**(`status`): `void`

`exit(bool status)`; statement terminates contract execution.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `status` | `boolean` | If status is true, contract succeeds; otherwise, it fails. |

#### Returns

`void`

#### Defined in

[src/smart-contract/builtins/functions.ts:81](https://github.com/sCrypt-Inc/scrypt-ts/blob/5acfc51/src/smart-contract/builtins/functions.ts#L81)
