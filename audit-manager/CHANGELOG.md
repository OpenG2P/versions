# audit-manager

_Published automatically._

**Repository:** [github.com/OpenG2P/audit-manager](https://github.com/OpenG2P/audit-manager) · **Container images:** [Container Registry](https://hub.docker.com/r/openg2p/openg2p-audit-manager)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.25`](#v-0-0-0-develop-25) | 2026-08-28 | develop |  |
| [`1.0.1`](#v-1-0-1) | 2026-07-17 | release |  |
| [`1.0.0`](#v-1-0-0) | 2026-07-13 | release |  |

# Releases

<a id="v-1-0-1"></a>

## audit-manager 1.0.1 — 2026-07-17

<!-- build:1.0.1 revision:b63bc77 ts:1784246400 -->

_commit `b63bc77` · changes since release 1.0.0_

**Chart:** [openg2p-audit-manager 1.0.1](https://openg2p.github.io/openg2p-helm/openg2p-audit-manager-1.0.1.tgz)

### Summary

- Switched CI from GitHub Actions to GitLab for build and publish processes.
- Dropped support for GitHub Actions in the CI pipeline.

### Changes

- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`b63bc77`](https://gitlab.com/openg2p/audit-manager/-/commit/b63bc7753efed44a199939a6033c99539d628295))

<a id="v-1-0-0"></a>

## audit-manager 1.0.0 — 2026-07-13

<!-- build:1.0.0 revision:2c920b4 ts:1783900800 -->

_commit `2c920b4` · first release_

**Chart:** [openg2p-audit-manager 1.0.0](https://openg2p.github.io/openg2p-helm/openg2p-audit-manager-1.0.0.tgz)

### Summary

- Improved system stability and bug fixes.
- Enhanced API documentation and integration capabilities.
- Streamlined internal processes and code structure.

### Changes

- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`2c920b4`](https://github.com/OpenG2P/audit-manager/commit/2c920b4db9827ae216e3d712f657a0f2bc0492e5))
- [G2P-4818](https://openg2p.atlassian.net/browse/G2P-4818) Test script to call partner api added. ([`01daf0c`](https://github.com/OpenG2P/audit-manager/commit/01daf0c352b8572ef57144299d89fde03656b037))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) tpl applied to variables. ([`7b97069`](https://github.com/OpenG2P/audit-manager/commit/7b970697881f76777fd7612dc195a54c3a02b129))
- chore: auto-generate OpenAPI spec [skip ci] ([`b355590`](https://github.com/OpenG2P/audit-manager/commit/b35559029ab3aaf53d0b193858d25824a61f412c))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Uninstall script added. ([`bc5d101`](https://github.com/OpenG2P/audit-manager/commit/bc5d1018dbea50dabe6e3142034c556c1ada838f))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Few bugs fixed ([`0ba7140`](https://github.com/OpenG2P/audit-manager/commit/0ba71400946df72f30bbc8b2b1de51b4f886a299))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Fixes in schema for actor fields. ([`c9d554b`](https://github.com/OpenG2P/audit-manager/commit/c9d554baff6b5b5273cf80f3cb454852f8110463))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) OpenAPI docs enriched. ([`3450fe8`](https://github.com/OpenG2P/audit-manager/commit/3450fe8dd72171245ccd3f900e878186821bea46))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) OpenAPI json written. ([`56aac35`](https://github.com/OpenG2P/audit-manager/commit/56aac35a1d09e1e2876f46a3b0b8d9c0efc2c0a7))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) URLs updated. ([`4377bc5`](https://github.com/OpenG2P/audit-manager/commit/4377bc5fb8fe6661eef6d3fc9b6bad1cd0128f8e))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Helm publish issue fix attempt. ([`4ee51a3`](https://github.com/OpenG2P/audit-manager/commit/4ee51a3ad841a55aa7e23ebbfc14b3ed0fa822fa))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Kafka init bugs fixed. Added gitignore. ([`86dcd2a`](https://github.com/OpenG2P/audit-manager/commit/86dcd2aa5065306ea08f0d4b43834369351de78c))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Documentation moved to Gitbook ([`20545ea`](https://github.com/OpenG2P/audit-manager/commit/20545ea9aa351d26c115486c78159e9b2f861579))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Column structure simplified. ([`5a224f3`](https://github.com/OpenG2P/audit-manager/commit/5a224f36179af85c3f0d78cb08001489ab0963b1))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Fixes. ([`4e75b8d`](https://github.com/OpenG2P/audit-manager/commit/4e75b8d7c0244c970beb3d852c8c334edf0723ca))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Fix attempt for docker build failure. Renaming. ([`476718d`](https://github.com/OpenG2P/audit-manager/commit/476718d698b2dd8a9f5adfa633250de67f3dc986))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Initial version. WIP. ([`8b174a7`](https://github.com/OpenG2P/audit-manager/commit/8b174a70aeab0b676babc3ac72af075ddf8b7426))
- Initial commit ([`06d5c61`](https://github.com/OpenG2P/audit-manager/commit/06d5c61632c103036c0eacac375b080c1d6fe341))

# Develop builds

<a id="v-0-0-0-develop-25"></a>

## audit-manager — develop 0.0.0-develop.25 (2026-08-28)

_commit `36dbf77` · changes since 1.0.0_
<!-- build:0.0.0-develop.25 revision:36dbf77a0c0ff8afc9a10a1de769b3bdf06d5fd6 ts:1787878791 -->

**Chart:** [openg2p-audit-manager 0.0.0-develop.25](https://openg2p.github.io/openg2p-helm/openg2p-audit-manager-0.0.0-develop.25.tgz)

### Summary

- **Major:** Migration to GitLab for CI/CD, replacing GitHub Actions with a new `.gitlab-ci.yml` configuration and disabling build/publish on GitHub.
- Container registry updated for the audit manager, reflecting changes in deployment strategy.
- GitHub repository remains accessible in a read-only state for reference, but active development has shifted to GitLab.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`36dbf77`](https://github.com/OpenG2P/audit-manager/commit/36dbf77a0c0ff8afc9a10a1de769b3bdf06d5fd6))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) audit manager container regitry changed ([`80dbc1c`](https://github.com/OpenG2P/audit-manager/commit/80dbc1c4d762b12ae19f0ee494d4df041451e831))
- Moved to GitLab: openg2p/audit-manager (read-only; build/publish disabled) ([`42bc760`](https://github.com/OpenG2P/audit-manager/commit/42bc760109bb718406069da8b82efac8fdd63de6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`b63bc77`](https://github.com/OpenG2P/audit-manager/commit/b63bc7753efed44a199939a6033c99539d628295))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
