# awe changelog

_Published automatically._

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.66`](#v-0-0-0-develop-66) | 2026-07-17 | develop |

<a id="v-0-0-0-develop-66"></a>

## awe — Unreleased (0.0.0-develop.66, 2026-07-17)

_commit `eb178cd` · baseline: release v1.0.0_
<!-- build:0.0.0-develop.66 revision:eb178cd8dfdd9b5a4b18f36615664b48a69e0f5f -->

### Summary

_All changes since release v1.0.0:_

- Breaking Change: CI has been switched from GitHub Actions to GitLab CI, affecting the build and publish process.
- New Feature: Added Keycloak user management endpoints and integrated them into the UI.
- New Feature: Introduced the `assignee_name` field to the ApprovalTask model and updated related logic.
- Auto-generated OpenAPI specifications for improved API documentation.
- Updated version numbers in Chart.yaml, pyproject.toml, package.json, and package-lock.json for consistency.
- Fixed CI configuration to use a PEP 440-valid version placeholder in pyproject.toml.

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

