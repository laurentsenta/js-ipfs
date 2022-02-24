[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / GetResult

# Interface: GetResult

[dag](../modules/dag.md).GetResult

## Table of contents

### Properties

- [remainderPath](dag.GetResult.md#remainderpath)
- [value](dag.GetResult.md#value)

## Properties

### remainderPath

• `Optional` **remainderPath**: `string`

The remainder of the Path that the node was unable to resolve or what was left in a localResolve scenario

#### Defined in

[dag/index.ts:130](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L130)

___

### value

• **value**: `any`

The value or node that was fetched during the get operation

#### Defined in

[dag/index.ts:125](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L125)
