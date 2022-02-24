[ipfs-core-types](../README.md) / [Modules](../modules.md) / [config](../modules/config.md) / API

# Interface: API<OptionExtension\>

[config](../modules/config.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Properties

- [profiles](config.API.md#profiles)

### Methods

- [get](config.API.md#get)
- [getAll](config.API.md#getall)
- [replace](config.API.md#replace)
- [set](config.API.md#set)

## Properties

### profiles

• **profiles**: `API`<{}\>

#### Defined in

[config/index.ts:29](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L29)

## Methods

### get

▸ **get**(`key`, `options?`): `Promise`<`string` \| `object`\>

Returns a value from the currently being used config. If the daemon
is off, it returns the value from the stored config.

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string` \| `object`\>

#### Defined in

[config/index.ts:9](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L9)

___

### getAll

▸ **getAll**(`options?`): `Promise`<[`Config`](config.Config.md)\>

Returns the full config been used. If the daemon is off, it returns the
stored config

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Config`](config.Config.md)\>

#### Defined in

[config/index.ts:15](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L15)

___

### replace

▸ **replace**(`config`, `options?`): `Promise`<`void`\>

Replaces the full config. Note that restarting the node will be
necessary for any change to take effect.

#### Parameters

| Name | Type |
| :------ | :------ |
| `config` | [`Config`](config.Config.md) |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[config/index.ts:27](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L27)

___

### set

▸ **set**(`key`, `value`, `options?`): `Promise`<`void`\>

Adds or replaces a config value. Note that restarting the node will be
necessary for any change to take effect.

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |
| `value` | `any` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`void`\>

#### Defined in

[config/index.ts:21](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/config/index.ts#L21)
