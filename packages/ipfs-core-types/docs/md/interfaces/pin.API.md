[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pin](../modules/pin.md) / API

# Interface: API<OptionExtension\>

[pin](../modules/pin.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Properties

- [remote](pin.API.md#remote)

### Methods

- [add](pin.API.md#add)
- [addAll](pin.API.md#addall)
- [ls](pin.API.md#ls)
- [rm](pin.API.md#rm)
- [rmAll](pin.API.md#rmall)

## Properties

### remote

• **remote**: `API`<`OptionExtension`\>

#### Defined in

[pin/index.ts:95](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L95)

## Methods

### add

▸ **add**(`cid`, `options?`): `Promise`<`CID`\>

Adds an IPFS block to the pinset and also stores it to the IPFS
repo. pinset is the set of hashes currently pinned (not gc'able)

**`example`**
```js
const cid = CID.parse('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
const pinned of ipfs.pin.add(cid))
console.log(pinned)
// Logs:
// CID('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `string` \| `CID` |
| `options?` | [`AddOptions`](pin.AddOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[pin/index.ts:19](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L19)

___

### addAll

▸ **addAll**(`source`, `options?`): `AsyncIterable`<`CID`\>

Adds multiple IPFS blocks to the pinset and also stores it to the IPFS
repo. pinset is the set of hashes currently pinned (not gc'able)

**`example`**
```js
const cid = CID.parse('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
for await (const cid of ipfs.pin.addAll([cid])) {
  console.log(cid)
}
// Logs:
// CID('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `source` | [`AwaitIterable`](../modules/index.md#awaititerable)<[`AddInput`](../modules/pin.md#addinput)\> |
| `options?` | [`AddAllOptions`](pin.AddAllOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`CID`\>

#### Defined in

[pin/index.ts:35](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L35)

___

### ls

▸ **ls**(`options?`): `AsyncIterable`<[`LsResult`](pin.LsResult.md)\>

List all the objects pinned to local storage

**`example`**
```js
for await (const { cid, type } of ipfs.pin.ls()) {
  console.log({ cid, type })
}
// { cid: CID(Qmc5XkteJdb337s7VwFBAGtiaoj2QCEzyxtNRy3iMudc3E), type: 'recursive' }
// { cid: CID(QmZbj5ruYneZb8FuR9wnLqJCpCXMQudhSdWhdhp5U1oPWJ), type: 'indirect' }
// { cid: CID(QmSo73bmN47gBxMNqbdV6rZ4KJiqaArqJ1nu5TvFhqqj1R), type: 'indirect' }

const paths = [
  CID.parse('Qmc5..'),
  CID.parse('QmZb..'),
  CID.parse('QmSo..')
]
for await (const { cid, type } of ipfs.pin.ls({ paths })) {
  console.log({ cid, type })
}
// { cid: CID(Qmc5XkteJdb337s7VwFBAGtiaoj2QCEzyxtNRy3iMudc3E), type: 'recursive' }
// { cid: CID(QmZbj5ruYneZb8FuR9wnLqJCpCXMQudhSdWhdhp5U1oPWJ), type: 'indirect' }
// { cid: CID(QmSo73bmN47gBxMNqbdV6rZ4KJiqaArqJ1nu5TvFhqqj1R), type: 'indirect' }
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`LsOptions`](pin.LsOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`LsResult`](pin.LsResult.md)\>

#### Defined in

[pin/index.ts:62](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L62)

___

### rm

▸ **rm**(`ipfsPath`, `options?`): `Promise`<`CID`\>

Unpin this block from your repo

**`example`**
```js
const cid = CID.parse('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
const result = await ipfs.pin.rm(cid)
console.log(result)
// prints the CID that was unpinned
// CID('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `string` \| `CID` |
| `options?` | [`RmOptions`](pin.RmOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[pin/index.ts:76](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L76)

___

### rmAll

▸ **rmAll**(`source`, `options?`): `AsyncIterable`<`CID`\>

Unpin one or more blocks from your repo

**`example`**
```js
const source = [
  CID.parse('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
]
for await (const cid of ipfs.pin.rmAll(source)) {
  console.log(cid)
}
// prints the CIDs that were unpinned
// CID('QmWATWQ7fVPP2EFGu71UkfnqhYXDYH566qy47CnJDgvs8u')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `source` | [`AwaitIterable`](../modules/index.md#awaititerable)<[`RmAllInput`](pin.RmAllInput.md)\> |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`CID`\>

#### Defined in

[pin/index.ts:93](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L93)
