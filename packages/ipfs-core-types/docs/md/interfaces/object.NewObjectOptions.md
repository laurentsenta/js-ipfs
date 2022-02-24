[ipfs-core-types](../README.md) / [Modules](../modules.md) / [object](../modules/object.md) / NewObjectOptions

# Interface: NewObjectOptions

[object](../modules/object.md).NewObjectOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`NewObjectOptions`**

## Table of contents

### Properties

- [preload](object.NewObjectOptions.md#preload)
- [signal](object.NewObjectOptions.md#signal)
- [template](object.NewObjectOptions.md#template)
- [timeout](object.NewObjectOptions.md#timeout)

## Properties

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

### template

• `Optional` **template**: ``"unixfs-dir"``

#### Defined in

[object/index.ts:18](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L18)

___

### timeout

• `Optional` **timeout**: `number`

Can be provided to a function that starts a long running task, which will
be aborted after provided timeout (in ms).

#### Inherited from

[AbortOptions](index.AbortOptions.md).[timeout](index.AbortOptions.md#timeout)

#### Defined in

[utils.ts:109](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L109)
