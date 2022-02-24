[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / ReadOptions

# Interface: ReadOptions

[files](../modules/files.md).ReadOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`ReadOptions`**

## Table of contents

### Properties

- [length](files.ReadOptions.md#length)
- [offset](files.ReadOptions.md#offset)
- [signal](files.ReadOptions.md#signal)
- [timeout](files.ReadOptions.md#timeout)

## Properties

### length

• `Optional` **length**: `number`

An optional max length to read from the file

#### Defined in

[files/index.ts:400](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L400)

___

### offset

• `Optional` **offset**: `number`

An offset to start reading the file from

#### Defined in

[files/index.ts:395](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L395)

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
