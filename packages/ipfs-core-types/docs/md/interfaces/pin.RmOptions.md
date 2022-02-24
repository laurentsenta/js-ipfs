[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pin](../modules/pin.md) / RmOptions

# Interface: RmOptions

[pin](../modules/pin.md).RmOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`RmOptions`**

## Table of contents

### Properties

- [recursive](pin.RmOptions.md#recursive)
- [signal](pin.RmOptions.md#signal)
- [timeout](pin.RmOptions.md#timeout)

## Properties

### recursive

• `Optional` **recursive**: `boolean`

#### Defined in

[pin/index.ts:167](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L167)

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
