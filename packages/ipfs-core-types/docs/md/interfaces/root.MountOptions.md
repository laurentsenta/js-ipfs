[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / MountOptions

# Interface: MountOptions

[root](../modules/root.md).MountOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`MountOptions`**

## Table of contents

### Properties

- [ipfsPath](root.MountOptions.md#ipfspath)
- [ipnsPath](root.MountOptions.md#ipnspath)
- [signal](root.MountOptions.md#signal)
- [timeout](root.MountOptions.md#timeout)

## Properties

### ipfsPath

• `Optional` **ipfsPath**: `string`

#### Defined in

[root.ts:319](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L319)

___

### ipnsPath

• `Optional` **ipnsPath**: `string`

#### Defined in

[root.ts:320](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L320)

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
