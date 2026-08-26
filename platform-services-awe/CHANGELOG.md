# platform-services/awe

_Published automatically._

**Repository:** [gitlab.com/openg2p/platform-services/awe](https://gitlab.com/openg2p/platform-services/awe) · **Container images:** [Container Registry](https://gitlab.com/openg2p/platform-services/awe/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.72`](#v-0-0-0-develop-72) | 2026-08-26 | develop |
| [`0.0.0-develop.71`](#v-0-0-0-develop-71) | 2026-08-24 | develop |

# Develop builds

<a id="v-0-0-0-develop-72"></a>

## platform-services/awe — develop 0.0.0-develop.72 (2026-08-26)

_commit `28b16cc` · changes since 0.0.0-develop.71_
<!-- build:0.0.0-develop.72 revision:28b16ccd573c6a9b5d21831f23d999db48f7b8a0 ts:1787719338 -->

**Chart:** [openg2p-awe 0.0.0-develop.72](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-awe-0.0.0-develop.72.tgz)

### Changes

- Keycloak-init new location and version updated. ([`28b16cc`](https://gitlab.com/openg2p/platform-services/awe/-/commit/28b16ccd573c6a9b5d21831f23d999db48f7b8a0))

<a id="v-0-0-0-develop-71"></a>

## platform-services/awe — develop 0.0.0-develop.71 (2026-08-24)

_commit `4037431` · changes since 1.1.0_
<!-- build:0.0.0-develop.71 revision:4037431fe9cd5d824c3cf04ff513e4ea4a1de2f7 ts:1787590177 -->

**Chart:** [openg2p-awe 0.0.0-develop.71](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-awe-0.0.0-develop.71.tgz)

### Summary

- Security enhancements: added configurable SSL verification for Keycloak HTTP calls and support for multiple token issuers to resolve 'Invalid issuer' errors.
- Feature addition: introduced an option to view policies within the platform.
- Infrastructure updates: applied platform-service group changes to the AWE component.

### Changes

- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on awe ([`4037431`](https://gitlab.com/openg2p/platform-services/awe/-/commit/4037431fe9cd5d824c3cf04ff513e4ea4a1de2f7))
- [G2P-5521](https://openg2p.atlassian.net/browse/G2P-5521) Option to view policy added. ([`dce3f9c`](https://gitlab.com/openg2p/platform-services/awe/-/commit/dce3f9c036b3dbf8d4a1ad4f81fa2ccd0e7aafc5))
- [G2P-5498](https://openg2p.atlassian.net/browse/G2P-5498) Add configurable SSL verification for Keycloak HTTP calls ([`b75612d`](https://gitlab.com/openg2p/platform-services/awe/-/commit/b75612d89ce98e5b4e9501b4cfb84d2222406264))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) AWE: accept multiple token issuers (issuer + additional_issuers) so tokens minted via the public Keycloak hostname validate alongside in-cluster ones; fixes 'Invalid issuer' on registry-forwarded user tokens ([`201996b`](https://gitlab.com/openg2p/platform-services/awe/-/commit/201996b6919f3e74def2b6bac25cf5306c5f2e3c))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
