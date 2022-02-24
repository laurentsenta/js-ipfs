[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dht](../modules/dht.md) / PeerResponseEvent

# Interface: PeerResponseEvent

[dht](../modules/dht.md).PeerResponseEvent

## Table of contents

### Properties

- [closer](dht.PeerResponseEvent.md#closer)
- [from](dht.PeerResponseEvent.md#from)
- [messageName](dht.PeerResponseEvent.md#messagename)
- [messageType](dht.PeerResponseEvent.md#messagetype)
- [name](dht.PeerResponseEvent.md#name)
- [providers](dht.PeerResponseEvent.md#providers)
- [record](dht.PeerResponseEvent.md#record)
- [type](dht.PeerResponseEvent.md#type)

## Properties

### closer

• **closer**: [`PeerData`](dht.PeerData.md)[]

#### Defined in

[dht/index.ts:122](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L122)

___

### from

• **from**: `string`

#### Defined in

[dht/index.ts:116](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L116)

___

### messageName

• **messageName**: ``"PUT_VALUE"`` \| ``"GET_VALUE"`` \| ``"ADD_PROVIDER"`` \| ``"GET_PROVIDERS"`` \| ``"FIND_NODE"`` \| ``"PING"``

#### Defined in

[dht/index.ts:120](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L120)

___

### messageType

• **messageType**: [`MessageType`](../enums/dht.MessageType.md)

#### Defined in

[dht/index.ts:119](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L119)

___

### name

• **name**: ``"PEER_RESPONSE"``

#### Defined in

[dht/index.ts:118](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L118)

___

### providers

• **providers**: [`PeerData`](dht.PeerData.md)[]

#### Defined in

[dht/index.ts:121](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L121)

___

### record

• `Optional` **record**: [`DHTRecord`](dht.DHTRecord.md)

#### Defined in

[dht/index.ts:123](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L123)

___

### type

• **type**: [`PEER_RESPONSE`](../enums/dht.EventTypes.md#peer_response)

#### Defined in

[dht/index.ts:117](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L117)
