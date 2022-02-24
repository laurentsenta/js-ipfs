[ipfs-core-types](../README.md) / [Modules](../modules.md) / [swarm](../modules/swarm.md) / PeersOptions

# Interface: PeersOptions

[swarm](../modules/swarm.md).PeersOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`PeersOptions`**

## Table of contents

### Properties

- [direction](swarm.PeersOptions.md#direction)
- [latency](swarm.PeersOptions.md#latency)
- [signal](swarm.PeersOptions.md#signal)
- [streams](swarm.PeersOptions.md#streams)
- [timeout](swarm.PeersOptions.md#timeout)
- [verbose](swarm.PeersOptions.md#verbose)

## Properties

### direction

• `Optional` **direction**: `boolean`

#### Defined in

[swarm/index.ts:37](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L37)

___

### latency

• `Optional` **latency**: `boolean`

#### Defined in

[swarm/index.ts:40](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L40)

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

### streams

• `Optional` **streams**: `boolean`

#### Defined in

[swarm/index.ts:38](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L38)

___

### timeout

• `Optional` **timeout**: `number`

Can be provided to a function that starts a long running task, which will
be aborted after provided timeout (in ms).

#### Inherited from

[AbortOptions](index.AbortOptions.md).[timeout](index.AbortOptions.md#timeout)

#### Defined in

[utils.ts:109](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L109)

___

### verbose

• `Optional` **verbose**: `boolean`

#### Defined in

[swarm/index.ts:39](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/swarm/index.ts#L39)
