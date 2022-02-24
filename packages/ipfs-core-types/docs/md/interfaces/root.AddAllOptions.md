[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / AddAllOptions

# Interface: AddAllOptions

[root](../modules/root.md).AddAllOptions

## Hierarchy

- [`AddOptions`](root.AddOptions.md)

  ↳ **`AddAllOptions`**

## Table of contents

### Properties

- [blockWriteConcurrency](root.AddAllOptions.md#blockwriteconcurrency)
- [chunker](root.AddAllOptions.md#chunker)
- [cidVersion](root.AddAllOptions.md#cidversion)
- [enableShardingExperiment](root.AddAllOptions.md#enableshardingexperiment)
- [fileImportConcurrency](root.AddAllOptions.md#fileimportconcurrency)
- [hashAlg](root.AddAllOptions.md#hashalg)
- [onlyHash](root.AddAllOptions.md#onlyhash)
- [pin](root.AddAllOptions.md#pin)
- [preload](root.AddAllOptions.md#preload)
- [progress](root.AddAllOptions.md#progress)
- [rawLeaves](root.AddAllOptions.md#rawleaves)
- [shardSplitThreshold](root.AddAllOptions.md#shardsplitthreshold)
- [signal](root.AddAllOptions.md#signal)
- [timeout](root.AddAllOptions.md#timeout)
- [trickle](root.AddAllOptions.md#trickle)
- [wrapWithDirectory](root.AddAllOptions.md#wrapwithdirectory)

## Properties

### blockWriteConcurrency

• `Optional` **blockWriteConcurrency**: `number`

How many blocks from a file to write concurrently

#### Inherited from

[AddOptions](root.AddOptions.md).[blockWriteConcurrency](root.AddOptions.md#blockwriteconcurrency)

#### Defined in

[root.ts:212](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L212)

___

### chunker

• `Optional` **chunker**: `string`

Chunking algorithm used to build ipfs DAGs. (defaults to 'size-262144')

#### Inherited from

[AddOptions](root.AddOptions.md).[chunker](root.AddOptions.md#chunker)

#### Defined in

[root.ts:157](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L157)

___

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use when storing the data

#### Inherited from

[AddOptions](root.AddOptions.md).[cidVersion](root.AddOptions.md#cidversion)

#### Defined in

[root.ts:161](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L161)

___

### enableShardingExperiment

• `Optional` **enableShardingExperiment**: `boolean`

Allows to create directories with an unlimited number of entries currently
size of unixfs directories is limited by the maximum block size.
** Note ** that this is an experimental feature. (Defaults to `false`)

#### Defined in

[root.ts:222](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L222)

___

### fileImportConcurrency

• `Optional` **fileImportConcurrency**: `number`

How many files to write concurrently

#### Defined in

[root.ts:233](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L233)

___

### hashAlg

• `Optional` **hashAlg**: `string`

Multihash hashing algorithm to use. (Defaults to 'sha2-256')

#### Inherited from

[AddOptions](root.AddOptions.md).[hashAlg](root.AddOptions.md#hashalg)

#### Defined in

[root.ts:166](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L166)

___

### onlyHash

• `Optional` **onlyHash**: `boolean`

If true, will not add blocks to the blockstore. (Defaults to `false`)

#### Inherited from

[AddOptions](root.AddOptions.md).[onlyHash](root.AddOptions.md#onlyhash)

#### Defined in

[root.ts:171](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L171)

___

### pin

• `Optional` **pin**: `boolean`

Pin this object when adding. (Defaults to `true`)

#### Inherited from

[AddOptions](root.AddOptions.md).[pin](root.AddOptions.md#pin)

#### Defined in

[root.ts:176](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L176)

___

### preload

• `Optional` **preload**: `boolean`

Whether to preload all blocks created during this operation

#### Inherited from

[AddOptions](root.AddOptions.md).[preload](root.AddOptions.md#preload)

#### Defined in

[root.ts:207](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L207)

___

### progress

• `Optional` **progress**: [`AddProgressFn`](root.AddProgressFn.md)

A function that will be called with the number of bytes added as a file is
added to ipfs and the path of the file being added.

**Note** It will not be called for directory entries.

#### Inherited from

[AddOptions](root.AddOptions.md).[progress](root.AddOptions.md#progress)

#### Defined in

[root.ts:184](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L184)

___

### rawLeaves

• `Optional` **rawLeaves**: `boolean`

If true, DAG leaves will contain raw file data and not be wrapped in a
protobuf. (Defaults to `false`)

#### Inherited from

[AddOptions](root.AddOptions.md).[rawLeaves](root.AddOptions.md#rawleaves)

#### Defined in

[root.ts:190](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L190)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

Directories with more than this number of files will be created as HAMT -
sharded directories. (Defaults to 1000)

#### Defined in

[root.ts:228](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L228)

___

### signal

• `Optional` **signal**: `AbortSignal`

Can be provided to a function that starts a long running task, which will
be aborted when signal is triggered.

#### Inherited from

[AddOptions](root.AddOptions.md).[signal](root.AddOptions.md#signal)

#### Defined in

[utils.ts:104](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L104)

___

### timeout

• `Optional` **timeout**: `number`

Can be provided to a function that starts a long running task, which will
be aborted after provided timeout (in ms).

#### Inherited from

[AddOptions](root.AddOptions.md).[timeout](root.AddOptions.md#timeout)

#### Defined in

[utils.ts:109](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L109)

___

### trickle

• `Optional` **trickle**: `boolean`

If true will use the
[trickle DAG](https://godoc.org/github.com/ipsn/go-ipfs/gxlibs/github.com/ipfs/go-unixfs/importer/trickle)
format for DAG generation. (Defaults to `false`).

#### Inherited from

[AddOptions](root.AddOptions.md).[trickle](root.AddOptions.md#trickle)

#### Defined in

[root.ts:197](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L197)

___

### wrapWithDirectory

• `Optional` **wrapWithDirectory**: `boolean`

Adds a wrapping node around the content. (Defaults to `false`)

#### Inherited from

[AddOptions](root.AddOptions.md).[wrapWithDirectory](root.AddOptions.md#wrapwithdirectory)

#### Defined in

[root.ts:202](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L202)
