[ipfs-core-types](../README.md) / [Modules](../modules.md) / [root](../modules/root.md) / IDOptions

# Interface: IDOptions

[root](../modules/root.md).IDOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`IDOptions`**

## Table of contents

### Properties

- [peerId](root.IDOptions.md#peerid)
- [signal](root.IDOptions.md#signal)
- [timeout](root.IDOptions.md#timeout)

## Properties

### peerId

• `Optional` **peerId**: `string`

#### Defined in

[root.ts:270](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/root.ts#L270)

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
