# consent-manager

_Published automatically._

**Repository:** [github.com/OpenG2P/consent-manager](https://github.com/OpenG2P/consent-manager) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.57`](#v-0-0-0-develop-57) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-57"></a>

## consent-manager — develop 0.0.0-develop.57 (2026-08-28)

_commit `c67030b` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.57 revision:c67030b14e70decb46d2ebdbba07e4c9e63def7f ts:1787881677 -->

**Chart:** [openg2p-consent-manager 0.0.0-develop.57](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-0.0.0-develop.57.tgz)

### Summary

- **Major:** Migration to GitLab: repository moved from GitHub, with updated README to reflect the change and disabled auto build/publish on GitHub.
- CI/CD enhancements: implemented a central build-publish workflow, replacing the previous docker-build and helm-publish processes; fixed chart job in GitLab pipeline.
- Image and chart publishing: consent-manager images and charts are now published exclusively to GitLab, with adjustments to avoid name clashes and ensure proper versioning.
- Environment variable fix: resolved duplicate SANITY_VERIFY_TLS environment variable issue in the cm-sanity Job, preventing job failures.
- Job name alignment: introduced sanity.nameOverride to ensure consistency in job naming when API components are renamed.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`c67030b`](https://github.com/OpenG2P/consent-manager/commit/c67030b14e70decb46d2ebdbba07e4c9e63def7f))
- Keycloak-init new location and version updated. ([`a434f9b`](https://github.com/OpenG2P/consent-manager/commit/a434f9b73a744aaa2687aa6917e39de3f514ebd4))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Point image source and project URLs at the new GitLab location (openg2p/platform-services/consent-manager). ([`81e8fd6`](https://github.com/OpenG2P/consent-manager/commit/81e8fd6f8a0bd1bcdc53ea83ae474abaa1bebe2c))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on consent-manager ([`9b09d4c`](https://github.com/OpenG2P/consent-manager/commit/9b09d4c655eaab0d52f456d9e07ed316736f0a94))
- Fix duplicate SANITY_VERIFY_TLS env in the cm-sanity Job (emitted both inline and via the shared pmSeedEnv helper), which made server-side apply reject the Job with "duplicate entries for key" and fail the release ([`a9f7c06`](https://github.com/OpenG2P/consent-manager/commit/a9f7c0684d3c0eb3286da61d81ed6f3343c6915b))
- The sanity and pm-seed Jobs hardcoded &lt;release&gt;-sanity / &lt;release&gt;-pm-seed, so when the API components are renamed via nameOverride the sanity Job name no longer lines up with them. Add sanity.nameOverride (default "" = no change) inserted as an infix: e.g. "cm" -&gt; &lt;release&gt;-cm-sanity / &lt;release&gt;-cm-pm-seed. ([`954ee5f`](https://github.com/OpenG2P/consent-manager/commit/954ee5f21b87245c3c5dfc2583552881f23d4f77))
- Minor edit to just stimulate helm publish. ([`64fa696`](https://github.com/OpenG2P/consent-manager/commit/64fa6965a4a6dcd68af70ba02290271a59deff09))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Freeze GitHub repo: add "moved to GitLab" README notice and disable auto build/publish (remove push/tag triggers). ([`d826db5`](https://github.com/OpenG2P/consent-manager/commit/d826db55ac86bac7cd3e6c70b55540bce3caeaf6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Re-run GitLab pipeline with fixed chart job ([`51fd07c`](https://github.com/OpenG2P/consent-manager/commit/51fd07c2a7e90c6ccd76436172f331ae373f023d))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Minor edit of README. ([`58f81a4`](https://github.com/OpenG2P/consent-manager/commit/58f81a4a14490f5d5edefde87efbdfc35b376f9f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Minor edit of README. ([`f87a6ea`](https://github.com/OpenG2P/consent-manager/commit/f87a6eaea7eda4839134990bc82c6a1da88e3a98))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Moved repo from Github as is. ([`8bf5787`](https://github.com/OpenG2P/consent-manager/commit/8bf57873609d7fafd1030d7d91b40f02fab4852b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Grant packages: write in caller to satisfy reusable workflow (fix startup failure) ([`88041e0`](https://github.com/OpenG2P/consent-manager/commit/88041e0bb0e001338e2ccdded9eb334108c614d3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish consent-manager images and chart to GitLab; drop GHCR ([`b38f1e7`](https://github.com/OpenG2P/consent-manager/commit/b38f1e7e9691d25f6e50ebcdd6d882412dcb0a3c))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) consent-manager: publish images + chart to GHCR (chart under charts/ to avoid image name clash) ([`b736910`](https://github.com/OpenG2P/consent-manager/commit/b73691010948b6fb58607aef4825f28b4f23ae3b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish images + chart to GHCR only (OCI), values to ghcr.io ([`6f7508a`](https://github.com/OpenG2P/consent-manager/commit/6f7508aa35737986fec55598e0a692384da7bf63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) clarify changelog workflow_dispatch input descriptions ([`326edee`](https://github.com/OpenG2P/consent-manager/commit/326edeebd7ca9b5284da5991f14b571046442ce6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) forward changelog dispatch inputs to central workflow ([`75b649f`](https://github.com/OpenG2P/consent-manager/commit/75b649f3ceafb79f250ea20d8464e94323d56d63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix in publish. ([`9ff69b6`](https://github.com/OpenG2P/consent-manager/commit/9ff69b6b74defc2d7f51095bd9504db1f108f95b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) ci: replace docker-build + helm-publish with central build-publish workflow ([`0a508a6`](https://github.com/OpenG2P/consent-manager/commit/0a508a6e8ecbbb33d5b1d6ad898c28e409c051b1))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
