[ipfs-core-types](../README.md) / [Modules](../modules.md) / [block](../modules/block.md) / API

# Interface: API<OptionExtension\>

[block](../modules/block.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [get](block.API.md#get)
- [put](block.API.md#put)
- [rm](block.API.md#rm)
- [stat](block.API.md#stat)

## Methods

### get

▸ **get**(`cid`, `options?`): `Promise`<`Uint8Array`\>

Get a raw IPFS block

**`example`**
```js
const block = await ipfs.block.get(cid)
console.log(block)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `PreloadOptions` & `OptionExtension` |

#### Returns

`Promise`<`Uint8Array`\>

#### Defined in

[block/index.ts:14](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L14)

___

### put

▸ **put**(`block`, `options?`): `Promise`<`CID`\>

Stores a Uint8Array as a block in the underlying blockstore

**`example`**
```js
import * as dagPB from '@ipld/dag-pb'
// Defaults
const encoder = new TextEncoder()
const decoder = new TextDecoder()

const bytes = encoder.encode('a serialized object')
const cid = await ipfs.block.put(bytes)

console.log(decoder.decode(block.data))
// Logs:
// a serialized object
console.log(block.cid.toString())
// Logs:
// the CID of the object

// With custom format and hashtype through CID
import { CID } from 'multiformats/cid'
const another = encoder.encode('another serialized object')
const cid = CID.createV1(dagPB.code, multihash)
const block = await ipfs.block.put(another, cid)
console.log(decoder.decode(block.data))

// Logs:
// a serialized object
console.log(block.cid.toString())
// Logs:
// the CID of the object
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `block` | `Uint8Array` |
| `options?` | [`PutOptions`](block.PutOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[block/index.ts:50](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L50)

___

### rm

▸ **rm**(`cid`, `options?`): `AsyncIterable`<[`RmResult`](block.RmResult.md)\>

Remove one or more IPFS block(s) from the underlying block store

**`example`**
```js
for await (const result of ipfs.block.rm(cid)) {
  if (result.error) {
    console.error(`Failed to remove block ${result.cid} due to ${result.error.message}`)
  } else {
   console.log(`Removed block ${result.cid}`)
  }
}
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` \| `CID`[] |
| `options?` | [`RmOptions`](block.RmOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`RmResult`](block.RmResult.md)\>

#### Defined in

[block/index.ts:66](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L66)

___

### stat

▸ **stat**(`cid`, `options?`): `Promise`<[`StatResult`](block.StatResult.md)\>

Print information of a raw IPFS block

**`example`**
```js
const cid = CID.parse('QmQULBtTjNcMwMr4VMNknnVv3RpytrLSdgpvMcTnfNhrBJ')
const stats = await ipfs.block.stat(cid)
console.log(stats.cid.toString())
// Logs: QmQULBtTjNcMwMr4VMNknnVv3RpytrLSdgpvMcTnfNhrBJ
console.log(stat.size)
// Logs: 3739
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `PreloadOptions` & `OptionExtension` |

#### Returns

`Promise`<[`StatResult`](block.StatResult.md)\>

#### Defined in

[block/index.ts:81](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L81)
