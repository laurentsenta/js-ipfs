[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / AddOptions

# Interface: AddOptions

[root](../modules/root.md).AddOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`AddOptions`**

  ↳↳ [`AddAllOptions`](root.AddAllOptions.md)

## Table of contents

### Properties

- [blockWriteConcurrency](root.AddOptions.md#blockwriteconcurrency)
- [chunker](root.AddOptions.md#chunker)
- [cidVersion](root.AddOptions.md#cidversion)
- [hashAlg](root.AddOptions.md#hashalg)
- [onlyHash](root.AddOptions.md#onlyhash)
- [pin](root.AddOptions.md#pin)
- [preload](root.AddOptions.md#preload)
- [progress](root.AddOptions.md#progress)
- [rawLeaves](root.AddOptions.md#rawleaves)
- [signal](root.AddOptions.md#signal)
- [timeout](root.AddOptions.md#timeout)
- [trickle](root.AddOptions.md#trickle)
- [wrapWithDirectory](root.AddOptions.md#wrapwithdirectory)

## Properties

### blockWriteConcurrency

• `Optional` **blockWriteConcurrency**: `number`

How many blocks from a file to write concurrently

#### Defined in

[root.ts:212](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L212)

___

### chunker

• `Optional` **chunker**: `string`

Chunking algorithm used to build ipfs DAGs. (defaults to 'size-262144')

#### Defined in

[root.ts:157](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L157)

___

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use when storing the data

#### Defined in

[root.ts:161](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L161)

___

### hashAlg

• `Optional` **hashAlg**: `string`

Multihash hashing algorithm to use. (Defaults to 'sha2-256')

#### Defined in

[root.ts:166](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L166)

___

### onlyHash

• `Optional` **onlyHash**: `boolean`

If true, will not add blocks to the blockstore. (Defaults to `false`)

#### Defined in

[root.ts:171](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L171)

___

### pin

• `Optional` **pin**: `boolean`

Pin this object when adding. (Defaults to `true`)

#### Defined in

[root.ts:176](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L176)

___

### preload

• `Optional` **preload**: `boolean`

Whether to preload all blocks created during this operation

#### Defined in

[root.ts:207](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L207)

___

### progress

• `Optional` **progress**: [`AddProgressFn`](root.AddProgressFn.md)

A function that will be called with the number of bytes added as a file is
added to ipfs and the path of the file being added.

**Note** It will not be called for directory entries.

#### Defined in

[root.ts:184](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L184)

___

### rawLeaves

• `Optional` **rawLeaves**: `boolean`

If true, DAG leaves will contain raw file data and not be wrapped in a
protobuf. (Defaults to `false`)

#### Defined in

[root.ts:190](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L190)

___

### signal

• `Optional` **signal**: `AbortSignal`

Can be provided to a function that starts a long running task, which will
be aborted when signal is triggered.

#### Inherited from

[AbortOptions](index.AbortOptions.md).[signal](index.AbortOptions.md#signal)

#### Defined in

[utils.ts:104](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L104)

___

### timeout

• `Optional` **timeout**: `number`

Can be provided to a function that starts a long running task, which will
be aborted after provided timeout (in ms).

#### Inherited from

[AbortOptions](index.AbortOptions.md).[timeout](index.AbortOptions.md#timeout)

#### Defined in

[utils.ts:109](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L109)

___

### trickle

• `Optional` **trickle**: `boolean`

If true will use the
[trickle DAG](https://godoc.org/github.com/ipsn/go-ipfs/gxlibs/github.com/ipfs/go-unixfs/importer/trickle)
format for DAG generation. (Defaults to `false`).

#### Defined in

[root.ts:197](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L197)

___

### wrapWithDirectory

• `Optional` **wrapWithDirectory**: `boolean`

Adds a wrapping node around the content. (Defaults to `false`)

#### Defined in

[root.ts:202](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L202)
