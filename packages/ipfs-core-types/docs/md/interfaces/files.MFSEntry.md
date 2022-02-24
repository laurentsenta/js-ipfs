[ipfs-core-types](../README.md) / [Modules](../modules.md) / [files](../modules/files.md) / MFSEntry

# Interface: MFSEntry

[files](../modules/files.md).MFSEntry

## Table of contents

### Properties

- [cid](files.MFSEntry.md#cid)
- [mode](files.MFSEntry.md#mode)
- [mtime](files.MFSEntry.md#mtime)
- [name](files.MFSEntry.md#name)
- [size](files.MFSEntry.md#size)
- [type](files.MFSEntry.md#type)

## Properties

### cid

• **cid**: `CID`

The CID of the object

#### Defined in

[files/index.ts:182](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L182)

___

### mode

• `Optional` **mode**: `number`

The UnixFS mode as a Number

#### Defined in

[files/index.ts:187](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L187)

___

### mtime

• `Optional` **mtime**: `Mtime`

An object with numeric secs and nsecs properties

#### Defined in

[files/index.ts:192](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L192)

___

### name

• **name**: `string`

The object's name

#### Defined in

[files/index.ts:167](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L167)

___

### size

• **size**: `number`

The size of the file in bytes

#### Defined in

[files/index.ts:177](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L177)

___

### type

• **type**: ``"file"`` \| ``"directory"``

The object's type (directory or file)

#### Defined in

[files/index.ts:172](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/files/index.ts#L172)
