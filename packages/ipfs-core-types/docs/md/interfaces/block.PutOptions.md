[ipfs-core-types](../README.md) / [Modules](../modules.md) / [block](../modules/block.md) / PutOptions

# Interface: PutOptions

[block](../modules/block.md).PutOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`PutOptions`**

## Table of contents

### Properties

- [format](block.PutOptions.md#format)
- [mhtype](block.PutOptions.md#mhtype)
- [pin](block.PutOptions.md#pin)
- [preload](block.PutOptions.md#preload)
- [signal](block.PutOptions.md#signal)
- [timeout](block.PutOptions.md#timeout)
- [version](block.PutOptions.md#version)

## Properties

### format

• `Optional` **format**: `string`

The codec to use to create the CID

#### Defined in

[block/index.ts:88](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L88)

___

### mhtype

• `Optional` **mhtype**: `string`

Multihash hashing algorithm to use. (Defaults to 'sha2-256')

#### Defined in

[block/index.ts:93](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L93)

___

### pin

• `Optional` **pin**: `boolean`

Pin this block when adding. (Defaults to `false`)

#### Defined in

[block/index.ts:103](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L103)

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

___

### version

• `Optional` **version**: `CIDVersion`

The version to use to create the CID

#### Defined in

[block/index.ts:98](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L98)
