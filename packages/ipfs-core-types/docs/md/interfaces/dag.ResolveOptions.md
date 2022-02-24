[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / ResolveOptions

# Interface: ResolveOptions

[dag](../modules/dag.md).ResolveOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`ResolveOptions`**

## Table of contents

### Properties

- [path](dag.ResolveOptions.md#path)
- [preload](dag.ResolveOptions.md#preload)
- [signal](dag.ResolveOptions.md#signal)
- [timeout](dag.ResolveOptions.md#timeout)

## Properties

### path

• `Optional` **path**: `string`

If ipfsPath is a CID, you may pass a path here

#### Defined in

[dag/index.ts:188](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L188)

___

### preload

• `Optional` **preload**: `boolean`

#### Inherited from

PreloadOptions.preload

#### Defined in

[utils.ts:113](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L113)

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
