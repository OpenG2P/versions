# awe

_Published automatically._

**Repository:** [gitlab.com/openg2p/awe](https://gitlab.com/openg2p/awe) · **Container images:** [Container Registry](https://gitlab.com/openg2p/awe/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.70`](#v-0-0-0-develop-70) | 2026-08-16 | develop |
| [`0.0.0-develop.69`](#v-0-0-0-develop-69) | 2026-08-11 | develop |
| [`1.1.0`](#v-1-1-0) | 2026-07-17 | release |
| [`1.1.0-rc.66`](#v-1-1-0-rc-66) | 2026-07-17 | release candidate |

# Releases

<a id="v-1-1-0"></a>

## awe 1.1.0 — 2026-07-17

_commit `eb178cd` · changes since release v1.0.0_

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

<a id="v-1-1-0-rc-66"></a>

## awe 1.1.0-rc.66 — 2026-07-17

_commit `eb178cd` · baseline: release v1.0.0_
<!-- build:1.1.0-rc.66 revision:eb178cd8dfdd9b5a4b18f36615664b48a69e0f5f -->

### Summary

_All changes since release v1.0.0:_

- Breaking change: CI has been switched from GitHub Actions to GitLab CI.
- Added Keycloak user management endpoints and integrated UI in the application.
- New field `assignee_name` added to the ApprovalTask model with updated related logic.
- Auto-generated OpenAPI specifications for improved API documentation.
- Updated version numbers in Chart.yaml, pyproject.toml, package.json, and package-lock.json for consistency.

### Since last release (v1.0.0)

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

# Develop builds

<a id="v-0-0-0-develop-70"></a>

## awe — develop 0.0.0-develop.70 (2026-08-16)

_commit `dce3f9c` · changes since 0.0.0-develop.69_
<!-- build:0.0.0-develop.70 revision:dce3f9c036b3dbf8d4a1ad4f81fa2ccd0e7aafc5 ts:1786852644 -->

**Chart:** [openg2p-awe 0.0.0-develop.70](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-awe-0.0.0-develop.70.tgz)

### Changes since 0.0.0-develop.69

- [G2P-5521](https://openg2p.atlassian.net/browse/G2P-5521) Option to view policy added. ([`dce3f9c`](https://gitlab.com/openg2p/awe/-/commit/dce3f9c036b3dbf8d4a1ad4f81fa2ccd0e7aafc5))

<a id="v-0-0-0-develop-69"></a>

## awe — develop 0.0.0-develop.69 (2026-08-11)

_commit `23deb3e` · changes since 1.1.0_
<!-- build:0.0.0-develop.69 revision:23deb3e6f7a2aba9f337ba1ed08c6f50c13125f7 ts:1786452836 -->

**Chart:** [openg2p-awe 0.0.0-develop.69](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-awe-0.0.0-develop.69.tgz)

### Summary

- Authentication enhancements: added support for multiple token issuers in AWE, allowing validation of tokens from both public Keycloak and in-cluster issuers, and introduced configurable SSL verification for Keycloak HTTP calls.
- Security improvements: addressed 'Invalid issuer' errors for registry-forwarded user tokens, ensuring smoother authentication flows.

### Changes since 1.1.0

- [G2P-5498](https://openg2p.atlassian.net/browse/G2P-5498) Add configurable SSL verification for Keycloak HTTP calls ([`b75612d`](https://gitlab.com/openg2p/awe/-/commit/b75612d89ce98e5b4e9501b4cfb84d2222406264))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) AWE: accept multiple token issuers (issuer + additional_issuers) so tokens minted via the public Keycloak hostname validate alongside in-cluster ones; fixes 'Invalid issuer' on registry-forwarded user tokens ([`201996b`](https://gitlab.com/openg2p/awe/-/commit/201996b6919f3e74def2b6bac25cf5306c5f2e3c))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
