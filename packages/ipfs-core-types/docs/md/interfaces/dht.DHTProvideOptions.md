[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dht](../modules/dht.md) / DHTProvideOptions

# Interface: DHTProvideOptions

[dht](../modules/dht.md).DHTProvideOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`DHTProvideOptions`**

## Table of contents

### Properties

- [recursive](dht.DHTProvideOptions.md#recursive)
- [signal](dht.DHTProvideOptions.md#signal)
- [timeout](dht.DHTProvideOptions.md#timeout)

## Properties

### recursive

• `Optional` **recursive**: `boolean`

#### Defined in

[dht/index.ts:70](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L70)

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
