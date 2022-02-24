[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / PingOptions

# Interface: PingOptions

[root](../modules/root.md).PingOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`PingOptions`**

## Table of contents

### Properties

- [count](root.PingOptions.md#count)
- [signal](root.PingOptions.md#signal)
- [timeout](root.PingOptions.md#timeout)

## Properties

### count

• `Optional` **count**: `number`

#### Defined in

[root.ts:304](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L304)

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
