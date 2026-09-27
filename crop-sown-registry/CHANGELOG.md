# crop-sown-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/crop-sown-registry](https://github.com/OpenG2P/crop-sown-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.4`](#v-0-0-0-develop-4) | 2026-09-27 | develop |  |

# Develop builds

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
