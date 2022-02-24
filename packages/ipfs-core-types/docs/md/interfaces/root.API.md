[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / API

# Interface: API<OptionExtension\>

[root](../modules/root.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Hierarchy

- **`API`**

  ↳ [`IPFS`](index.IPFS.md)

## Table of contents

### Methods

- [add](root.API.md#add)
- [addAll](root.API.md#addall)
- [cat](root.API.md#cat)
- [commands](root.API.md#commands)
- [dns](root.API.md#dns)
- [get](root.API.md#get)
- [id](root.API.md#id)
- [isOnline](root.API.md#isonline)
- [ls](root.API.md#ls)
- [mount](root.API.md#mount)
- [ping](root.API.md#ping)
- [resolve](root.API.md#resolve)
- [start](root.API.md#start)
- [stop](root.API.md#stop)
- [version](root.API.md#version)

## Methods

### add

▸ **add**(`entry`, `options?`): `Promise`<[`AddResult`](root.AddResult.md)\>

Import a file or data into IPFS

#### Parameters

| Name | Type |
| :------ | :------ |
| `entry` | `ImportCandidate` |
| `options?` | [`AddOptions`](root.AddOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`AddResult`](root.AddResult.md)\>

#### Defined in

[root.ts:10](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L10)

___

### addAll

▸ **addAll**(`source`, `options?`): `AsyncIterable`<[`AddResult`](root.AddResult.md)\>

Import multiple files and data into IPFS

#### Parameters

| Name | Type |
| :------ | :------ |
| `source` | `ImportCandidateStream` |
| `options?` | [`AddAllOptions`](root.AddAllOptions.md) & [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`AddResult`](root.AddResult.md)\>

#### Defined in

[root.ts:15](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L15)

___

### cat

▸ **cat**(`ipfsPath`, `options?`): `AsyncIterable`<`Uint8Array`\>

Returns content of the file addressed by a valid IPFS Path or CID

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`CatOptions`](root.CatOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`Uint8Array`\>

#### Defined in

[root.ts:20](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L20)

___

### commands

▸ **commands**(`options?`): `Promise`<`string`[]\>

Returns a list of available commands

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[root.ts:130](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L130)

___

### dns

▸ **dns**(`domain`, `options?`): `Promise`<`string`\>

Resolve DNS links

#### Parameters

| Name | Type |
| :------ | :------ |
| `domain` | `string` |
| `options?` | [`DNSOptions`](root.DNSOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string`\>

#### Defined in

[root.ts:58](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L58)

___

### get

▸ **get**(`ipfsPath`, `options?`): `AsyncIterable`<`Uint8Array`\>

Fetch a file or an entire directory tree from IPFS that is addressed by a
valid IPFS Path

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`GetOptions`](root.GetOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`Uint8Array`\>

#### Defined in

[root.ts:26](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L26)

___

### id

▸ **id**(`options?`): `Promise`<[`IDResult`](root.IDResult.md)\>

Returns the identity of the Peer

**`example`**
```js
const identity = await ipfs.id()
console.log(identity)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`IDOptions`](root.IDOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`IDResult`](root.IDResult.md)\>

#### Defined in

[root.ts:42](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L42)

___

### isOnline

▸ **isOnline**(): `boolean`

Returns true if this IPFS node is online - that is, it's listening on network addresses
for incoming connections

#### Returns

`boolean`

#### Defined in

[root.ts:138](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L138)

___

### ls

▸ **ls**(`ipfsPath`, `options?`): `AsyncIterable`<[`IPFSEntry`](root.IPFSEntry.md)\>

Lists a directory from IPFS that is addressed by a valid IPFS Path

#### Parameters

| Name | Type |
| :------ | :------ |
| `ipfsPath` | `IPFSPath` |
| `options?` | [`ListOptions`](root.ListOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`IPFSEntry`](root.IPFSEntry.md)\>

#### Defined in

[root.ts:31](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L31)

___

### mount

▸ **mount**(`options?`): `Promise`<[`MountResult`](root.MountResult.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`MountOptions`](root.MountOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`MountResult`](root.MountResult.md)\>

#### Defined in

[root.ts:132](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L132)

___

### ping

▸ **ping**(`peerId`, `options?`): `AsyncIterable`<[`PingResult`](root.PingResult.md)\>

Send echo request packets to IPFS hosts.

**`example`**
```js
for await (const res of ipfs.ping('Qmhash')) {
  if (res.time) {
    console.log(`Pong received: time=${res.time} ms`)
  } else {
    console.log(res.text)
  }
}
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `peerId` | `string` |
| `options?` | [`PingOptions`](root.PingOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`PingResult`](root.PingResult.md)\>

#### Defined in

[root.ts:84](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L84)

___

### resolve

▸ **resolve**(`name`, `options?`): `Promise`<`string`\>

Resolve the value of names to IPFS

There are a number of mutable name protocols that can link among themselves
and into IPNS. For example IPNS references can (currently) point at an IPFS
object, and DNS links can point at other DNS links, IPNS entries, or IPFS
objects. This command accepts any of these identifiers and resolves them
to the referenced item.

**`example`**
```js
// Resolve the value of your identity:
const name = '/ipns/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy'

const res = await ipfs.resolve(name)
console.log(res)
// Logs: /ipfs/Qmcqtw8FfrVSBaRmbWwHxt3AuySBhJLcvmFYi3Lbc4xnwj

// Resolve the value of another name recursively:
const name = '/ipns/QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n'

// Where:
// /ipns/QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n
// ...resolves to:
// /ipns/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
// ...which in turn resolves to:
// /ipfs/Qmcqtw8FfrVSBaRmbWwHxt3AuySBhJLcvmFYi3Lbc4xnwj

const res = await ipfs.resolve(name, { recursive: true })
console.log(res)
// Logs: /ipfs/Qmcqtw8FfrVSBaRmbWwHxt3AuySBhJLcvmFYi3Lbc4xnwj

// Resolve the value of an IPFS path:
const name = '/ipfs/QmeZy1fGbwgVSrqbfh9fKQrAWgeyRnj7h8fsHS1oy3k99x/beep/boop'
const res = await ipfs.resolve(name)
console.log(res)
// Logs: /ipfs/QmYRMjyvAiHKN9UTi8Bzt1HUspmSRD8T8DwxfSMzLgBon1
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `options?` | [`ResolveOptions`](root.ResolveOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string`\>

#### Defined in

[root.ts:125](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L125)

___

### start

▸ **start**(): `Promise`<`void`\>

Start the node

#### Returns

`Promise`<`void`\>

#### Defined in

[root.ts:63](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L63)

___

### stop

▸ **stop**(`options?`): `Promise`<`void`\>

Stop the node

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[root.ts:68](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L68)

___

### version

▸ **version**(`options?`): `Promise`<[`VersionResult`](root.VersionResult.md)\>

Returns the implementation version

**`example`**
```js
const version = await ipfs.version()
console.log(version)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`VersionResult`](root.VersionResult.md)\>

#### Defined in

[root.ts:53](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L53)
