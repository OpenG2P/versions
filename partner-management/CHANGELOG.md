# partner-management

_Published automatically._

**Repository:** [github.com/OpenG2P/partner-management](https://github.com/OpenG2P/partner-management) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.0.2-rc.28`](#v-1-0-2-rc-28) | 2026-09-01 | release candidate |  |
| [`1.0.1`](#v-1-0-1) | 2026-09-01 | release |  |
| [`1.0.1-rc.26`](#v-1-0-1-rc-26) | 2026-09-01 | release candidate |  |
| [`1.0.0`](#v-1-0-0) | 2026-09-01 | release |  |
| [`1.0.0-rc.25`](#v-1-0-0-rc-25) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.26`](#v-0-0-0-develop-26) | 2026-09-01 | develop |  |
| [`1.0.0-rc.24`](#v-1-0-0-rc-24) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.24`](#v-0-0-0-develop-24) | 2026-08-28 | develop |  |
| [`0.0.0-develop.23`](#v-0-0-0-develop-23) | 2026-08-28 | develop |  |

# Releases

<a id="v-1-0-1"></a>

## partner-management 1.0.1 — 2026-09-01

<!-- build:1.0.1 revision:a90fbed5a350bd26c75967896f4d36c2078b475e ts:1788255698 -->

_commit `a90fbed` · changes since release 1.0.0_

**Same artifact as [`1.0.1-rc.26`](#v-1-0-1-rc-26)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [partner-management 1.0.1](https://openg2p.github.io/openg2p-helm/partner-management-1.0.1.tgz)

### Release notes

**Updated**
 - fastapi-commons : 1.2.0

### Summary

- Dependency update: upgraded FastAPI common version to 1.2.0, impacting Docker configurations. 
- Code maintenance: minor adjustments made with 2 insertions and 2 deletions across relevant files.

### Changes

- Update fastapi common version to 1.2.0 ([`a90fbed`](https://github.com/OpenG2P/partner-management/commit/a90fbed5a350bd26c75967896f4d36c2078b475e))

<a id="v-1-0-0"></a>

## partner-management 1.0.0 — 2026-09-01

<!-- build:1.0.0 revision:f7cb2194c4aed70f74e2ff23f7d9e53973fac2e9 ts:1788253407 -->

_commit `f7cb219` · first release_

**Same artifact as [`1.0.0-rc.25`](#v-1-0-0-rc-25)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [partner-management 1.0.0](https://openg2p.github.io/openg2p-helm/partner-management-1.0.0.tgz)

### Release notes

**Full Changelog**: https://github.com/OpenG2P/partner-management/commits/1.0.0

### Summary

- **Major:** Migration to GitLab CI: switched from GitHub Actions to GitLab CI for build and publish processes, with a new `.gitlab-ci.yml` configuration.
- Authentication updates: fixed environment variable prefixes for partner management, ensuring `AUTH_ENABLED` functions correctly; added IAM registration support.
- Keycloak enhancements: updated keycloak-init to version 1.2.0 and adjusted its location; resolved issues with the keycloak-service-account-role job.
- Dependency management: corrected Docker image sources to prevent pulling from Docker Hub; updated references in fastapi-common.
- Testing improvements: implemented automatic test execution from the bridge, with enhancements to workflow scoping and fixes for sanity tests.
- Minor UI adjustments and corrections made to the default audit manager URL; added `questions.yaml` for improved auditing capabilities.

### Changes

- Update keycloak-init version to 1.2.0 ([`f7cb219`](https://github.com/OpenG2P/partner-management/commit/f7cb2194c4aed70f74e2ff23f7d9e53973fac2e9))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) fix InvalidImageName in the keycloak-service-account-role job ([`bb96ff2`](https://github.com/OpenG2P/partner-management/commit/bb96ff24d1d64538d361ad065707729a668b214c))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`9c388db`](https://github.com/OpenG2P/partner-management/commit/9c388db10e676a6ee3b31cc139551640266a3d99))
- Fix PM auth env prefix: the chart set COMMON_AUTH_* but Settings overrides env_prefix to partner_manager_, so with extra="allow" the JSON list arrived as an unparsed str and crashed staff-portal-api with a pydantic list_type ValidationError; renamed all four to PARTNER_MANAGER_AUTH_* (verified against the 0.0.0-develop.18 image), which also makes AUTH_ENABLED actually take effect for the first time ([`0afcbb5`](https://github.com/OpenG2P/partner-management/commit/0afcbb54b48a8ad44ba0c59acb758a78b2cbf5e9))
- Keycloak-init new location and version updated. ([`c2462ac`](https://github.com/OpenG2P/partner-management/commit/c2462ac259961f70f599a1903c053e4f6da1bfe5))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Update fastapi-common references and partner management authentication configuration ([`72cd04f`](https://github.com/OpenG2P/partner-management/commit/72cd04f3f3909b201835328b3989d4e5fd47cb1c))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add IAM registration support for Partner Management ([`1d35ff5`](https://github.com/OpenG2P/partner-management/commit/1d35ff58c48eff8afeec6b50d0b5b8ad1a47eeb3))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on partner-management ([`914c6a4`](https://github.com/OpenG2P/partner-management/commit/914c6a4a6728253c585b7d61d38375b440c82a8a))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Dockers were being picked from Docker Hub. Corrected. ([`2085c3d`](https://github.com/OpenG2P/partner-management/commit/2085c3d1c815126e7e0e5b153a29513962f71506))
- git commit -am "Repo moved to GitLab; archive notice, remove CI [skip ci]" ([`c6aab45`](https://github.com/OpenG2P/partner-management/commit/c6aab4558779be8bc6f91d5d138fb632f8dda024))
- Minor edit to test build and push pipeline on Gitlab ([`0951fe0`](https://github.com/OpenG2P/partner-management/commit/0951fe0f018011035818ec4b8b9d9a495a5c68e2))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`7cae5ea`](https://github.com/OpenG2P/partner-management/commit/7cae5ead0b6ffba592676467331ee1722894dfd4))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`5d68968`](https://github.com/OpenG2P/partner-management/commit/5d68968984ff2f37e119e2fce7390719f7c68af4))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Changes for automatic tests running from bridge. ([`c886641`](https://github.com/OpenG2P/partner-management/commit/c886641bc0f826f8b68759c073aeed5bcfda476a))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) fixes related to sanity tests on bridge. ([`bcf3228`](https://github.com/OpenG2P/partner-management/commit/bcf32282bb84e2244c8924243fbe6a8675e8f180))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Workflow scoped better. ([`9b34617`](https://github.com/OpenG2P/partner-management/commit/9b34617ac2560d72c568a7fa1582114d29bf262e))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Minor changes in UI. ([`feffc35`](https://github.com/OpenG2P/partner-management/commit/feffc35fb635425b41de53adbfe8d3f52eb10e42))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Default audit manager URL corrected. ([`4d1afdd`](https://github.com/OpenG2P/partner-management/commit/4d1afdd8cf81c6aa92e6691902d8d026d2149622))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) questions.yaml added. ([`74a4114`](https://github.com/OpenG2P/partner-management/commit/74a41147c1919c9af2582dc8c398a70fc4081932))
-  [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261)  Auditing added. ([`f9ed65b`](https://github.com/OpenG2P/partner-management/commit/f9ed65bcc6b84340a473a8704ac332c8510a98a7))

# Release candidates

<a id="v-1-0-2-rc-28"></a>

## partner-management 1.0.2-rc.28 — 2026-09-01

_commit `5be30eb` · changes since 0.0.0-develop.24_
<!-- build:1.0.2-rc.28 revision:5be30ebc43a5aacc2a6e14978cdafe7ee1e04f4d ts:1788260833 -->

**Chart:** [partner-management 1.0.2-rc.28](https://openg2p.github.io/openg2p-helm/partner-management-1.0.2-rc.28.tgz)

### Summary

- Dependency updates: upgraded image tags to version 1.0.2, fastapi common to 1.2.0, and keycloak-init to 1.2.0.

### Changes

- Update image tags to version 1.0.2 ([`7d90e45`](https://github.com/OpenG2P/partner-management/commit/7d90e45ade6054f7c4a48d5bb96c0198fedfd957))
- Update fastapi common version to 1.2.0 ([`a90fbed`](https://github.com/OpenG2P/partner-management/commit/a90fbed5a350bd26c75967896f4d36c2078b475e))
- Update keycloak-init version to 1.2.0 ([`f7cb219`](https://github.com/OpenG2P/partner-management/commit/f7cb2194c4aed70f74e2ff23f7d9e53973fac2e9))

<a id="v-1-0-1-rc-26"></a>

## partner-management 1.0.1-rc.26 — 2026-09-01

_commit `a90fbed` · changes since 0.0.0-develop.24_
<!-- build:1.0.1-rc.26 revision:a90fbed5a350bd26c75967896f4d36c2078b475e ts:1788255698 -->

**Chart:** [partner-management 1.0.1-rc.26](https://openg2p.github.io/openg2p-helm/partner-management-1.0.1-rc.26.tgz)

### Summary

- Dependency updates: upgraded fastapi common to version 1.2.0 and keycloak-init to version 1.2.0.

### Changes

- Update fastapi common version to 1.2.0 ([`a90fbed`](https://github.com/OpenG2P/partner-management/commit/a90fbed5a350bd26c75967896f4d36c2078b475e))
- Update keycloak-init version to 1.2.0 ([`f7cb219`](https://github.com/OpenG2P/partner-management/commit/f7cb2194c4aed70f74e2ff23f7d9e53973fac2e9))

<a id="v-1-0-0-rc-25"></a>

## partner-management 1.0.0-rc.25 — 2026-09-01

_commit `f7cb219` · changes since 1.0.0-rc.24_
<!-- build:1.0.0-rc.25 revision:f7cb2194c4aed70f74e2ff23f7d9e53973fac2e9 ts:1788253407 -->

**Chart:** [partner-management 1.0.0-rc.25](https://openg2p.github.io/openg2p-helm/partner-management-1.0.0-rc.25.tgz)

### Changes

- Update keycloak-init version to 1.2.0 ([`f7cb219`](https://github.com/OpenG2P/partner-management/commit/f7cb2194c4aed70f74e2ff23f7d9e53973fac2e9))

<a id="v-1-0-0-rc-24"></a>

## partner-management 1.0.0-rc.24 — 2026-09-01

_commit `bb96ff2` · changes since 0.0.0-develop.24_
<!-- build:1.0.0-rc.24 revision:bb96ff24d1d64538d361ad065707729a668b214c ts:1787913288 -->

**Chart:** [partner-management 1.0.0-rc.24](https://openg2p.github.io/openg2p-helm/partner-management-1.0.0-rc.24.tgz)

### Changes

_No new commits since 0.0.0-develop.24._

# Develop builds

<a id="v-0-0-0-develop-26"></a>

## partner-management — develop 0.0.0-develop.26 (2026-09-01)

_commit `11b3618` · changes since 0.0.0-develop.24_
<!-- build:0.0.0-develop.26 revision:11b36183194b792201deb579e5698ff2aef93ad5 ts:1788251230 -->

**Chart:** [partner-management 0.0.0-develop.26](https://openg2p.github.io/openg2p-helm/partner-management-0.0.0-develop.26.tgz)

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) bump ui dependencies to clear open security advisories ([`f383795`](https://github.com/OpenG2P/partner-management/commit/f383795af4f9fb9a607c5dcc78859be945584706))

<a id="v-0-0-0-develop-24"></a>

## partner-management — develop 0.0.0-develop.24 (2026-08-28)

_commit `bb96ff2` · changes since 0.0.0-develop.23_
<!-- build:0.0.0-develop.24 revision:bb96ff24d1d64538d361ad065707729a668b214c ts:1787913288 -->

**Chart:** [partner-management 0.0.0-develop.24](https://openg2p.github.io/openg2p-helm/partner-management-0.0.0-develop.24.tgz)

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) fix InvalidImageName in the keycloak-service-account-role job ([`bb96ff2`](https://github.com/OpenG2P/partner-management/commit/bb96ff24d1d64538d361ad065707729a668b214c))

<a id="v-0-0-0-develop-23"></a>

## partner-management — develop 0.0.0-develop.23 (2026-08-28)

_commit `9c388db` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.23 revision:9c388db10e676a6ee3b31cc139551640266a3d99 ts:1787881675 -->

**Chart:** [partner-management 0.0.0-develop.23](https://openg2p.github.io/openg2p-helm/partner-management-0.0.0-develop.23.tgz)

### Summary

- **Major:** CI migration to GitLab, dropping GitHub Actions; includes new CI implementation and minor adjustments to the build and push pipeline.
- Authentication fixes: corrected environment variable prefixes for partner management, ensuring AUTH_ENABLED functions properly for the first time.
- Keycloak updates: new location and version adjustments, along with enhancements to partner management authentication configuration.
- New feature: added IAM registration support for Partner Management, improving user management capabilities.
- Docker configuration: corrected image sourcing to prevent reliance on Docker Hub.
- Testing improvements: automatic tests now run from the bridge, with enhancements to workflow scoping and fixes for sanity tests.
- Minor UI changes and updates to the default audit manager URL, alongside the addition of auditing features and a new questions.yaml file.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`9c388db`](https://github.com/OpenG2P/partner-management/commit/9c388db10e676a6ee3b31cc139551640266a3d99))
- Fix PM auth env prefix: the chart set COMMON_AUTH_* but Settings overrides env_prefix to partner_manager_, so with extra="allow" the JSON list arrived as an unparsed str and crashed staff-portal-api with a pydantic list_type ValidationError; renamed all four to PARTNER_MANAGER_AUTH_* (verified against the 0.0.0-develop.18 image), which also makes AUTH_ENABLED actually take effect for the first time ([`0afcbb5`](https://github.com/OpenG2P/partner-management/commit/0afcbb54b48a8ad44ba0c59acb758a78b2cbf5e9))
- Keycloak-init new location and version updated. ([`c2462ac`](https://github.com/OpenG2P/partner-management/commit/c2462ac259961f70f599a1903c053e4f6da1bfe5))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Update fastapi-common references and partner management authentication configuration ([`72cd04f`](https://github.com/OpenG2P/partner-management/commit/72cd04f3f3909b201835328b3989d4e5fd47cb1c))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add IAM registration support for Partner Management ([`1d35ff5`](https://github.com/OpenG2P/partner-management/commit/1d35ff58c48eff8afeec6b50d0b5b8ad1a47eeb3))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on partner-management ([`914c6a4`](https://github.com/OpenG2P/partner-management/commit/914c6a4a6728253c585b7d61d38375b440c82a8a))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Dockers were being picked from Docker Hub. Corrected. ([`2085c3d`](https://github.com/OpenG2P/partner-management/commit/2085c3d1c815126e7e0e5b153a29513962f71506))
- git commit -am "Repo moved to GitLab; archive notice, remove CI [skip ci]" ([`c6aab45`](https://github.com/OpenG2P/partner-management/commit/c6aab4558779be8bc6f91d5d138fb632f8dda024))
- Minor edit to test build and push pipeline on Gitlab ([`0951fe0`](https://github.com/OpenG2P/partner-management/commit/0951fe0f018011035818ec4b8b9d9a495a5c68e2))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`7cae5ea`](https://github.com/OpenG2P/partner-management/commit/7cae5ead0b6ffba592676467331ee1722894dfd4))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`5d68968`](https://github.com/OpenG2P/partner-management/commit/5d68968984ff2f37e119e2fce7390719f7c68af4))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Changes for automatic tests running from bridge. ([`c886641`](https://github.com/OpenG2P/partner-management/commit/c886641bc0f826f8b68759c073aeed5bcfda476a))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) fixes related to sanity tests on bridge. ([`bcf3228`](https://github.com/OpenG2P/partner-management/commit/bcf32282bb84e2244c8924243fbe6a8675e8f180))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Workflow scoped better. ([`9b34617`](https://github.com/OpenG2P/partner-management/commit/9b34617ac2560d72c568a7fa1582114d29bf262e))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Minor changes in UI. ([`feffc35`](https://github.com/OpenG2P/partner-management/commit/feffc35fb635425b41de53adbfe8d3f52eb10e42))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Default audit manager URL corrected. ([`4d1afdd`](https://github.com/OpenG2P/partner-management/commit/4d1afdd8cf81c6aa92e6691902d8d026d2149622))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) questions.yaml added. ([`74a4114`](https://github.com/OpenG2P/partner-management/commit/74a41147c1919c9af2582dc8c398a70fc4081932))
-  [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261)  Auditing added. ([`f9ed65b`](https://github.com/OpenG2P/partner-management/commit/f9ed65bcc6b84340a473a8704ac332c8510a98a7))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Initial version. WIP. ([`1821653`](https://github.com/OpenG2P/partner-management/commit/18216532dff90a6a28bf3689619bf06124e9a0f1))
- Initial commit ([`fcc8ceb`](https://github.com/OpenG2P/partner-management/commit/fcc8ceb2e2941e58c4153a0ad043f0a4c98b60f5))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
