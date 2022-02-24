[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pin](../modules/pin.md) / LsOptions

# Interface: LsOptions

[pin](../modules/pin.md).LsOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`LsOptions`**

## Table of contents

### Properties

- [paths](pin.LsOptions.md#paths)
- [signal](pin.LsOptions.md#signal)
- [timeout](pin.LsOptions.md#timeout)
- [type](pin.LsOptions.md#type)

## Properties

### paths

• `Optional` **paths**: `string` \| `CID` \| `string`[] \| `CID`[]

#### Defined in

[pin/index.ts:156](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L156)

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

___

### type

• `Optional` **type**: [`PinQueryType`](../modules/pin.md#pinquerytype)

#### Defined in

[pin/index.ts:157](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L157)
