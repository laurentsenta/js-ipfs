[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / StatResult

# Interface: StatResult

[files](../modules/files.md).StatResult

## Table of contents

### Properties

- [blocks](files.StatResult.md#blocks)
- [cid](files.StatResult.md#cid)
- [cumulativeSize](files.StatResult.md#cumulativesize)
- [local](files.StatResult.md#local)
- [mode](files.StatResult.md#mode)
- [mtime](files.StatResult.md#mtime)
- [size](files.StatResult.md#size)
- [sizeLocal](files.StatResult.md#sizelocal)
- [type](files.StatResult.md#type)
- [withLocality](files.StatResult.md#withlocality)

## Properties

### blocks

• **blocks**: `number`

If type is directory, this is the number of files in the directory. If it is file it is the number of blocks that make up the file

#### Defined in

[files/index.ts:319](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L319)

___

### cid

• **cid**: `CID`

A CID instance

#### Defined in

[files/index.ts:299](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L299)

___

### cumulativeSize

• **cumulativeSize**: `number`

The size of the DAGNodes making up the file in Bytes

#### Defined in

[files/index.ts:309](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L309)

___

### local

• `Optional` **local**: `boolean`

Indicates if the queried dag is fully present locally

#### Defined in

[files/index.ts:329](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L329)

___

### mode

• `Optional` **mode**: `number`

UnixFS mode if applicable

#### Defined in

[files/index.ts:339](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L339)

___

### mtime

• `Optional` **mtime**: `Mtime`

UnixFS mtime if applicable

#### Defined in

[files/index.ts:344](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L344)

___

### size

• **size**: `number`

The file size in Bytes

#### Defined in

[files/index.ts:304](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L304)

___

### sizeLocal

• `Optional` **sizeLocal**: `number`

Indicates the cumulative size of the data present locally

#### Defined in

[files/index.ts:334](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L334)

___

### type

• **type**: ``"file"`` \| ``"directory"``

Either directory or file

#### Defined in

[files/index.ts:314](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L314)

___

### withLocality

• **withLocality**: `boolean`

Indicates if locality information is present

#### Defined in

[files/index.ts:324](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L324)
