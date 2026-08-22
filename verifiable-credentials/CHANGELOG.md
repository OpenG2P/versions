# verifiable-credentials

_Published automatically._

**Repository:** [gitlab.com/openg2p/verifiable-credentials](https://gitlab.com/openg2p/verifiable-credentials) · **Container images:** [Container Registry](https://gitlab.com/openg2p/verifiable-credentials/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.11`](#v-0-0-0-develop-11) | 2026-08-22 | develop |
| [`0.0.0-develop.10`](#v-0-0-0-develop-10) | 2026-08-20 | develop |
| [`0.0.0-develop.9`](#v-0-0-0-develop-9) | 2026-08-20 | develop |
| [`0.0.0-develop.8`](#v-0-0-0-develop-8) | 2026-08-19 | develop |

# Develop builds

<a id="v-0-0-0-develop-11"></a>

## verifiable-credentials — develop 0.0.0-develop.11 (2026-08-22)

_commit `dde15fe` · changes since 0.0.0-develop.10_
<!-- build:0.0.0-develop.11 revision:dde15fe252f5c1e92702c53a452f9f34d3cc74cf ts:1787360495 -->

**Chart:** [openg2p-inji-certify 0.0.0-develop.11](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-inji-certify-0.0.0-develop.11.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Back up the signing keystore to a Secret, resolve did:web, and expose credential validity ([`dde15fe`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/dde15fe252f5c1e92702c53a452f9f34d3cc74cf))

<a id="v-0-0-0-develop-10"></a>

## verifiable-credentials — develop 0.0.0-develop.10 (2026-08-20)

_commit `5c213c8` · changes since 0.0.0-develop.9_
<!-- build:0.0.0-develop.10 revision:5c213c802cc11e0100003b5d4bc54781fa5669bd ts:1787215038 -->

**Chart:** [openg2p-inji-certify 0.0.0-develop.10](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-inji-certify-0.0.0-develop.10.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix Certify startup: drop the mock VCI plugin, add issuer display, roll pods on config change ([`5c213c8`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/5c213c802cc11e0100003b5d4bc54781fa5669bd))

<a id="v-0-0-0-develop-9"></a>

## verifiable-credentials — develop 0.0.0-develop.9 (2026-08-20)

_commit `4913b68` · changes since 0.0.0-develop.8_
<!-- build:0.0.0-develop.9 revision:4913b686653ee799975bc89d77beede6c3df52eb ts:1787213655 -->

**Chart:** [openg2p-inji-certify 0.0.0-develop.9](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-inji-certify-0.0.0-develop.9.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Clarify keystore install options so the issuer identity is not lost ([`4913b68`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/4913b686653ee799975bc89d77beede6c3df52eb))

<a id="v-0-0-0-develop-8"></a>

## verifiable-credentials — develop 0.0.0-develop.8 (2026-08-19)

_commit `349592a` · changes since the start_
<!-- build:0.0.0-develop.8 revision:349592aee450eb9b3edf1d5172c463d1813932b9 ts:1787104226 -->

**Chart:** [openg2p-inji-certify 0.0.0-develop.8](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-inji-certify-0.0.0-develop.8.tgz)

### Summary

- **Major:** Migration of VC issuance to GitLab with a new CI pipeline and Helm chart integration.
- Issuer-related updates and removal of unused components to streamline the implementation.
- Phase 1 implementation enhancements, focusing on issuer specifications and modularization.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Migrate VC issuance to GitLab with CI pipeline and chart conformance ([`349592a`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/349592aee450eb9b3edf1d5172c463d1813932b9))
- Updated ([`490a310`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/490a310b5f0f7bacd7d4353224c798145ee241d7))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Issuer related updates. ([`b2ae74b`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/b2ae74b7a94db333ce8609a60234182eaadcea1d))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ununsed parts removed. ([`0cbd0ed`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/0cbd0ed2188b1b6eba86df0963dbb2e45b2251f9))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Only issuer specified here. Rest should be part of modules. ([`ee80dbc`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/ee80dbce42d9d72c34e92e453cd9d37b21a68c71))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Several updates for phase 1 implementations. Helm chart added. ([`0e37a5b`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/0e37a5bfd00b037a64be83ba462f177661883e9d))
- Initial commit ([`d338c46`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/d338c468eff6987c4fab624810f83528fbd24ff6))
- Initial commit ([`04a65e5`](https://gitlab.com/openg2p/verifiable-credentials/-/commit/04a65e566a0934adeb109540ab8631f8d6d3291a))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
