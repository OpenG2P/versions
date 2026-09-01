# verifiable-credentials

_Published automatically._

**Repository:** [github.com/OpenG2P/verifiable-credentials](https://github.com/OpenG2P/verifiable-credentials)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.16`](#v-0-0-0-develop-16) | 2026-09-01 | develop |  |
| [`0.0.0-develop.15`](#v-0-0-0-develop-15) | 2026-08-31 | develop |  |
| [`0.0.0-develop.14`](#v-0-0-0-develop-14) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-16"></a>

## verifiable-credentials — develop 0.0.0-develop.16 (2026-09-01)

_commit `67b7893` · changes since 0.0.0-develop.15_
<!-- build:0.0.0-develop.16 revision:67b7893cdddbc2e288990f89ab512657fdec57a1 ts:1788224071 -->

**Charts:** [openg2p-inji-certify 0.0.0-develop.16](https://openg2p.github.io/openg2p-helm/openg2p-inji-certify-0.0.0-develop.16.tgz) · [openg2p-inji-verify 0.0.0-develop.16](https://openg2p.github.io/openg2p-helm/openg2p-inji-verify-0.0.0-develop.16.tgz)

**Chart:** [2 charts 0.0.0-develop.16](https://openg2p.github.io/openg2p-helm/index.yaml)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Serve the JWKS at the well-known path a verifier resolves ([`67b7893`](https://github.com/OpenG2P/verifiable-credentials/commit/67b7893cdddbc2e288990f89ab512657fdec57a1))

<a id="v-0-0-0-develop-15"></a>

## verifiable-credentials — develop 0.0.0-develop.15 (2026-08-31)

_commit `2ad48fd` · changes since 0.0.0-develop.14_
<!-- build:0.0.0-develop.15 revision:2ad48fdf69bd3649dc26ed3ee67fbb065b8aca52 ts:1788139964 -->

**Chart:** [2 charts 0.0.0-develop.15](https://openg2p.github.io/openg2p-helm/index.yaml)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add a stateless Inji Verify chart and publish it alongside Certify ([`2ad48fd`](https://github.com/OpenG2P/verifiable-credentials/commit/2ad48fdf69bd3649dc26ed3ee67fbb065b8aca52))

<a id="v-0-0-0-develop-14"></a>

## verifiable-credentials — develop 0.0.0-develop.14 (2026-08-28)

_commit `e9b9a19` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.14 revision:e9b9a19e72d90d55f4b96d1998364dd825f7cf82 ts:1787893366 -->

**Chart:** [openg2p-inji-certify 0.0.0-develop.14](https://openg2p.github.io/openg2p-helm/openg2p-inji-certify-0.0.0-develop.14.tgz)

### Summary

- **Major:** Migration of VC issuance to GitLab with CI pipeline and chart conformance, enhancing build and deployment processes.
- Improvements to Certify schema creation by using an init container instead of a post-install hook, and fixing startup issues by dropping the mock VCI plugin and adding issuer display.
- Security enhancements include backing up the signing keystore to a Secret and scoping the keystore-backup permission to its own ServiceAccount.
- Clarifications on keystore install options to ensure issuer identity retention and updates related to issuer specifications and phase 1 implementations.
- Removal of unused components and consolidation of issuer-related updates to streamline the codebase.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub ([`e9b9a19`](https://github.com/OpenG2P/verifiable-credentials/commit/e9b9a19e72d90d55f4b96d1998364dd825f7cf82))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Create the Certify schema from an init container instead of a post-install hook ([`60d98a8`](https://github.com/OpenG2P/verifiable-credentials/commit/60d98a8d3ae6fe83e3fd1326a5ce6ca6fc967731))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Replace unavailable images and scope the keystore-backup permission to its own ServiceAccount ([`3e9d762`](https://github.com/OpenG2P/verifiable-credentials/commit/3e9d7629b5a158fa5030e1a9f18a00b91cac5d7c))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Back up the signing keystore to a Secret, resolve did:web, and expose credential validity ([`dde15fe`](https://github.com/OpenG2P/verifiable-credentials/commit/dde15fe252f5c1e92702c53a452f9f34d3cc74cf))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix Certify startup: drop the mock VCI plugin, add issuer display, roll pods on config change ([`5c213c8`](https://github.com/OpenG2P/verifiable-credentials/commit/5c213c802cc11e0100003b5d4bc54781fa5669bd))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Clarify keystore install options so the issuer identity is not lost ([`4913b68`](https://github.com/OpenG2P/verifiable-credentials/commit/4913b686653ee799975bc89d77beede6c3df52eb))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Migrate VC issuance to GitLab with CI pipeline and chart conformance ([`349592a`](https://github.com/OpenG2P/verifiable-credentials/commit/349592aee450eb9b3edf1d5172c463d1813932b9))
- Updated ([`490a310`](https://github.com/OpenG2P/verifiable-credentials/commit/490a310b5f0f7bacd7d4353224c798145ee241d7))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Issuer related updates. ([`b2ae74b`](https://github.com/OpenG2P/verifiable-credentials/commit/b2ae74b7a94db333ce8609a60234182eaadcea1d))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ununsed parts removed. ([`0cbd0ed`](https://github.com/OpenG2P/verifiable-credentials/commit/0cbd0ed2188b1b6eba86df0963dbb2e45b2251f9))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Only issuer specified here. Rest should be part of modules. ([`ee80dbc`](https://github.com/OpenG2P/verifiable-credentials/commit/ee80dbce42d9d72c34e92e453cd9d37b21a68c71))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Several updates for phase 1 implementations. Helm chart added. ([`0e37a5b`](https://github.com/OpenG2P/verifiable-credentials/commit/0e37a5bfd00b037a64be83ba462f177661883e9d))
- Initial commit ([`d338c46`](https://github.com/OpenG2P/verifiable-credentials/commit/d338c468eff6987c4fab624810f83528fbd24ff6))
- Initial commit ([`04a65e5`](https://github.com/OpenG2P/verifiable-credentials/commit/04a65e566a0934adeb109540ab8631f8d6d3291a))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
