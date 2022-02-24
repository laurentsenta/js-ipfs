[ipfs-core-types](../README.md) / [Modules](../modules.md) / dht

# Module: dht

## Table of contents

### Enumerations

- [EventTypes](../enums/dht.EventTypes.md)
- [MessageType](../enums/dht.MessageType.md)

### Interfaces

- [API](../interfaces/dht.API.md)
- [AddingPeerEvent](../interfaces/dht.AddingPeerEvent.md)
- [DHTProvideOptions](../interfaces/dht.DHTProvideOptions.md)
- [DHTRecord](../interfaces/dht.DHTRecord.md)
- [DialingPeerEvent](../interfaces/dht.DialingPeerEvent.md)
- [FinalPeerEvent](../interfaces/dht.FinalPeerEvent.md)
- [PeerData](../interfaces/dht.PeerData.md)
- [PeerResponseEvent](../interfaces/dht.PeerResponseEvent.md)
- [PeerResult](../interfaces/dht.PeerResult.md)
- [ProviderEvent](../interfaces/dht.ProviderEvent.md)
- [QueryErrorEvent](../interfaces/dht.QueryErrorEvent.md)
- [SendingQueryEvent](../interfaces/dht.SendingQueryEvent.md)
- [ValueEvent](../interfaces/dht.ValueEvent.md)

### Type aliases

- [MessageName](dht.md#messagename)
- [QueryEvent](dht.md#queryevent)

## Type aliases

### MessageName

Ƭ **MessageName**: keyof typeof [`MessageType`](../enums/dht.MessageType.md)

#### Defined in

[dht/index.ts:101](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L101)

___

### QueryEvent

Ƭ **QueryEvent**: [`SendingQueryEvent`](../interfaces/dht.SendingQueryEvent.md) \| [`PeerResponseEvent`](../interfaces/dht.PeerResponseEvent.md) \| [`FinalPeerEvent`](../interfaces/dht.FinalPeerEvent.md) \| [`QueryErrorEvent`](../interfaces/dht.QueryErrorEvent.md) \| [`ProviderEvent`](../interfaces/dht.ProviderEvent.md) \| [`ValueEvent`](../interfaces/dht.ValueEvent.md) \| [`AddingPeerEvent`](../interfaces/dht.AddingPeerEvent.md) \| [`DialingPeerEvent`](../interfaces/dht.DialingPeerEvent.md)

#### Defined in

[dht/index.ts:166](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dht/index.ts#L166)
