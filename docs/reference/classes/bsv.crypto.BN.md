[scrypt-ts](../README.md) / [bsv](../modules/bsv.md) / [crypto](../modules/bsv.crypto.md) / BN

# Class: BN

[bsv](../modules/bsv.md).[crypto](../modules/bsv.crypto.md).BN

## Table of contents

### Constructors

- [constructor](bsv.crypto.BN.md#constructor)

### Properties

- [One](bsv.crypto.BN.md#one)

### Methods

- [abs](bsv.crypto.BN.md#abs)
- [add](bsv.crypto.BN.md#add)
- [and](bsv.crypto.BN.md#and)
- [bincn](bsv.crypto.BN.md#bincn)
- [bitLength](bsv.crypto.BN.md#bitlength)
- [byteLength](bsv.crypto.BN.md#bytelength)
- [clone](bsv.crypto.BN.md#clone)
- [cmp](bsv.crypto.BN.md#cmp)
- [div](bsv.crypto.BN.md#div)
- [divRound](bsv.crypto.BN.md#divround)
- [egcd](bsv.crypto.BN.md#egcd)
- [eq](bsv.crypto.BN.md#eq)
- [eqn](bsv.crypto.BN.md#eqn)
- [gcd](bsv.crypto.BN.md#gcd)
- [gt](bsv.crypto.BN.md#gt)
- [gte](bsv.crypto.BN.md#gte)
- [gten](bsv.crypto.BN.md#gten)
- [invm](bsv.crypto.BN.md#invm)
- [isBN](bsv.crypto.BN.md#isbn)
- [isEven](bsv.crypto.BN.md#iseven)
- [isNeg](bsv.crypto.BN.md#isneg)
- [isOdd](bsv.crypto.BN.md#isodd)
- [isZero](bsv.crypto.BN.md#iszero)
- [lt](bsv.crypto.BN.md#lt)
- [lte](bsv.crypto.BN.md#lte)
- [lten](bsv.crypto.BN.md#lten)
- [maskn](bsv.crypto.BN.md#maskn)
- [mod](bsv.crypto.BN.md#mod)
- [mul](bsv.crypto.BN.md#mul)
- [neg](bsv.crypto.BN.md#neg)
- [notn](bsv.crypto.BN.md#notn)
- [or](bsv.crypto.BN.md#or)
- [pow](bsv.crypto.BN.md#pow)
- [setn](bsv.crypto.BN.md#setn)
- [shln](bsv.crypto.BN.md#shln)
- [shrn](bsv.crypto.BN.md#shrn)
- [sqr](bsv.crypto.BN.md#sqr)
- [sub](bsv.crypto.BN.md#sub)
- [testn](bsv.crypto.BN.md#testn)
- [toArray](bsv.crypto.BN.md#toarray)
- [toBuffer](bsv.crypto.BN.md#tobuffer)
- [toJSON](bsv.crypto.BN.md#tojson)
- [toNumber](bsv.crypto.BN.md#tonumber)
- [toSM](bsv.crypto.BN.md#tosm)
- [toString](bsv.crypto.BN.md#tostring)
- [xor](bsv.crypto.BN.md#xor)
- [zeroBits](bsv.crypto.BN.md#zerobits)
- [fromBuffer](bsv.crypto.BN.md#frombuffer)
- [fromHex](bsv.crypto.BN.md#fromhex)
- [fromNumber](bsv.crypto.BN.md#fromnumber)
- [fromSM](bsv.crypto.BN.md#fromsm)
- [fromString](bsv.crypto.BN.md#fromstring)

## Constructors

### constructor

• **new BN**(`number`, `base?`, `endian?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `number` | `string` \| `number` \| `bigint` \| `number`[] \| readonly `number`[] \| `Buffer` \| [`BN`](bsv.crypto.BN.md) |
| `base?` | `number` |
| `endian?` | [`Endianness`](../modules/bsv.crypto.md#endianness) |

#### Defined in

node_modules/bsv/index.d.ts:207

## Properties

### One

• **One**: [`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:213

## Methods

### abs

▸ **abs**(): [`BN`](bsv.crypto.BN.md)

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:240

___

### add

▸ **add**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:241

▸ **add**(`one`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `one` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:266

___

### and

▸ **and**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:251

___

### bincn

▸ **bincn**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:258

___

### bitLength

▸ **bitLength**(): `number`

#### Returns

`number`

#### Defined in

node_modules/bsv/index.d.ts:221

___

### byteLength

▸ **byteLength**(): `number`

#### Returns

`number`

#### Defined in

node_modules/bsv/index.d.ts:223

___

### clone

▸ **clone**(): [`BN`](bsv.crypto.BN.md)

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:215

___

### cmp

▸ **cmp**(`b`): `number`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`number`

#### Defined in

node_modules/bsv/index.d.ts:228

___

### div

▸ **div**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:246

___

### divRound

▸ **divRound**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:248

___

### egcd

▸ **egcd**(`b`): `Object`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `a` | [`BN`](bsv.crypto.BN.md) |
| `b` | [`BN`](bsv.crypto.BN.md) |
| `gcd` | [`BN`](bsv.crypto.BN.md) |

#### Defined in

node_modules/bsv/index.d.ts:262

___

### eq

▸ **eq**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:233

___

### eqn

▸ **eqn**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:234

___

### gcd

▸ **gcd**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:261

___

### gt

▸ **gt**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:231

___

### gte

▸ **gte**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:232

___

### gten

▸ **gten**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:235

___

### invm

▸ **invm**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:263

___

### isBN

▸ **isBN**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:237

___

### isEven

▸ **isEven**(): `boolean`

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:225

___

### isNeg

▸ **isNeg**(): `boolean`

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:224

___

### isOdd

▸ **isOdd**(): `boolean`

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:226

___

### isZero

▸ **isZero**(): `boolean`

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:227

___

### lt

▸ **lt**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:229

___

### lte

▸ **lte**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:230

___

### lten

▸ **lten**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `any` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:236

___

### maskn

▸ **maskn**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:257

___

### mod

▸ **mod**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:247

___

### mul

▸ **mul**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:243

___

### neg

▸ **neg**(): [`BN`](bsv.crypto.BN.md)

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:239

▸ **neg**(): [`BN`](bsv.crypto.BN.md)

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:265

___

### notn

▸ **notn**(`w`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `w` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:259

___

### or

▸ **or**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:250

___

### pow

▸ **pow**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:245

___

### setn

▸ **setn**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:253

___

### shln

▸ **shln**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:254

___

### shrn

▸ **shrn**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:255

___

### sqr

▸ **sqr**(): [`BN`](bsv.crypto.BN.md)

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:244

___

### sub

▸ **sub**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:242

___

### testn

▸ **testn**(`b`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | `number` |

#### Returns

`boolean`

#### Defined in

node_modules/bsv/index.d.ts:256

___

### toArray

▸ **toArray**(`endian?`, `length?`): `number`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `endian?` | [`Endianness`](../modules/bsv.crypto.md#endianness) |
| `length?` | `number` |

#### Returns

`number`[]

#### Defined in

node_modules/bsv/index.d.ts:219

___

### toBuffer

▸ **toBuffer**(`opts?`): `Buffer`

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`IOpts`](../interfaces/bsv.crypto.IOpts.md) |

#### Returns

`Buffer`

#### Defined in

node_modules/bsv/index.d.ts:220

___

### toJSON

▸ **toJSON**(): `string`

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:218

___

### toNumber

▸ **toNumber**(): `number`

#### Returns

`number`

#### Defined in

node_modules/bsv/index.d.ts:217

▸ **toNumber**(): `number`

#### Returns

`number`

#### Defined in

node_modules/bsv/index.d.ts:268

___

### toSM

▸ **toSM**(`opts?`): `Buffer`

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`IOpts`](../interfaces/bsv.crypto.IOpts.md) |

#### Returns

`Buffer`

#### Defined in

node_modules/bsv/index.d.ts:267

___

### toString

▸ **toString**(`base?`, `length?`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `base?` | `number` \| ``"hex"`` |
| `length?` | `number` |

#### Returns

`string`

#### Defined in

node_modules/bsv/index.d.ts:216

___

### xor

▸ **xor**(`b`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `b` | [`BN`](bsv.crypto.BN.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:252

___

### zeroBits

▸ **zeroBits**(): `number`

#### Returns

`number`

#### Defined in

node_modules/bsv/index.d.ts:222

___

### fromBuffer

▸ `Static` **fromBuffer**(`buf`, `opts?`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `buf` | `Buffer` |
| `opts?` | [`IOpts`](../interfaces/bsv.crypto.IOpts.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:269

___

### fromHex

▸ `Static` **fromHex**(`hex`, `opts?`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hex` | `string` |
| `opts?` | [`IOpts`](../interfaces/bsv.crypto.IOpts.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:272

___

### fromNumber

▸ `Static` **fromNumber**(`n`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `n` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:270

___

### fromSM

▸ `Static` **fromSM**(`buf`, `opts?`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `buf` | `Buffer` |
| `opts?` | [`IOpts`](../interfaces/bsv.crypto.IOpts.md) |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:264

___

### fromString

▸ `Static` **fromString**(`hex`, `base?`): [`BN`](bsv.crypto.BN.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hex` | `string` |
| `base?` | `number` |

#### Returns

[`BN`](bsv.crypto.BN.md)

#### Defined in

node_modules/bsv/index.d.ts:273
