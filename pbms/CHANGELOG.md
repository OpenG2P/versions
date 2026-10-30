# pbms

_Published automatically._

**Repository:** [github.com/OpenG2P/pbms](https://github.com/OpenG2P/pbms) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.18`](#v-0-0-0-develop-18) | 2026-10-30 | develop |  |
| [`0.0.0-develop.11`](#v-0-0-0-develop-11) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-18"></a>

## pbms — develop 0.0.0-develop.18 (2026-10-30)

_commit `6e69621` · changes since 0.0.0-develop.11_
<!-- build:0.0.0-develop.18 revision:6e6962128616de9dbc56642a3618f32c207af75f ts:1793365610 -->

**Chart:** [openg2p-pbms-platform 0.0.0-develop.18](https://openg2p.github.io/openg2p-helm/openg2p-pbms-platform-0.0.0-develop.18.tgz)

### Summary

- **Major:** Refactor of Helm chart, renaming to `openg2p-pbms-platform`, and merging Celery beat and worker into a single image.
- Refactoring of background task routing and search functionality through adapters, enhancing modularity.
- Registry extensions have been relocated to `pbms-connectors`, streamlining the architecture.
- Transition from `sql_query` rules to `pbms_domain`, simplifying rule management. 
- CI improvements with the publication of base images and platform charts for better deployment processes.

### Changes

- [G2P-5803](https://openg2p.atlassian.net/browse/G2P-5803) build(ci): publish base images and platform chart ([`e079ecf`](https://github.com/OpenG2P/pbms/commit/e079ecfddd3fdf91100293493b058e27ed64354b))
- [G2P-5803](https://openg2p.atlassian.net/browse/G2P-5803) refactor(helm)!: rename chart to openg2p-pbms-platform ([`08c8534`](https://github.com/OpenG2P/pbms/commit/08c85342fefcb5fa5de30041cf3d5790867d6b52))
- [G2P-5803](https://openg2p.atlassian.net/browse/G2P-5803) refactor!: merge celery beat and worker into one image ([`0c7bbb3`](https://github.com/OpenG2P/pbms/commit/0c7bbb35bb273bb68a777a372a7b57fc0933f72c))
- [G2P-5803](https://openg2p.atlassian.net/browse/G2P-5803) refactor!: route bg tasks and search through adapters ([`254ab60`](https://github.com/OpenG2P/pbms/commit/254ab6011440c23b1dfa4e05c2a3f04e5468c0fe))
- [G2P-5803](https://openg2p.atlassian.net/browse/G2P-5803) refactor!: move registry extensions to pbms-connectors ([`4bf6f59`](https://github.com/OpenG2P/pbms/commit/4bf6f59f8a10f02a3ce4c58443d617163139300c))
- [G2P-5803](https://openg2p.atlassian.net/browse/G2P-5803) refactor!: drop sql_query rules in favor of pbms_domain ([`a98dbf3`](https://github.com/OpenG2P/pbms/commit/a98dbf339e72dad024d4bc4446018a36e51d99fa))

<a id="v-0-0-0-develop-11"></a>

## pbms — develop 0.0.0-develop.11 (2026-08-28)

_commit `aa1ce60` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.11 revision:aa1ce60cdd91a8c01148c044caef9e27049741af ts:1787893044 -->

**Chart:** [openg2p-pbms 0.0.0-develop.11](https://openg2p.github.io/openg2p-helm/openg2p-pbms-0.0.0-develop.11.tgz)

### Summary

- **Major:** Migration to GitLab for CI/CD, dropping GitHub Actions and enabling a central build-publish pipeline for multiple images and charts.
- Dependency updates: versions for core components and Postgres-init chart have been updated, and the odoo-commons pin has been removed from the Dockerfile.
- Consolidation efforts are ongoing, with multiple work-in-progress commits aimed at streamlining the codebase.
- Documentation added with the creation of a README.md file to improve project clarity.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`aa1ce60`](https://github.com/OpenG2P/pbms/commit/aa1ce60cdd91a8c01148c044caef9e27049741af))
- Moved to GitLab: openg2p/pbms/pbms (read-only; build/publish disabled) ([`3c3448a`](https://github.com/OpenG2P/pbms/commit/3c3448a5d72eb79190c8287fe017cee46eadb893))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`9129bbd`](https://github.com/OpenG2P/pbms/commit/9129bbd4fb4f73fa37af929a44a7124071d845f3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Drop odoo-commons pin on the core image (Dockerfile clones by ref name, not SHA) ([`0e54e65`](https://github.com/OpenG2P/pbms/commit/0e54e65238d79f8d1fbd7bf0bd8c43b381874188))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Adopt central build-publish CI (5 images + openg2p-pbms chart + changelog); remove old docker/helm workflows. Pull g2p-bridge models from GitLab develop (was the GitHub mirror) ([`5248e61`](https://github.com/OpenG2P/pbms/commit/5248e61241476d0d93bdc50de48d86b30677082c))
- [G2P-3614](https://openg2p.atlassian.net/browse/G2P-3614) versions updated. ([`565993f`](https://github.com/OpenG2P/pbms/commit/565993fd5e86ed5a9f2754ac86127354d50c98fd))
- [G2P-3614](https://openg2p.atlassian.net/browse/G2P-3614) Postgres-init chart version updated. ([`82c20f6`](https://github.com/OpenG2P/pbms/commit/82c20f68361ef60e305b2b58ef7cd56b3ef9fedd))
- [G2P-3614](https://openg2p.atlassian.net/browse/G2P-3614) Consolidation. WIP. ([`36b2fee`](https://github.com/OpenG2P/pbms/commit/36b2feeef878f2d33b1a7e8c1fbae3abf145671f))
- [G2P-3614](https://openg2p.atlassian.net/browse/G2P-3614) Consolidation. WIP. ([`7fe8455`](https://github.com/OpenG2P/pbms/commit/7fe8455c55dc4cccf46eafd9c4d09c06569ca9be))
- Create README.md ([`29cd29e`](https://github.com/OpenG2P/pbms/commit/29cd29e674f88b583e73cdf9742d95306de31f5e))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
