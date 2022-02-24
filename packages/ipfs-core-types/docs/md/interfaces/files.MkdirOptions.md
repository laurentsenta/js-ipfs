[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / MkdirOptions

# Interface: MkdirOptions

[files](../modules/files.md).MkdirOptions

## Hierarchy

- [`MFSOptions`](files.MFSOptions.md)

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`MkdirOptions`**

## Table of contents

### Properties

- [cidVersion](files.MkdirOptions.md#cidversion)
- [flush](files.MkdirOptions.md#flush)
- [hashAlg](files.MkdirOptions.md#hashalg)
- [mode](files.MkdirOptions.md#mode)
- [mtime](files.MkdirOptions.md#mtime)
- [parents](files.MkdirOptions.md#parents)
- [shardSplitThreshold](files.MkdirOptions.md#shardsplitthreshold)
- [signal](files.MkdirOptions.md#signal)
- [timeout](files.MkdirOptions.md#timeout)

## Properties

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use for any updated entries

#### Defined in

[files/index.ts:270](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L270)

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

[files/index.ts:265](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L265)

___

### mode

• `Optional` **mode**: `number`

An integer that represents the file mode

#### Defined in

[files/index.ts:255](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L255)

___

### mtime

• `Optional` **mtime**: `MtimeLike`

A Date object, an object with { secs, nsecs } properties where secs is the number of seconds since (positive) or before (negative) the Unix Epoch began and nsecs is the number of nanoseconds since the last full second, or the output of process.hrtime()

#### Defined in

[files/index.ts:260](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L260)

___

### parents

• `Optional` **parents**: `boolean`

If true, create intermediate directories

#### Defined in

[files/index.ts:250](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L250)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

The threshold for splitting any modified folders into HAMT shards

#### Defined in

[files/index.ts:275](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L275)

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
