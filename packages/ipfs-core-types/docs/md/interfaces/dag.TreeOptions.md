[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / TreeOptions

# Interface: TreeOptions

[dag](../modules/dag.md).TreeOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`TreeOptions`**

## Table of contents

### Properties

- [path](dag.TreeOptions.md#path)
- [preload](dag.TreeOptions.md#preload)
- [recursive](dag.TreeOptions.md#recursive)
- [signal](dag.TreeOptions.md#signal)
- [timeout](dag.TreeOptions.md#timeout)

## Properties

### path

• `Optional` **path**: `string`

An optional path within the DAG to resolve

#### Defined in

[dag/index.ts:176](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L176)

___

### preload

• `Optional` **preload**: `boolean`

#### Inherited from

PreloadOptions.preload

#### Defined in

[utils.ts:113](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L113)

___

### recursive

• `Optional` **recursive**: `boolean`

If set to true, it will follow the links and continuously run tree on them, returning all the paths in the graph

#### Defined in

[dag/index.ts:181](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L181)

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
