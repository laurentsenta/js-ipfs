[ipfs-core-types](../README.md) / [Modules](../modules.md) / [log](../modules/log.md) / API

# Interface: API<OptionExtension\>

[log](../modules/log.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [level](log.API.md#level)
- [ls](log.API.md#ls)
- [tail](log.API.md#tail)

## Methods

### level

▸ **level**(`subsystem`, `level`, `options?`): `Promise`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `subsystem` | `string` |
| `level` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`any`\>

#### Defined in

[log/index.ts:4](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/log/index.ts#L4)

___

### ls

▸ **ls**(`options?`): `Promise`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`any`\>

#### Defined in

[log/index.ts:5](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/log/index.ts#L5)

___

### tail

▸ **tail**(`options?`): `AsyncIterable`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`AsyncIterable`<`any`\>

#### Defined in

[log/index.ts:6](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/log/index.ts#L6)
