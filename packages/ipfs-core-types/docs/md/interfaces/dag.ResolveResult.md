[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / ResolveResult

# Interface: ResolveResult

[dag](../modules/dag.md).ResolveResult

## Table of contents

### Properties

- [cid](dag.ResolveResult.md#cid)
- [remainderPath](dag.ResolveResult.md#remainderpath)

## Properties

### cid

• **cid**: `CID`

The last CID encountered during the traversal and the path to the end of the IPFS path inside the node referenced by the CID

#### Defined in

[dag/index.ts:195](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L195)

___

### remainderPath

• `Optional` **remainderPath**: `string`

The remainder of the Path that the node was unable to resolve

#### Defined in

[dag/index.ts:200](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L200)
