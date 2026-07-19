# g2p-bridge/g2p-bridge

_Published automatically._

**Repository:** [gitlab.com/openg2p/g2p-bridge/g2p-bridge](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge) · **Container images:** [Container Registry](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.101`](#v-0-0-0-develop-101) | 2026-07-19 | develop |
| [`0.0.0-develop.100`](#v-0-0-0-develop-100) | 2026-07-19 | develop |
| [`0.0.0-develop.99`](#v-0-0-0-develop-99) | 2026-07-19 | develop |
| [`1.1.0`](#v-1-1-0) | 2026-07-18 | release |

# Releases

<a id="v-1-1-0"></a>

## g2p-bridge/g2p-bridge 1.1.0 — 2026-07-18

<!-- build:1.1.0 revision:60b33bea497c51647d1d016f5a10364d13b080f9 ts:1784373563 -->

_commit `60b33be` · changes since release v1.0.0_

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

<a id="v-0-0-0-develop-101"></a>

## g2p-bridge/g2p-bridge — develop 0.0.0-develop.101 (2026-07-19)

_commit `06b4b92` · baseline: release 1.1.0 · previous build 0.0.0-develop.100_
<!-- build:0.0.0-develop.101 revision:06b4b923dcaa1cef037fbe9922930aa86280bf34 ts:1784430303 -->

### Summary

_All changes since release 1.1.0:_

- Removed the legacy Keymanager crypto backend, eliminating dead signing code and related dependencies (keycloak-init, chart/config/docs).
- Moved connectors to a new repository, g2p-bridge-connectors, allowing the Celery image to pull them by git reference.
- Fixed the mapper initialization order for connectors to ensure proper functionality.

### New in this build (since 0.0.0-develop.100)

- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Remove legacy Keymanager crypto backend (dead signing code, keycloak-init dep, chart/config/docs) ([`06b4b92`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/06b4b923dcaa1cef037fbe9922930aa86280bf34))

### Since last release (1.1.0)

- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Remove legacy Keymanager crypto backend (dead signing code, keycloak-init dep, chart/config/docs) ([`06b4b92`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/06b4b923dcaa1cef037fbe9922930aa86280bf34))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Bump connectors: fix mapper init order so FA ([`b49ba73`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/b49ba7355f406b0a426ed85a7c61d7d92b80e209))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Move connectors to g2p-bridge-connectors; Celery image pulls them by git ref. ([`46330ab`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/46330abec1a0238a4ccaced036d7650665c4606c))

<a id="v-0-0-0-develop-100"></a>

## g2p-bridge/g2p-bridge — develop 0.0.0-develop.100 (2026-07-19)

_commit `b49ba73` · baseline: release 1.1.0 · previous build 0.0.0-develop.99_
<!-- build:0.0.0-develop.100 revision:b49ba7355f406b0a426ed85a7c61d7d92b80e209 ts:1784427876 -->

### Summary

_All changes since release 1.1.0:_

- Major refactor: Moved connectors to a new repository, `g2p-bridge-connectors`, with Celery now pulling them by git reference.
- Fixed mapper initialization order for the FA connector to ensure proper functionality.
- Removed 97 files related to various extensions, including configuration files and documentation, streamlining the codebase.
- Updated dependency manifests for multiple extensions, including `agency-allocator`, `bank-connectors`, `geo-resolver`, `mapper-connectors`, and `notification-connectors`.

### New in this build (since 0.0.0-develop.99)

- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Bump connectors: fix mapper init order so FA ([`b49ba73`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/b49ba7355f406b0a426ed85a7c61d7d92b80e209))

### Since last release (1.1.0)

- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Bump connectors: fix mapper init order so FA ([`b49ba73`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/b49ba7355f406b0a426ed85a7c61d7d92b80e209))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Move connectors to g2p-bridge-connectors; Celery image pulls them by git ref. ([`46330ab`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/46330abec1a0238a4ccaced036d7650665c4606c))

<a id="v-0-0-0-develop-99"></a>

## g2p-bridge/g2p-bridge — develop 0.0.0-develop.99 (2026-07-19)

_commit `46330ab` · baseline: release 1.1.0 · previous build 0.0.0-develop.98_
<!-- build:0.0.0-develop.99 revision:46330abec1a0238a4ccaced036d7650665c4606c ts:1784423985 -->

### Summary

_All changes since release 1.1.0:_

- Major refactor: Connectors have been moved to the new `g2p-bridge-connectors` repository, with the Celery image now pulling them by git reference.
- Removed 97 files related to extensions, including configuration files and documentation, streamlining the project structure.
- Updated dependency manifests for multiple extensions, including `agency-allocator`, `bank-connectors`, `geo-resolver`, `mapper-connectors`, and `notification-connectors`.
- Significant reduction in codebase size with 2714 deletions, indicating a major cleanup and optimization effort.

### Since last release (1.1.0)

- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Move connectors to g2p-bridge-connectors; Celery image pulls them by git ref. ([`46330ab`](https://gitlab.com/openg2p/g2p-bridge/g2p-bridge/-/commit/46330abec1a0238a4ccaced036d7650665c4606c))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 3 develop builds** and the **latest 3 release
> candidates** per release line. Older develop builds and release candidates
> are pruned as they are superseded, and a release's candidates are removed
> once it ships. Those versions still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
