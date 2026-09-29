# crop-sown-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/crop-sown-registry](https://github.com/OpenG2P/crop-sown-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.11`](#v-0-0-0-develop-11) | 2026-09-29 | develop |  |
| [`0.0.0-develop.9`](#v-0-0-0-develop-9) | 2026-09-28 | develop |  |
| [`0.0.0-develop.6`](#v-0-0-0-develop-6) | 2026-09-28 | develop |  |
| [`0.0.0-develop.5`](#v-0-0-0-develop-5) | 2026-09-27 | develop |  |
| [`0.0.0-develop.4`](#v-0-0-0-develop-4) | 2026-09-27 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-11"></a>

## crop-sown-registry — develop 0.0.0-develop.11 (2026-09-29)

_commit `393f014` · changes since 0.0.0-develop.9_
<!-- build:0.0.0-develop.11 revision:393f0146b22f583f85ae4849e5a995b6c25e8254 ts:1790646685 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.11](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.11.tgz)

### Summary

- **Major:** Introduced uninstall-registry.sh for streamlined removal of the registry, tailored for this release's persistent volumes.
- Version bump to RP 0.0.0-develop.444, indicating ongoing development and updates.

### Changes

- Bumped up RP version to 0.0.0-develop.444 ([`393f014`](https://github.com/OpenG2P/crop-sown-registry/commit/393f0146b22f583f85ae4849e5a995b6c25e8254))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Add uninstall-registry.sh (adapted from FR; no Superset step; only this release's PVs) ([`4cfd71a`](https://github.com/OpenG2P/crop-sown-registry/commit/4cfd71ab7ea66cd4e38c3cf59e0aa24ff4aeaa71))

<a id="v-0-0-0-develop-9"></a>

## crop-sown-registry — develop 0.0.0-develop.9 (2026-09-28)

_commit `525af83` · changes since 0.0.0-develop.6_
<!-- build:0.0.0-develop.9 revision:525af83ab52079d3e9639a605dd69f6cd96dd4a6 ts:1790616352 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.9](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.9.tgz)

### Summary

- Version update: bumped RP version to 0.0.0-develop.441.
- Testing enhancements: enabled sanity tests to improve reliability.
- Feature addition: implemented farmer season summary as an activity aggregate.

### Changes

- Bumped up RP version to 0.0.0-develop.441 ([`525af83`](https://github.com/OpenG2P/crop-sown-registry/commit/525af83ab52079d3e9639a605dd69f6cd96dd4a6))
- Sanity test enabled. ([`63649c4`](https://github.com/OpenG2P/crop-sown-registry/commit/63649c4dfd3a14e4f67a16538edf65d24e59bd4a))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Farmer season summary as an activity aggregate ([`8b54199`](https://github.com/OpenG2P/crop-sown-registry/commit/8b54199173d4d8d57bdfddc7103f5357075c7290))

<a id="v-0-0-0-develop-6"></a>

## crop-sown-registry — develop 0.0.0-develop.6 (2026-09-28)

_commit `4534b35` · changes since 0.0.0-develop.5_
<!-- build:0.0.0-develop.6 revision:4534b35ce82f69825a43546640bf47ba1606b2cd ts:1790561390 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.6](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.6.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Fix Helm form: questions.own.yaml must be a bare list so the inherited registry questions (images etc.) are kept; add ODK URL question ([`4534b35`](https://github.com/OpenG2P/crop-sown-registry/commit/4534b35ce82f69825a43546640bf47ba1606b2cd))

<a id="v-0-0-0-develop-5"></a>

## crop-sown-registry — develop 0.0.0-develop.5 (2026-09-27)

_commit `e3b9c2f` · changes since 0.0.0-develop.4_
<!-- build:0.0.0-develop.5 revision:e3b9c2f9b8005ab0846c573ff1975177e4305c82 ts:1790525469 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.5](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.5.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Read all code lists live from Master Data (ETH pack agriculture domain); drop CS_* lookup data; pin RP 0.0.0-develop.439 ([`e3b9c2f`](https://github.com/OpenG2P/crop-sown-registry/commit/e3b9c2f9b8005ab0846c573ff1975177e4305c82))

<a id="v-0-0-0-develop-4"></a>

## crop-sown-registry — develop 0.0.0-develop.4 (2026-09-27)

_commit `158ae4a` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.4 revision:158ae4ae07b780e21b1a5fd2d41bed0b9a6346ef ts:1790476942 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.4](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.4.tgz)

### Summary

- **Major:** Introduced the Crop Sown Registry, enabling activity registration of crop seasons on the registry platform.
- Dependency management: pinned Crop Sown Registry to registry-platform version 0.0.0-develop.438 and updated the bump script to prevent generation of Chart.lock and chart tgz files.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Stop tracking generated Chart.lock and chart tgz; bump script no longer generates them ([`158ae4a`](https://github.com/OpenG2P/crop-sown-registry/commit/158ae4ae07b780e21b1a5fd2d41bed0b9a6346ef))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Pin Crop Sown Registry to registry-platform 0.0.0-develop.438; fix bump-rp-version.sh repo refresh ([`589961c`](https://github.com/OpenG2P/crop-sown-registry/commit/589961cb20df2b0cb0972f8ae2db1305971c1488))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Add Crop Sown Registry: activity register of crop seasons on the registry platform ([`a0340ba`](https://github.com/OpenG2P/crop-sown-registry/commit/a0340ba73fe7adce60273010a54d6e937193cc33))
- Initial commit ([`69aec11`](https://github.com/OpenG2P/crop-sown-registry/commit/69aec119f90d6158e856092197f5638fa5c52588))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
