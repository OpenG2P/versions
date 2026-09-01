# awe

_Published automatically._

**Repository:** [github.com/OpenG2P/awe](https://github.com/OpenG2P/awe) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.2.1`](#v-1-2-1) | 2026-09-01 | release |  |
| [`1.2.1-rc.82`](#v-1-2-1-rc-82) | 2026-09-01 | release candidate |  |
| [`1.2.0`](#v-1-2-0) | 2026-09-01 | release |  |
| [`1.2.0-rc.81`](#v-1-2-0-rc-81) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.81`](#v-0-0-0-develop-81) | 2026-09-01 | develop |  |
| [`1.2.0-rc.80`](#v-1-2-0-rc-80) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.80`](#v-0-0-0-develop-80) | 2026-09-01 | develop |  |
| [`1.1.1-rc.69`](#v-1-1-1-rc-69) | 2026-08-28 | release candidate |  |
| [`0.0.0-develop.78`](#v-0-0-0-develop-78) | 2026-08-28 | develop |  |
| [`1.1.0`](#v-1-1-0) | 2026-07-17 | release |  |

# Releases

<a id="v-1-2-1"></a>

## awe 1.2.1 — 2026-09-01

<!-- build:1.2.1 revision:b76e63a471f0aeb690216a5337f47f7783dcc39c ts:1788259714 -->

_commit `b76e63a` · changes since release 1.2.0_

**Same artifact as [`1.2.1-rc.82`](#v-1-2-1-rc-82)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-awe 1.2.1](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.2.1.tgz)

### Release notes

Updated docker image tag in helm chart values to 1.2.1.

### Summary

- Dependency update: upgraded image tags to version 1.2.1 for improved performance and security.

### Changes

- Update image tags to version 1.2.1 ([`b76e63a`](https://github.com/OpenG2P/awe/commit/b76e63a471f0aeb690216a5337f47f7783dcc39c))

<a id="v-1-2-0"></a>

## awe 1.2.0 — 2026-09-01

<!-- build:1.2.0 revision:623beec073a3e405066c53e7d2f5c6193a75dad4 ts:1788256395 -->

_commit `623beec` · changes since release 1.1.0_

**Same artifact as [`1.2.0-rc.81`](#v-1-2-0-rc-81)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-awe 1.2.0](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.2.0.tgz)

### Release notes

## What's Changed
* Enhance indexing for ApprovalTask and ApprovalDecision models by @vin0dkhichar in https://github.com/OpenG2P/awe/pull/28


**Full Changelog**: https://github.com/OpenG2P/awe/compare/1.1.0...1.2.0

### Summary

- **Major:** Migration to GitLab for repository management; GitHub repository is now read-only with build/publish disabled.
- Keycloak integration: updated to version 1.2.0, with new location and pinned version for stability; added configurable SSL verification for HTTP calls.
- Enhancements to token management: support for multiple token issuers to resolve 'Invalid issuer' errors, improving compatibility with public Keycloak hostname.
- New features: added IAM registration Job and ConfigMap for AWE admin SPA, and introduced an option to view policies.
- Improved data handling: enhanced indexing for ApprovalTask and ApprovalDecision models to optimize performance.

### Changes

- Bump keycloak-init version to 1.2.0 ([`623beec`](https://github.com/OpenG2P/awe/commit/623beec073a3e405066c53e7d2f5c6193a75dad4))
- Enhance indexing for ApprovalTask and ApprovalDecision models ([`a4fb948`](https://github.com/OpenG2P/awe/commit/a4fb948280d2c45c005ea94ef2cc51479708f82e))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Pin keycloak-init to a version published on GitHub ([`5ce7e7e`](https://github.com/OpenG2P/awe/commit/5ce7e7e1cb1d3cf15b486bc3789b2ed38b77356c))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`c3759d1`](https://github.com/OpenG2P/awe/commit/c3759d17ae2b704ee6ed27a62b2bc05a5fb69007))
- Keycloak-init new location and version updated. ([`28b16cc`](https://github.com/OpenG2P/awe/commit/28b16ccd573c6a9b5d21831f23d999db48f7b8a0))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add IAM registration Job and ConfigMap for AWE admin SPA ([`3131c68`](https://github.com/OpenG2P/awe/commit/3131c6856f5e5273639fd96f0599a4df8f0fd9bc))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on awe ([`4037431`](https://github.com/OpenG2P/awe/commit/4037431fe9cd5d824c3cf04ff513e4ea4a1de2f7))
- [G2P-5521](https://openg2p.atlassian.net/browse/G2P-5521) Option to view policy added. ([`dce3f9c`](https://github.com/OpenG2P/awe/commit/dce3f9c036b3dbf8d4a1ad4f81fa2ccd0e7aafc5))
- [G2P-5498](https://openg2p.atlassian.net/browse/G2P-5498) Add configurable SSL verification for Keycloak HTTP calls ([`b75612d`](https://github.com/OpenG2P/awe/commit/b75612d89ce98e5b4e9501b4cfb84d2222406264))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) AWE: accept multiple token issuers (issuer + additional_issuers) so tokens minted via the public Keycloak hostname validate alongside in-cluster ones; fixes 'Invalid issuer' on registry-forwarded user tokens ([`201996b`](https://github.com/OpenG2P/awe/commit/201996b6919f3e74def2b6bac25cf5306c5f2e3c))
- Moved to GitLab: openg2p/awe (read-only; build/publish disabled) ([`1f4f542`](https://github.com/OpenG2P/awe/commit/1f4f54287f09724901502f689642ef042331717c))

<a id="v-1-1-0"></a>

## awe 1.1.0 — 2026-07-17

<!-- build:1.1.0 revision:eb178cd ts:1784246400 -->

_commit `eb178cd` · changes since release v1.0.0_

**Chart:** [openg2p-awe 1.1.0](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.1.0.tgz)

### Summary

- Breaking Change: CI has been switched from GitHub Actions to GitLab CI, impacting the build and publish process.
- New Feature: Added Keycloak user management endpoints and integrated UI in the application.
- New Feature: Introduced `assignee_name` field to the ApprovalTask model and updated related logic.
- Dependency Update: Version numbers have been updated in Chart.yaml, pyproject.toml, package.json, and package-lock.json.
- Chore: Auto-generated OpenAPI specification to improve API documentation.

### Changes

- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`eb178cd`](https://gitlab.com/openg2p/awe/-/commit/eb178cd8dfdd9b5a4b18f36615664b48a69e0f5f))
- chore: auto-generate OpenAPI spec [skip ci] ([`11235c6`](https://gitlab.com/openg2p/awe/-/commit/11235c6c39a50bc3f3f38dbbaa90e69447bd204e))
- fix(ci): use PEP 440-valid version placeholder in pyproject.toml ([`b786573`](https://gitlab.com/openg2p/awe/-/commit/b786573f57d08750e265e81c5006f9e8291ff3f3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335)  New CI implemented. ([`308c276`](https://gitlab.com/openg2p/awe/-/commit/308c276ff851945a4cf108085631aae9f53e6c83))
- Update version to develop in Chart.yaml and pyproject.toml ([`c5dd71c`](https://gitlab.com/openg2p/awe/-/commit/c5dd71cded22fbe00df5be33d2c61b9a94c78da9))
- Update version to develop in package.json and package-lock.json ([`8d5e562`](https://gitlab.com/openg2p/awe/-/commit/8d5e5622942140f5a4d049f71b4e9cbb7ad634c4))
- Versions updated ([`77d4013`](https://gitlab.com/openg2p/awe/-/commit/77d4013a147aee60c6351a887d66740c83b24e09))
- chore: auto-generate OpenAPI spec [skip ci] ([`2208256`](https://gitlab.com/openg2p/awe/-/commit/2208256f50113df1f707385651ec6857adb9485c))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Add assignee_name field to ApprovalTask model and update related logic ([`04cda7b`](https://gitlab.com/openg2p/awe/-/commit/04cda7b97caa0c682d3245c86966d1bf219762b8))
- [G2P-5147](https://openg2p.atlassian.net/browse/G2P-5147) Add Keycloak user management endpoints and UI integration in awe ([`169c313`](https://gitlab.com/openg2p/awe/-/commit/169c3137d97f6dd2598e7e3985ee9f1ba2bf1abe))

# Release candidates

<a id="v-1-2-1-rc-82"></a>

## awe 1.2.1-rc.82 — 2026-09-01

_commit `b76e63a` · changes since 0.0.0-develop.80_
<!-- build:1.2.1-rc.82 revision:b76e63a471f0aeb690216a5337f47f7783dcc39c ts:1788259714 -->

**Chart:** [openg2p-awe 1.2.1-rc.82](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.2.1-rc.82.tgz)

### Summary

- Dependency updates: updated image tags to version 1.2.1 and bumped keycloak-init version to 1.2.0.

### Changes

- Update image tags to version 1.2.1 ([`b76e63a`](https://github.com/OpenG2P/awe/commit/b76e63a471f0aeb690216a5337f47f7783dcc39c))
- Bump keycloak-init version to 1.2.0 ([`623beec`](https://github.com/OpenG2P/awe/commit/623beec073a3e405066c53e7d2f5c6193a75dad4))

<a id="v-1-2-0-rc-81"></a>

## awe 1.2.0-rc.81 — 2026-09-01

_commit `623beec` · changes since 1.2.0-rc.80_
<!-- build:1.2.0-rc.81 revision:623beec073a3e405066c53e7d2f5c6193a75dad4 ts:1788256395 -->

**Chart:** [openg2p-awe 1.2.0-rc.81](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.2.0-rc.81.tgz)

### Changes

- Bump keycloak-init version to 1.2.0 ([`623beec`](https://github.com/OpenG2P/awe/commit/623beec073a3e405066c53e7d2f5c6193a75dad4))

<a id="v-1-2-0-rc-80"></a>

## awe 1.2.0-rc.80 — 2026-09-01

_commit `fb0c1f2` · changes since 0.0.0-develop.80_
<!-- build:1.2.0-rc.80 revision:fb0c1f298729a8fc60ec5557200429439f8db638 ts:1788256034 -->

**Chart:** [openg2p-awe 1.2.0-rc.80](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.2.0-rc.80.tgz)

### Changes

_No new commits since 0.0.0-develop.80._

<a id="v-1-1-1-rc-69"></a>

## awe 1.1.1-rc.69 — 2026-08-28

_commit `27c7f19` · changes since 1.1.0_
<!-- build:1.1.1-rc.69 revision:27c7f193d85b09af7f457a0a44fba7386f4085d7 ts:1787914240 -->

**Chart:** [openg2p-awe 1.1.1-rc.69](https://openg2p.github.io/openg2p-helm/openg2p-awe-1.1.1-rc.69.tgz)

### Changes

- Update version to 1.1.0 in Chart.yaml, pyproject.toml, package.json, and package-lock.json ([`e5a25b4`](https://github.com/OpenG2P/awe/commit/e5a25b441a5d04671b55f035b126c0a0c7ab5632))

# Develop builds

<a id="v-0-0-0-develop-81"></a>

## awe — develop 0.0.0-develop.81 (2026-09-01)

_commit `5f393eb` · changes since 0.0.0-develop.80_
<!-- build:0.0.0-develop.81 revision:5f393eb0e64c3ae444ce4c0a5de42f32277f698f ts:1788256326 -->

**Chart:** [openg2p-awe 0.0.0-develop.81](https://openg2p.github.io/openg2p-helm/openg2p-awe-0.0.0-develop.81.tgz)

### Changes

- updated fastapi-common to 1.2.0 ([`5f393eb`](https://github.com/OpenG2P/awe/commit/5f393eb0e64c3ae444ce4c0a5de42f32277f698f))

<a id="v-0-0-0-develop-80"></a>

## awe — develop 0.0.0-develop.80 (2026-09-01)

_commit `fb0c1f2` · changes since 0.0.0-develop.78_
<!-- build:0.0.0-develop.80 revision:fb0c1f298729a8fc60ec5557200429439f8db638 ts:1788256034 -->

**Chart:** [openg2p-awe 0.0.0-develop.80](https://openg2p.github.io/openg2p-helm/openg2p-awe-0.0.0-develop.80.tgz)

### Changes

- Enhance indexing for ApprovalTask and ApprovalDecision models ([`a4fb948`](https://github.com/OpenG2P/awe/commit/a4fb948280d2c45c005ea94ef2cc51479708f82e))

<a id="v-0-0-0-develop-78"></a>

## awe — develop 0.0.0-develop.78 (2026-08-28)

_commit `5ce7e7e` · changes since 1.1.0_
<!-- build:0.0.0-develop.78 revision:5ce7e7e1cb1d3cf15b486bc3789b2ed38b77356c ts:1787885128 -->

**Chart:** [openg2p-awe 0.0.0-develop.78](https://openg2p.github.io/openg2p-helm/openg2p-awe-0.0.0-develop.78.tgz)

### Summary

- **Major:** Migration to GitLab for repository management; GitHub repository is now read-only with build/publish disabled.
- Keycloak updates: pinned `keycloak-init` to a specific version, updated its location, and added configurable SSL verification for HTTP calls.
- New features: introduced IAM registration Job and ConfigMap for AWE admin SPA, and added an option to view policies.
- Token handling improvements: enabled support for multiple token issuers to resolve 'Invalid issuer' errors for user tokens. 
- Platform service adjustments: applied changes related to the platform-service group for AWE.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Pin keycloak-init to a version published on GitHub ([`5ce7e7e`](https://github.com/OpenG2P/awe/commit/5ce7e7e1cb1d3cf15b486bc3789b2ed38b77356c))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`c3759d1`](https://github.com/OpenG2P/awe/commit/c3759d17ae2b704ee6ed27a62b2bc05a5fb69007))
- Keycloak-init new location and version updated. ([`28b16cc`](https://github.com/OpenG2P/awe/commit/28b16ccd573c6a9b5d21831f23d999db48f7b8a0))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add IAM registration Job and ConfigMap for AWE admin SPA ([`3131c68`](https://github.com/OpenG2P/awe/commit/3131c6856f5e5273639fd96f0599a4df8f0fd9bc))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on awe ([`4037431`](https://github.com/OpenG2P/awe/commit/4037431fe9cd5d824c3cf04ff513e4ea4a1de2f7))
- [G2P-5521](https://openg2p.atlassian.net/browse/G2P-5521) Option to view policy added. ([`dce3f9c`](https://github.com/OpenG2P/awe/commit/dce3f9c036b3dbf8d4a1ad4f81fa2ccd0e7aafc5))
- [G2P-5498](https://openg2p.atlassian.net/browse/G2P-5498) Add configurable SSL verification for Keycloak HTTP calls ([`b75612d`](https://github.com/OpenG2P/awe/commit/b75612d89ce98e5b4e9501b4cfb84d2222406264))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) AWE: accept multiple token issuers (issuer + additional_issuers) so tokens minted via the public Keycloak hostname validate alongside in-cluster ones; fixes 'Invalid issuer' on registry-forwarded user tokens ([`201996b`](https://github.com/OpenG2P/awe/commit/201996b6919f3e74def2b6bac25cf5306c5f2e3c))
- Moved to GitLab: openg2p/awe (read-only; build/publish disabled) ([`1f4f542`](https://github.com/OpenG2P/awe/commit/1f4f54287f09724901502f689642ef042331717c))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
