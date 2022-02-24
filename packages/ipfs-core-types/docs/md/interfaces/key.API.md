[ipfs-core-types](../README.md) / [Modules](../modules.md) / [key](../modules/key.md) / API

# Interface: API<OptionExtension\>

[key](../modules/key.md).API

## Type parameters

| Name | Type |
| :------ | :------ |
| `OptionExtension` | {} |

## Table of contents

### Methods

- [export](key.API.md#export)
- [gen](key.API.md#gen)
- [import](key.API.md#import)
- [info](key.API.md#info)
- [list](key.API.md#list)
- [rename](key.API.md#rename)
- [rm](key.API.md#rm)

## Methods

### export

▸ **export**(`name`, `password`, `options?`): `Promise`<`string`\>

Remove a key

**`example`**
```js
const pem = await ipfs.key.export('self', 'password')

console.log(pem)
// -----BEGIN ENCRYPTED PRIVATE KEY-----
// MIIFDTA/BgkqhkiG9w0BBQ0wMjAaBgkqhkiG9w0BBQwwDQQIpdO40RVyBwACAWQw
// ...
// YA==
// -----END ENCRYPTED PRIVATE KEY-----
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `password` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<`string`\>

#### Defined in

[key/index.ts:84](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L84)

___

### gen

▸ **gen**(`name`, `options?`): `Promise`<[`Key`](key.Key.md)\>

Generate a new key

**`example`**
```js
const key = await ipfs.key.gen('my-key', {
  type: 'rsa',
  size: 2048
})

console.log(key)
// { id: 'QmYWqAFvLWb2G5A69JGXui2JJXzaHXiUEmQkQgor6kNNcJ',
//  name: 'my-key' }
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `options?` | [`GenOptions`](key.GenOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Key`](key.Key.md)\>

#### Defined in

[key/index.ts:19](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L19)

___

### import

▸ **import**(`name`, `pem`, `password`, `options?`): `Promise`<[`Key`](key.Key.md)\>

Remove a key

**`example`**
```js
const key = await ipfs.key.import('clone', pem, 'password')

console.log(key)
// { id: 'QmQRiays958UM7norGRQUG3tmrLq8pJdmJarwYSk2eLthQ',
//   name: 'clone' }
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `pem` | `string` |
| `password` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Key`](key.Key.md)\>

#### Defined in

[key/index.ts:98](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L98)

___

### info

▸ **info**(`name`, `options?`): `Promise`<[`Key`](key.Key.md)\>

Return the id and name of a key

* @example
```js
const { id, name } = await ipfs.key.info('key-name')
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Key`](key.Key.md)\>

#### Defined in

[key/index.ts:108](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L108)

___

### list

▸ **list**(`options?`): `Promise`<[`Key`](key.Key.md)[]\>

List all the keys

**`example`**
```js
const keys = await ipfs.key.list()

console.log(keys)
// [
//   { id: 'QmTe4tuceM2sAmuZiFsJ9tmAopA8au71NabBDdpPYDjxAb',
//     name: 'self' },
//   { id: 'QmWETF5QvzGnP7jKq5sPDiRjSM2fzwzNsna4wSBEzRzK6W',
//     name: 'my-key' }
// ]
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Key`](key.Key.md)[]\>

#### Defined in

[key/index.ts:37](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L37)

___

### rename

▸ **rename**(`oldName`, `newName`, `options?`): `Promise`<[`RenameKeyResult`](key.RenameKeyResult.md)\>

Rename a key

**`example`**
```js
const key = await ipfs.key.rename('my-key', 'my-new-key')

console.log(key)
// { id: 'Qmd4xC46Um6s24MradViGLFtMitvrR4SVexKUgPgFjMNzg',
//   was: 'my-key',
//   now: 'my-new-key',
//   overwrite: false }
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `oldName` | `string` |
| `newName` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`RenameKeyResult`](key.RenameKeyResult.md)\>

#### Defined in

[key/index.ts:67](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L67)

___

### rm

▸ **rm**(`name`, `options?`): `Promise`<[`Key`](key.Key.md)\>

Remove a key

**`example`**
```js
const key = await ipfs.key.rm('my-key')

console.log(key)
// { id: 'QmWETF5QvzGnP7jKq5sPDiRjSM2fzwzNsna4wSBEzRzK6W',
//   name: 'my-key' }
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `options?` | [`AbortOptions`](index.AbortOptions.md) & `OptionExtension` |

#### Returns

`Promise`<[`Key`](key.Key.md)\>

#### Defined in

[key/index.ts:51](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/key/index.ts#L51)
