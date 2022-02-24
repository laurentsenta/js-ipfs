[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / ResolveOptions

# Interface: ResolveOptions

[root](../modules/root.md).ResolveOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`ResolveOptions`**

## Table of contents

### Properties

- [cidBase](root.ResolveOptions.md#cidbase)
- [recursive](root.ResolveOptions.md#recursive)
- [signal](root.ResolveOptions.md#signal)
- [timeout](root.ResolveOptions.md#timeout)

## Properties

### cidBase

• `Optional` **cidBase**: `string`

#### Defined in

[root.ts:315](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L315)

___

### recursive

• `Optional` **recursive**: `boolean`

#### Defined in

[root.ts:314](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L314)

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
