[scrypt-ts](../README.md) / [bsv](../modules/bsv.md) / PrivateKey

# Class: PrivateKey

[bsv](../modules/bsv.md).PrivateKey

## Table of contents

### Constructors

- [constructor](bsv.PrivateKey.md#constructor)

### Properties

- [bn](bsv.PrivateKey.md#bn)
- [compressed](bsv.PrivateKey.md#compressed)
- [network](bsv.PrivateKey.md#network)
- [publicKey](bsv.PrivateKey.md#publickey)

### Methods

- [inspect](bsv.PrivateKey.md#inspect)
- [toAddress](bsv.PrivateKey.md#toaddress)
- [toBigNumber](bsv.PrivateKey.md#tobignumber)
- [toBuffer](bsv.PrivateKey.md#tobuffer)
- [toHex](bsv.PrivateKey.md#tohex)
- [toJSON](bsv.PrivateKey.md#tojson)
- [toObject](bsv.PrivateKey.md#toobject)
- [toPublicKey](bsv.PrivateKey.md#topublickey)
- [toString](bsv.PrivateKey.md#tostring)
- [toWIF](bsv.PrivateKey.md#towif)
- [fromBuffer](bsv.PrivateKey.md#frombuffer)
- [fromHex](bsv.PrivateKey.md#fromhex)
- [fromRandom](bsv.PrivateKey.md#fromrandom)
- [fromString](bsv.PrivateKey.md#fromstring)
- [fromWIF](bsv.PrivateKey.md#fromwif)
- [getValidationError](bsv.PrivateKey.md#getvalidationerror)
- [isValid](bsv.PrivateKey.md#isvalid)

## Constructors

### constructor

• **new PrivateKey**(`key?`, `network?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `key?` | `string` \| [`PrivateKey`](bsv.PrivateKey.md) |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Defined in

node_modules/bsv/index.d.ts:565

## Properties

### bn

• `Readonly` **bn**: [`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:567

___

### compressed

• `Readonly` **compressed**: `boolean`

#### Defined in

node_modules/bsv/index.d.ts:570

___

### network

• `Readonly` **network**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:571

___

### publicKey

• `Readonly` **publicKey**: [`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:569

## Methods

### inspect

▸ **inspect**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:582

___

### toAddress

▸ **toAddress**(`network?`): [`Address`](bsv.Address.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `network?` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`Address`](bsv.Address.md)

#### Defined in

node_modules/bsv/index.d.ts:573

___

### toBigNumber

▸ **toBigNumber**(): `any`

#### Returns

`any`

#### Defined in

node_modules/bsv/index.d.ts:580

___

### toBuffer

▸ **toBuffer**(): `Buffer`

#### Returns

`Buffer`

#### Defined in

node_modules/bsv/index.d.ts:581

___

### toHex

▸ **toHex**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:579

___

### toJSON

▸ **toJSON**(): `object`

#### Returns

`object`

#### Defined in

node_modules/bsv/index.d.ts:577

___

### toObject

▸ **toObject**(): `object`

#### Returns

`object`

#### Defined in

node_modules/bsv/index.d.ts:576

___

### toPublicKey

▸ **toPublicKey**(): [`PublicKey`](bsv.PublicKey.md)

#### Returns

[`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:574

___

### toString

▸ **toString**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:575

___

### toWIF

▸ **toWIF**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:578

___

### fromBuffer

▸ `Static` **fromBuffer**(`buf`, `network`): [`PrivateKey`](bsv.PrivateKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `buf` | `Buffer` |
| `network` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`PrivateKey`](bsv.PrivateKey.md)

#### Defined in

node_modules/bsv/index.d.ts:587

___

### fromHex

▸ `Static` **fromHex**(`hex`, `network`): [`PrivateKey`](bsv.PrivateKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hex` | `string` |
| `network` | [`Type`](../modules/bsv.Networks.md#type) |

#### Returns

[`PrivateKey`](bsv.PrivateKey.md)

#### Defined in

node_modules/bsv/index.d.ts:588

___

### fromRandom

▸ `Static` **fromRandom**(`netowrk?`): [`PrivateKey`](bsv.PrivateKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `netowrk?` | `string` |

#### Returns

[`PrivateKey`](bsv.PrivateKey.md)

#### Defined in

node_modules/bsv/index.d.ts:586

___

### fromString

▸ `Static` **fromString**(`str`): [`PrivateKey`](bsv.PrivateKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `str` | `string` |

#### Returns

[`PrivateKey`](bsv.PrivateKey.md)

#### Defined in

node_modules/bsv/index.d.ts:584

___

### fromWIF

▸ `Static` **fromWIF**(`str`): [`PrivateKey`](bsv.PrivateKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `str` | `string` |

#### Returns

[`PrivateKey`](bsv.PrivateKey.md)

#### Defined in

node_modules/bsv/index.d.ts:585

___

### getValidationError

▸ `Static` **getValidationError**(`data`): `any`

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `string` |

#### Returns

`any`

#### Defined in

node_modules/bsv/index.d.ts:589

___

### isValid

▸ `Static` **isValid**(`data`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `string` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:590
