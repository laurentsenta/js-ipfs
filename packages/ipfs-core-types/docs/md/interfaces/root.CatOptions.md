[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / CatOptions

# Interface: CatOptions

[root](../modules/root.md).CatOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`CatOptions`**

## Table of contents

### Properties

- [length](root.CatOptions.md#length)
- [offset](root.CatOptions.md#offset)
- [preload](root.CatOptions.md#preload)
- [signal](root.CatOptions.md#signal)
- [timeout](root.CatOptions.md#timeout)

## Properties

### length

• `Optional` **length**: `number`

An optional max length to read from the file

#### Defined in

[root.ts:256](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L256)

___

### offset

• `Optional` **offset**: `number`

An offset to start reading the file from

#### Defined in

[root.ts:252](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L252)

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
