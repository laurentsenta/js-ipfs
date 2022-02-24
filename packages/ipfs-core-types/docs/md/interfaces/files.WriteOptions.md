[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / WriteOptions

# Interface: WriteOptions

[files](../modules/files.md).WriteOptions

## Hierarchy

- [`MFSOptions`](files.MFSOptions.md)

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`WriteOptions`**

## Table of contents

### Properties

- [cidVersion](files.WriteOptions.md#cidversion)
- [create](files.WriteOptions.md#create)
- [flush](files.WriteOptions.md#flush)
- [hashAlg](files.WriteOptions.md#hashalg)
- [length](files.WriteOptions.md#length)
- [mode](files.WriteOptions.md#mode)
- [mtime](files.WriteOptions.md#mtime)
- [offset](files.WriteOptions.md#offset)
- [parents](files.WriteOptions.md#parents)
- [progress](files.WriteOptions.md#progress)
- [rawLeaves](files.WriteOptions.md#rawleaves)
- [reduceSingleLeafToSelf](files.WriteOptions.md#reducesingleleaftoself)
- [shardSplitThreshold](files.WriteOptions.md#shardsplitthreshold)
- [signal](files.WriteOptions.md#signal)
- [strategy](files.WriteOptions.md#strategy)
- [timeout](files.WriteOptions.md#timeout)
- [truncate](files.WriteOptions.md#truncate)

## Properties

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use for any updated entries

#### Defined in

[files/index.ts:452](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L452)

___

### create

• `Optional` **create**: `boolean`

Create the MFS path if it does not exist

#### Defined in

[files/index.ts:417](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L417)

___

### flush

• `Optional` **flush**: `boolean`

If true the changes will be immediately flushed to disk

#### Inherited from

[MFSOptions](files.MFSOptions.md).[flush](files.MFSOptions.md#flush)

#### Defined in

[files/index.ts:199](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L199)

___

### hashAlg

• `Optional` **hashAlg**: `string`

The hash algorithm to use for any updated entries

#### Defined in

[files/index.ts:447](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L447)

___

### length

• `Optional` **length**: `number`

Optionally limit how many bytes are written

#### Defined in

[files/index.ts:412](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L412)

___

### mode

• `Optional` **mode**: `number`

An integer that represents the file mode

#### Defined in

[files/index.ts:437](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L437)

___

### mtime

• `Optional` **mtime**: `MtimeLike`

A Date object, an object with { secs, nsecs } properties where secs is the number of seconds since (positive) or before (negative) the Unix Epoch began and nsecs is the number of nanoseconds since the last full second, or the output of process.hrtime()

#### Defined in

[files/index.ts:442](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L442)

___

### offset

• `Optional` **offset**: `number`

An offset within the file to start writing at

#### Defined in

[files/index.ts:407](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L407)

___

### parents

• `Optional` **parents**: `boolean`

Create intermediate MFS paths if they do not exist

#### Defined in

[files/index.ts:422](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L422)

___

### progress

• `Optional` **progress**: [`AddProgressFn`](root.AddProgressFn.md)

Callback to be notified of write progress

#### Defined in

[files/index.ts:472](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L472)

___

### rawLeaves

• `Optional` **rawLeaves**: `boolean`

If true, DAG leaves will contain raw file data and not be wrapped in a protobuf

#### Defined in

[files/index.ts:432](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L432)

___

### reduceSingleLeafToSelf

• `Optional` **reduceSingleLeafToSelf**: `boolean`

If writing a file and only a single leaf would be present, store the file data in the root node

#### Defined in

[files/index.ts:462](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L462)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

The threshold for splitting any modified folders into HAMT shards

#### Defined in

[files/index.ts:457](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L457)

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

### strategy

• `Optional` **strategy**: ``"balanced"`` \| ``"trickle"``

What sort of DAG structure to create

#### Defined in

[files/index.ts:467](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L467)

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

### truncate

• `Optional` **truncate**: `boolean`

Truncate the file at the MFS path if it would have been larger than the passed content

#### Defined in

[files/index.ts:427](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L427)
