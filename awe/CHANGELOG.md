# awe changelog

_Published automatically._

| Version | Date | Type |
| --- | --- | --- |
| [`1.1.0`](#v-1-1-0) | 2026-07-17 | release |
| [`0.0.0-develop.67`](#v-0-0-0-develop-67) | 2026-07-17 | develop |

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

<a id="v-0-0-0-develop-67"></a>

## awe — Unreleased (0.0.0-develop.67, 2026-07-17)

_commit `201996b` · baseline: release 1.1.0_
<!-- build:0.0.0-develop.67 revision:201996b6919f3e74def2b6bac25cf5306c5f2e3c -->

### Summary

_All changes since release 1.1.0:_

- Added support for multiple token issuers, allowing tokens minted via the public Keycloak hostname to validate alongside in-cluster tokens, resolving the 'Invalid issuer' error on registry-forwarded user tokens.

### Since last release (1.1.0)

- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) AWE: accept multiple token issuers (issuer + additional_issuers) so tokens minted via the public Keycloak hostname validate alongside in-cluster ones; fixes 'Invalid issuer' on registry-forwarded user tokens ([`201996b`](https://gitlab.com/openg2p/awe/-/commit/201996b6919f3e74def2b6bac25cf5306c5f2e3c))

