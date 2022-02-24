[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / ImportOptions

# Interface: ImportOptions

[dag](../modules/dag.md).ImportOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`ImportOptions`**

## Table of contents

### Properties

- [pinRoots](dag.ImportOptions.md#pinroots)
- [preload](dag.ImportOptions.md#preload)
- [signal](dag.ImportOptions.md#signal)
- [timeout](dag.ImportOptions.md#timeout)

## Properties

### pinRoots

• `Optional` **pinRoots**: `boolean`

Recursively pin roots for the imported CARs, defaults to true.

#### Defined in

[dag/index.ts:210](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L210)

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
