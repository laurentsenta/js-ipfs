[ipfs-core-types](../README.md) / [Modules](../modules.md) / [name](../modules/name.md) / API

# Interface: API<OptionExtension\>

[name](../modules/name.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Properties

- [pubsub](name.API.md#pubsub)

### Methods

- [publish](name.API.md#publish)
- [resolve](name.API.md#resolve)

## Properties

### pubsub

• **pubsub**: `API`<{}\>

#### Defined in

[name/index.ts:41](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L41)

## Methods

### publish

▸ **publish**(`value`, `options?`): `Promise`<[`PublishResult`](name.PublishResult.md)\>

IPNS is a PKI namespace, where names are the hashes of public keys, and
the private key enables publishing new (signed) values. In both publish
and resolve, the default name used is the node's own PeerID,
which is the hash of its public key.

**`example`**
```js
// The address of your files.
const addr = '/ipfs/QmbezGequPwcsWo8UL4wDF6a8hYwM1hmbzYv2mnKkEWaUp'
const res = await ipfs.name.publish(addr)
// You now have a res which contains two fields:
//   - name: the name under which the content was published.
//   - value: the "real" address to which Name points.
console.log(`https://gateway.ipfs.io/ipns/${res.name}`)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `string` \| `CID` |
| `options?` | [`PublishOptions`](name.PublishOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`PublishResult`](name.PublishResult.md)\>

#### Defined in

[name/index.ts:23](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L23)

___

### resolve

▸ **resolve**(`value`, `options?`): `AsyncIterable`<`string`\>

Given a key, query the DHT for its best value.

**`example`**
```js
// The IPNS address you want to resolve
const addr = '/ipns/ipfs.io'

for await (const name of ipfs.name.resolve(addr)) {
  console.log(name)
}
// Logs: /ipfs/QmQrX8hka2BtNHa8N8arAq16TCVx5qHcb46c5yPewRycLm
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `string` |
| `options?` | [`ResolveOptions`](name.ResolveOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`string`\>

#### Defined in

[name/index.ts:39](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L39)
