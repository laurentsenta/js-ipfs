[ipfs-core-types](../README.md) / [Modules](../modules.md) / [swarm](../modules/swarm.md) / API

# Interface: API<OptionExtension\>

[swarm](../modules/swarm.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [addrs](swarm.API.md#addrs)
- [connect](swarm.API.md#connect)
- [disconnect](swarm.API.md#disconnect)
- [localAddrs](swarm.API.md#localaddrs)
- [peers](swarm.API.md#peers)

## Methods

### addrs

▸ **addrs**(`options?`): `Promise`<[`AddrsResult`](swarm.AddrsResult.md)[]\>

List of known addresses of each peer connected

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`AddrsResult`](swarm.AddrsResult.md)[]\>

#### Defined in

[swarm/index.ts:8](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L8)

___

### connect

▸ **connect**(`addr`, `options?`): `Promise`<`void`\>

Open a connection to a given address or peer id

#### Parameters

| Name | Type |
| :------ | :------ |
| `addr` | `string` \| `Multiaddr` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[swarm/index.ts:13](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L13)

___

### disconnect

▸ **disconnect**(`addr`, `options?`): `Promise`<`void`\>

Close a connection to a given address or peer id

#### Parameters

| Name | Type |
| :------ | :------ |
| `addr` | `string` \| `Multiaddr` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[swarm/index.ts:18](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L18)

___

### localAddrs

▸ **localAddrs**(`options?`): `Promise`<`Multiaddr`[]\>

Local addresses this node is listening on

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`Multiaddr`[]\>

#### Defined in

[swarm/index.ts:23](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L23)

___

### peers

▸ **peers**(`options?`): `Promise`<[`PeersResult`](swarm.PeersResult.md)[]\>

Return a list of connected peers

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`PeersOptions`](swarm.PeersOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`PeersResult`](swarm.PeersResult.md)[]\>

#### Defined in

[swarm/index.ts:28](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L28)
