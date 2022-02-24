[ipfs-core-types](../README.md) / [Modules](../modules.md) / [object](../modules/object.md) / API

# Interface: API<OptionExtension\>

[object](../modules/object.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Properties

- [patch](object.API.md#patch)

### Methods

- [data](object.API.md#data)
- [get](object.API.md#get)
- [links](object.API.md#links)
- [new](object.API.md#new)
- [put](object.API.md#put)
- [stat](object.API.md#stat)

## Properties

### patch

• **patch**: `API`<{}\>

#### Defined in

[object/index.ts:14](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L14)

## Methods

### data

▸ **data**(`cid`, `options?`): `Promise`<`Uint8Array`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `PreloadOptions` & `OptionExtension` |

#### Returns

`Promise`<`Uint8Array`\>

#### Defined in

[object/index.ts:10](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L10)

___

### get

▸ **get**(`cid`, `options?`): `Promise`<`PBNode`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `PreloadOptions` & `OptionExtension` |

#### Returns

`Promise`<`PBNode`\>

#### Defined in

[object/index.ts:9](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L9)

___

### links

▸ **links**(`cid`, `options?`): `Promise`<`PBLink`[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `PreloadOptions` & `OptionExtension` |

#### Returns

`Promise`<`PBLink`[]\>

#### Defined in

[object/index.ts:11](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L11)

___

### new

▸ **new**(`options?`): `Promise`<`CID`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`NewObjectOptions`](object.NewObjectOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[object/index.ts:7](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L7)

___

### put

▸ **put**(`obj`, `options?`): `Promise`<`CID`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `obj` | `PBNode` |
| `options?` | [`PutOptions`](object.PutOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`CID`\>

#### Defined in

[object/index.ts:8](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L8)

___

### stat

▸ **stat**(`cid`, `options?`): `Promise`<[`StatResult`](object.StatResult.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `cid` | `CID` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `PreloadOptions` & `OptionExtension` |

#### Returns

`Promise`<[`StatResult`](object.StatResult.md)\>

#### Defined in

[object/index.ts:12](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/object/index.ts#L12)
