[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / MvOptions

# Interface: MvOptions

[files](../modules/files.md).MvOptions

## Hierarchy

- [`MFSOptions`](files.MFSOptions.md)

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`MvOptions`**

## Table of contents

### Properties

- [cidVersion](files.MvOptions.md#cidversion)
- [flush](files.MvOptions.md#flush)
- [hashAlg](files.MvOptions.md#hashalg)
- [parents](files.MvOptions.md#parents)
- [shardSplitThreshold](files.MvOptions.md#shardsplitthreshold)
- [signal](files.MvOptions.md#signal)
- [timeout](files.MvOptions.md#timeout)

## Properties

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use for any updated entries

#### Defined in

[files/index.ts:489](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L489)

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

[files/index.ts:484](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L484)

___

### parents

• `Optional` **parents**: `boolean`

Create intermediate MFS paths if they do not exist

#### Defined in

[files/index.ts:479](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L479)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

The threshold for splitting any modified folders into HAMT shards

#### Defined in

[files/index.ts:494](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L494)

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
