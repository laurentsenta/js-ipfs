[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dht](../modules/dht.md) / API

# Interface: API<OptionExtension\>

[dht](../modules/dht.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [findPeer](dht.API.md#findpeer)
- [findProvs](dht.API.md#findprovs)
- [get](dht.API.md#get)
- [provide](dht.API.md#provide)
- [put](dht.API.md#put)
- [query](dht.API.md#query)

## Methods

### findPeer

▸ **findPeer**(`peerId`, `options?`): `AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

Query the DHT for all multiaddresses associated with a `PeerId`.

**`example`**
```js
const info = await ipfs.dht.findPeer('QmcZf59bWwK5XFi76CZX8cbJ4BhTzzA3gU1ZjYZcYW3dwt')

console.log(info.id)
// QmcZf59bWwK5XFi76CZX8cbJ4BhTzzA3gU1ZjYZcYW3dwt

info.addrs.forEach(addr => console.log(addr.toString()))
// '/ip4/147.75.94.115/udp/4001/quic'
// '/ip6/2604:1380:3000:1f00::1/udp/4001/quic'
// '/dnsaddr/bootstrap.libp2p.io'
// '/ip6/2604:1380:3000:1f00::1/tcp/4001'
// '/ip4/147.75.94.115/tcp/4001'
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `peerId` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

#### Defined in

[dht/index.ts:24](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L24)

___

### findProvs

▸ **findProvs**(`cid`, `options?`): `AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

Find peers in the DHT that can provide a specific value, given a CID.

**`example`**
```js
const providers = ipfs.dht.findProvs('QmdPAhQRxrDKqkGPvQzBvjYe3kU8kiEEAd2J6ETEamKAD9')
for await (const provider of providers) {
  console.log(provider.id.toString())
}
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

#### Defined in

[dht/index.ts:37](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L37)

___

### get

▸ **get**(`key`, `options?`): `AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

Given a key, query the DHT for its best value.

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` \| `Uint8Array` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

#### Defined in

[dht/index.ts:42](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L42)

___

### provide

▸ **provide**(`cid`, `options?`): `AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

Announce to the network that we are providing given values.

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`DHTProvideOptions`](dht.DHTProvideOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

#### Defined in

[dht/index.ts:47](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L47)

___

### put

▸ **put**(`key`, `value`, `options?`): `AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

Write a key/value pair to the DHT.

Given a key of the form /foo/bar and a value of any
form, this will write that value to the DHT with
that key.

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` \| `Uint8Array` |
| `value` | `Uint8Array` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

#### Defined in

[dht/index.ts:56](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L56)

___

### query

▸ **query**(`peerId`, `options?`): `AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

Find the closest peers to a given `PeerId` or `CID`, by querying the DHT.

#### Parameters

| Name | Type |
| :------ | :------ |
| `peerId` | `string` \| `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<[`QueryEvent`](../modules/dht.md#queryevent)\>

#### Defined in

[dht/index.ts:61](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L61)
