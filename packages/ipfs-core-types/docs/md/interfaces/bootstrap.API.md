[ipfs-core-types](../README.md) / [Modules](../modules.md) / [bootstrap](../modules/bootstrap.md) / API

# Interface: API<OptionExtension\>

[bootstrap](../modules/bootstrap.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [add](bootstrap.API.md#add)
- [clear](bootstrap.API.md#clear)
- [list](bootstrap.API.md#list)
- [reset](bootstrap.API.md#reset)
- [rm](bootstrap.API.md#rm)

## Methods

### add

▸ **add**(`addr`, `options?`): `Promise`<{ `Peers`: `Multiaddr`[]  }\>

Add a peer address to the bootstrap list

**`example`**
```js
const validIp4 = '/ip4/104....9z'

const res = await ipfs.bootstrap.add(validIp4)
console.log(res.Peers)
// Logs:
// ['/ip4/104....9z']
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `addr` | `Multiaddr` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<{ `Peers`: `Multiaddr`[]  }\>

#### Defined in

[bootstrap/index.ts:18](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bootstrap/index.ts#L18)

___

### clear

▸ **clear**(`options?`): `Promise`<{ `Peers`: `Multiaddr`[]  }\>

Remove all peer addresses from the bootstrap list

**`example`**
```js
const res = await ipfs.bootstrap.clear()
console.log(res.Peers)
// Logs:
// [address1, address2, ...]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<{ `Peers`: `Multiaddr`[]  }\>

#### Defined in

[bootstrap/index.ts:70](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bootstrap/index.ts#L70)

___

### list

▸ **list**(`options?`): `Promise`<{ `Peers`: `Multiaddr`[]  }\>

List all peer addresses in the bootstrap list

**`example`**
```js
const res = await ipfs.bootstrap.list()
console.log(res.Peers)
// Logs:
// [address1, address2, ...]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<{ `Peers`: `Multiaddr`[]  }\>

#### Defined in

[bootstrap/index.ts:44](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bootstrap/index.ts#L44)

___

### reset

▸ **reset**(`options?`): `Promise`<{ `Peers`: `Multiaddr`[]  }\>

Reset the bootstrap list to contain only the default bootstrap nodes

**`example`**
```js
const res = await ipfs.bootstrap.list()
console.log(res.Peers)
// Logs:
// [address1, address2, ...]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<{ `Peers`: `Multiaddr`[]  }\>

#### Defined in

[bootstrap/index.ts:31](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bootstrap/index.ts#L31)

___

### rm

▸ **rm**(`addr`, `options?`): `Promise`<{ `Peers`: `Multiaddr`[]  }\>

Remove a peer address from the bootstrap list

**`example`**
```js
const res = await ipfs.bootstrap.list()
console.log(res.Peers)
// Logs:
// [address1, address2, ...]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `addr` | `Multiaddr` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<{ `Peers`: `Multiaddr`[]  }\>

#### Defined in

[bootstrap/index.ts:57](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/bootstrap/index.ts#L57)
