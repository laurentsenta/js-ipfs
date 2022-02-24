[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / GetOptions

# Interface: GetOptions

[root](../modules/root.md).GetOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`GetOptions`**

## Table of contents

### Properties

- [archive](root.GetOptions.md#archive)
- [compress](root.GetOptions.md#compress)
- [compressionLevel](root.GetOptions.md#compressionlevel)
- [preload](root.GetOptions.md#preload)
- [signal](root.GetOptions.md#signal)
- [timeout](root.GetOptions.md#timeout)

## Properties

### archive

• `Optional` **archive**: `boolean`

#### Defined in

[root.ts:260](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L260)

___

### compress

• `Optional` **compress**: `boolean`

#### Defined in

[root.ts:261](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L261)

___

### compressionLevel

• `Optional` **compressionLevel**: ``0`` \| ``1`` \| ``-1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9``

#### Defined in

[root.ts:262](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L262)

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
