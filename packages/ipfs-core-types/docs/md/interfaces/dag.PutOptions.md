[ipfs-core-types](../README.md) / [Modules](../modules.md) / [dag](../modules/dag.md) / PutOptions

# Interface: PutOptions

[dag](../modules/dag.md).PutOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

- `PreloadOptions`

  ↳ **`PutOptions`**

## Table of contents

### Properties

- [hashAlg](dag.PutOptions.md#hashalg)
- [inputCodec](dag.PutOptions.md#inputcodec)
- [onlyHash](dag.PutOptions.md#onlyhash)
- [pin](dag.PutOptions.md#pin)
- [preload](dag.PutOptions.md#preload)
- [signal](dag.PutOptions.md#signal)
- [storeCodec](dag.PutOptions.md#storecodec)
- [timeout](dag.PutOptions.md#timeout)
- [version](dag.PutOptions.md#version)

## Properties

### hashAlg

• `Optional` **hashAlg**: `string`

Multihash hashing algorithm to use (defaults to 'sha2-256')

#### Defined in

[dag/index.ts:147](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L147)

___

### inputCodec

• `Optional` **inputCodec**: `string`

The codec that the input object is encoded with if a pre-encoded object is supplied.

#### Defined in

[dag/index.ts:137](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L137)

___

### onlyHash

• `Optional` **onlyHash**: `boolean`

If true no blocks will be written to the underlying blockstore

#### Defined in

[dag/index.ts:162](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L162)

___

### pin

• `Optional` **pin**: `boolean`

Pin this block when adding. (Defaults to `false`)

#### Defined in

[dag/index.ts:157](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L157)

___

### preload

• `Optional` **preload**: `boolean`

#### Inherited from

PreloadOptions.preload

#### Defined in

[utils.ts:113](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L113)

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

### storeCodec

• `Optional` **storeCodec**: `string`

The codec that the stored object will be encoded with (defaults to 'dag-cbor')

#### Defined in

[dag/index.ts:142](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L142)

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

### version

• `Optional` **version**: `CIDVersion`

The version to use to create the CID (default to 1)

#### Defined in

[dag/index.ts:152](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/dag/index.ts#L152)
