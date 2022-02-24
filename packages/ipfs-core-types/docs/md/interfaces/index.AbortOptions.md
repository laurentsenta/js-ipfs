[ipfs-core-types](../README.md) / [Modules](../modules.md) / [index](../modules/index.md) / AbortOptions

# Interface: AbortOptions

[index](../modules/index.md).AbortOptions

Common options across all cancellable requests.

## Hierarchy

- **`AbortOptions`**

  ↳ [`AddOptions`](root.AddOptions.md)

  ↳ [`CatOptions`](root.CatOptions.md)

  ↳ [`GetOptions`](root.GetOptions.md)

  ↳ [`ListOptions`](root.ListOptions.md)

  ↳ [`IDOptions`](root.IDOptions.md)

  ↳ [`DNSOptions`](root.DNSOptions.md)

  ↳ [`PingOptions`](root.PingOptions.md)

  ↳ [`ResolveOptions`](root.ResolveOptions.md)

  ↳ [`MountOptions`](root.MountOptions.md)

  ↳ [`PutOptions`](block.PutOptions.md)

  ↳ [`RmOptions`](block.RmOptions.md)

  ↳ [`GetOptions`](dag.GetOptions.md)

  ↳ [`PutOptions`](dag.PutOptions.md)

  ↳ [`RmOptions`](dag.RmOptions.md)

  ↳ [`TreeOptions`](dag.TreeOptions.md)

  ↳ [`ResolveOptions`](dag.ResolveOptions.md)

  ↳ [`ExportOptions`](dag.ExportOptions.md)

  ↳ [`ImportOptions`](dag.ImportOptions.md)

  ↳ [`DHTProvideOptions`](dht.DHTProvideOptions.md)

  ↳ [`ChmodOptions`](files.ChmodOptions.md)

  ↳ [`CpOptions`](files.CpOptions.md)

  ↳ [`MkdirOptions`](files.MkdirOptions.md)

  ↳ [`StatOptions`](files.StatOptions.md)

  ↳ [`TouchOptions`](files.TouchOptions.md)

  ↳ [`RmOptions`](files.RmOptions.md)

  ↳ [`ReadOptions`](files.ReadOptions.md)

  ↳ [`WriteOptions`](files.WriteOptions.md)

  ↳ [`MvOptions`](files.MvOptions.md)

  ↳ [`GenOptions`](key.GenOptions.md)

  ↳ [`PublishOptions`](name.PublishOptions.md)

  ↳ [`ResolveOptions`](name.ResolveOptions.md)

  ↳ [`NewObjectOptions`](object.NewObjectOptions.md)

  ↳ [`PutOptions`](object.PutOptions.md)

  ↳ [`AddOptions`](pin.AddOptions.md)

  ↳ [`AddAllOptions`](pin.AddAllOptions.md)

  ↳ [`LsOptions`](pin.LsOptions.md)

  ↳ [`RmOptions`](pin.RmOptions.md)

  ↳ [`SubscribeOptions`](pubsub.SubscribeOptions.md)

  ↳ [`RefsOptions`](refs.RefsOptions.md)

  ↳ [`GCOptions`](repo.GCOptions.md)

  ↳ [`BWOptions`](stats.BWOptions.md)

  ↳ [`PeersOptions`](swarm.PeersOptions.md)

## Table of contents

### Properties

- [signal](index.AbortOptions.md#signal)
- [timeout](index.AbortOptions.md#timeout)

## Properties

### signal

• `Optional` **signal**: `AbortSignal`

Can be provided to a function that starts a long running task, which will
be aborted when signal is triggered.

#### Defined in

[utils.ts:104](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L104)

___

### timeout

• `Optional` **timeout**: `number`

Can be provided to a function that starts a long running task, which will
be aborted after provided timeout (in ms).

#### Defined in

[utils.ts:109](https://github.com/ipfs/js-ipfs/blob/1655368d/packages/ipfs-core-types/src/utils.ts#L109)
