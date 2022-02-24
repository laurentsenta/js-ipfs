[ipfs-core-types](../README.md) / [Modules](../modules.md) / [bitswap](../modules/bitswap.md) / API

# Interface: API<OptionExtension\>

[bitswap](../modules/bitswap.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [stat](bitswap.API.md#stat)
- [unwant](bitswap.API.md#unwant)
- [wantlist](bitswap.API.md#wantlist)
- [wantlistForPeer](bitswap.API.md#wantlistforpeer)

## Methods

### stat

▸ **stat**(`options?`): `Promise`<[`Stats`](bitswap.Stats.md)\>

Show diagnostic information on the bitswap agent.
Note: `bitswap.stat` and `stats.bitswap` can be used interchangeably.

**`example`**
```js
const stats = await ipfs.bitswap.stat()
console.log(stats)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Stats`](bitswap.Stats.md)\>

#### Defined in

[bitswap/index.ts:57](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bitswap/index.ts#L57)

___

### unwant

▸ **unwant**(`cids`, `options?`): `Promise`<`void`\>

Removes one or more CIDs from the wantlist

**`example`**
```JavaScript
let list = await ipfs.bitswap.wantlist()
console.log(list)
// [ CID('QmHash') ]

await ipfs.bitswap.unwant(cid)

list = await ipfs.bitswap.wantlist()
console.log(list)
// []
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cids` | `CID` \| `CID`[] |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[bitswap/index.ts:45](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bitswap/index.ts#L45)

___

### wantlist

▸ **wantlist**(`options?`): `Promise`<`CID`[]\>

Returns the wantlist for your node

**`example`**
```js
const list = await ipfs.bitswap.wantlist()
console.log(list)
// [ CID('QmHash') ]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`[]\>

#### Defined in

[bitswap/index.ts:15](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bitswap/index.ts#L15)

___

### wantlistForPeer

▸ **wantlistForPeer**(`peerId`, `options?`): `Promise`<`CID`[]\>

Returns the wantlist for a connected peer

**`example`**
```js
const list = await ipfs.bitswap.wantlistForPeer(peerId)
console.log(list)
// [ CID('QmHash') ]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `peerId` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`[]\>

#### Defined in

[bitswap/index.ts:27](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bitswap/index.ts#L27)
