[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pin](../modules/pin.md) / AddOptions

# Interface: AddOptions

[pin](../modules/pin.md).AddOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`AddOptions`**

## Table of contents

### Properties

- [lock](pin.AddOptions.md#lock)
- [preload](pin.AddOptions.md#preload)
- [recursive](pin.AddOptions.md#recursive)
- [signal](pin.AddOptions.md#signal)
- [timeout](pin.AddOptions.md#timeout)

## Properties

### lock

• `Optional` **lock**: `boolean`

Internal option used to control whether to create a repo write lock during a pinning operation

#### Defined in

[pin/index.ts:112](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L112)

___

### preload

• `Optional` **preload**: `boolean`

Whether to preload all blocks pinned during this operation

#### Defined in

[pin/index.ts:107](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L107)

___

### recursive

• `Optional` **recursive**: `boolean`

If true, pin all blocked linked to from the pinned CID

#### Defined in

[pin/index.ts:102](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L102)

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
