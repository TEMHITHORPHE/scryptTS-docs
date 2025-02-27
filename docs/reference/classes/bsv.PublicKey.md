[scrypt-ts](../README.md) / [bsv](../modules/bsv.md) / PublicKey

# Class: PublicKey

[bsv](../modules/bsv.md).PublicKey

## Table of contents

### Constructors

- [constructor](bsv.PublicKey.md#constructor)

### Properties

- [compressed](bsv.PublicKey.md#compressed)
- [network](bsv.PublicKey.md#network)
- [point](bsv.PublicKey.md#point)

### Methods

- [inspect](bsv.PublicKey.md#inspect)
- [toAddress](bsv.PublicKey.md#toaddress)
- [toBuffer](bsv.PublicKey.md#tobuffer)
- [toDER](bsv.PublicKey.md#toder)
- [toHex](bsv.PublicKey.md#tohex)
- [toObject](bsv.PublicKey.md#toobject)
- [toString](bsv.PublicKey.md#tostring)
- [fromBuffer](bsv.PublicKey.md#frombuffer)
- [fromDER](bsv.PublicKey.md#fromder)
- [fromHex](bsv.PublicKey.md#fromhex)
- [fromPrivateKey](bsv.PublicKey.md#fromprivatekey)
- [fromString](bsv.PublicKey.md#fromstring)
- [getValidationError](bsv.PublicKey.md#getvalidationerror)
- [isValid](bsv.PublicKey.md#isvalid)

## Constructors

### constructor

• **new PublicKey**(`source`, `extra?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `source` | `string` \| [`PublicKey`](bsv.PublicKey.md) \| [`Point`](bsv.crypto.Point.md) |
| `extra?` | `object` |

#### Defined in

node_modules/bsv/index.d.ts:594

## Properties

### compressed

• `Readonly` **compressed**: `boolean`

#### Defined in

node_modules/bsv/index.d.ts:597

___

### network

• `Readonly` **network**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:598

___

### point

• `Readonly` **point**: [`Point`](bsv.crypto.Point.md)

#### Defined in

node_modules/bsv/index.d.ts:596

## Methods

### inspect

▸ **inspect**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:606

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

node_modules/bsv/index.d.ts:603

___

### toBuffer

▸ **toBuffer**(): `Buffer`

#### Returns

`Buffer`

#### Defined in

node_modules/bsv/index.d.ts:602

___

### toDER

▸ **toDER**(): `Buffer`

#### Returns

`Buffer`

#### Defined in

node_modules/bsv/index.d.ts:600

___

### toHex

▸ **toHex**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:605

___

### toObject

▸ **toObject**(): `object`

#### Returns

`object`

#### Defined in

node_modules/bsv/index.d.ts:601

___

### toString

▸ **toString**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:604

___

### fromBuffer

▸ `Static` **fromBuffer**(`buf`, `strict?`): [`PublicKey`](bsv.PublicKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `buf` | `Buffer` |
| `strict?` | `boolean` |

#### Returns

[`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:609

___

### fromDER

▸ `Static` **fromDER**(`buf`, `strict?`): [`PublicKey`](bsv.PublicKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `buf` | `Buffer` |
| `strict?` | `boolean` |

#### Returns

[`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:610

___

### fromHex

▸ `Static` **fromHex**(`hex`): [`PublicKey`](bsv.PublicKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hex` | `string` |

#### Returns

[`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:614

___

### fromPrivateKey

▸ `Static` **fromPrivateKey**(`privateKey`): [`PublicKey`](bsv.PublicKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `privateKey` | [`PrivateKey`](bsv.PrivateKey.md) |

#### Returns

[`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:608

___

### fromString

▸ `Static` **fromString**(`str`): [`PublicKey`](bsv.PublicKey.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `str` | `string` |

#### Returns

[`PublicKey`](bsv.PublicKey.md)

#### Defined in

node_modules/bsv/index.d.ts:613

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

node_modules/bsv/index.d.ts:615

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

node_modules/bsv/index.d.ts:616
