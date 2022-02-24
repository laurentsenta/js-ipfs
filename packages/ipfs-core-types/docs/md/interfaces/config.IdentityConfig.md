[ipfs-core-types](../README.md) / [Modules](../modules.md) / [config](../modules/config.md) / IdentityConfig

# Interface: IdentityConfig

[config](../modules/config.md).IdentityConfig

## Table of contents

### Properties

- [PeerID](config.IdentityConfig.md#peerid)
- [PrivKey](config.IdentityConfig.md#privkey)

## Properties

### PeerID

• **PeerID**: `string`

The unique PKI identity label for this configs peer. Set on init and never
read, its merely here for convenience. IPFS will always generate the peerID
from its keypair at runtime.

#### Defined in

[config/index.ts:107](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L107)

___

### PrivKey

• **PrivKey**: `string`

The base64 encoded protobuf describing (and containing) the nodes private key.

#### Defined in

[config/index.ts:112](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L112)
