# keycloak-init

_Published automatically._

**Repository:** [github.com/OpenG2P/keycloak-init](https://github.com/OpenG2P/keycloak-init) · **Container images:** [Container Registry](https://hub.docker.com/r/openg2p/keycloak-init)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.2.0-rc.60`](#v-1-2-0-rc-60) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.60`](#v-0-0-0-develop-60) | 2026-08-28 | develop |  |

# Release candidates

<a id="v-1-2-0-rc-60"></a>

## keycloak-init 1.2.0-rc.60 — 2026-09-01

_commit `480a324` · changes since 0.0.0-develop.60_
<!-- build:1.2.0-rc.60 revision:480a3241b49e0b9a9c827a19bd57d112da94178a ts:1787881518 -->

**Chart:** [keycloak-init 1.2.0-rc.60](https://openg2p.github.io/openg2p-helm/keycloak-init-1.2.0-rc.60.tgz)

### Changes

_No new commits since 0.0.0-develop.60._

# Develop builds

<a id="v-0-0-0-develop-60"></a>

## keycloak-init — develop 0.0.0-develop.60 (2026-08-28)

_commit `480a324` · changes since v1.1.1_
<!-- build:0.0.0-develop.60 revision:480a3241b49e0b9a9c827a19bd57d112da94178a ts:1787881518 -->

**Chart:** [keycloak-init 0.0.0-develop.60](https://openg2p.github.io/openg2p-helm/keycloak-init-0.0.0-develop.60.tgz)

### Summary

- **Major:** Migration to GitLab for CI/CD, including the switch from GitHub Actions to GitLab CI and the removal of GitHub build/publish workflows.
- Build and publish processes reinstated on GitHub for legacy support, while new workflows point to the GitLab registry.
- Realm display name customization added for login pages, enhancing user experience.
- Minor corrections made to image tags and development versioning for consistency.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`480a324`](https://github.com/OpenG2P/keycloak-init/commit/480a3241b49e0b9a9c827a19bd57d112da94178a))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Let a realm set the display name shown on its login page ([`f41c5e7`](https://github.com/OpenG2P/keycloak-init/commit/f41c5e79360fd75877b24e8e4361d8f27ffe9117))
- Moved to GitLab: openg2p/keycloak/keycloak-init (read-only; build/publish disabled) ([`4e24219`](https://github.com/OpenG2P/keycloak-init/commit/4e24219b8bc2bebc3addb161c0606d89d97dc3ce))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Point the chart at the GitLab registry, drop the superseded Docker Hub workflows, and name the init Job by its pod-template hash ([`d9d792d`](https://github.com/OpenG2P/keycloak-init/commit/d9d792d2a0812cc81417cfbef147039de11e0884))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`9c34ee3`](https://github.com/OpenG2P/keycloak-init/commit/9c34ee3cf88f410b63f6565e20d4861acc02fa9b))
- Image tag corrected. ([`0372871`](https://github.com/OpenG2P/keycloak-init/commit/0372871de5ecdd78776162991e25ca7f18ebda12))
- Develop version corrected. ([`281115a`](https://github.com/OpenG2P/keycloak-init/commit/281115a8c97126b1432b6619c033211fbee8760b))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
