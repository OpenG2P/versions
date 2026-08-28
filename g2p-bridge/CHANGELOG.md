# g2p-bridge

_Published automatically._

**Repository:** [github.com/OpenG2P/g2p-bridge](https://github.com/OpenG2P/g2p-bridge) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.108`](#v-0-0-0-develop-108) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-108"></a>

## g2p-bridge — develop 0.0.0-develop.108 (2026-08-28)

_commit `317a66d` · changes since 1.2.0_
<!-- build:0.0.0-develop.108 revision:317a66dfad955cbf0066987d6c7c1861ed37b8a5 ts:1787892284 -->

**Chart:** [openg2p-bridge 0.0.0-develop.108](https://openg2p.github.io/openg2p-helm/openg2p-bridge-0.0.0-develop.108.tgz)

### Summary

- **Major:** Migration to GitLab for repository management, with GitHub workflows removed and build/publish functionality disabled.
- Build and publish functionality reinstated on GitHub for version control.
- Reversion of versions for the develop branch to maintain consistency.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`317a66d`](https://github.com/OpenG2P/g2p-bridge/commit/317a66dfad955cbf0066987d6c7c1861ed37b8a5))
- Github workflows removed, as they are not required on Gitlab. Versions reverted for develop branch. ([`4bcae93`](https://github.com/OpenG2P/g2p-bridge/commit/4bcae93fcd9b7c82f280f189c8f52441ff07e36b))
- Moved to GitLab: openg2p/g2p-bridge/g2p-bridge (read-only; build/publish disabled) ([`8f18a70`](https://github.com/OpenG2P/g2p-bridge/commit/8f18a70ada1c391a5016cd686ed04e62ccd54ead))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
