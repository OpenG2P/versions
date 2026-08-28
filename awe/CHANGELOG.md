# awe

_Published automatically._

**Repository:** [github.com/OpenG2P/awe](https://github.com/OpenG2P/awe) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.78`](#v-0-0-0-develop-78) | 2026-08-28 | develop |  |

# Develop builds

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
