# g2p-bridge

_Published automatically._

**Repository:** [github.com/OpenG2P/g2p-bridge](https://github.com/OpenG2P/g2p-bridge) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.108`](#v-0-0-0-develop-108) | 2026-08-28 | develop |  |
| [`1.2.0`](#v-1-2-0) | 2026-07-19 | release |  |
| [`1.1.0`](#v-1-1-0) | 2026-07-18 | release |  |

# Releases

<a id="v-1-2-0"></a>

## g2p-bridge 1.2.0 — 2026-07-19

<!-- build:1.2.0 revision:e812f7cdc817eea83c1ba5e229b0f049ffd7cb22 ts:1784450114 -->

_commit `e812f7c` · changes since release 1.1.0_

**Chart:** [openg2p-bridge 1.2.0](https://openg2p.github.io/openg2p-helm/openg2p-bridge-1.2.0.tgz)

### Release notes

Pegging a stable version; Major restructuring - connectors moved to another repo; fastapi lib version frozen

### Summary

- Removed the legacy Keymanager crypto backend, eliminating dead signing code and related dependencies.
- Changed the SPAR build dependency from GitHub to GitLab, pointing to `spar@develop` for consistency.
- Updated the FastAPI version to 'develop' for uniformity across builds.
- Pinned down the FastAPI version to create a frozen version for stability.
- Fixed the mapper initialization order in connectors to ensure proper functionality.
- Moved connectors to the `g2p-bridge-connectors` repository, allowing Celery to pull them by git reference.

### Changes

- Pinning down fast api version for creating a frozen version. ([`e812f7c`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/e812f7cdc817eea83c1ba5e229b0f049ffd7cb22))
- Changed up fastapi version to 'develop' for consistency across builds. ([`233dd85`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/233dd856e0b975566afe5c65eb46c352f993081e))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Point SPAR build dep to gitlab spar@develop (core/models); was github openg2p-spar@2.0 ([`db6a44b`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/db6a44b8c9f61634b15de00821d5a6af10b68059))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Remove legacy Keymanager crypto backend (dead signing code, keycloak-init dep, chart/config/docs) ([`06b4b92`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/06b4b923dcaa1cef037fbe9922930aa86280bf34))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Bump connectors: fix mapper init order so FA ([`b49ba73`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/b49ba7355f406b0a426ed85a7c61d7d92b80e209))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Move connectors to g2p-bridge-connectors; Celery image pulls them by git ref. ([`46330ab`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/46330abec1a0238a4ccaced036d7650665c4606c))

<a id="v-1-1-0"></a>

## g2p-bridge 1.1.0 — 2026-07-18

<!-- build:1.1.0 revision:60b33bea497c51647d1d016f5a10364d13b080f9 ts:1784373563 -->

_commit `60b33be` · changes since release v1.0.0_

**Chart:** [openg2p-bridge 1.1.0](https://openg2p.github.io/openg2p-helm/openg2p-bridge-1.1.0.tgz)

### Release notes

Security feature: signature verification enabled; Keymanager removed; passes sanity test

### Summary

- Keymanager removed; signing now uses local crypto instead of Keymanager.
- Major changes for using local crypto rather than Keymanager, with most updates in fastapi common.
- CI switched to GitLab, dropping GitHub Actions for build and publish processes.
- New CI implementation introduced.
- Integration with partner management service completed.
- Bug fixes in sanity tests, including multiple corrections and a fix attempt for failed tests.
- Docker build fixed to resolve previous issues.
- API walkthrough corrected for improved clarity.
- Names adjusted as partner management is now installed via commons-services.
- Defaults updated and test cases revised to reflect recent changes.

### Changes

- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`60b33be`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/60b33bea497c51647d1d016f5a10364d13b080f9))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`781a1af`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/781a1af4ffd17da58a638f886ad3e974076fab04))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) API walkthrough corrected. ([`d16e532`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/d16e53249d3f54be7b7c6bf5e85cbf122d01d6ef))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Bug in sanity testing fixed. ([`6a275d1`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/6a275d19d8427068b352e9bc3c1d563307a12c74))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Adjusting names as PM is now installed via commons-services. ([`dfd9502`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/dfd9502daae88ded68d0dcde0682b6dfd15e22e3))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Cleanups. ([`5bbb210`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/5bbb2104ef80078bc22d70e2740df794f85b4f16))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Integration with partner management service. ([`418e720`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/418e720a20c5fd28edd1a67e102db4e1aca47fb2))
- Keymanager removed ([`f61be96`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/f61be96591d853323148b3b1774de677c8f2f6dc))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Sanity test hook corrected ([`d420ee3`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/d420ee34d61caba692963856f4e8d8727badd351))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) bug fix in sanity tests ([`999da27`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/999da277e9dd267b29eaa91049bd8bbc78f48464))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Fix attempt for failed sanity ([`413775e`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/413775e0f47959dbc44e36777e10931f1d730356))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) bug fix in sanity tests ([`cd6d165`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/cd6d165447c96f1d13573fa88784f3d0a9613a6f))
-  [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) bug fix in sanity tests ([`fe6f16d`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/fe6f16d518ae0584155bf18c4cc882def81ad7de))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) bug fix in sanity tests ([`ba22f5e`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/ba22f5eb2f6e40c980cbe1bf805444d2b54fbb4a))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Docker build fixed ([`147c1df`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/147c1df0551f2a8f45639649d8f255ceee5766aa))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Defaults updated. ([`d3e9e68`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/d3e9e688a4ffec853cc08bdcbfd18d829277f658))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Test cases updated for these changes. ([`c23a1bf`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/c23a1bf7ca6efc8aed66be57016763b24b9be576))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Major changes for using local crypto rather than Keymanager. Most changes in fastapi common. ([`dd8ed19`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/dd8ed19c2caf4d8f4506eac5b21e0049c79e2c3c))

# Develop builds

<a id="v-0-0-0-develop-108"></a>

## g2p-bridge — develop 0.0.0-develop.108 (2026-08-28)

_commit `317a66d` · changes since 1.2.0_
<!-- build:0.0.0-develop.108 revision:317a66dfad955cbf0066987d6c7c1861ed37b8a5 ts:1787892284 -->

**Chart:** [openg2p-bridge 0.0.0-develop.108](https://openg2p.github.io/openg2p-helm/openg2p-bridge-0.0.0-develop.108.tgz)

### Summary

- **Major:** Migration to GitLab for repository management, with GitHub workflows removed and build/publish functionality disabled.
- Reversion of versioning for the develop branch to align with the new GitLab setup.
- Resumption of build and publish processes on GitHub for the project.

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
