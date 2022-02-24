[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pin](../modules/pin.md) / AddAllOptions

# Interface: AddAllOptions

[pin](../modules/pin.md).AddAllOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`AddAllOptions`**

## Table of contents

### Properties

- [lock](pin.AddAllOptions.md#lock)
- [preload](pin.AddAllOptions.md#preload)
- [signal](pin.AddAllOptions.md#signal)
- [timeout](pin.AddAllOptions.md#timeout)

## Properties

### lock

• `Optional` **lock**: `boolean`

Internal option used to control whether to create a repo write lock during a pinning operation

#### Defined in

[pin/index.ts:124](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L124)

___

### preload

• `Optional` **preload**: `boolean`

Whether to preload all blocks pinned during this operation

#### Defined in

[pin/index.ts:119](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L119)

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
