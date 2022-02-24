[ipfs-core-types](../README.md) / [Modules](../modules.md) / [pin](../modules/pin.md) / AddInputWithOptions

# Interface: AddInputWithOptions

[pin](../modules/pin.md).AddInputWithOptions

## Table of contents

### Properties

- [cid](pin.AddInputWithOptions.md#cid)
- [comments](pin.AddInputWithOptions.md#comments)
- [path](pin.AddInputWithOptions.md#path)
- [recursive](pin.AddInputWithOptions.md#recursive)

## Properties

### cid

• `Optional` **cid**: `CID`

A CID to pin - nb. you must pass either `cid` or `path`, not both

#### Defined in

[pin/index.ts:133](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L133)

___

### comments

• `Optional` **comments**: `string`

A human readable string to store with this pin

#### Defined in

[pin/index.ts:148](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L148)

___

### path

• `Optional` **path**: `string`

An IPFS path to pin - nb. you must pass either `cid` or `path`, not both

#### Defined in

[pin/index.ts:138](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L138)

___

### recursive

• `Optional` **recursive**: `boolean`

If true, pin all blocked linked to from the pinned CID

#### Defined in

[pin/index.ts:143](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/pin/index.ts#L143)
