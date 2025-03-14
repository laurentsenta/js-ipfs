# Change Log

All notable changes to this project will be documented in this file.
See [Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [0.153.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.152.2...interface-ipfs-core@0.153.0) (2021-12-15)


### Bug Fixes

* **pubsub:** multibase in pubsub http rpc ([#3922](https://github.com/ipfs/js-ipfs/issues/3922)) ([6eeaca4](https://github.com/ipfs/js-ipfs/commit/6eeaca452c36fa13be42d704575c577e4ca938f1))
* return nested value from dag.get ([#3966](https://github.com/ipfs/js-ipfs/issues/3966)) ([45ac973](https://github.com/ipfs/js-ipfs/commit/45ac9730d6484e8324acfbc3579fce052b8452d7)), closes [#3957](https://github.com/ipfs/js-ipfs/issues/3957)


### chore

* Bump @ipld/dag-cbor to v7 ([#3977](https://github.com/ipfs/js-ipfs/issues/3977)) ([73476f5](https://github.com/ipfs/js-ipfs/commit/73476f55e39ecfb01eb2b4880637aad658f51bc2))


### Features

* dht client ([#3947](https://github.com/ipfs/js-ipfs/issues/3947)) ([62d8ecb](https://github.com/ipfs/js-ipfs/commit/62d8ecbc723e693a2544e69172d99c576d187c23))
* update DAG API to match go-ipfs@0.10 changes ([#3917](https://github.com/ipfs/js-ipfs/issues/3917)) ([38c01be](https://github.com/ipfs/js-ipfs/commit/38c01be03b4fd5f401cd9b698cfdb4237d835b01))


### BREAKING CHANGES

* **pubsub:** We had to make breaking changes to `pubsub` commands sent over HTTP RPC  to fix data corruption caused by topic names and payload bytes that included `\n`. More details in https://github.com/ipfs/go-ipfs/issues/7939 and https://github.com/ipfs/go-ipfs/pull/8183 
* On decode of CBOR blocks, `undefined` values will be coerced to `null`
* `ipfs.dag.put` no longer accepts a `format` arg, it is now `storeCodec` and `inputCodec`.  `'json'` has become `'dag-json'`, `'cbor'` has become `'dag-cbor'` and so on
* The DHT API has been refactored to return async iterators of query events





### [0.154.1](https://www.github.com/ipfs/js-ipfs/compare/interface-ipfs-core-v0.154.0...interface-ipfs-core-v0.154.1) (2022-02-06)


### Bug Fixes

* **dag:** replace custom dag walk with multiformats/traversal ([#3950](https://www.github.com/ipfs/js-ipfs/issues/3950)) ([596b1f4](https://www.github.com/ipfs/js-ipfs/commit/596b1f48a014083b1736e4ad7e746c652d2583b1))
* override hashing algorithm when importing files ([#4042](https://www.github.com/ipfs/js-ipfs/issues/4042)) ([709831f](https://www.github.com/ipfs/js-ipfs/commit/709831f61a822d28a6b8e4d6ddc2b659a836079f)), closes [#3952](https://www.github.com/ipfs/js-ipfs/issues/3952)


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * ipfs-core-types bumped from ^0.10.0 to ^0.10.1

## [0.154.0](https://www.github.com/ipfs/js-ipfs/compare/interface-ipfs-core-v0.153.0...interface-ipfs-core-v0.154.0) (2022-01-27)


### ⚠ BREAKING CHANGES

* peerstore methods are now all async, the repo is migrated to v12
* node 15+ is required

### Features

* add support for dag-jose codec ([#4028](https://www.github.com/ipfs/js-ipfs/issues/4028)) ([fbe1492](https://www.github.com/ipfs/js-ipfs/commit/fbe1492395ad98e620a872208530a3f8f61535a9))
* libp2p async peerstore ([#4018](https://www.github.com/ipfs/js-ipfs/issues/4018)) ([a6b201a](https://www.github.com/ipfs/js-ipfs/commit/a6b201af2c3697430ab0ebe002dd573d185f1ac0))


### Bug Fixes

* remove abort-controller deps ([#4015](https://www.github.com/ipfs/js-ipfs/issues/4015)) ([902e887](https://www.github.com/ipfs/js-ipfs/commit/902e887e1acac87f607324fa7cb5ad4b14aefcf3))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * ipfs-core-types bumped from ^0.9.0 to ^0.10.0

## [0.152.2](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.152.1...interface-ipfs-core@0.152.2) (2021-11-24)

**Note:** Version bump only for package interface-ipfs-core





## [0.152.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.152.0...interface-ipfs-core@0.152.1) (2021-11-19)

**Note:** Version bump only for package interface-ipfs-core





# [0.152.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.151.1...interface-ipfs-core@0.152.0) (2021-11-12)


### Bug Fixes

* do not accept single items for ipfs.add ([#3900](https://github.com/ipfs/js-ipfs/issues/3900)) ([04e3cf3](https://github.com/ipfs/js-ipfs/commit/04e3cf3f46b585c4644cba70516f375e95361f52))
* do not lose files when writing files into subshards that contain other subshards ([#3936](https://github.com/ipfs/js-ipfs/issues/3936)) ([8a3ed19](https://github.com/ipfs/js-ipfs/commit/8a3ed19575beaafe5dfd3bce310a548950c148d0)), closes [#3921](https://github.com/ipfs/js-ipfs/issues/3921)


### BREAKING CHANGES

* errors will now be thrown if multiple items are passed to `ipfs.add` or single items to `ipfs.addAll` (n.b. you can still pass a list of a single item to `ipfs.addAll`)





## [0.151.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.151.0...interface-ipfs-core@0.151.1) (2021-09-28)

**Note:** Version bump only for package interface-ipfs-core





# [0.151.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.150.4...interface-ipfs-core@0.151.0) (2021-09-24)


### Features

* pull in new globSource ([#3889](https://github.com/ipfs/js-ipfs/issues/3889)) ([be4a542](https://github.com/ipfs/js-ipfs/commit/be4a5428ebc4b05a2edd9a91bf9df6416c1a8c2b))
* switch to esm ([#3879](https://github.com/ipfs/js-ipfs/issues/3879)) ([9a40109](https://github.com/ipfs/js-ipfs/commit/9a40109632e5b4837eb77a2f57dbc77fbf1fe099))


### BREAKING CHANGES

* the globSource api has changed from `globSource(dir, opts)` to `globSource(dir, pattern, opts)`
* There are no default exports and everything is now dual published as ESM/CJS





## [0.150.4](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.150.3...interface-ipfs-core@0.150.4) (2021-09-17)

**Note:** Version bump only for package interface-ipfs-core





## [0.150.3](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.150.2...interface-ipfs-core@0.150.3) (2021-09-17)

**Note:** Version bump only for package interface-ipfs-core





## [0.150.2](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.150.1...interface-ipfs-core@0.150.2) (2021-09-02)


### Bug Fixes

* declare types in .ts files ([#3840](https://github.com/ipfs/js-ipfs/issues/3840)) ([eba5fe6](https://github.com/ipfs/js-ipfs/commit/eba5fe6832858107b3e1ae02c99de674622f12b4))
* remove client-side timeout from http rpc calls ([#3178](https://github.com/ipfs/js-ipfs/issues/3178)) ([f11220e](https://github.com/ipfs/js-ipfs/commit/f11220e00a12afed5ebbbd8b4c5134595aea735d)), closes [#3161](https://github.com/ipfs/js-ipfs/issues/3161)
* remove use of instanceof for CID class ([#3847](https://github.com/ipfs/js-ipfs/issues/3847)) ([ebbb12d](https://github.com/ipfs/js-ipfs/commit/ebbb12db523c53ce8e4ddae5266cd9acb3504431))





## [0.150.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.150.0...interface-ipfs-core@0.150.1) (2021-08-25)

**Note:** Version bump only for package interface-ipfs-core





# [0.150.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.149.0...interface-ipfs-core@0.150.0) (2021-08-17)


### Bug Fixes

* pin nanoid version ([#3807](https://github.com/ipfs/js-ipfs/issues/3807)) ([474523a](https://github.com/ipfs/js-ipfs/commit/474523ab8702729f697843d433a7a08baf2d101f))
* throw error on missing input to add/addAll ([#3818](https://github.com/ipfs/js-ipfs/issues/3818)) ([1343708](https://github.com/ipfs/js-ipfs/commit/1343708f70d7298b6677555803d68ff282d89439)), closes [#3788](https://github.com/ipfs/js-ipfs/issues/3788)


### Features

* pubsub over gRPC ([#3813](https://github.com/ipfs/js-ipfs/issues/3813)) ([e7d5509](https://github.com/ipfs/js-ipfs/commit/e7d5509c87e87aed6be3c1d0b2a01ab74cdc1ed9)), closes [#3741](https://github.com/ipfs/js-ipfs/issues/3741)





# [0.149.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.148.0...interface-ipfs-core@0.149.0) (2021-08-11)


### Bug Fixes

* return rate in/out as number ([#3798](https://github.com/ipfs/js-ipfs/issues/3798)) ([2f3df7a](https://github.com/ipfs/js-ipfs/commit/2f3df7a70fe94d6bdf20947854dc9d0b88cb759a)), closes [#3782](https://github.com/ipfs/js-ipfs/issues/3782)


### Features

* ed25519 keys by default ([#3693](https://github.com/ipfs/js-ipfs/issues/3693)) ([33fa734](https://github.com/ipfs/js-ipfs/commit/33fa7341c3baaf0926d887c071cc6fbce5ac49a8))
* make ipfs.get output tarballs ([#3785](https://github.com/ipfs/js-ipfs/issues/3785)) ([1ad6001](https://github.com/ipfs/js-ipfs/commit/1ad60018d39d5b46c484756631e30e1989fd8eba))


### BREAKING CHANGES

* rateIn/rateOut are returned as numbers
* the output type of `ipfs.get` has changed and the `recursive` option has been removed from `ipfs.ls` since it was not supported everywhere





# [0.148.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.147.0...interface-ipfs-core@0.148.0) (2021-07-27)


### Bug Fixes

* fix flaky pubsub test ([#3761](https://github.com/ipfs/js-ipfs/issues/3761)) ([8bcf56f](https://github.com/ipfs/js-ipfs/commit/8bcf56fbec7324dc13d3ec5dce08806a6ef2f974))
* flaky timeout test ([#3767](https://github.com/ipfs/js-ipfs/issues/3767)) ([55afc2f](https://github.com/ipfs/js-ipfs/commit/55afc2f8ee483f4b2807598b7371561d39229e17))
* make "ipfs resolve" cli command recursive by default ([#3707](https://github.com/ipfs/js-ipfs/issues/3707)) ([399ce36](https://github.com/ipfs/js-ipfs/commit/399ce367a1dbc531b52fe228ee4212008c9a1091)), closes [#3692](https://github.com/ipfs/js-ipfs/issues/3692)


### Features

* implement dag import/export ([#3728](https://github.com/ipfs/js-ipfs/issues/3728)) ([700765b](https://github.com/ipfs/js-ipfs/commit/700765be2634fa5d2d71d8b87cf68c9cd328d2c4)), closes [#2953](https://github.com/ipfs/js-ipfs/issues/2953) [#2745](https://github.com/ipfs/js-ipfs/issues/2745)
* upgrade to the new multiformats ([#3556](https://github.com/ipfs/js-ipfs/issues/3556)) ([d13d15f](https://github.com/ipfs/js-ipfs/commit/d13d15f022a87d04a35f0f7822142f9cb898479c))


### BREAKING CHANGES

* resolve is now recursive by default

Co-authored-by: Alex Potsides <alex@achingbrain.net>
* ipld-formats no longer supported, use multiformat BlockCodecs instead

Co-authored-by: Rod Vagg <rod@vagg.org>
Co-authored-by: achingbrain <alex@achingbrain.net>





# [0.147.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.146.1...interface-ipfs-core@0.147.0) (2021-06-18)


### Features

* support v2 ipns signatures ([#3708](https://github.com/ipfs/js-ipfs/issues/3708)) ([ade01d1](https://github.com/ipfs/js-ipfs/commit/ade01d138bb185fda902c0a3f7fa14d5bfd48a5e))





## [0.146.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.146.0...interface-ipfs-core@0.146.1) (2021-06-05)


### Bug Fixes

* stalling subscription on (node) http-client when daemon is stopped ([#3468](https://github.com/ipfs/js-ipfs/issues/3468)) ([0266abf](https://github.com/ipfs/js-ipfs/commit/0266abf0c4b817636172f78c6e91eb4dd5aad451)), closes [#3465](https://github.com/ipfs/js-ipfs/issues/3465)





# [0.146.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.145.1...interface-ipfs-core@0.146.0) (2021-05-26)


### Features

* allow passing the id of a network peer to ipfs.id ([#3386](https://github.com/ipfs/js-ipfs/issues/3386)) ([00fd709](https://github.com/ipfs/js-ipfs/commit/00fd709a7b71e7cf354ea452ebce460dd7375d34))





## [0.145.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.145.0...interface-ipfs-core@0.145.1) (2021-05-11)


### Bug Fixes

* ipfs get with raw blocks ([#3683](https://github.com/ipfs/js-ipfs/issues/3683)) ([28235b0](https://github.com/ipfs/js-ipfs/commit/28235b02558c513e1119dfd3d12b622d67546eca)), closes [#3682](https://github.com/ipfs/js-ipfs/issues/3682)





# [0.145.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.144.2...interface-ipfs-core@0.145.0) (2021-05-10)


### Bug Fixes

* mark ipld options as partial ([#3669](https://github.com/ipfs/js-ipfs/issues/3669)) ([f98af8e](https://github.com/ipfs/js-ipfs/commit/f98af8ed24784929898bb5d33a64dc442c77074d))
* only accept cid for ipfs.dag.get ([#3675](https://github.com/ipfs/js-ipfs/issues/3675)) ([bb8f8bc](https://github.com/ipfs/js-ipfs/commit/bb8f8bc501ffc1ee0f064ba61ec0bca4015bf6ad)), closes [#3637](https://github.com/ipfs/js-ipfs/issues/3637)


### chore

* upgrade deps with new typedefs ([#3550](https://github.com/ipfs/js-ipfs/issues/3550)) ([a418a52](https://github.com/ipfs/js-ipfs/commit/a418a521574c878d7aabd0ad2fd8d516908a3756))


### Features

* support identity hash in block.get + dag.get ([#3616](https://github.com/ipfs/js-ipfs/issues/3616)) ([28ad9ad](https://github.com/ipfs/js-ipfs/commit/28ad9ad6e50abb89a366ecd6b5301e848f0e9962))


### BREAKING CHANGES

* all core api methods now have types, some method signatures have changed, named exports are now used by the http, grpc and ipfs client modules





## [0.144.2](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.144.1...interface-ipfs-core@0.144.2) (2021-03-09)


### Bug Fixes

* update to new aegir ([#3528](https://github.com/ipfs/js-ipfs/issues/3528)) ([49f7880](https://github.com/ipfs/js-ipfs/commit/49f78807d7e26483bd926b45cc7e0f797d77e41b))





## [0.144.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.144.0...interface-ipfs-core@0.144.1) (2021-02-08)

**Note:** Version bump only for package interface-ipfs-core





# [0.144.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.143.1...interface-ipfs-core@0.144.0) (2021-02-01)


### Bug Fixes

* updates webpack example to use v5 ([#3512](https://github.com/ipfs/js-ipfs/issues/3512)) ([c7110db](https://github.com/ipfs/js-ipfs/commit/c7110db71b5c0f0f9f415f31f91b5b228341e13e)), closes [#3511](https://github.com/ipfs/js-ipfs/issues/3511)


### chore

* update deps ([#3514](https://github.com/ipfs/js-ipfs/issues/3514)) ([061d77c](https://github.com/ipfs/js-ipfs/commit/061d77cc03f40af5a3bc3590481e1e5836e7f0d8))


### Features

* support  remote pinning services in ipfs-http-client ([#3293](https://github.com/ipfs/js-ipfs/issues/3293)) ([ba240fd](https://github.com/ipfs/js-ipfs/commit/ba240fdf93edc88028315483240d7822a7ca88ed))


### BREAKING CHANGES

* ipfs-repo upgrade requires repo migration to v10





## [0.143.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.143.0...interface-ipfs-core@0.143.1) (2021-01-20)

**Note:** Version bump only for package interface-ipfs-core





# [0.143.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.142.3...interface-ipfs-core@0.143.0) (2021-01-15)


### chore

* update libp2p to 0.30 ([#3427](https://github.com/ipfs/js-ipfs/issues/3427)) ([a39e6fb](https://github.com/ipfs/js-ipfs/commit/a39e6fb372bf9e7782462b6a4b7530a3f8c9b3f1))


### Features

* add grpc server and client ([#3403](https://github.com/ipfs/js-ipfs/issues/3403)) ([a9027e0](https://github.com/ipfs/js-ipfs/commit/a9027e0ec0cea9a4f34b4f2f52e09abb35237384)), closes [#2519](https://github.com/ipfs/js-ipfs/issues/2519) [#2838](https://github.com/ipfs/js-ipfs/issues/2838) [#2943](https://github.com/ipfs/js-ipfs/issues/2943) [#2854](https://github.com/ipfs/js-ipfs/issues/2854) [#2864](https://github.com/ipfs/js-ipfs/issues/2864)
* allow passing a http.Agent to the grpc client ([#3477](https://github.com/ipfs/js-ipfs/issues/3477)) ([c5f0bc5](https://github.com/ipfs/js-ipfs/commit/c5f0bc5eeee15369b7d02901035b04184a8608d2)), closes [#3474](https://github.com/ipfs/js-ipfs/issues/3474)


### BREAKING CHANGES

* The websocket transport will only dial DNS+WSS addresses - see https://github.com/libp2p/js-libp2p-websockets/releases/tag/v0.15.0

Co-authored-by: Hugo Dias <hugomrdias@gmail.com>





## [0.142.3](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.142.2...interface-ipfs-core@0.142.3) (2020-12-16)


### Bug Fixes

* fix ipfs.ls() for a single file object ([#3440](https://github.com/ipfs/js-ipfs/issues/3440)) ([f243dd1](https://github.com/ipfs/js-ipfs/commit/f243dd1c37fcb9786d77d129cd9b238457d18a15))
* regressions introduced by new releases of CID & multicodec ([#3442](https://github.com/ipfs/js-ipfs/issues/3442)) ([b5152d8](https://github.com/ipfs/js-ipfs/commit/b5152d8cc93ecc8d39fc353ea66d7eaf1661e3c0)), closes [/github.com/multiformats/js-cid/commit/0e11f035c9230e7f6d79c159ace9b80de88cb5eb#diff-25a6634263c1b1f6fc4697a04e2b9904ea4b042a89af59dc93ec1f5d44848a26](https://github.com//github.com/multiformats/js-cid/commit/0e11f035c9230e7f6d79c159ace9b80de88cb5eb/issues/diff-25a6634263c1b1f6fc4697a04e2b9904ea4b042a89af59dc93ec1f5d44848a26)





## [0.142.2](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.142.1...interface-ipfs-core@0.142.2) (2020-11-25)

**Note:** Version bump only for package interface-ipfs-core





## [0.142.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.142.0...interface-ipfs-core@0.142.1) (2020-11-16)


### Bug Fixes

* align behaviour between go and js for content without paths ([#3385](https://github.com/ipfs/js-ipfs/issues/3385)) ([334873d](https://github.com/ipfs/js-ipfs/commit/334873d3784e2baa2b19f8f69b5aade36715ba03))
* ensure correct progress is reported ([#3384](https://github.com/ipfs/js-ipfs/issues/3384)) ([633d870](https://github.com/ipfs/js-ipfs/commit/633d8704f74534542f54536bc6960528214339a2))
* report ipfs.add progress over http ([#3310](https://github.com/ipfs/js-ipfs/issues/3310)) ([39cad4b](https://github.com/ipfs/js-ipfs/commit/39cad4b76b950ea6a76477fd01f8631b8bd9aa1e))





# [0.142.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.141.0...interface-ipfs-core@0.142.0) (2020-11-09)


### Features

* pass file name to add/addAll progress handler ([#3372](https://github.com/ipfs/js-ipfs/issues/3372)) ([69681a7](https://github.com/ipfs/js-ipfs/commit/69681a7d7a8434c11f6f10e370e324f5a3d31042)), closes [ipfs/js-ipfs-unixfs#87](https://github.com/ipfs/js-ipfs-unixfs/issues/87)





# [0.141.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.140.0...interface-ipfs-core@0.141.0) (2020-10-28)


### Bug Fixes

* files ls should return string ([#3352](https://github.com/ipfs/js-ipfs/issues/3352)) ([16ecc74](https://github.com/ipfs/js-ipfs/commit/16ecc7485dfbb1f0c827c5f804974bb804f3dafd)), closes [#3345](https://github.com/ipfs/js-ipfs/issues/3345) [#2939](https://github.com/ipfs/js-ipfs/issues/2939) [#3330](https://github.com/ipfs/js-ipfs/issues/3330) [#2948](https://github.com/ipfs/js-ipfs/issues/2948)
* use fetch in electron renderer and electron-fetch in main ([#3251](https://github.com/ipfs/js-ipfs/issues/3251)) ([639d71f](https://github.com/ipfs/js-ipfs/commit/639d71f7ac8f66d9633e753a2a6be927e14a5af0))


### Features

* type check & generate defs from jsdoc ([#3281](https://github.com/ipfs/js-ipfs/issues/3281)) ([bbcaf34](https://github.com/ipfs/js-ipfs/commit/bbcaf34111251b142273a5675f4754ff68bd9fa0))


### BREAKING CHANGES

* types returned by `ipfs.files.ls` are now strings, in line with the docs but different to previous behaviour

Co-authored-by: Geoffrey Cohler <g.cohler@computer.org>





# [0.140.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.139.1...interface-ipfs-core@0.140.0) (2020-09-03)


### Bug Fixes

* handle progress for empty files ([#3260](https://github.com/ipfs/js-ipfs/issues/3260)) ([9c36cb8](https://github.com/ipfs/js-ipfs/commit/9c36cb8f0c122e78c3cda3d0769d66c4d380787a)), closes [#3255](https://github.com/ipfs/js-ipfs/issues/3255)


### Features

* add protocol list to ipfs id ([#3250](https://github.com/ipfs/js-ipfs/issues/3250)) ([1b6cf60](https://github.com/ipfs/js-ipfs/commit/1b6cf600a6b1348199457ca1fe6f314b6eff8c46))
* ipns publish example ([#3207](https://github.com/ipfs/js-ipfs/issues/3207)) ([91faec6](https://github.com/ipfs/js-ipfs/commit/91faec6e3d89b0d9883b8d7815c276d44048e739))
* store pins in datastore instead of a DAG ([#2771](https://github.com/ipfs/js-ipfs/issues/2771)) ([64b7fe4](https://github.com/ipfs/js-ipfs/commit/64b7fe41738cbe96d5a9075f0c01156c6f889c40))
* update hapi to v20 ([#3245](https://github.com/ipfs/js-ipfs/issues/3245)) ([1aeef89](https://github.com/ipfs/js-ipfs/commit/1aeef89c73f42a2f6cceb7f0598400141ce40e23))





## [0.139.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.139.0...interface-ipfs-core@0.139.1) (2020-08-24)


### Bug Fixes

* validate ipns records with inline public keys ([#3224](https://github.com/ipfs/js-ipfs/issues/3224)) ([5cc0e08](https://github.com/ipfs/js-ipfs/commit/5cc0e086b036e7ba40b09768b67b7067adca43c1))





# [0.139.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.138.0...interface-ipfs-core@0.139.0) (2020-08-12)


### Bug Fixes

* support keychain without pass ([#3212](https://github.com/ipfs/js-ipfs/issues/3212)) ([7e0e85c](https://github.com/ipfs/js-ipfs/commit/7e0e85c2f003a09845b1dbe4200ca61366933b05))


### Features

* share IPFS node between browser tabs ([#3081](https://github.com/ipfs/js-ipfs/issues/3081)) ([1b8b1b8](https://github.com/ipfs/js-ipfs/commit/1b8b1b822a252498889c54972a1f57e1fedc39d0)), closes [#3022](https://github.com/ipfs/js-ipfs/issues/3022)


### BREAKING CHANGES

* remove support for key.export over the http api





# [0.138.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.137.0...interface-ipfs-core@0.138.0) (2020-07-16)


### Bug Fixes

* optional arguments go in the options object ([#3118](https://github.com/ipfs/js-ipfs/issues/3118)) ([8cb8c73](https://github.com/ipfs/js-ipfs/commit/8cb8c73037e44894d756b70f344b3282463206f9))


### Features

* add interface and http client versions to version output ([#3125](https://github.com/ipfs/js-ipfs/issues/3125)) ([65f8b23](https://github.com/ipfs/js-ipfs/commit/65f8b23f550f939e94aaf6939894a513519e6d68)), closes [#2878](https://github.com/ipfs/js-ipfs/issues/2878)
* store blocks by multihash instead of CID ([#3124](https://github.com/ipfs/js-ipfs/issues/3124)) ([03b17f5](https://github.com/ipfs/js-ipfs/commit/03b17f5e2d290e84aa0cb541079b79e468e7d1bd))





# [0.137.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.136.0...interface-ipfs-core@0.137.0) (2020-06-24)


### Features

* add config.getAll ([#3071](https://github.com/ipfs/js-ipfs/issues/3071)) ([16587f1](https://github.com/ipfs/js-ipfs/commit/16587f16e1b3ae525c099b1975748510638aceee))





# [0.136.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.135.1...interface-ipfs-core@0.136.0) (2020-06-05)


### Features

* sync with go-ipfs 0.5 ([#3013](https://github.com/ipfs/js-ipfs/issues/3013)) ([0900bb9](https://github.com/ipfs/js-ipfs/commit/0900bb9b8123edb689a137a006c5507d8503f693))





## [0.135.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.135.0...interface-ipfs-core@0.135.1) (2020-05-29)

**Note:** Version bump only for package interface-ipfs-core





# [0.135.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.134.3...interface-ipfs-core@0.135.0) (2020-05-18)


### Bug Fixes

* fixes browser script tag example ([#3034](https://github.com/ipfs/js-ipfs/issues/3034)) ([ee8b769](https://github.com/ipfs/js-ipfs/commit/ee8b769b96f7e3c8414bbf85853ab4e21e8fd11c)), closes [#3027](https://github.com/ipfs/js-ipfs/issues/3027)
* remove node globals ([#2932](https://github.com/ipfs/js-ipfs/issues/2932)) ([d0d2f74](https://github.com/ipfs/js-ipfs/commit/d0d2f74cef4e439c6d2baadba1f1f9f52534fcba))
* typeof bug when passing timeout to dag.get ([#3035](https://github.com/ipfs/js-ipfs/issues/3035)) ([026a542](https://github.com/ipfs/js-ipfs/commit/026a5423e00992968840c9236afe47bdab9ee834))


### Features

* cancellable api calls ([#2993](https://github.com/ipfs/js-ipfs/issues/2993)) ([2b24f59](https://github.com/ipfs/js-ipfs/commit/2b24f590041a0df9da87b75ae2344232fe22fe3a)), closes [#3015](https://github.com/ipfs/js-ipfs/issues/3015)





## [0.134.3](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.134.2...interface-ipfs-core@0.134.3) (2020-05-05)

**Note:** Version bump only for package interface-ipfs-core





## [0.134.2](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.134.1...interface-ipfs-core@0.134.2) (2020-05-05)


### Bug Fixes

* pass headers to request ([#3018](https://github.com/ipfs/js-ipfs/issues/3018)) ([3ba00f8](https://github.com/ipfs/js-ipfs/commit/3ba00f8c6a8a057c5776d539a671a74d9565fb29)), closes [#3017](https://github.com/ipfs/js-ipfs/issues/3017)





## [0.134.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.134.0...interface-ipfs-core@0.134.1) (2020-04-28)


### Bug Fixes

* fix gc tests ([#3008](https://github.com/ipfs/js-ipfs/issues/3008)) ([9f7f03e](https://github.com/ipfs/js-ipfs/commit/9f7f03e1ea672834b7f984657c7d7d7c768bcd6c))





# [0.134.0](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.133.1...interface-ipfs-core@0.134.0) (2020-04-16)


### Bug Fixes

* make http api only accept POST requests ([#2977](https://github.com/ipfs/js-ipfs/issues/2977)) ([943d4a8](https://github.com/ipfs/js-ipfs/commit/943d4a8cf2d4c4ff5ecd4814c59cb0aae0cfa1fd))
* pass timeout arg to server ([#2979](https://github.com/ipfs/js-ipfs/issues/2979)) ([049f085](https://github.com/ipfs/js-ipfs/commit/049f085fd206a1afb729fa825d8df38bf7aa8549))


### BREAKING CHANGES

* Where we used to accept all and any HTTP methods, now only POST is
accepted.  The API client will now only send POST requests too.

* test: add tests to make sure we are post-only

* chore: upgrade ipfs-utils

* fix: return 405 instead of 404 for bad methods

* fix: reject browsers that do not send an origin

Also fixes running interface tests over http in browsers against
js-ipfs





## [0.133.1](https://github.com/ipfs/js-ipfs/compare/interface-ipfs-core@0.133.0...interface-ipfs-core@0.133.1) (2020-04-08)

**Note:** Version bump only for package interface-ipfs-core





# 0.133.0 (2020-03-31)


### Bug Fixes

* avoid throw error when use readme code ([#2934](https://github.com/ipfs/js-ipfs/issues/2934)) ([b18f6e1](https://github.com/ipfs/js-ipfs/commit/b18f6e1a791f9c72c9f35ec78c471879bbdc1525))
* dont include util.textencoder in the browser ([#2919](https://github.com/ipfs/js-ipfs/issues/2919)) ([3207e3b](https://github.com/ipfs/js-ipfs/commit/3207e3b35c9c250332c03dd2a066e8ebcda35e43))


### chore

* move mfs and multipart files into core ([#2811](https://github.com/ipfs/js-ipfs/issues/2811)) ([82b9e08](https://github.com/ipfs/js-ipfs/commit/82b9e085330e6c6290e6f3dd29678247984ffdce))
* update dep version and ignore interop test for raw leaves ([#2747](https://github.com/ipfs/js-ipfs/issues/2747)) ([6376cec](https://github.com/ipfs/js-ipfs/commit/6376cec2b4beccef4751c498088f600ec7788118))


### Features

* remove ky from http-client and utils ([#2810](https://github.com/ipfs/js-ipfs/issues/2810)) ([9bc9625](https://github.com/ipfs/js-ipfs/commit/9bc96252686d0bbbfdb2a3300bb17b80eafdaf00)), closes [#2801](https://github.com/ipfs/js-ipfs/issues/2801)


### BREAKING CHANGES

* When the path passed to `ipfs.files.stat(path)` was a hamt sharded dir, the resovled
value returned by js-ipfs previously had a `type` property of with a value of
`'hamt-sharded-directory'`.  To bring it in line with go-ipfs this value is now
`'directory'`.
* Files that fit into one block imported with either `--cid-version=1`
or `--raw-leaves=true` previously returned a CID that resolved to
a raw node (e.g. a buffer). Returned CIDs now resolve to a `dag-pb`
node that contains a UnixFS entry. This is to allow setting metadata
on small files with CIDv1.





<a name="0.132.0"></a>
# [0.132.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.7...v0.132.0) (2020-02-09)


### Bug Fixes

* add object.stat timeout leeway ([#586](https://github.com/ipfs/interface-ipfs-core/issues/586)) ([8b45ad0](https://github.com/ipfs/interface-ipfs-core/commit/8b45ad0))



<a name="0.131.7"></a>
## [0.131.7](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.6...v0.131.7) (2020-02-03)


### Bug Fixes

* only expect no multiaddrs if node is in-proc webworker ([4e25b4f](https://github.com/ipfs/interface-ipfs-core/commit/4e25b4f))



<a name="0.131.6"></a>
## [0.131.6](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.5...v0.131.6) (2020-02-03)


### Bug Fixes

* use go for webworker tests ([3a96093](https://github.com/ipfs/interface-ipfs-core/commit/3a96093))



<a name="0.131.5"></a>
## [0.131.5](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.4...v0.131.5) (2020-02-03)


### Bug Fixes

* do not spawn go nodes with webrtc swarm addresses ([c633d08](https://github.com/ipfs/interface-ipfs-core/commit/c633d08))



<a name="0.131.4"></a>
## [0.131.4](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.3...v0.131.4) (2020-02-02)


### Bug Fixes

* use js for pubsub tests as before ([ade2145](https://github.com/ipfs/interface-ipfs-core/commit/ade2145))



<a name="0.131.3"></a>
## [0.131.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.2...v0.131.3) (2020-02-02)


### Bug Fixes

* spawn dialable nodes when testing with webworkers ([df7cb3a](https://github.com/ipfs/interface-ipfs-core/commit/df7cb3a))



<a name="0.131.2"></a>
## [0.131.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.1...v0.131.2) (2020-02-01)


### Bug Fixes

* fix swarm peer tests for electron ([ac7cedf](https://github.com/ipfs/interface-ipfs-core/commit/ac7cedf))



<a name="0.131.1"></a>
## [0.131.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.131.0...v0.131.1) (2020-01-31)


### Bug Fixes

* fix up peer test ([0b80a20](https://github.com/ipfs/interface-ipfs-core/commit/0b80a20))



<a name="0.131.0"></a>
# [0.131.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.130.0...v0.131.0) (2020-01-31)


### Bug Fixes

* do not assume certain implementations of ipfs are present ([#584](https://github.com/ipfs/interface-ipfs-core/issues/584)) ([3d24911](https://github.com/ipfs/interface-ipfs-core/commit/3d24911))



<a name="0.130.0"></a>
# [0.130.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.129.0...v0.130.0) (2020-01-29)


### Code Refactoring

* return peer ids as strings ([#581](https://github.com/ipfs/interface-ipfs-core/issues/581)) ([153fd24](https://github.com/ipfs/interface-ipfs-core/commit/153fd24))


### BREAKING CHANGES

* Where `PeerID`s were previously [CID]s, now they are Strings

- `ipfs.bitswap.stat().peers[n]` is now a String (was a CID)
- `ipfs.dht.findPeer().id` is now a String (was a CID)
- `ipfs.dht.findProvs()[n].id` is now a String (was a CID)
- `ipfs.dht.provide()[n].id` is now a String (was a CID)
- `ipfs.dht.put()[n].id` is now a String (was a CID)
- `ipfs.dht.query()[n].id` is now a String (was a CID)
- `ipfs.id().id` is now a String (was a CID)
- `ipfs.id().addresses[n]` are now [Multiaddr]s (were Strings)

[CID]: https://www.npmjs.com/package/cids
[Multiaddr]: https://www.npmjs.com/package/multiaddr



<a name="0.129.0"></a>
# [0.129.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.128.0...v0.129.0) (2020-01-23)



<a name="0.128.0"></a>
# [0.128.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.127.0...v0.128.0) (2020-01-22)



<a name="0.127.0"></a>
# [0.127.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.126.0...v0.127.0) (2020-01-11)



<a name="0.126.0"></a>
# [0.126.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.125.0...v0.126.0) (2020-01-09)



<a name="0.125.0"></a>
# [0.125.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.124.1...v0.125.0) (2019-12-11)


### Bug Fixes

* handle err on both start and stop echo-server ([#569](https://github.com/ipfs/interface-ipfs-core/issues/569)) ([d25c6f6](https://github.com/ipfs/interface-ipfs-core/commit/d25c6f6))


### Features

* add support for new ipfsd-ctl ([#541](https://github.com/ipfs/interface-ipfs-core/issues/541)) ([a27cfa7](https://github.com/ipfs/interface-ipfs-core/commit/a27cfa7))



## [0.124.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.124.0...v0.124.1) (2019-12-10)



<a name="0.124.0"></a>
# [0.124.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.123.0...v0.124.0) (2019-12-02)



<a name="0.123.0"></a>
# [0.123.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.122.0...v0.123.0) (2019-11-27)



<a name="0.122.0"></a>
# [0.122.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.121.0...v0.122.0) (2019-11-26)



<a name="0.121.0"></a>
# [0.121.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.120.0...v0.121.0) (2019-11-19)


### Bug Fixes

* allow offline option casing ([#561](https://github.com/ipfs/interface-ipfs-core/issues/561)) ([f08b0fd](https://github.com/ipfs/interface-ipfs-core/commit/f08b0fd))



<a name="0.120.0"></a>
# [0.120.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.119.0...v0.120.0) (2019-11-19)


### Bug Fixes

* parents option and ls stream flow ([#558](https://github.com/ipfs/interface-ipfs-core/issues/558)) ([b9df5fb](https://github.com/ipfs/interface-ipfs-core/commit/b9df5fb))



<a name="0.119.0"></a>
# [0.119.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.118.0...v0.119.0) (2019-11-11)



<a name="0.118.0"></a>
# [0.118.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.117.2...v0.118.0) (2019-11-06)


### Features

* test ipns resolve of peerid as cid ([#553](https://github.com/ipfs/interface-ipfs-core/issues/553)) ([9193957](https://github.com/ipfs/interface-ipfs-core/commit/9193957))



## [0.117.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.117.1...v0.117.2) (2019-10-05)



## [0.117.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.117.0...v0.117.1) (2019-10-05)



# [0.117.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.116.0...v0.117.0) (2019-10-04)


### Documentation

* add dry-run config test and change new/old for original/updated ([e206aa7](https://github.com/ipfs/interface-ipfs-core/commit/e206aa7))


### BREAKING CHANGES

* `ipfs.config.profiles.apply` now returns `original`/`updated` keys
in the diff because using `new` stops us from destructuring in js.



# [0.116.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.115.3...v0.116.0) (2019-10-04)


### Features

* add test for listing config profiles ([142a373](https://github.com/ipfs/interface-ipfs-core/commit/142a373))



## [0.115.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.115.2...v0.115.3) (2019-10-04)



## [0.115.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.115.1...v0.115.2) (2019-10-04)


### Bug Fixes

* configure chai for use by other modules ([77c8be9](https://github.com/ipfs/interface-ipfs-core/commit/77c8be9))
* make invalid url actually invalid ([30a84fb](https://github.com/ipfs/interface-ipfs-core/commit/30a84fb))
* test setting boolean configs keys on boolean fields ([d937fc1](https://github.com/ipfs/interface-ipfs-core/commit/d937fc1))



<a name="0.115.1"></a>
## [0.115.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.115.0...v0.115.1) (2019-10-01)



<a name="0.115.0"></a>
# [0.115.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.114.0...v0.115.0) (2019-09-25)



<a name="0.114.0"></a>
# [0.114.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.113.1...v0.114.0) (2019-09-16)


### Bug Fixes

* change swarm test ([00341f9](https://github.com/ipfs/interface-ipfs-core/commit/00341f9))
* new setup ([b724e65](https://github.com/ipfs/interface-ipfs-core/commit/b724e65))



<a name="0.113.1"></a>
## [0.113.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.113.0...v0.113.1) (2019-09-13)


### Bug Fixes

* make pubsub unsubscribe tests work in electron renderer ([eedfe3d](https://github.com/ipfs/interface-ipfs-core/commit/eedfe3d))



<a name="0.113.0"></a>
# [0.113.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.112.0...v0.113.0) (2019-09-05)


### Bug Fixes

* **package:** update ipfs-utils to version 0.1.0 ([#521](https://github.com/ipfs/interface-ipfs-core/issues/521)) ([56caa89](https://github.com/ipfs/interface-ipfs-core/commit/56caa89))



<a name="0.112.0"></a>
# [0.112.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.111.1...v0.112.0) (2019-09-03)


### Bug Fixes

* supported add inputs ([#519](https://github.com/ipfs/interface-ipfs-core/issues/519)) ([ddc4fe7](https://github.com/ipfs/interface-ipfs-core/commit/ddc4fe7))



<a name="0.111.1"></a>
## [0.111.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.111.0...v0.111.1) (2019-08-30)


### Bug Fixes

* change `cp` and `mv` tests to the current spec ([#515](https://github.com/ipfs/interface-ipfs-core/issues/515)) ([b107e57](https://github.com/ipfs/interface-ipfs-core/commit/b107e57))



<a name="0.111.0"></a>
# [0.111.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.110.0...v0.111.0) (2019-08-28)



<a name="0.110.0"></a>
# [0.110.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.109.1...v0.110.0) (2019-08-27)


### Bug Fixes

* reduce the number of concurrent requests in browser ([#505](https://github.com/ipfs/interface-ipfs-core/issues/505)) ([7596634](https://github.com/ipfs/interface-ipfs-core/commit/7596634))



<a name="0.109.1"></a>
## [0.109.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.109.0...v0.109.1) (2019-08-06)



<a name="0.109.0"></a>
# [0.109.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.108.1...v0.109.0) (2019-07-26)


### Bug Fixes

* resolve IPNS recursively test ([#507](https://github.com/ipfs/interface-ipfs-core/issues/507)) ([1db8abe](https://github.com/ipfs/interface-ipfs-core/commit/1db8abe))



<a name="0.108.1"></a>
## [0.108.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.108.0...v0.108.1) (2019-07-25)


### Bug Fixes

* reword resolve test with async/await ([#504](https://github.com/ipfs/interface-ipfs-core/issues/504)) ([3f7410a](https://github.com/ipfs/interface-ipfs-core/commit/3f7410a))
* use the correct option name for files.ls long ([#502](https://github.com/ipfs/interface-ipfs-core/issues/502)) ([ed4988d](https://github.com/ipfs/interface-ipfs-core/commit/ed4988d))



<a name="0.108.0"></a>
# [0.108.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.107.3...v0.108.0) (2019-07-17)


### Features

* tests for config profile endpoint ([#488](https://github.com/ipfs/interface-ipfs-core/issues/488)) ([e45f39c](https://github.com/ipfs/interface-ipfs-core/commit/e45f39c))



<a name="0.107.3"></a>
## [0.107.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.107.2...v0.107.3) (2019-07-16)



<a name="0.107.2"></a>
## [0.107.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.107.1...v0.107.2) (2019-07-16)


### Bug Fixes

* pin.ls ignored opts when hash was present ([#375](https://github.com/ipfs/interface-ipfs-core/issues/375)) ([be72ed6](https://github.com/ipfs/interface-ipfs-core/commit/be72ed6))



<a name="0.107.1"></a>
## [0.107.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.107.0...v0.107.1) (2019-07-11)



<a name="0.107.0"></a>
# [0.107.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.106.0...v0.107.0) (2019-07-11)


### Bug Fixes

* repo.gc() response format ([#492](https://github.com/ipfs/interface-ipfs-core/issues/492)) ([a2ec3f6](https://github.com/ipfs/interface-ipfs-core/commit/a2ec3f6))



<a name="0.106.0"></a>
# [0.106.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.105.1...v0.106.0) (2019-07-05)



<a name="0.105.1"></a>
## [0.105.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.105.0...v0.105.1) (2019-07-03)


### Bug Fixes

* wait for one key to be the required key not all ([#490](https://github.com/ipfs/interface-ipfs-core/issues/490)) ([acea55f](https://github.com/ipfs/interface-ipfs-core/commit/acea55f))



<a name="0.105.0"></a>
# [0.105.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.104.2...v0.105.0) (2019-06-20)


### Features

* add support to resolve dns to ipns ([#458](https://github.com/ipfs/interface-ipfs-core/issues/458)) ([cd41a3c](https://github.com/ipfs/interface-ipfs-core/commit/cd41a3c))



<a name="0.104.2"></a>
## [0.104.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.104.1...v0.104.2) (2019-05-31)



<a name="0.104.1"></a>
## [0.104.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.104.0...v0.104.1) (2019-05-31)


### Bug Fixes

* dht tests ([#486](https://github.com/ipfs/interface-ipfs-core/issues/486)) ([2952672](https://github.com/ipfs/interface-ipfs-core/commit/2952672))
* use cidVersion option ([#484](https://github.com/ipfs/interface-ipfs-core/issues/484)) ([e00eb4a](https://github.com/ipfs/interface-ipfs-core/commit/e00eb4a))
* **package:** update async to version 3.0.1 ([#481](https://github.com/ipfs/interface-ipfs-core/issues/481)) ([b60fe33](https://github.com/ipfs/interface-ipfs-core/commit/b60fe33))



<a name="0.104.0"></a>
# [0.104.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.103.0...v0.104.0) (2019-05-24)



<a name="0.103.0"></a>
# [0.103.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.102.0...v0.103.0) (2019-05-21)



<a name="0.102.0"></a>
# [0.102.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.101.1...v0.102.0) (2019-05-16)


### Features

* add tests for add data using File DOM api ([#461](https://github.com/ipfs/interface-ipfs-core/issues/461)) ([86a1f3f](https://github.com/ipfs/interface-ipfs-core/commit/86a1f3f))



<a name="0.101.1"></a>
## [0.101.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.101.0...v0.101.1) (2019-05-16)


### Bug Fixes

* use fixtures for refs tests ([#471](https://github.com/ipfs/interface-ipfs-core/issues/471)) ([3f30830](https://github.com/ipfs/interface-ipfs-core/commit/3f30830))



<a name="0.101.0"></a>
# [0.101.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.100.1...v0.101.0) (2019-05-15)



<a name="0.100.1"></a>
## [0.100.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.100.0...v0.100.1) (2019-05-13)


### Reverts

* add test for Object.links with CBOR ([#465](https://github.com/ipfs/interface-ipfs-core/issues/465)) ([4c3d84d](https://github.com/ipfs/interface-ipfs-core/commit/4c3d84d))



<a name="0.100.0"></a>
# [0.100.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.99.2...v0.100.0) (2019-05-08)



<a name="0.99.2"></a>
## [0.99.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.99.1...v0.99.2) (2019-04-08)



<a name="0.99.1"></a>
## [0.99.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.99.0...v0.99.1) (2019-04-04)


### Bug Fixes

* swarm addrs test ([#454](https://github.com/ipfs/interface-ipfs-core/issues/454)) ([16ad830](https://github.com/ipfs/interface-ipfs-core/commit/16ad830))



<a name="0.99.0"></a>
# [0.99.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.98.1...v0.99.0) (2019-03-13)


### Bug Fixes

* don't expect ipfs to preserve a leading slash ([#440](https://github.com/ipfs/interface-ipfs-core/issues/440)) ([d3ad40b](https://github.com/ipfs/interface-ipfs-core/commit/d3ad40b))
* ls files sizes for compat with go-ipfs 0.4.19 ([#449](https://github.com/ipfs/interface-ipfs-core/issues/449)) ([2ef1480](https://github.com/ipfs/interface-ipfs-core/commit/2ef1480)), closes [#427](https://github.com/ipfs/interface-ipfs-core/issues/427)



<a name="0.98.1"></a>
## [0.98.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.98.0...v0.98.1) (2019-03-13)



<a name="0.98.0"></a>
# [0.98.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.97.1...v0.98.0) (2019-02-26)



<a name="0.97.1"></a>
## [0.97.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.97.0...v0.97.1) (2019-02-19)


### Bug Fixes

* populate in series ([#443](https://github.com/ipfs/interface-ipfs-core/issues/443)) ([06a3980](https://github.com/ipfs/interface-ipfs-core/commit/06a3980))



<a name="0.97.0"></a>
# [0.97.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.96.1...v0.97.0) (2019-02-19)


### Bug Fixes

* add new SSL certificate ([#432](https://github.com/ipfs/interface-ipfs-core/issues/432)) ([fe539e6](https://github.com/ipfs/interface-ipfs-core/commit/fe539e6))
* add test for dag get with localResolve option ([#433](https://github.com/ipfs/interface-ipfs-core/issues/433)) ([44d4803](https://github.com/ipfs/interface-ipfs-core/commit/44d4803))



<a name="0.96.1"></a>
## [0.96.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.96.0...v0.96.1) (2019-01-15)



<a name="0.96.0"></a>
# [0.96.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.95.0...v0.96.0) (2019-01-14)



<a name="0.95.0"></a>
# [0.95.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.94.0...v0.95.0) (2019-01-04)



<a name="0.94.0"></a>
# [0.94.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.93.0...v0.94.0) (2018-12-16)



<a name="0.93.0"></a>
# [0.93.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.92.0...v0.93.0) (2018-12-14)


### Bug Fixes

* allow only by object ([#407](https://github.com/ipfs/interface-ipfs-core/issues/407)) ([1766ef4](https://github.com/ipfs/interface-ipfs-core/commit/1766ef4))
* dht find peer ([#418](https://github.com/ipfs/interface-ipfs-core/issues/418)) ([8b890b6](https://github.com/ipfs/interface-ipfs-core/commit/8b890b6))



<a name="0.92.0"></a>
# [0.92.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.91.1...v0.92.0) (2018-12-12)


### Bug Fixes

* addFromURL case ([#415](https://github.com/ipfs/interface-ipfs-core/issues/415)) ([f54422d](https://github.com/ipfs/interface-ipfs-core/commit/f54422d))



<a name="0.91.1"></a>
## [0.91.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.91.0...v0.91.1) (2018-12-11)


### Bug Fixes

* change find provs options test ([#416](https://github.com/ipfs/interface-ipfs-core/issues/416)) ([3c08aa2](https://github.com/ipfs/interface-ipfs-core/commit/3c08aa2))



<a name="0.91.0"></a>
# [0.91.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.90.0...v0.91.0) (2018-12-10)


### Bug Fixes

* another typo ([87bcd68](https://github.com/ipfs/interface-ipfs-core/commit/87bcd68))
* typos ([e7b8697](https://github.com/ipfs/interface-ipfs-core/commit/e7b8697))
* update dht responses ([#389](https://github.com/ipfs/interface-ipfs-core/issues/389)) ([c4bea6f](https://github.com/ipfs/interface-ipfs-core/commit/c4bea6f))
* Updated link in README ([#411](https://github.com/ipfs/interface-ipfs-core/issues/411)) ([81a5798](https://github.com/ipfs/interface-ipfs-core/commit/81a5798))



<a name="0.90.0"></a>
# [0.90.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.89.0...v0.90.0) (2018-12-05)



<a name="0.89.0"></a>
# [0.89.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.88.0...v0.89.0) (2018-12-03)


### Bug Fixes

* code blocks for the code ([36cf442](https://github.com/ipfs/interface-ipfs-core/commit/36cf442))
* ipns over pubsub tests ([#395](https://github.com/ipfs/interface-ipfs-core/issues/395)) ([e872b8a](https://github.com/ipfs/interface-ipfs-core/commit/e872b8a))



<a name="0.88.0"></a>
# [0.88.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.87.0...v0.88.0) (2018-11-27)



<a name="0.87.0"></a>
# [0.87.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.86.0...v0.87.0) (2018-11-26)



<a name="0.86.0"></a>
# [0.86.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.85.0...v0.86.0) (2018-11-12)


### Features

* move regular files api to top level, add addFromFs and addFromURL ([#378](https://github.com/ipfs/interface-ipfs-core/issues/378)) ([3dc7278](https://github.com/ipfs/interface-ipfs-core/commit/3dc7278))



<a name="0.85.0"></a>
# [0.85.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.84.3...v0.85.0) (2018-11-12)


### Bug Fixes

* updates ipld-dag-pb dep to version without .cid properties ([#388](https://github.com/ipfs/interface-ipfs-core/issues/388)) ([b8f7b9a](https://github.com/ipfs/interface-ipfs-core/commit/b8f7b9a))



<a name="0.84.3"></a>
## [0.84.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.84.2...v0.84.3) (2018-10-31)


### Bug Fixes

* we cant rely on error messages yet, not standardized ([fdb4998](https://github.com/ipfs/interface-ipfs-core/commit/fdb4998))



<a name="0.84.2"></a>
## [0.84.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.84.1...v0.84.2) (2018-10-31)



<a name="0.84.1"></a>
## [0.84.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.84.0...v0.84.1) (2018-10-31)



<a name="0.84.0"></a>
# [0.84.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.83.0...v0.84.0) (2018-10-31)


### Bug Fixes

* ping tests ([cd00d5d](https://github.com/ipfs/interface-ipfs-core/commit/cd00d5d))
* remove antipattern from ping tests ([2e822b6](https://github.com/ipfs/interface-ipfs-core/commit/2e822b6))



<a name="0.83.0"></a>
# [0.83.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.82.0...v0.83.0) (2018-10-30)



<a name="0.82.0"></a>
# [0.82.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.81.0...v0.82.0) (2018-10-30)



<a name="0.81.0"></a>
# [0.81.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.80.0...v0.81.0) (2018-10-29)



<a name="0.80.0"></a>
# [0.80.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.79.0...v0.80.0) (2018-10-18)



<a name="0.79.0"></a>
# [0.79.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.78.0...v0.79.0) (2018-10-15)


### Bug Fixes

* dht find peer and providers ([#368](https://github.com/ipfs/interface-ipfs-core/issues/368)) ([40f796f](https://github.com/ipfs/interface-ipfs-core/commit/40f796f))



<a name="0.78.0"></a>
# [0.78.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.77.1...v0.78.0) (2018-09-20)


### Bug Fixes

* example links in miscellaneous spec section ([#364](https://github.com/ipfs/interface-ipfs-core/issues/364)) ([45e8142](https://github.com/ipfs/interface-ipfs-core/commit/45e8142))
* test for buffer with options ([#370](https://github.com/ipfs/interface-ipfs-core/issues/370)) ([d456245](https://github.com/ipfs/interface-ipfs-core/commit/d456245))



<a name="0.77.1"></a>
## [0.77.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.77.0...v0.77.1) (2018-09-05)


### Bug Fixes

* bitswap.stat docs ([#355](https://github.com/ipfs/interface-ipfs-core/issues/355)) ([f146e1b](https://github.com/ipfs/interface-ipfs-core/commit/f146e1b))
* block CID links ([#356](https://github.com/ipfs/interface-ipfs-core/issues/356)) ([9c4d6e1](https://github.com/ipfs/interface-ipfs-core/commit/9c4d6e1))
* block stat return value key ([1e02740](https://github.com/ipfs/interface-ipfs-core/commit/1e02740))
* ipfs.io now should be resolved recursively ([#362](https://github.com/ipfs/interface-ipfs-core/issues/362)) ([d80d3a3](https://github.com/ipfs/interface-ipfs-core/commit/d80d3a3))



<a name="0.77.0"></a>
# [0.77.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.76.1...v0.77.0) (2018-08-28)


### Bug Fixes

* remove bitswap.unwant ([#353](https://github.com/ipfs/interface-ipfs-core/issues/353)) ([6065f63](https://github.com/ipfs/interface-ipfs-core/commit/6065f63)), closes [#339](https://github.com/ipfs/interface-ipfs-core/issues/339)



<a name="0.76.1"></a>
## [0.76.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.76.0...v0.76.1) (2018-08-16)


### Bug Fixes

* allow retries for DNS test due to dependence on external services ([#352](https://github.com/ipfs/interface-ipfs-core/issues/352)) ([5b3f5a8](https://github.com/ipfs/interface-ipfs-core/commit/5b3f5a8))
* typo ([b9dc12a](https://github.com/ipfs/interface-ipfs-core/commit/b9dc12a))
* typo ([2fbf551](https://github.com/ipfs/interface-ipfs-core/commit/2fbf551))



<a name="0.76.0"></a>
# [0.76.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.75.2...v0.76.0) (2018-08-10)


### Features

* ipns working locally ([#327](https://github.com/ipfs/interface-ipfs-core/issues/327)) ([49a4827](https://github.com/ipfs/interface-ipfs-core/commit/49a4827))



<a name="0.75.2"></a>
## [0.75.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.75.1...v0.75.2) (2018-08-09)


### Bug Fixes

* **spec/dag:** fix wrong example output for sha3-512 hash algorithm ([#347](https://github.com/ipfs/interface-ipfs-core/issues/347)) ([bfdda8a](https://github.com/ipfs/interface-ipfs-core/commit/bfdda8a)), closes [#307](https://github.com/ipfs/interface-ipfs-core/issues/307)
* update error messages in line with go ([#348](https://github.com/ipfs/interface-ipfs-core/issues/348)) ([a173a42](https://github.com/ipfs/interface-ipfs-core/commit/a173a42))



<a name="0.75.1"></a>
## [0.75.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.75.0...v0.75.1) (2018-08-06)


### Bug Fixes

* ensure test for resolve recursive has another node ([#346](https://github.com/ipfs/interface-ipfs-core/issues/346)) ([09c2637](https://github.com/ipfs/interface-ipfs-core/commit/09c2637))



<a name="0.75.0"></a>
# [0.75.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.74.1...v0.75.0) (2018-08-06)


### Bug Fixes

* expect config to be an object ([#344](https://github.com/ipfs/interface-ipfs-core/issues/344)) ([eca00b9](https://github.com/ipfs/interface-ipfs-core/commit/eca00b9))
* more time for CI to resolve recursively ([79b747e](https://github.com/ipfs/interface-ipfs-core/commit/79b747e))



<a name="0.74.1"></a>
## [0.74.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.74.0...v0.74.1) (2018-08-06)


### Bug Fixes

* give more time for teardown after resolve ([#345](https://github.com/ipfs/interface-ipfs-core/issues/345)) ([1db498f](https://github.com/ipfs/interface-ipfs-core/commit/1db498f))



<a name="0.74.0"></a>
# [0.74.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.73.0...v0.74.0) (2018-08-02)


### Features

* **dht:** add API to allow options in `findprovs()` ([#337](https://github.com/ipfs/interface-ipfs-core/issues/337)) ([99f74f5](https://github.com/ipfs/interface-ipfs-core/commit/99f74f5)), closes [/github.com/ipfs/js-ipfs/issues/1322#issuecomment-385336102](https://github.com//github.com/ipfs/js-ipfs/issues/1322/issues/issuecomment-385336102)



<a name="0.73.0"></a>
# [0.73.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.72.1...v0.73.0) (2018-08-02)



<a name="0.72.1"></a>
## [0.72.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.72.0...v0.72.1) (2018-07-16)


### Bug Fixes

* unsubscribe in series for go-ipfs ([#326](https://github.com/ipfs/interface-ipfs-core/issues/326)) ([8e487da](https://github.com/ipfs/interface-ipfs-core/commit/8e487da))



<a name="0.72.0"></a>
# [0.72.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.71.0...v0.72.0) (2018-07-05)



<a name="0.71.0"></a>
# [0.71.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.70.3...v0.71.0) (2018-07-03)


### Bug Fixes

* revert to serialized pubsub operations ([#319](https://github.com/ipfs/interface-ipfs-core/issues/319)) ([4b5534e](https://github.com/ipfs/interface-ipfs-core/commit/4b5534e))



<a name="0.70.3"></a>
## [0.70.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.70.2...v0.70.3) (2018-07-03)


### Bug Fixes

* allow passing only to suites with skip lists ([#321](https://github.com/ipfs/interface-ipfs-core/issues/321)) ([c47c4ce](https://github.com/ipfs/interface-ipfs-core/commit/c47c4ce))
* allow skip with object but no reason ([#318](https://github.com/ipfs/interface-ipfs-core/issues/318)) ([ef91026](https://github.com/ipfs/interface-ipfs-core/commit/ef91026))
* license ([#312](https://github.com/ipfs/interface-ipfs-core/issues/312)) ([8fa3e98](https://github.com/ipfs/interface-ipfs-core/commit/8fa3e98))



<a name="0.70.2"></a>
## [0.70.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.70.1...v0.70.2) (2018-06-29)



<a name="0.70.1"></a>
## [0.70.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.70.0...v0.70.1) (2018-06-27)


### Bug Fixes

* allow null skip for subsystems ([5df855c](https://github.com/ipfs/interface-ipfs-core/commit/5df855c))



<a name="0.70.0"></a>
# [0.70.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.69.1...v0.70.0) (2018-06-27)


### Features

* modularise tests by command, add tools to skip and only ([#290](https://github.com/ipfs/interface-ipfs-core/issues/290)) ([e232d8c](https://github.com/ipfs/interface-ipfs-core/commit/e232d8c))


### BREAKING CHANGES

* Consumers of this test suite now have fine grained control over what tests are run. Tests can now be skipped and "onlyed" (run only specific tests). This can be done on a test, command and sub-system level. See the updated usage guide for instructions: https://github.com/ipfs/js-ipfs/blob/master/packages/interface-ipfs-core/README.md#usage.

This means that tests skips depending on implementation (e.g. go/js), environment (e.g. node/browser) or platform (e.g. macOS/linux/windows) that were previously present in this suite have been removed. Consumers of this library should add their own skips based on the implementation that's being tested and the environment/platform that the tests are running on.

The following other breaking changes have been made:

1. The common object passed to test suites has changed. It must now be a function that returns a common object (same shape and functions as before).
2. The `ipfs.ls` tests (not MFS `ipfs.files.ls`) is now a root level suite. You'll need to import it and use like `tests.ls(createCommon)` to have those tests run.
3. The `generic` suite (an alias to `miscellaneous`) has been removed.

See https://github.com/ipfs/interface-ipfs-core/pull/290 for more details.

License: MIT
Signed-off-by: Alan Shaw <alan@tableflip.io>



<a name="0.69.1"></a>
## [0.69.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.69.0...v0.69.1) (2018-06-26)


### Bug Fixes

* do not rely on discovery for ping tests ([3acd6fd](https://github.com/ipfs/interface-ipfs-core/commit/3acd6fd)), closes [#310](https://github.com/ipfs/interface-ipfs-core/issues/310)



<a name="0.69.0"></a>
# [0.69.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.68.2...v0.69.0) (2018-06-22)



<a name="0.68.2"></a>
## [0.68.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.68.1...v0.68.2) (2018-06-19)


### Bug Fixes

* increase bitswap setup timeout for CI ([5886445](https://github.com/ipfs/interface-ipfs-core/commit/5886445))



<a name="0.68.1"></a>
## [0.68.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.68.0...v0.68.1) (2018-06-18)


### Bug Fixes

* removes error code checks for bitswap offline tests ([b152856](https://github.com/ipfs/interface-ipfs-core/commit/b152856))



<a name="0.68.0"></a>
# [0.68.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.67.0...v0.68.0) (2018-06-18)


### Bug Fixes

* improve bitswap wantlist and unwant docs ([7737546](https://github.com/ipfs/interface-ipfs-core/commit/7737546))
* linting errors ([fcc834c](https://github.com/ipfs/interface-ipfs-core/commit/fcc834c))
* removes duplicated TOC for pubsub ([a358cf7](https://github.com/ipfs/interface-ipfs-core/commit/a358cf7))


### Features

* add bitswap.unwant javascript spec ([df4e677](https://github.com/ipfs/interface-ipfs-core/commit/df4e677))
* add bitswap.unwant javascript spec ([d75a361](https://github.com/ipfs/interface-ipfs-core/commit/d75a361))
* add bitswap.unwant javascript spec ([c291ca9](https://github.com/ipfs/interface-ipfs-core/commit/c291ca9))
* add peerId param to bitswap.wantlist ([9f81bcb](https://github.com/ipfs/interface-ipfs-core/commit/9f81bcb))



<a name="0.67.0"></a>
# [0.67.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.66.4...v0.67.0) (2018-06-04)



<a name="0.66.4"></a>
## [0.66.4](https://github.com/ipfs/interface-ipfs-core/compare/v0.66.3...v0.66.4) (2018-05-30)


### Bug Fixes

* wait for put in object.patch.addLink before hook ([31c52d1](https://github.com/ipfs/interface-ipfs-core/commit/31c52d1))



<a name="0.66.3"></a>
## [0.66.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.66.2...v0.66.3) (2018-05-25)


### Bug Fixes

* correctly differentiate pong responses ([688f4d7](https://github.com/ipfs/interface-ipfs-core/commit/688f4d7))



<a name="0.66.2"></a>
## [0.66.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.66.1...v0.66.2) (2018-05-18)


### Bug Fixes

* spawn in series ([d976699](https://github.com/ipfs/interface-ipfs-core/commit/d976699))



<a name="0.66.1"></a>
## [0.66.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.66.0...v0.66.1) (2018-05-17)


### Bug Fixes

* increase timeouts ([9cba111](https://github.com/ipfs/interface-ipfs-core/commit/9cba111))
* remove .only ([45fab1c](https://github.com/ipfs/interface-ipfs-core/commit/45fab1c))
* wait until nodes are connected before starting ping tests ([1b60f24](https://github.com/ipfs/interface-ipfs-core/commit/1b60f24))
* **pubsub:** clear interval on error ([d074e13](https://github.com/ipfs/interface-ipfs-core/commit/d074e13))



<a name="0.66.0"></a>
# [0.66.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.9...v0.66.0) (2018-05-16)



<a name="0.65.9"></a>
## [0.65.9](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.8...v0.65.9) (2018-05-16)


### Bug Fixes

* add "files." to read* headers ([8b39b12](https://github.com/ipfs/interface-ipfs-core/commit/8b39b12))
* linting warnings ([aae31b0](https://github.com/ipfs/interface-ipfs-core/commit/aae31b0))


### Features

* add utils to spawn multiple nodes and get their ID ([e77a2f6](https://github.com/ipfs/interface-ipfs-core/commit/e77a2f6))



<a name="0.65.8"></a>
## [0.65.8](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.7...v0.65.8) (2018-05-15)



<a name="0.65.7"></a>
## [0.65.7](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.6...v0.65.7) (2018-05-15)



<a name="0.65.6"></a>
## [0.65.6](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.5...v0.65.6) (2018-05-15)



<a name="0.65.5"></a>
## [0.65.5](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.4...v0.65.5) (2018-05-12)



<a name="0.65.4"></a>
## [0.65.4](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.3...v0.65.4) (2018-05-11)



<a name="0.65.3"></a>
## [0.65.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.2...v0.65.3) (2018-05-11)



<a name="0.65.2"></a>
## [0.65.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.1...v0.65.2) (2018-05-11)



<a name="0.65.1"></a>
## [0.65.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.65.0...v0.65.1) (2018-05-11)



<a name="0.65.0"></a>
# [0.65.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.64.3...v0.65.0) (2018-05-11)


### Bug Fixes

* many fixes for pubsub tests with new async unsubscribe ([2019c45](https://github.com/ipfs/interface-ipfs-core/commit/2019c45))
* pubsub subscribe call with options ([c43f8bc](https://github.com/ipfs/interface-ipfs-core/commit/c43f8bc))
* remove .only ([251cffd](https://github.com/ipfs/interface-ipfs-core/commit/251cffd))
* remove duplicate async.each ([f798597](https://github.com/ipfs/interface-ipfs-core/commit/f798597))



<a name="0.64.3"></a>
## [0.64.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.64.2...v0.64.3) (2018-05-06)


### Bug Fixes

* Typos on bundled libraries pull request ([2972426](https://github.com/ipfs/interface-ipfs-core/commit/2972426))


### Features

* add onlyHash option to files.add ([#259](https://github.com/ipfs/interface-ipfs-core/issues/259)) ([63179b9](https://github.com/ipfs/interface-ipfs-core/commit/63179b9))


### Performance Improvements

* **pubsub:** Change pubsub tests to do lighter load testing ([90a1520](https://github.com/ipfs/interface-ipfs-core/commit/90a1520))



<a name="0.64.2"></a>
## [0.64.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.64.1...v0.64.2) (2018-04-23)



<a name="0.64.1"></a>
## [0.64.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.64.0...v0.64.1) (2018-04-23)


### Bug Fixes

* this.skip needs to be under a function declaration ([2545ddd](https://github.com/ipfs/interface-ipfs-core/commit/2545ddd))



<a name="0.64.0"></a>
# [0.64.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.62.0...v0.64.0) (2018-04-23)


### Features

* adds pull stream tests for files.add ([d75986a](https://github.com/ipfs/interface-ipfs-core/commit/d75986a))
* better badge ([#246](https://github.com/ipfs/interface-ipfs-core/issues/246)) ([a3869bf](https://github.com/ipfs/interface-ipfs-core/commit/a3869bf))



<a name="0.63.0"></a>
# [0.63.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.62.0...v0.63.0) (2018-04-23)


### Features

* adds pull stream tests for files.add ([d75986a](https://github.com/ipfs/interface-ipfs-core/commit/d75986a))



<a name="0.62.0"></a>
# [0.62.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.61.0...v0.62.0) (2018-04-14)



<a name="0.61.0"></a>
# [0.61.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.60.1...v0.61.0) (2018-04-10)



<a name="0.60.1"></a>
## [0.60.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.60.0...v0.60.1) (2018-04-05)


### Bug Fixes

* fix wrapWithDirectory test ([a97c087](https://github.com/ipfs/interface-ipfs-core/commit/a97c087))



<a name="0.60.0"></a>
# [0.60.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.59.0...v0.60.0) (2018-04-05)


### Features

* Provide access to bundled libraries when in browser ([db83b50](https://github.com/ipfs/interface-ipfs-core/commit/db83b50))



<a name="0.59.0"></a>
# [0.59.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.58.0...v0.59.0) (2018-04-03)


### Features

* add wrapWithDirectory to files.add et al ([03eec9e](https://github.com/ipfs/interface-ipfs-core/commit/03eec9e))



<a name="0.58.0"></a>
# [0.58.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.57.0...v0.58.0) (2018-03-22)


### Bug Fixes

* wrong description ([bad70ac](https://github.com/ipfs/interface-ipfs-core/commit/bad70ac))



<a name="0.57.0"></a>
# [0.57.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.6...v0.57.0) (2018-03-16)



<a name="0.56.6"></a>
## [0.56.6](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.5...v0.56.6) (2018-03-16)



<a name="0.56.5"></a>
## [0.56.5](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.4...v0.56.5) (2018-03-16)


### Bug Fixes

* go-ipfs has not shipped withLocal yet ([58b1fe2](https://github.com/ipfs/interface-ipfs-core/commit/58b1fe2))



<a name="0.56.4"></a>
## [0.56.4](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.3...v0.56.4) (2018-03-16)



<a name="0.56.3"></a>
## [0.56.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.2...v0.56.3) (2018-03-16)



<a name="0.56.2"></a>
## [0.56.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.1...v0.56.2) (2018-03-16)



<a name="0.56.1"></a>
## [0.56.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.56.0...v0.56.1) (2018-03-16)


### Bug Fixes

* don't error to specific ([ec16016](https://github.com/ipfs/interface-ipfs-core/commit/ec16016))
* fix broken stat tests ([#236](https://github.com/ipfs/interface-ipfs-core/issues/236)) ([fcb8341](https://github.com/ipfs/interface-ipfs-core/commit/fcb8341)), closes [/github.com/ipfs/interface-ipfs-core/commit/c4934ca0b3b43f5bfc1ff5dd38f85d945d3244de#diff-0a6449ecfa8b9e3d807f53dde24eca71R66](https://github.com//github.com/ipfs/interface-ipfs-core/commit/c4934ca0b3b43f5bfc1ff5dd38f85d945d3244de/issues/diff-0a6449ecfa8b9e3d807f53dde24eca71R66)



<a name="0.56.0"></a>
# [0.56.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.55.1...v0.56.0) (2018-03-12)


### Features

* complete files.stat with the 'with-local' option ([#227](https://github.com/ipfs/interface-ipfs-core/issues/227)) ([5969fed](https://github.com/ipfs/interface-ipfs-core/commit/5969fed))



<a name="0.55.1"></a>
## [0.55.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.55.0...v0.55.1) (2018-03-09)


### Bug Fixes

* files.add accepts object ([88a635a](https://github.com/ipfs/interface-ipfs-core/commit/88a635a))



<a name="0.55.0"></a>
# [0.55.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.54.0...v0.55.0) (2018-03-09)


### Bug Fixes

* only skip if it is go-ipfs on Windows ([0df216f](https://github.com/ipfs/interface-ipfs-core/commit/0df216f))



<a name="0.54.0"></a>
# [0.54.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.53.0...v0.54.0) (2018-03-07)


### Bug Fixes

* fixes doc and adds test assertion that peer is a PeerId in return value from swarm.peers ([#230](https://github.com/ipfs/interface-ipfs-core/issues/230)) ([db530d7](https://github.com/ipfs/interface-ipfs-core/commit/db530d7))



<a name="0.53.0"></a>
# [0.53.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.52.0...v0.53.0) (2018-03-07)


### Bug Fixes

* adapt dag tests to current environment ([7a6fc5f](https://github.com/ipfs/interface-ipfs-core/commit/7a6fc5f))
* bwPullStream example ([59bd7ac](https://github.com/ipfs/interface-ipfs-core/commit/59bd7ac))



<a name="0.52.0"></a>
# [0.52.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.51.0...v0.52.0) (2018-02-15)


### Features

* allow stats tests to run on js-ipfs ([#216](https://github.com/ipfs/interface-ipfs-core/issues/216)) ([f6e5f55](https://github.com/ipfs/interface-ipfs-core/commit/f6e5f55))



<a name="0.51.0"></a>
# [0.51.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.50.1...v0.51.0) (2018-02-15)


### Bug Fixes

* bootstrap add test ([df01cc5](https://github.com/ipfs/interface-ipfs-core/commit/df01cc5))


### Features

* **bootstrap:** add the spec ([427338e](https://github.com/ipfs/interface-ipfs-core/commit/427338e))



<a name="0.50.1"></a>
## [0.50.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.50.0...v0.50.1) (2018-02-14)


### Bug Fixes

* add pointer to files-mfs tests ([6bc22c9](https://github.com/ipfs/interface-ipfs-core/commit/6bc22c9))



<a name="0.50.0"></a>
# [0.50.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.49.2...v0.50.0) (2018-02-14)


### Features

* factor out mfs tests to separate file ([91666ca](https://github.com/ipfs/interface-ipfs-core/commit/91666ca))



<a name="0.49.2"></a>
## [0.49.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.49.1...v0.49.2) (2018-02-14)


### Bug Fixes

* remove unnecessary console.log ([e27d3e0](https://github.com/ipfs/interface-ipfs-core/commit/e27d3e0))



<a name="0.49.1"></a>
## [0.49.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.49.0...v0.49.1) (2018-02-12)


### Bug Fixes

* remove .only ([44cdaed](https://github.com/ipfs/interface-ipfs-core/commit/44cdaed))



<a name="0.49.0"></a>
# [0.49.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.48.0...v0.49.0) (2018-02-12)


### Bug Fixes

* use latest fixture loading ([#218](https://github.com/ipfs/interface-ipfs-core/issues/218)) ([e054097](https://github.com/ipfs/interface-ipfs-core/commit/e054097))



<a name="0.48.0"></a>
# [0.48.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.47.0...v0.48.0) (2018-02-07)



<a name="0.47.0"></a>
# [0.47.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.46.0...v0.47.0) (2018-02-07)


### Features

* add stats.bwPullStream and stats.bwReadableStream ([#211](https://github.com/ipfs/interface-ipfs-core/issues/211)) ([4421eb2](https://github.com/ipfs/interface-ipfs-core/commit/4421eb2))



<a name="0.46.0"></a>
# [0.46.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.44.0...v0.46.0) (2018-02-02)



<a name="0.45.0"></a>
# [0.45.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.44.0...v0.45.0) (2018-02-02)



<a name="0.44.0"></a>
# [0.44.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.43.0...v0.44.0) (2018-02-02)


### Features

* ipfs.shutdown test ([#214](https://github.com/ipfs/interface-ipfs-core/issues/214)) ([e911c6c](https://github.com/ipfs/interface-ipfs-core/commit/e911c6c))
* Link stats.repo and stats.bitswap ([#210](https://github.com/ipfs/interface-ipfs-core/issues/210)) ([0c40084](https://github.com/ipfs/interface-ipfs-core/commit/0c40084))
* shutdown spec ([9d91267](https://github.com/ipfs/interface-ipfs-core/commit/9d91267))



<a name="0.43.0"></a>
# [0.43.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.42.1...v0.43.0) (2018-01-25)



<a name="0.42.1"></a>
## [0.42.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.42.0...v0.42.1) (2018-01-25)


### Bug Fixes

* stats not implemented on jsipfs ([#209](https://github.com/ipfs/interface-ipfs-core/issues/209)) ([af32ecf](https://github.com/ipfs/interface-ipfs-core/commit/af32ecf))



<a name="0.42.0"></a>
# [0.42.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.41.1...v0.42.0) (2018-01-25)


### Bug Fixes

* Update PUBSUB.md ([#204](https://github.com/ipfs/interface-ipfs-core/issues/204)) ([0409e3a](https://github.com/ipfs/interface-ipfs-core/commit/0409e3a))


### Features

* add stats spec ([220483f](https://github.com/ipfs/interface-ipfs-core/commit/220483f))
* REPO spec ([#207](https://github.com/ipfs/interface-ipfs-core/issues/207)) ([803a3ef](https://github.com/ipfs/interface-ipfs-core/commit/803a3ef))
* spec MFS Actions ([#206](https://github.com/ipfs/interface-ipfs-core/issues/206)) ([7431098](https://github.com/ipfs/interface-ipfs-core/commit/7431098))



<a name="0.41.1"></a>
## [0.41.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.41.0...v0.41.1) (2018-01-19)


### Bug Fixes

* Revert "feat: use new ipfsd-ctl ([#186](https://github.com/ipfs/interface-ipfs-core/issues/186))" ([#203](https://github.com/ipfs/interface-ipfs-core/issues/203)) ([67b74a3](https://github.com/ipfs/interface-ipfs-core/commit/67b74a3))



<a name="0.41.0"></a>
# [0.41.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.40.0...v0.41.0) (2018-01-19)


### Features

* use new ipfsd-ctl ([#186](https://github.com/ipfs/interface-ipfs-core/issues/186)) ([4d4ef7f](https://github.com/ipfs/interface-ipfs-core/commit/4d4ef7f))



<a name="0.40.0"></a>
# [0.40.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.39.0...v0.40.0) (2018-01-12)



<a name="0.39.0"></a>
# [0.39.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.38.0...v0.39.0) (2018-01-10)



<a name="0.38.0"></a>
# [0.38.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.37.0...v0.38.0) (2018-01-05)


### Features

* normalize KEY API ([#192](https://github.com/ipfs/interface-ipfs-core/issues/192)) ([5a21d6c](https://github.com/ipfs/interface-ipfs-core/commit/5a21d6c))
* normalize NAME API ([#190](https://github.com/ipfs/interface-ipfs-core/issues/190)) ([9670c1a](https://github.com/ipfs/interface-ipfs-core/commit/9670c1a))



<a name="0.37.0"></a>
# [0.37.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.16...v0.37.0) (2017-12-28)



<a name="0.36.16"></a>
## [0.36.16](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.15...v0.36.16) (2017-12-18)


### Bug Fixes

* key.rm test ([#185](https://github.com/ipfs/interface-ipfs-core/issues/185)) ([211e2c5](https://github.com/ipfs/interface-ipfs-core/commit/211e2c5))



<a name="0.36.15"></a>
## [0.36.15](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.14...v0.36.15) (2017-12-12)


### Bug Fixes

* cat not found message in go-ipfs ([#183](https://github.com/ipfs/interface-ipfs-core/issues/183)) ([8e3645e](https://github.com/ipfs/interface-ipfs-core/commit/8e3645e))



<a name="0.36.14"></a>
## [0.36.14](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.13...v0.36.14) (2017-12-12)



<a name="0.36.13"></a>
## [0.36.13](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.12...v0.36.13) (2017-12-10)


### Features

* key tests ([#180](https://github.com/ipfs/interface-ipfs-core/issues/180)) ([b75e13b](https://github.com/ipfs/interface-ipfs-core/commit/b75e13b))



<a name="0.36.12"></a>
## [0.36.12](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.11...v0.36.12) (2017-12-05)



<a name="0.36.11"></a>
## [0.36.11](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.10...v0.36.11) (2017-11-26)



<a name="0.36.10"></a>
## [0.36.10](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.9...v0.36.10) (2017-11-25)



<a name="0.36.9"></a>
## [0.36.9](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.8...v0.36.9) (2017-11-23)



<a name="0.36.8"></a>
## [0.36.8](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.7...v0.36.8) (2017-11-22)


### Bug Fixes

* **pubsub:** swarm connect to local servers ([#175](https://github.com/ipfs/interface-ipfs-core/issues/175)) ([09d9573](https://github.com/ipfs/interface-ipfs-core/commit/09d9573))



<a name="0.36.7"></a>
## [0.36.7](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.6...v0.36.7) (2017-11-20)



<a name="0.36.6"></a>
## [0.36.6](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.4...v0.36.6) (2017-11-20)



<a name="0.36.5"></a>
## [0.36.5](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.4...v0.36.5) (2017-11-20)



<a name="0.36.4"></a>
## [0.36.4](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.3...v0.36.4) (2017-11-17)



<a name="0.36.3"></a>
## [0.36.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.2...v0.36.3) (2017-11-17)



<a name="0.36.2"></a>
## [0.36.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.1...v0.36.2) (2017-11-17)



<a name="0.36.1"></a>
## [0.36.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.36.0...v0.36.1) (2017-11-17)



<a name="0.36.0"></a>
# [0.36.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.35.0...v0.36.0) (2017-11-17)



<a name="0.35.0"></a>
# [0.35.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.34.3...v0.35.0) (2017-11-16)


### Bug Fixes

* **pubsub:** topicCIDs should be topicIDs ([#169](https://github.com/ipfs/interface-ipfs-core/issues/169)) ([d357f5f](https://github.com/ipfs/interface-ipfs-core/commit/d357f5f))



<a name="0.34.3"></a>
## [0.34.3](https://github.com/ipfs/interface-ipfs-core/compare/v0.34.2...v0.34.3) (2017-11-14)



<a name="0.34.2"></a>
## [0.34.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.34.0...v0.34.2) (2017-11-13)



<a name="0.34.1"></a>
## [0.34.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.34.0...v0.34.1) (2017-11-13)



<a name="0.34.0"></a>
# [0.34.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.33.2...v0.34.0) (2017-11-13)



<a name="0.33.2"></a>
## [0.33.2](https://github.com/ipfs/interface-ipfs-core/compare/v0.33.1...v0.33.2) (2017-11-09)


### Bug Fixes

* **package:** aegir is a dependency ([#166](https://github.com/ipfs/interface-ipfs-core/issues/166)) ([72f2f56](https://github.com/ipfs/interface-ipfs-core/commit/72f2f56))



<a name="0.33.1"></a>
## [0.33.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.33.0...v0.33.1) (2017-10-22)



<a name="0.33.0"></a>
# [0.33.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.32.1...v0.33.0) (2017-10-22)



<a name="0.32.1"></a>
## [0.32.1](https://github.com/ipfs/interface-ipfs-core/compare/v0.32.0...v0.32.1) (2017-10-18)


### Bug Fixes

* make tests consistent across js-ipfs/go-ipfs ([#158](https://github.com/ipfs/interface-ipfs-core/issues/158)) ([a5a4c37](https://github.com/ipfs/interface-ipfs-core/commit/a5a4c37))



<a name="0.32.0"></a>
# [0.32.0](https://github.com/ipfs/interface-ipfs-core/compare/v0.31.19...v0.32.0) (2017-10-18)


### Features

* add progress bar tests ([#155](https://github.com/ipfs/interface-ipfs-core/issues/155)) ([fad3fa2](https://github.com/ipfs/interface-ipfs-core/commit/fad3fa2))



<a name="0.31.19"></a>
## [0.31.19](https://github.com/ipfs/interface-ipfs-core/compare/v0.31.18...v0.31.19) (2017-09-04)


### Bug Fixes

* remove superfluous console.logs ([442ea74](https://github.com/ipfs/interface-ipfs-core/commit/442ea74))