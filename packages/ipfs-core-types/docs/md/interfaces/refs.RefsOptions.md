[ipfs-core-types](../README.md) / [Modules](../modules.md) / [refs](../modules/refs.md) / RefsOptions

# Interface: RefsOptions

[refs](../modules/refs.md).RefsOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`RefsOptions`**

## Table of contents

### Properties

- [edges](refs.RefsOptions.md#edges)
- [format](refs.RefsOptions.md#format)
- [maxDepth](refs.RefsOptions.md#maxdepth)
- [preload](refs.RefsOptions.md#preload)
- [recursive](refs.RefsOptions.md#recursive)
- [signal](refs.RefsOptions.md#signal)
- [timeout](refs.RefsOptions.md#timeout)
- [unique](refs.RefsOptions.md#unique)

## Properties

### edges

• `Optional` **edges**: `boolean`

#### Defined in

[refs/index.ts:21](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/refs/index.ts#L21)

___

### format

• `Optional` **format**: `string`

#### Defined in

[refs/index.ts:20](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/refs/index.ts#L20)

___

### maxDepth

• `Optional` **maxDepth**: `number`

#### Defined in

[refs/index.ts:22](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/refs/index.ts#L22)

___

### preload

• `Optional` **preload**: `boolean`

#### Inherited from

PreloadOptions.preload

#### Defined in

[utils.ts:113](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L113)

___

### recursive

• `Optional` **recursive**: `boolean`

#### Defined in

[refs/index.ts:18](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/refs/index.ts#L18)

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

___

### unique

• `Optional` **unique**: `boolean`

#### Defined in

[refs/index.ts:19](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/refs/index.ts#L19)
