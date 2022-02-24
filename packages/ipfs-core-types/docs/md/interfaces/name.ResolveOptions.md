[ipfs-core-types](../README.md) / [Modules](../modules.md) / [name](../modules/name.md) / ResolveOptions

# Interface: ResolveOptions

[name](../modules/name.md).ResolveOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`ResolveOptions`**

## Table of contents

### Properties

- [nocache](name.ResolveOptions.md#nocache)
- [recursive](name.ResolveOptions.md#recursive)
- [signal](name.ResolveOptions.md#signal)
- [timeout](name.ResolveOptions.md#timeout)

## Properties

### nocache

• `Optional` **nocache**: `boolean`

do not use cached entries

#### Defined in

[name/index.ts:93](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L93)

___

### recursive

• `Optional` **recursive**: `boolean`

resolve until the result is not an IPNS name

#### Defined in

[name/index.ts:88](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L88)

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
