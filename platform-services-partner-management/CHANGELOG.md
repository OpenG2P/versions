# platform-services/partner-management

_Published automatically._

**Repository:** [gitlab.com/openg2p/platform-services/partner-management](https://gitlab.com/openg2p/platform-services/partner-management) · **Container images:** [Container Registry](https://gitlab.com/openg2p/platform-services/partner-management/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.15`](#v-0-0-0-develop-15) | 2026-08-26 | develop |
| [`0.0.0-develop.14`](#v-0-0-0-develop-14) | 2026-08-25 | develop |

# Develop builds

<a id="v-0-0-0-develop-15"></a>

## platform-services/partner-management — develop 0.0.0-develop.15 (2026-08-26)

_commit `c2462ac` · changes since 0.0.0-develop.14_
<!-- build:0.0.0-develop.15 revision:c2462ac259961f70f599a1903c053e4f6da1bfe5 ts:1787719371 -->

**Chart:** [partner-management 0.0.0-develop.15](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/partner-management-0.0.0-develop.15.tgz)

### Changes

- Keycloak-init new location and version updated. ([`c2462ac`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/c2462ac259961f70f599a1903c053e4f6da1bfe5))

<a id="v-0-0-0-develop-14"></a>

## platform-services/partner-management — develop 0.0.0-develop.14 (2026-08-25)

_commit `914c6a4` · changes since the start_
<!-- build:0.0.0-develop.14 revision:914c6a4a6728253c585b7d61d38375b440c82a8a ts:1787595382 -->

**Chart:** [partner-management 0.0.0-develop.14](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/partner-management-0.0.0-develop.14.tgz)

### Summary

- **Major:** CI transition to GitLab with new pipeline implementation, dropping GitHub Actions for build and publish processes.
- Docker source correction: switched from Docker Hub to a more secure source for Docker images.
- Testing enhancements: automatic tests now run from the bridge, with improvements to sanity tests and better workflow scoping.
- UI adjustments and minor fixes, including corrections to the default audit manager URL and the addition of `questions.yaml`.
- Initial auditing features introduced as part of ongoing development efforts.

### Changes

- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on partner-management ([`914c6a4`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/914c6a4a6728253c585b7d61d38375b440c82a8a))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Dockers were being picked from Docker Hub. Corrected. ([`2085c3d`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/2085c3d1c815126e7e0e5b153a29513962f71506))
- Minor edit to test build and push pipeline on Gitlab ([`0951fe0`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/0951fe0f018011035818ec4b8b9d9a495a5c68e2))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`7cae5ea`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/7cae5ead0b6ffba592676467331ee1722894dfd4))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`5d68968`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/5d68968984ff2f37e119e2fce7390719f7c68af4))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Changes for automatic tests running from bridge. ([`c886641`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/c886641bc0f826f8b68759c073aeed5bcfda476a))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) fixes related to sanity tests on bridge. ([`bcf3228`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/bcf32282bb84e2244c8924243fbe6a8675e8f180))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Workflow scoped better. ([`9b34617`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/9b34617ac2560d72c568a7fa1582114d29bf262e))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Minor changes in UI. ([`feffc35`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/feffc35fb635425b41de53adbfe8d3f52eb10e42))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Default audit manager URL corrected. ([`4d1afdd`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/4d1afdd8cf81c6aa92e6691902d8d026d2149622))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) questions.yaml added. ([`74a4114`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/74a41147c1919c9af2582dc8c398a70fc4081932))
-  [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261)  Auditing added. ([`f9ed65b`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/f9ed65bcc6b84340a473a8704ac332c8510a98a7))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Initial version. WIP. ([`1821653`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/18216532dff90a6a28bf3689619bf06124e9a0f1))
- Initial commit ([`fcc8ceb`](https://gitlab.com/openg2p/platform-services/partner-management/-/commit/fcc8ceb2e2941e58c4153a0ad043f0a4c98b60f5))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
