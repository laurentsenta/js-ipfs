[ipfs-core-types](../README.md) / [Modules](../modules.md) / [object](../modules/object.md) / PutOptions

# Interface: PutOptions

[object](../modules/object.md).PutOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`PutOptions`**

## Table of contents

### Properties

- [pin](object.PutOptions.md#pin)
- [preload](object.PutOptions.md#preload)
- [signal](object.PutOptions.md#signal)
- [timeout](object.PutOptions.md#timeout)

## Properties

### pin

• `Optional` **pin**: `boolean`

#### Defined in

[object/index.ts:31](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L31)

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
