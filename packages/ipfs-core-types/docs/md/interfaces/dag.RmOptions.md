[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / RmOptions

# Interface: RmOptions

[dag](../modules/dag.md).RmOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`RmOptions`**

## Table of contents

### Properties

- [force](dag.RmOptions.md#force)
- [signal](dag.RmOptions.md#signal)
- [timeout](dag.RmOptions.md#timeout)

## Properties

### force

• `Optional` **force**: `boolean`

Ignores non-existent blocks

#### Defined in

[dag/index.ts:169](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L169)

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
