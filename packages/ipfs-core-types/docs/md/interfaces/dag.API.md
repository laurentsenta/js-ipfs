[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / API

# Interface: API<OptionExtension\>

[dag](../modules/dag.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [export](dag.API.md#export)
- [get](dag.API.md#get)
- [import](dag.API.md#import)
- [put](dag.API.md#put)
- [resolve](dag.API.md#resolve)

## Methods

### export

▸ **export**(`root`, `options?`): `AsyncIterable`<`Uint8Array`\>

Exports a CAR for the entire DAG available from the given root CID. The CAR will have a single
root and IPFS will attempt to fetch and bundle all blocks that are linked within the connected
DAG.

#### Parameters

| Name | Type |
| :------ | :------ |
| `root` | `CID` |
| `options?` | [`ExportOptions`](dag.ExportOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`Uint8Array`\>

#### Defined in

[dag/index.ts:100](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L100)

___

### get

▸ **get**(`cid`, `options?`): `Promise`<[`GetResult`](dag.GetResult.md)\>

Retrieve an IPLD format node

**`example`**
```js
// example obj
const obj = {
  a: 1,
  b: [1, 2, 3],
  c: {
    ca: [5, 6, 7],
    cb: 'foo'
  }
}

const cid = await ipfs.dag.put(obj, { storeCodec: 'dag-cbor', hashAlg: 'sha2-256' })
console.log(cid.toString())
// zdpuAmtur968yprkhG9N5Zxn6MFVoqAWBbhUAkNLJs2UtkTq5

async function getAndLog(cid, path) {
  const result = await ipfs.dag.get(cid, { path })
  console.log(result.value)
}

await getAndLog(cid, '/a')
// Logs:
// 1

await getAndLog(cid, '/b')
// Logs:
// [1, 2, 3]

await getAndLog(cid, '/c')
// Logs:
// {
//   ca: [5, 6, 7],
//   cb: 'foo'
// }

await getAndLog(cid, '/c/ca/1')
// Logs:
// 6
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`GetOptions`](dag.GetOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`GetResult`](dag.GetResult.md)\>

#### Defined in

[dag/index.ts:49](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L49)

___

### import

▸ **import**(`sources`, `options?`): `AsyncIterable`<[`ImportResult`](dag.ImportResult.md)\>

Import all blocks from one or more CARs and optionally recursively pin the roots identified
within the CARs.

#### Parameters

| Name | Type |
| :------ | :------ |
| `sources` | `Iterable`<`Uint8Array`\> \| `AsyncIterable`<`Uint8Array`\> \| `AsyncIterable`<`AsyncIterable`<`Uint8Array`\>\> \| `Iterable`<`AsyncIterable`<`Uint8Array`\>\> |
| `options?` | [`ImportOptions`](dag.ImportOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`ImportResult`](dag.ImportResult.md)\>

#### Defined in

[dag/index.ts:106](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L106)

___

### put

▸ **put**(`node`, `options?`): `Promise`<`CID`\>

Store an IPLD format node

**`example`**
```js
const obj = { simple: 'object' }
const cid = await ipfs.dag.put(obj, { storeCodec: 'dag-cbor', hashAlg: 'sha2-512' })

console.log(cid.toString())
// zBwWX9ecx5F4X54WAjmFLErnBT6ByfNxStr5ovowTL7AhaUR98RWvXPS1V3HqV1qs3r5Ec5ocv7eCdbqYQREXNUfYNuKG
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `node` | `any` |
| `options?` | [`PutOptions`](dag.PutOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[dag/index.ts:63](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L63)

___

### resolve

▸ **resolve**(`ipfsPath`, `options?`): `Promise`<[`ResolveResult`](dag.ResolveResult.md)\>

Returns the CID and remaining path of the node at the end of the passed IPFS path

**`example`**
```JavaScript
// example obj
const obj = {
  a: 1,
  b: [1, 2, 3],
  c: {
    ca: [5, 6, 7],
    cb: 'foo'
  }
}

const cid = await ipfs.dag.put(obj, { storeCodec: 'dag-cbor', hashAlg: 'sha2-256' })
console.log(cid.toString())
// bafyreicyer3d34cutdzlsbe2nqu5ye62mesuhwkcnl2ypdwpccrsecfmjq

const result = await ipfs.dag.resolve(`${cid}/c/cb`)
console.log(result)
// Logs:
// {
//   cid: CID(bafyreicyer3d34cutdzlsbe2nqu5ye62mesuhwkcnl2ypdwpccrsecfmjq),
//   remainderPath: 'c/cb'
// }
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`ResolveOptions`](dag.ResolveOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`ResolveResult`](dag.ResolveResult.md)\>

#### Defined in

[dag/index.ts:93](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L93)
