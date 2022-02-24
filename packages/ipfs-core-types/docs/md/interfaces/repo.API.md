[ipfs-core-types](../README.md) / [Modules](../modules.md) / [repo](../modules/repo.md) / API

# Interface: API<OptionExtension\>

[repo](../modules/repo.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [gc](repo.API.md#gc)
- [stat](repo.API.md#stat)
- [version](repo.API.md#version)

## Methods

### gc

▸ **gc**(`options?`): `AsyncIterable`<[`GCResult`](../modules/repo.md#gcresult)\>

Perform garbage collection on the repo

Any unpinned blocks will be deleted

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`GCOptions`](repo.GCOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`GCResult`](../modules/repo.md#gcresult)\>

#### Defined in

[repo/index.ts:10](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/repo/index.ts#L10)

___

### stat

▸ **stat**(`options?`): `Promise`<[`StatResult`](repo.StatResult.md)\>

Return stats about the repo

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`StatResult`](repo.StatResult.md)\>

#### Defined in

[repo/index.ts:15](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/repo/index.ts#L15)

___

### version

▸ **version**(`options?`): `Promise`<`number`\>

If the repo has been initialized, report the current version,
otherwise report the version that would be initialized

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`number`\>

#### Defined in

[repo/index.ts:21](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/repo/index.ts#L21)
