[ipfs-core-types](../README.md) / [Modules](../modules.md) / [diag](../modules/diag.md) / API

# Interface: API<OptionExtension\>

[diag](../modules/diag.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [cmds](diag.API.md#cmds)
- [net](diag.API.md#net)
- [sys](diag.API.md#sys)

## Methods

### cmds

▸ **cmds**(`options?`): `Promise`<[`CmdsResult`](diag.CmdsResult.md)[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`CmdsResult`](diag.CmdsResult.md)[]\>

#### Defined in

[diag/index.ts:4](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/diag/index.ts#L4)

___

### net

▸ **net**(`options?`): `Promise`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`any`\>

#### Defined in

[diag/index.ts:5](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/diag/index.ts#L5)

___

### sys

▸ **sys**(`options?`): `Promise`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`any`\>

#### Defined in

[diag/index.ts:6](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/diag/index.ts#L6)
