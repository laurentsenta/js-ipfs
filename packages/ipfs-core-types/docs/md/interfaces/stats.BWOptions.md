[ipfs-core-types](../README.md) / [Modules](../modules.md) / [stats](../modules/stats.md) / BWOptions

# Interface: BWOptions

[stats](../modules/stats.md).BWOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`BWOptions`**

## Table of contents

### Properties

- [interval](stats.BWOptions.md#interval)
- [peer](stats.BWOptions.md#peer)
- [poll](stats.BWOptions.md#poll)
- [proto](stats.BWOptions.md#proto)
- [signal](stats.BWOptions.md#signal)
- [timeout](stats.BWOptions.md#timeout)

## Properties

### interval

• `Optional` **interval**: `number`

#### Defined in

[stats/index.ts:19](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L19)

___

### peer

• `Optional` **peer**: `string`

#### Defined in

[stats/index.ts:16](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L16)

___

### poll

• `Optional` **poll**: `boolean`

#### Defined in

[stats/index.ts:18](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L18)

___

### proto

• `Optional` **proto**: `string`

#### Defined in

[stats/index.ts:17](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/stats/index.ts#L17)

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
