[ipfs-core-types](../README.md) / [Modules](../modules.md) / [repo](../modules/repo.md) / GCOptions

# Interface: GCOptions

[repo](../modules/repo.md).GCOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`GCOptions`**

## Table of contents

### Properties

- [quiet](repo.GCOptions.md#quiet)
- [signal](repo.GCOptions.md#signal)
- [timeout](repo.GCOptions.md#timeout)

## Properties

### quiet

• `Optional` **quiet**: `boolean`

#### Defined in

[repo/index.ts:25](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/repo/index.ts#L25)

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
