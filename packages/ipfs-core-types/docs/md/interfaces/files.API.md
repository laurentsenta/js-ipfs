[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / API

# Interface: API<OptionExtension\>

[files](../modules/files.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [chmod](files.API.md#chmod)
- [cp](files.API.md#cp)
- [flush](files.API.md#flush)
- [ls](files.API.md#ls)
- [mkdir](files.API.md#mkdir)
- [mv](files.API.md#mv)
- [read](files.API.md#read)
- [rm](files.API.md#rm)
- [stat](files.API.md#stat)
- [touch](files.API.md#touch)
- [write](files.API.md#write)

## Methods

### chmod

▸ **chmod**(`path`, `mode`, `options?`): `Promise`<`void`\>

Change mode for files and directories

**`example`**
```js
// To give a file -rwxrwxrwx permissions
await ipfs.files.chmod('/path/to/file.txt', parseInt('0777', 8))

// Alternatively
await ipfs.files.chmod('/path/to/file.txt', '+rwx')

// You can omit the leading `0` too
await ipfs.files.chmod('/path/to/file.txt', '777')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `path` | `string` |
| `mode` | `string` \| `number` |
| `options?` | [`ChmodOptions`](files.ChmodOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:22](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L22)

___

### cp

▸ **cp**(`from`, `to`, `options?`): `Promise`<`void`\>

Copy files from one location to another

- If from has multiple values then to must be a directory.
- If from has a single value and to exists and is a directory, from will be copied into to.
- If from has a single value and to exists and is a file, from must be a file and the contents of to will be replaced with the contents of from otherwise an error will be returned.
- If from is an IPFS path, and an MFS path exists with the same name, the IPFS path will be chosen.
- If from is an IPFS path and the content does not exist in your node's repo, only the root node of the source file with be retrieved from the network and linked to from the destination. The remainder of the file will be retrieved on demand.

**`example`**
```js
// To copy a file
await ipfs.files.cp('/src-file', '/dst-file')

// To copy a directory
await ipfs.files.cp('/src-dir', '/dst-dir')

// To copy multiple files to a directory
await ipfs.files.cp('/src-file1', '/src-file2', '/dst-dir')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `from` | `IPFSPath` \| `IPFSPath`[] |
| `to` | `string` |
| `options?` | [`CpOptions`](files.CpOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:45](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L45)

___

### flush

▸ **flush**(`ipfsPath`, `options?`): `Promise`<`CID`\>

Flush a given path's data to the disk

**`example`**
```js
const cid = await ipfs.files.flush('/')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[files/index.ts:146](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L146)

___

### ls

▸ **ls**(`ipfsPath`, `options?`): `AsyncIterable`<[`MFSEntry`](files.MFSEntry.md)\>

List directories in the local mutable namespace

**`example`**
```js
for await (const file of ipfs.files.ls('/screenshots')) {
  console.log(file.name)
}
// 2018-01-22T18:08:46.775Z.png
// 2018-01-22T18:08:49.184Z.png
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`MFSEntry`](files.MFSEntry.md)\>

#### Defined in

[files/index.ts:160](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L160)

___

### mkdir

▸ **mkdir**(`path`, `options?`): `Promise`<`void`\>

Make a directory in your MFS

#### Parameters

| Name | Type |
| :------ | :------ |
| `path` | `string` |
| `options?` | [`MkdirOptions`](files.MkdirOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:50](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L50)

___

### mv

▸ **mv**(`from`, `to`, `options?`): `Promise`<`void`\>

Move files from one location to another

- If from has multiple values then to must be a directory.
- If from has a single value and to exists and is a directory, from will be moved into to.
- If from has a single value and to exists and is a file, from must be a file and the contents of to will be replaced with the contents of from otherwise an error will be returned.
- If from is an IPFS path, and an MFS path exists with the same name, the IPFS path will be chosen.
- If from is an IPFS path and the content does not exist in your node's repo, only the root node of the source file with be retrieved from the network and linked to from the destination. The remainder of the file will be retrieved on demand.
- All values of from will be removed after the operation is complete unless they are an IPFS path.

**`example`**
```js
await ipfs.files.mv('/src-file', '/dst-file')

await ipfs.files.mv('/src-dir', '/dst-dir')

await ipfs.files.mv('/src-file1', '/src-file2', '/dst-dir')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `from` | `string` \| `string`[] |
| `to` | `string` |
| `options?` | [`MvOptions`](files.MvOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:136](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L136)

___

### read

▸ **read**(`ipfsPath`, `options?`): `AsyncIterable`<`Uint8Array`\>

Read a file

**`example`**
```js
const chunks = []

for await (const chunk of ipfs.files.read('/hello-world')) {
  chunks.push(chunk)
}

console.log(uint8ArrayConcat(chunks).toString())
// Hello, World!
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`ReadOptions`](files.ReadOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`Uint8Array`\>

#### Defined in

[files/index.ts:105](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L105)

___

### rm

▸ **rm**(`ipfsPaths`, `options?`): `Promise`<`void`\>

Remove a file or directory

**`example`**
```js
// To remove a file
await ipfs.files.rm('/my/beautiful/file.txt')

// To remove multiple files
await ipfs.files.rm(['/my/beautiful/file.txt', '/my/other/file.txt'])

// To remove a directory
await ipfs.files.rm('/my/beautiful/directory', { recursive: true })
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPaths` | `string` \| `string`[] |
| `options?` | [`RmOptions`](files.RmOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:88](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L88)

___

### stat

▸ **stat**(`ipfsPath`, `options?`): `Promise`<[`StatResult`](files.StatResult.md)\>

Get file or directory statistics

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`StatOptions`](files.StatOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`StatResult`](files.StatResult.md)\>

#### Defined in

[files/index.ts:55](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L55)

___

### touch

▸ **touch**(`ipfsPath`, `options?`): `Promise`<`void`\>

Update the mtime of a file or directory

**`example`**
```js
// set the mtime to the current time
await ipfs.files.touch('/path/to/file.txt')

// set the mtime to a specific time
await ipfs.files.touch('/path/to/file.txt', {
  mtime: new Date('May 23, 2014 14:45:14 -0700')
})
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `string` |
| `options?` | [`TouchOptions`](files.TouchOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:71](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L71)

___

### write

▸ **write**(`ipfsPath`, `content`, `options?`): `Promise`<`void`\>

Write to an MFS path

**`example`**
```js
await ipfs.files.write('/hello-world', new TextEncoder().encode('Hello, world!'))
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `string` |
| `content` | `string` \| `Blob` \| `Uint8Array` \| `Iterable`<`Uint8Array`\> \| `AsyncIterable`<`Uint8Array`\> |
| `options?` | [`WriteOptions`](files.WriteOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[files/index.ts:115](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L115)
