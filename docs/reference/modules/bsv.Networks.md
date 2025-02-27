[scrypt-ts](../README.md) / [bsv](bsv.md) / Networks

# Namespace: Networks

[bsv](bsv.md).Networks

## Table of contents

### Interfaces

- [Network](../interfaces/bsv.Networks.Network.md)

### Type Aliases

- [Type](bsv.Networks.md#type)

### Variables

- [defaultNetwork](bsv.Networks.md#defaultnetwork)
- [livenet](bsv.Networks.md#livenet)
- [mainnet](bsv.Networks.md#mainnet)
- [testnet](bsv.Networks.md#testnet)

### Functions

- [add](bsv.Networks.md#add)
- [get](bsv.Networks.md#get)
- [remove](bsv.Networks.md#remove)

## Type Aliases

### Type

Ƭ **Type**: ``"livenet"`` \| ``"testnet"`` \| [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:918

## Variables

### defaultNetwork

• `Const` **defaultNetwork**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:923

___

### livenet

• `Const` **livenet**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:920

___

### mainnet

• `Const` **mainnet**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:921

___

### testnet

• `Const` **testnet**: [`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:922

## Functions

### add

▸ **add**(`data`): [`Network`](../interfaces/bsv.Networks.Network.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `any` |

#### Returns

[`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:925

___

### get

▸ **get**(`args`, `keys`): [`Network`](../interfaces/bsv.Networks.Network.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `string` \| `number` \| [`Network`](../interfaces/bsv.Networks.Network.md) |
| `keys` | `string` \| `string`[] |

#### Returns

[`Network`](../interfaces/bsv.Networks.Network.md)

#### Defined in

node_modules/bsv/index.d.ts:927

___

### remove

▸ **remove**(`network`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `network` | [`Type`](bsv.Networks.md#type) |

#### Returns

`void`

#### Defined in

node_modules/bsv/index.d.ts:926
