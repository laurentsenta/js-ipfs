[ipfs-core-types](../README.md) / [Modules](../modules.md) / [name](../modules/name.md) / PublishOptions

# Interface: PublishOptions

[name](../modules/name.md).PublishOptions

## Hierarchy

- [`AbortOptions`](index.AbortOptions.md)

  ↳ **`PublishOptions`**

## Table of contents

### Properties

- [allowOffline](name.PublishOptions.md#allowoffline)
- [key](name.PublishOptions.md#key)
- [lifetime](name.PublishOptions.md#lifetime)
- [resolve](name.PublishOptions.md#resolve)
- [signal](name.PublishOptions.md#signal)
- [timeout](name.PublishOptions.md#timeout)
- [ttl](name.PublishOptions.md#ttl)

## Properties

### allowOffline

• `Optional` **allowOffline**: `boolean`

When offline, save the IPNS record
to the the local datastore without broadcasting to the network instead of
simply failing.

This option is not yet implemented in js-ipfs. See tracking issue [ipfs/js-ipfs#1997]
(https://github.com/ipfs/js-ipfs/issues/1997).

#### Defined in

[name/index.ts:69](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L69)

___

### key

• `Optional` **key**: `string`

Name of the key to be used

#### Defined in

[name/index.ts:60](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L60)

___

### lifetime

• `Optional` **lifetime**: `string`

Time duration of the record

#### Defined in

[name/index.ts:52](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L52)

___

### resolve

• `Optional` **resolve**: `boolean`

Resolve given path before publishing

#### Defined in

[name/index.ts:48](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L48)

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

### ttl

• `Optional` **ttl**: `string`

Time duration this record should be cached

#### Defined in

[name/index.ts:56](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/name/index.ts#L56)
