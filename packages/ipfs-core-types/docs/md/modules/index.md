[ipfs-core-types](../README.md) / [Modules](../modules.md) / index

# Module: index

## Table of contents

### Interfaces

- [AbortOptions](../interfaces/index.AbortOptions.md)
- [IPFS](../interfaces/index.IPFS.md)

### Type aliases

- [Await](index.md#await)
- [AwaitIterable](index.md#awaititerable)

## Type aliases

### Await

Ƭ **Await**<`T`\>: `T` \| `Promise`<`T`\>

Represents a value that you can await on, which is either value or a promise
of one.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[utils.ts:84](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L84)

___

### AwaitIterable

Ƭ **AwaitIterable**<`T`\>: `Iterable`<`T`\> \| `AsyncIterable`<`T`\>

Represents an iterable that can be used in `for await` loops, that is either
iterable or an async iterable.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[utils.ts:92](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L92)
