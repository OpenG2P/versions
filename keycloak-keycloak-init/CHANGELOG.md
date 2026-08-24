# keycloak/keycloak-init

_Published automatically._

**Repository:** [gitlab.com/openg2p/keycloak/keycloak-init](https://gitlab.com/openg2p/keycloak/keycloak-init) · **Container images:** [Container Registry](https://gitlab.com/openg2p/keycloak/keycloak-init/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.57`](#v-0-0-0-develop-57) | 2026-08-24 | develop |
| [`0.0.0-develop.56`](#v-0-0-0-develop-56) | 2026-08-23 | develop |

# Develop builds

<a id="v-0-0-0-develop-57"></a>

## keycloak/keycloak-init — develop 0.0.0-develop.57 (2026-08-24)

_commit `f41c5e7` · changes since 0.0.0-develop.56_
<!-- build:0.0.0-develop.57 revision:f41c5e79360fd75877b24e8e4361d8f27ffe9117 ts:1787545924 -->

**Chart:** [keycloak-init 0.0.0-develop.57](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/keycloak-init-0.0.0-develop.57.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Let a realm set the display name shown on its login page ([`f41c5e7`](https://gitlab.com/openg2p/keycloak/keycloak-init/-/commit/f41c5e79360fd75877b24e8e4361d8f27ffe9117))

<a id="v-0-0-0-develop-56"></a>

## keycloak/keycloak-init — develop 0.0.0-develop.56 (2026-08-23)

_commit `d9d792d` · changes since v1.1.1_
<!-- build:0.0.0-develop.56 revision:d9d792d2a0812cc81417cfbef147039de11e0884 ts:1787446044 -->

**Chart:** [keycloak-init 0.0.0-develop.56](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/keycloak-init-0.0.0-develop.56.tgz)

### Summary

- **Major:** Migration to GitLab CI: switched from GitHub Actions to GitLab CI for build and publish processes, enhancing integration with the GitLab ecosystem.
- Container management: transitioned chart configuration to point to the GitLab registry, removing outdated Docker Hub workflows.
- Versioning updates: corrected image tag and development version for improved accuracy in deployments.

### Changes

- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Point the chart at the GitLab registry, drop the superseded Docker Hub workflows, and name the init Job by its pod-template hash ([`d9d792d`](https://gitlab.com/openg2p/keycloak/keycloak-init/-/commit/d9d792d2a0812cc81417cfbef147039de11e0884))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`9c34ee3`](https://gitlab.com/openg2p/keycloak/keycloak-init/-/commit/9c34ee3cf88f410b63f6565e20d4861acc02fa9b))
- Image tag corrected. ([`0372871`](https://gitlab.com/openg2p/keycloak/keycloak-init/-/commit/0372871de5ecdd78776162991e25ca7f18ebda12))
- Develop version corrected. ([`281115a`](https://gitlab.com/openg2p/keycloak/keycloak-init/-/commit/281115a8c97126b1432b6619c033211fbee8760b))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
