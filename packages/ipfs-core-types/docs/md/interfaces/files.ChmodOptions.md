[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / ChmodOptions

# Interface: ChmodOptions

[files](../modules/files.md).ChmodOptions

## Hierarchy

- [`MFSOptions`](files.MFSOptions.md)

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`ChmodOptions`**

## Table of contents

### Properties

- [cidVersion](files.ChmodOptions.md#cidversion)
- [flush](files.ChmodOptions.md#flush)
- [hashAlg](files.ChmodOptions.md#hashalg)
- [recursive](files.ChmodOptions.md#recursive)
- [shardSplitThreshold](files.ChmodOptions.md#shardsplitthreshold)
- [signal](files.ChmodOptions.md#signal)
- [timeout](files.ChmodOptions.md#timeout)

## Properties

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use for any updated entries

#### Defined in

[files/index.ts:216](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L216)

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

[files/index.ts:211](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L211)

___

### recursive

• `Optional` **recursive**: `boolean`

If true mode will be applied to the entire tree under path

#### Defined in

[files/index.ts:206](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L206)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

The threshold for splitting any modified folders into HAMT shards

#### Defined in

[files/index.ts:221](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L221)

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
