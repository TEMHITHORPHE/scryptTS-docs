[scrypt-ts](../README.md) / [bsv](../modules/bsv.md) / Block

# Class: Block

[bsv](../modules/bsv.md).Block

## Table of contents

### Constructors

- [constructor](bsv.Block.md#constructor)

### Properties

- [hash](bsv.Block.md#hash)
- [header](bsv.Block.md#header)
- [height](bsv.Block.md#height)
- [transactions](bsv.Block.md#transactions)

## Constructors

### constructor

• **new Block**(`data`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `object` \| `Buffer` |

#### Defined in

node_modules/bsv/index.d.ts:561

## Properties

### hash

• **hash**: `string`

#### Defined in

node_modules/bsv/index.d.ts:553

___

### header

• **header**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `prevHash` | `string` |
| `time` | `number` |

#### Defined in

node_modules/bsv/index.d.ts:556

___

### height

• **height**: `number`

#### Defined in

node_modules/bsv/index.d.ts:554

___

### transactions

• **transactions**: [`Transaction`](bsv.Transaction-1.md)[]

#### Defined in

node_modules/bsv/index.d.ts:555
