[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pubsub](../modules/pubsub.md) / API

# Interface: API<OptionExtension\>

[pubsub](../modules/pubsub.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [ls](pubsub.API.md#ls)
- [peers](pubsub.API.md#peers)
- [publish](pubsub.API.md#publish)
- [setMaxListeners](pubsub.API.md#setmaxlisteners)
- [subscribe](pubsub.API.md#subscribe)
- [unsubscribe](pubsub.API.md#unsubscribe)

## Methods

### ls

▸ **ls**(`options?`): `Promise`<`string`[]\>

Returns the list of subscriptions the peer is subscribed to

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[pubsub/index.ts:61](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L61)

___

### peers

▸ **peers**(`topic`, `options?`): `Promise`<`string`[]\>

Returns the peers that are subscribed to one topic.

**`example`**
```js
const topic = 'fruit-of-the-day'

const peerIds = await ipfs.pubsub.peers(topic)
console.log(peerIds)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `topic` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[pubsub/index.ts:74](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L74)

___

### publish

▸ **publish**(`topic`, `data`, `options?`): `Promise`<`void`\>

Publish a data message to a pubsub topic

**`example`**
```js
const topic = 'fruit-of-the-day'
const msg = new TextEncoder().encode('banana')

await ipfs.pubsub.publish(topic, msg)
// msg was broadcasted
console.log(`published to ${topic}`)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `topic` | `string` |
| `data` | `Uint8Array` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[pubsub/index.ts:56](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L56)

___

### setMaxListeners

▸ `Optional` **setMaxListeners**(`max`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `max` | `number` |

#### Returns

`void`

#### Defined in

[pubsub/index.ts:76](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L76)

___

### subscribe

▸ **subscribe**(`topic`, `handler`, `options?`): `Promise`<`void`\>

Subscribe to a pubsub topic

**`example`**
```js
const topic = 'fruit-of-the-day'
const receiveMsg = (msg) => console.log(msg.data.toString())

await ipfs.pubsub.subscribe(topic, receiveMsg)
console.log(`subscribed to ${topic}`)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `topic` | `string` |
| `handler` | [`MessageHandlerFn`](pubsub.MessageHandlerFn.md) |
| `options?` | [`SubscribeOptions`](pubsub.SubscribeOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[pubsub/index.ts:16](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L16)

___

### unsubscribe

▸ **unsubscribe**(`topic`, `handler?`, `options?`): `Promise`<`void`\>

Unsubscribes from a pubsub topic

**`example`**
```js
const topic = 'fruit-of-the-day'
const receiveMsg = (msg) => console.log(msg.toString())

await ipfs.pubsub.subscribe(topic, receiveMsg)
console.log(`subscribed to ${topic}`)

await ipfs.pubsub.unsubscribe(topic, receiveMsg)
console.log(`unsubscribed from ${topic}`)

// Or removing all listeners:

const topic = 'fruit-of-the-day'
const receiveMsg = (msg) => console.log(msg.toString())
await ipfs.pubsub.subscribe(topic, receiveMsg);
// Will unsubscribe ALL handlers for the given topic
await ipfs.pubsub.unsubscribe(topic);
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `topic` | `string` |
| `handler?` | [`MessageHandlerFn`](pubsub.MessageHandlerFn.md) |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[pubsub/index.ts:41](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pubsub/index.ts#L41)
