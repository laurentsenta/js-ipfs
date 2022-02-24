[ipfs-core-types](../README.md) / [Modules](../modules.md) / [key](../modules/key.md) / GenOptions

# Interface: GenOptions

[key](../modules/key.md).GenOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`GenOptions`**

## Table of contents

### Properties

- [signal](key.GenOptions.md#signal)
- [size](key.GenOptions.md#size)
- [timeout](key.GenOptions.md#timeout)
- [type](key.GenOptions.md#type)

## Properties

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

• **size**: `number`

#### Defined in

[key/index.ts:113](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L113)

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

### type

• **type**: `string`

#### Defined in

[key/index.ts:112](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L112)
