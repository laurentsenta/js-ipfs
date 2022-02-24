[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / CpOptions

# Interface: CpOptions

[files](../modules/files.md).CpOptions

## Hierarchy

- [`MFSOptions`](files.MFSOptions.md)

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`CpOptions`**

## Table of contents

### Properties

- [cidVersion](files.CpOptions.md#cidversion)
- [flush](files.CpOptions.md#flush)
- [hashAlg](files.CpOptions.md#hashalg)
- [parents](files.CpOptions.md#parents)
- [shardSplitThreshold](files.CpOptions.md#shardsplitthreshold)
- [signal](files.CpOptions.md#signal)
- [timeout](files.CpOptions.md#timeout)

## Properties

### cidVersion

• `Optional` **cidVersion**: `CIDVersion`

The CID version to use for any updated entries

#### Defined in

[files/index.ts:238](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L238)

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

[files/index.ts:233](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L233)

___

### parents

• `Optional` **parents**: `boolean`

The value or node that was fetched during the get operation

#### Defined in

[files/index.ts:228](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L228)

___

### shardSplitThreshold

• `Optional` **shardSplitThreshold**: `number`

The threshold for splitting any modified folders into HAMT shards

#### Defined in

[files/index.ts:243](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L243)

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
