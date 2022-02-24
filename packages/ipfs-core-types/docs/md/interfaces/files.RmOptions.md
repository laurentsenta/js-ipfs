[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / RmOptions

# Interface: RmOptions

[files](../modules/files.md).RmOptions

## Hierarchy

- [`MFSOptions`](files.MFSOptions.md)

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`RmOptions`**

## Table of contents

### Properties

- [cidVersion](files.RmOptions.md#cidversion)
- [flush](files.RmOptions.md#flush)
- [hashAlg](files.RmOptions.md#hashalg)
- [recursive](files.RmOptions.md#recursive)
- [shardSplitThreshold](files.RmOptions.md#shardsplitthreshold)
- [signal](files.RmOptions.md#signal)
- [timeout](files.RmOptions.md#timeout)

## Properties

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use for any updated entries

#### Defined in

[files/index.ts:383](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L383)

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

[files/index.ts:378](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L378)

___

### recursive

• `Optional` **recursive**: `boolean`

If true all paths under the specifed path(s) will be removed

#### Defined in

[files/index.ts:373](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L373)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

The threshold for splitting any modified folders into HAMT shards

#### Defined in

[files/index.ts:388](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L388)

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
