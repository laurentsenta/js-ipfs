[ipfs-core-types](../README.md) / [Modules](../modules.md) / [stats](../modules/stats.md) / API

# Interface: API<OptionExtension\>

[stats](../modules/stats.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Properties

- [bitswap](stats.API.md#bitswap)
- [repo](stats.API.md#repo)

### Methods

- [bw](stats.API.md#bw)

## Properties

### bitswap

• **bitswap**: (`options?`: [`AbortOptions`](index.AbortOptions.md) & `OptionExtension`) => `Promise`<[`Stats`](bitswap.Stats.md)\>

#### Type declaration

▸ (`options?`): `Promise`<[`Stats`](bitswap.Stats.md)\>

Show diagnostic information on the bitswap agent.
Note: `bitswap.stat` and `stats.bitswap` can be used interchangeably.

**`example`**
```js
const stats = await ipfs.bitswap.stat()
console.log(stats)
```

##### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

##### Returns

`Promise`<[`Stats`](bitswap.Stats.md)\>

#### Defined in

[stats/index.ts:6](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L6)

___

### repo

• **repo**: (`options?`: [`AbortOptions`](index.AbortOptions.md) & `OptionExtension`) => `Promise`<[`StatResult`](repo.StatResult.md)\>

#### Type declaration

▸ (`options?`): `Promise`<[`StatResult`](repo.StatResult.md)\>

Return stats about the repo

##### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

##### Returns

`Promise`<[`StatResult`](repo.StatResult.md)\>

#### Defined in

[stats/index.ts:7](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L7)

## Methods

### bw

▸ **bw**(`options?`): `AsyncIterable`<[`BWResult`](stats.BWResult.md)\>

Return bandwith usage stats

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`BWOptions`](stats.BWOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`BWResult`](stats.BWResult.md)\>

#### Defined in

[stats/index.ts:12](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L12)
