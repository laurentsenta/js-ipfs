[ipfs-core-types](../README.md) / [Modules](../modules.md) / [block](../modules/block.md) / RmOptions

# Interface: RmOptions

[block](../modules/block.md).RmOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`RmOptions`**

## Table of contents

### Properties

- [force](block.RmOptions.md#force)
- [quiet](block.RmOptions.md#quiet)
- [signal](block.RmOptions.md#signal)
- [timeout](block.RmOptions.md#timeout)

## Properties

### force

• `Optional` **force**: `boolean`

Ignores non-existent blocks

#### Defined in

[block/index.ts:110](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L110)

___

### quiet

• `Optional` **quiet**: `boolean`

Do not return output if true

#### Defined in

[block/index.ts:115](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/block/index.ts#L115)

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
