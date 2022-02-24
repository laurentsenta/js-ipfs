[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / StatOptions

# Interface: StatOptions

[files](../modules/files.md).StatOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`StatOptions`**

## Table of contents

### Properties

- [hash](files.StatOptions.md#hash)
- [signal](files.StatOptions.md#signal)
- [size](files.StatOptions.md#size)
- [timeout](files.StatOptions.md#timeout)
- [withLocal](files.StatOptions.md#withlocal)

## Properties

### hash

• `Optional` **hash**: `boolean`

If true, return only the CID

#### Defined in

[files/index.ts:282](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L282)

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

### size

• `Optional` **size**: `boolean`

If true, return only the size

#### Defined in

[files/index.ts:287](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L287)

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

### withLocal

• `Optional` **withLocal**: `boolean`

If true, compute the amount of the DAG that is local and if possible the total size

#### Defined in

[files/index.ts:292](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L292)
