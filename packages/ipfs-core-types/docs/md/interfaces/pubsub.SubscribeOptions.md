[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pubsub](../modules/pubsub.md) / SubscribeOptions

# Interface: SubscribeOptions

[pubsub](../modules/pubsub.md).SubscribeOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`SubscribeOptions`**

## Table of contents

### Properties

- [signal](pubsub.SubscribeOptions.md#signal)
- [timeout](pubsub.SubscribeOptions.md#timeout)

### Methods

- [onError](pubsub.SubscribeOptions.md#onerror)

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

### timeout

• `Optional` **timeout**: `number`

Can be provided to a function that starts a long running task, which will
be aborted after provided timeout (in ms).

#### Inherited from

[AbortOptions](index.AbortOptions.md).[timeout](index.AbortOptions.md#timeout)

#### Defined in

[utils.ts:109](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L109)

## Methods

### onError

▸ `Optional` **onError**(`err`): `void`

A callback to receive an error if one occurs during processing
subscription messages. Only supported by ipfs-http-client.

#### Parameters

| Name | Type |
| :------ | :------ |
| `err` | `Error` |

#### Returns

`void`

#### Defined in

[pubsub/index.ts:91](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L91)
