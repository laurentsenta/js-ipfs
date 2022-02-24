[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / DNSOptions

# Interface: DNSOptions

[root](../modules/root.md).DNSOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`DNSOptions`**

## Table of contents

### Properties

- [recursive](root.DNSOptions.md#recursive)
- [signal](root.DNSOptions.md#signal)
- [timeout](root.DNSOptions.md#timeout)

## Properties

### recursive

• `Optional` **recursive**: `boolean`

#### Defined in

[root.ts:300](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L300)

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
