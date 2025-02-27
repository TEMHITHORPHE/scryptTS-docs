[scrypt-ts](../README.md) / [bsv](../modules/bsv.md) / Address

# Class: Address

[bsv](../modules/bsv.md).Address

## Table of contents

### Constructors

- [constructor](bsv.Address.md#constructor)

### Properties

- [hashBuffer](bsv.Address.md#hashbuffer)
- [network](bsv.Address.md#network)
- [type](bsv.Address.md#type)

### Methods

- [isValid](bsv.Address.md#isvalid)
- [toBuffer](bsv.Address.md#tobuffer)
- [toHex](bsv.Address.md#tohex)
- [toObject](bsv.Address.md#toobject)
- [toString](bsv.Address.md#tostring)
- [fromHex](bsv.Address.md#fromhex)
- [fromPrivateKey](bsv.Address.md#fromprivatekey)
- [fromPublicKey](bsv.Address.md#frompublickey)
- [fromPublicKeyHash](bsv.Address.md#frompublickeyhash)
- [fromScriptHash](bsv.Address.md#fromscripthash)
- [fromString](bsv.Address.md#fromstring)

## Constructors

### constructor

• **new Address**(`data`, `network?`, `type?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `string` \| `object` \| `Uint8Array` \| `Buffer` |
| `network?` | `string` \| [`Network`](../interfaces/bsv.Networks.Network.md) |
| `type?` | `string` |

#### Defined in

node_modules/bsv/index.d.ts:938

## Properties

### hashBuffer

• `Readonly` **hashBuffer**: `Buffer`

#### Defined in

node_modules/bsv/index.d.ts:934

___

### network

• `Readonly` **network**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:935

___

### type

• `Readonly` **type**: `string`

#### Defined in

node_modules/bsv/index.d.ts:936

## Methods

### isValid

▸ **isValid**(`data`, `network?`, `type?`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `string` \| `object` \| `Uint8Array` \| `Buffer` |
| `network?` | `string` \| [`Network`](../interfaces/bsv.Networks.Network.md) |
| `type?` | `string` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:958

___

### toBuffer

▸ **toBuffer**(): `Buffer`

#### Returns

`Buffer`

#### Defined in

node_modules/bsv/index.d.ts:963

___

### toHex

▸ **toHex**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:964

___

### toObject

▸ **toObject**(): `Object`

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `hash` | `string` |
| `network` | `string` |
| `type` | `string` |

#### Defined in

node_modules/bsv/index.d.ts:966

___

### toString

▸ **toString**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:965

___

### fromHex

▸ `Static` **fromHex**(`hex`, `network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hex` | `string` |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:944

___

### fromPrivateKey

▸ `Static` **fromPrivateKey**(`privateKey`, `network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `privateKey` | [`PrivateKey`](bsv.PrivateKey.md) |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:946

___

### fromPublicKey

▸ `Static` **fromPublicKey**(`data`, `network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | [`PublicKey`](bsv.PublicKey.md) |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:945

___

### fromPublicKeyHash

▸ `Static` **fromPublicKeyHash**(`hash`, `network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hash` | `Uint8Array` \| `Buffer` |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:950

___

### fromScriptHash

▸ `Static` **fromScriptHash**(`hash`, `network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hash` | `Uint8Array` \| `Buffer` |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:954

___

### fromString

▸ `Static` **fromString**(`address`, `network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `address` | `string` |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:943
