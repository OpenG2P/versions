# master-data-service

_Published automatically._

**Repository:** [github.com/OpenG2P/master-data-service](https://github.com/OpenG2P/master-data-service) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.1.0`](#v-1-1-0) | 2026-09-01 | release |  |
| [`1.1.0-rc.73`](#v-1-1-0-rc-73) | 2026-09-01 | release candidate |  |
| [`1.1.0-rc.72`](#v-1-1-0-rc-72) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.69`](#v-0-0-0-develop-69) | 2026-09-01 | develop |  |
| [`1.1.0-rc.71`](#v-1-1-0-rc-71) | 2026-09-01 | release candidate |  |
| [`1.1.0-rc.67`](#v-1-1-0-rc-67) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.68`](#v-0-0-0-develop-68) | 2026-08-28 | develop |  |
| [`0.0.0-develop.67`](#v-0-0-0-develop-67) | 2026-08-28 | develop |  |
| [`1.1.0-rc.63`](#v-1-1-0-rc-63) | 2026-08-28 | release candidate |  |
| [`1.1.0-rc.62`](#v-1-1-0-rc-62) | 2026-08-28 | release candidate |  |
| [`0.0.0-develop.66`](#v-0-0-0-develop-66) | 2026-08-28 | develop |  |

# Releases

<a id="v-1-1-0"></a>

## master-data-service 1.1.0 — 2026-09-01

<!-- build:1.1.0 revision:f0933664668c7752ff23f216259b722e437cba86 ts:1788261922 -->

_commit `f093366` · first release_

**Same artifact as [`1.1.0-rc.73`](#v-1-1-0-rc-73)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-master-data 1.1.0](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0.tgz)

### Release notes

## What's Changed
* [G2P-4934](https://openg2p.atlassian.net/browse/G2P-4934) - master-data seeding + docker by @PSNAppz in https://github.com/OpenG2P/master-data-service/pull/1
* Fix docker build issue by @PSNAppz in https://github.com/OpenG2P/master-data-service/pull/2
* [G2P-5264](https://openg2p.atlassian.net/browse/G2P-5264): Add get_all_g2p_geo_levels API endpoint and response handling by @mkumar-02 in https://github.com/OpenG2P/master-data-service/pull/4
* Refactor geo data loading to use a single denormalized CSV by @PSNAppz in https://github.com/OpenG2P/master-data-service/pull/3
* [G2P-5268](https://openg2p.atlassian.net/browse/G2P-5268): Added DataPolicy Repository by @mkumar-02 in https://github.com/OpenG2P/master-data-service/pull/5
* [G2P-5341](https://openg2p.atlassian.net/browse/G2P-5341): Clean up registry DB and data policy codechanges in data policy handling. by @mkumar-02 in https://github.com/OpenG2P/master-data-service/pull/9
* [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Enhance geo hierarchy management with improved child-level handling, dynamic UI updates, translations, and optimized geo-tree caching by @pjoshi751 in https://github.com/OpenG2P/master-data-service/pull/12
* Enhance seed data and fix pre-commit issues by @tahzeer in https://github.com/OpenG2P/master-data-service/pull/14

## New Contributors
* @PSNAppz made their first contribution in https://github.com/OpenG2P/master-data-service/pull/1
* @pjoshi751 made their first contribution in https://github.com/OpenG2P/master-data-service/pull/12
* @tahzeer made their first contribution in https://github.com/OpenG2P/master-data-service/pull/14

**Full Changelog**: https://github.com/OpenG2P/master-data-service/commits/1.1.0

### Summary

- **Major:** Refactor of Geo and Attribute components for improved functionality, UI consistency, and error handling, alongside a redesign of the master data UI.
- Data model enhancements: Added new prefixes and relationship attributes to `g2p_attribute_values` and `g2p_attributes` tables, and removed obsolete agricultural and social codelists and attributes.
- Dependency updates: Upgraded `keycloak-init` to 1.2.0, `iam` to 1.4.0, and `fastapi-common` to 1.2.0, with adjustments to repository references in Docker and CI configurations.
- Improved geo hierarchy management with dynamic UI updates, translations, and optimized geo-tree caching.
- Pre-commit and deployment fixes to enhance code quality and streamline processes.

### Changes

- Update image tags to version 1.1.0 ([`f093366`](https://github.com/OpenG2P/master-data-service/commit/f0933664668c7752ff23f216259b722e437cba86))
- keycloak-init(1.2.0) iam (1.4.0) and fastapi-common (1.2.0) updated ([`3ab8224`](https://github.com/OpenG2P/master-data-service/commit/3ab8224faeadc3be91762ecbbb24f00ca8cdf72f))
- [G2P-5616](https://openg2p.atlassian.net/browse/G2P-5616) Enhance seed data by adding new prefixes and relationship attributes to the g2p_attribute_values and g2p_attributes tables. ([`8d3afc6`](https://github.com/OpenG2P/master-data-service/commit/8d3afc622e511e03984b0c8edb0892ba53bba3f9))
- deployment pre-commit fix ([`99a1aa8`](https://github.com/OpenG2P/master-data-service/commit/99a1aa82232d045876c6ae536f58a48a9617e87f))
- pre-commit fixes ([`9cae598`](https://github.com/OpenG2P/master-data-service/commit/9cae598b110936c7ec97509c7f88184cb06eb040))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Point the iam-core pin at GitHub ([`4454ed8`](https://github.com/OpenG2P/master-data-service/commit/4454ed8eea85bc1984991c75c5a590025d296d57))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.1 release line with GitHub ([`4ffaad7`](https://github.com/OpenG2P/master-data-service/commit/4ffaad7339dadb2783ac9824c38bbfd417de0ff2))
- [G2P-5593](https://openg2p.atlassian.net/browse/G2P-5593) Refactor Geo and Attribute components for improved functionality and UI consistency ([`7945eda`](https://github.com/OpenG2P/master-data-service/commit/7945eda9b8e52bd84df122e7b1dccdfb66b6f62d))
- [G2P-5593](https://openg2p.atlassian.net/browse/G2P-5593) Redesign master data UI and enhance Geo components with error handling and UX improvements ([`edfc287`](https://github.com/OpenG2P/master-data-service/commit/edfc287f00bd450b06249d2163823912d04254f2))
- [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Enhance geo hierarchy management with improved child-level handling, dynamic UI updates, translations, and optimized geo-tree caching. ([`0aa5879`](https://github.com/OpenG2P/master-data-service/commit/0aa5879819f4d303746b7f9760c4c44c60bb7364))
- [G2P-5586](https://openg2p.atlassian.net/browse/G2P-5586) Update FASTAPI_COMMON_REF to version 1.2 and change repository URL in Dockerfile and .gitlab-ci.yml ([`f6c2bc4`](https://github.com/OpenG2P/master-data-service/commit/f6c2bc41b1c66ccc91a7e70fd325ec5d6916841d))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Refactor IAM register ConfigMap and Job templates for improved naming and annotations ([`3b1dae4`](https://github.com/OpenG2P/master-data-service/commit/3b1dae4711450994d4720113521a950f8ec1fa6d))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Removed obsolete agricultural and social codelists, attributes, and unused schema entries, while updating social codelists with new livelihood values and attributes. ([`980d938`](https://github.com/OpenG2P/master-data-service/commit/980d938095e95d456c645d805082304af27e2681))
- Refactor attribute and geo schemas to remove unused fields and simplify data models ([`a84cf6b`](https://github.com/OpenG2P/master-data-service/commit/a84cf6ba162bc350fcb66e4ec57ebde3ec2fb657))
- [G2P-5574](https://openg2p.atlassian.net/browse/G2P-5574) Add component label to master-data-api deployment and service ([`f809fa7`](https://github.com/OpenG2P/master-data-service/commit/f809fa7db597b29e7f52460c9c04912b95b471b2))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`446b691`](https://github.com/OpenG2P/master-data-service/commit/446b69150b93586b240be875353126203426f2b8))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update version numbers and pin IAM service reference to 1.4 ([`5efbd59`](https://github.com/OpenG2P/master-data-service/commit/5efbd59651052e0e20f025268f248f3ed2842464))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add configuration for Master Data UI deployment ([`86144ee`](https://github.com/OpenG2P/master-data-service/commit/86144ee891938e0d97537e471e0aa00536345320))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Update SQL codelists to handle conflicts and enhance Docker configurations ([`968c6fb`](https://github.com/OpenG2P/master-data-service/commit/968c6fb2693c947b7764baa9f1887b2d2461ef0e))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Add initial seed data for G2P attributes and values ([`a10123b`](https://github.com/OpenG2P/master-data-service/commit/a10123ba53ecf75d4cc2e8663b19d217851fd135))

# Release candidates

<a id="v-1-1-0-rc-73"></a>

## master-data-service 1.1.0-rc.73 — 2026-09-01

_commit `f093366` · changes since 1.1.0-rc.72_
<!-- build:1.1.0-rc.73 revision:f0933664668c7752ff23f216259b722e437cba86 ts:1788261922 -->

**Chart:** [openg2p-master-data 1.1.0-rc.73](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0-rc.73.tgz)

### Changes

- Update image tags to version 1.1.0 ([`f093366`](https://github.com/OpenG2P/master-data-service/commit/f0933664668c7752ff23f216259b722e437cba86))

<a id="v-1-1-0-rc-72"></a>

## master-data-service 1.1.0-rc.72 — 2026-09-01

_commit `3ab8224` · changes since 1.1.0-rc.71_
<!-- build:1.1.0-rc.72 revision:3ab8224faeadc3be91762ecbbb24f00ca8cdf72f ts:1788261744 -->

**Chart:** [openg2p-master-data 1.1.0-rc.72](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0-rc.72.tgz)

### Changes

- keycloak-init(1.2.0) iam (1.4.0) and fastapi-common (1.2.0) updated ([`3ab8224`](https://github.com/OpenG2P/master-data-service/commit/3ab8224faeadc3be91762ecbbb24f00ca8cdf72f))

<a id="v-1-1-0-rc-71"></a>

## master-data-service 1.1.0-rc.71 — 2026-09-01

_commit `e631dc5` · changes since 1.1.0-rc.67_
<!-- build:1.1.0-rc.71 revision:e631dc5af944d6a0aa0ec0dc48ee35b5a9f6319c ts:1788257788 -->

**Chart:** [openg2p-master-data 1.1.0-rc.71](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0-rc.71.tgz)

### Summary

- Data enhancement: added new prefixes and relationship attributes to the `g2p_attribute_values` and `g2p_attributes` tables.
- Code quality: implemented multiple pre-commit fixes to improve consistency and reduce errors during development.

### Changes

- [G2P-5616](https://openg2p.atlassian.net/browse/G2P-5616) Enhance seed data by adding new prefixes and relationship attributes to the g2p_attribute_values and g2p_attributes tables. ([`8d3afc6`](https://github.com/OpenG2P/master-data-service/commit/8d3afc622e511e03984b0c8edb0892ba53bba3f9))
- deployment pre-commit fix ([`99a1aa8`](https://github.com/OpenG2P/master-data-service/commit/99a1aa82232d045876c6ae536f58a48a9617e87f))
- pre-commit fixes ([`9cae598`](https://github.com/OpenG2P/master-data-service/commit/9cae598b110936c7ec97509c7f88184cb06eb040))

<a id="v-1-1-0-rc-67"></a>

## master-data-service 1.1.0-rc.67 — 2026-09-01

_commit `be21e73` · changes since 1.1.0-rc.63_
<!-- build:1.1.0-rc.67 revision:be21e7300f10f4f1008c0040c0bbede9d1aaf84e ts:1788257368 -->

**Chart:** [openg2p-master-data 1.1.0-rc.67](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0-rc.67.tgz)

### Summary

- UI enhancements: redesigned master data UI with improved Geo components, error handling, and UX improvements; added new components including AddButton, DeleteButton, and SearchInput.
- Geo management improvements: enhanced geo hierarchy management with better child-level handling, dynamic UI updates, translations, and optimized geo-tree caching.
- Refactoring: significant refactor of Geo and Attribute components for improved functionality and UI consistency.
- Dependency updates: modifications to dependency manifests in package.json and package-lock.json, reflecting changes in 2 dependencies.

### Changes

- [G2P-5593](https://openg2p.atlassian.net/browse/G2P-5593) Refactor Geo and Attribute components for improved functionality and UI consistency ([`7945eda`](https://github.com/OpenG2P/master-data-service/commit/7945eda9b8e52bd84df122e7b1dccdfb66b6f62d))
- [G2P-5593](https://openg2p.atlassian.net/browse/G2P-5593) Redesign master data UI and enhance Geo components with error handling and UX improvements ([`edfc287`](https://github.com/OpenG2P/master-data-service/commit/edfc287f00bd450b06249d2163823912d04254f2))
- [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Enhance geo hierarchy management with improved child-level handling, dynamic UI updates, translations, and optimized geo-tree caching. ([`0aa5879`](https://github.com/OpenG2P/master-data-service/commit/0aa5879819f4d303746b7f9760c4c44c60bb7364))

<a id="v-1-1-0-rc-63"></a>

## master-data-service 1.1.0-rc.63 — 2026-08-28

_commit `4454ed8` · changes since 1.1.0-rc.62_
<!-- build:1.1.0-rc.63 revision:4454ed8eea85bc1984991c75c5a590025d296d57 ts:1787897916 -->

**Chart:** [openg2p-master-data 1.1.0-rc.63](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0-rc.63.tgz)

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Point the iam-core pin at GitHub ([`4454ed8`](https://github.com/OpenG2P/master-data-service/commit/4454ed8eea85bc1984991c75c5a590025d296d57))

<a id="v-1-1-0-rc-62"></a>

## master-data-service 1.1.0-rc.62 — 2026-08-28

_commit `4ffaad7` · changes since the start (showing the latest 20 commits)_
<!-- build:1.1.0-rc.62 revision:4ffaad7339dadb2783ac9824c38bbfd417de0ff2 ts:1787897903 -->

**Chart:** [openg2p-master-data 1.1.0-rc.62](https://openg2p.github.io/openg2p-helm/openg2p-master-data-1.1.0-rc.62.tgz)

### Summary

- **Major:** Refactored IAM configuration: updated repository references to GitLab and pinned IAM service to version 1.4, enhancing deployment stability.
- Data model optimization: removed obsolete agricultural and social codelists, simplified attribute and geo schemas by eliminating unused fields, and updated social codelists with new livelihood values.
- Feature enhancements: added geo level management and initial seed data for G2P attributes, along with improved geo management dialogs and localization updates in the Master Data UI.
- Deployment improvements: aligned the master-data-api deployment with component labels, updated Docker configurations, and enhanced SQL codelists to handle conflicts.
- Migration fixes: adjusted migration logic to ensure proper sequencing of table creation and prevent initialization failures, while also improving visibility of geo-seed options in deployment configurations.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.1 release line with GitHub ([`4ffaad7`](https://github.com/OpenG2P/master-data-service/commit/4ffaad7339dadb2783ac9824c38bbfd417de0ff2))
- [G2P-5586](https://openg2p.atlassian.net/browse/G2P-5586) Update FASTAPI_COMMON_REF to version 1.2 and change repository URL in Dockerfile and .gitlab-ci.yml ([`f6c2bc4`](https://github.com/OpenG2P/master-data-service/commit/f6c2bc41b1c66ccc91a7e70fd325ec5d6916841d))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Refactor IAM register ConfigMap and Job templates for improved naming and annotations ([`3b1dae4`](https://github.com/OpenG2P/master-data-service/commit/3b1dae4711450994d4720113521a950f8ec1fa6d))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Removed obsolete agricultural and social codelists, attributes, and unused schema entries, while updating social codelists with new livelihood values and attributes. ([`980d938`](https://github.com/OpenG2P/master-data-service/commit/980d938095e95d456c645d805082304af27e2681))
- Refactor attribute and geo schemas to remove unused fields and simplify data models ([`a84cf6b`](https://github.com/OpenG2P/master-data-service/commit/a84cf6ba162bc350fcb66e4ec57ebde3ec2fb657))
- [G2P-5574](https://openg2p.atlassian.net/browse/G2P-5574) Add component label to master-data-api deployment and service ([`f809fa7`](https://github.com/OpenG2P/master-data-service/commit/f809fa7db597b29e7f52460c9c04912b95b471b2))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`446b691`](https://github.com/OpenG2P/master-data-service/commit/446b69150b93586b240be875353126203426f2b8))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update version numbers and pin IAM service reference to 1.4 ([`5efbd59`](https://github.com/OpenG2P/master-data-service/commit/5efbd59651052e0e20f025268f248f3ed2842464))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add configuration for Master Data UI deployment ([`86144ee`](https://github.com/OpenG2P/master-data-service/commit/86144ee891938e0d97537e471e0aa00536345320))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Update SQL codelists to handle conflicts and enhance Docker configurations ([`968c6fb`](https://github.com/OpenG2P/master-data-service/commit/968c6fb2693c947b7764baa9f1887b2d2461ef0e))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Add initial seed data for G2P attributes and values ([`a10123b`](https://github.com/OpenG2P/master-data-service/commit/a10123ba53ecf75d4cc2e8663b19d217851fd135))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`67c4be5`](https://github.com/OpenG2P/master-data-service/commit/67c4be52fe8bee62f65899917dea73d83a83a19c))
- [G2P-5458](https://openg2p.atlassian.net/browse/G2P-5458) feat: add attribute and geo level management ([`6bad7a4`](https://github.com/OpenG2P/master-data-service/commit/6bad7a4ce930de29f4da8e416f224f896d23ef89))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat: enhance geo management with new dialogs and localization updates ([`1e95c1a`](https://github.com/OpenG2P/master-data-service/commit/1e95c1a9b16943ea1e1b31fd20e97d0b6bfb9664))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add geo locations and reference data management ([`275bf51`](https://github.com/OpenG2P/master-data-service/commit/275bf51a08c07871b47f4a4e2f804a68ab9d4406))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456): initialize master-data-ui project with Next.js setup ([`876a1f4`](https://github.com/OpenG2P/master-data-service/commit/876a1f434b8ef207f39b826002b6dbcb47623baa))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Wait on the last table the migration creates, not the first. g2p_geo_levels is created before g2p_attributes and the sample tables, so gating on it proved only that the migration had started — wide enough for the loader to finish geo and then die on g2p_sample_households, which is the failure the guard exists to prevent. Waiting on g2p_sample_households proves the whole migration finished, since the creates are sequential and awaited. Also bounds the pg_isready loop, which could otherwise hang the init container indefinitely against an unreachable database. ([`a31a52b`](https://github.com/OpenG2P/master-data-service/commit/a31a52beab36324e77efd5dd96c74fc89c1f6c06))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Keep XKM as the chart default, and seed the whole pack rather than geography alone. Geography by itself leaves registries on their extension's own code lists, with no semantic role tags at all and no sample people — not a working default for anything downstream. The country itself stays a deployment decision: an install nobody configured must not attach invented figures to a real country's name or pick up a licence obligation by accident. ([`2476e12`](https://github.com/OpenG2P/master-data-service/commit/2476e12ba8ec64d515c5a35178661fc990be43b5))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Surface the country pack in questions.yaml. None of the geo-seed options were in the Rancher form, so the one place a deployment declares its country was reachable only by hand-editing values — an installer had no way to know the choice existed, and every install silently took the fictitious default. ([`e319189`](https://github.com/OpenG2P/master-data-service/commit/e319189f19fab97a0855c3e2165f9e78ccff4efb))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Lowercase the geo-seed Job name. This template renders at the chart root, where .Chart.Name is the vendored subchart name — the commons-services umbrella carries it as `masterData`, so the Job came out as commons-services-masterData-geo-seed, which Kubernetes rejects. The hook failed, no geography or code lists were seeded, and the whole commons-services release went to `failed`. The API templates were unaffected because they render against a scoped context whose nameOverride is already lowercase. ([`83bfaee`](https://github.com/OpenG2P/master-data-service/commit/83bfaee9ae49249adb12589b0da1a290bf02f9fa))

# Develop builds

<a id="v-0-0-0-develop-69"></a>

## master-data-service — develop 0.0.0-develop.69 (2026-09-01)

_commit `9297cb8` · changes since 0.0.0-develop.68_
<!-- build:0.0.0-develop.69 revision:9297cb8a7df5bda7470b29582c16a9275cecf079 ts:1788258060 -->

**Chart:** [openg2p-master-data 0.0.0-develop.69](https://openg2p.github.io/openg2p-helm/openg2p-master-data-0.0.0-develop.69.tgz)

### Changes

- fastapi-common updated to 1.2.0 ([`9297cb8`](https://github.com/OpenG2P/master-data-service/commit/9297cb8a7df5bda7470b29582c16a9275cecf079))

<a id="v-0-0-0-develop-68"></a>

## master-data-service — develop 0.0.0-develop.68 (2026-08-28)

_commit `cfc0c13` · changes since 0.0.0-develop.67_
<!-- build:0.0.0-develop.68 revision:cfc0c13dfd0dcc3ed058494e24ba953a3abf1094 ts:1787915008 -->

**Chart:** [openg2p-master-data 0.0.0-develop.68](https://openg2p.github.io/openg2p-helm/openg2p-master-data-0.0.0-develop.68.tgz)

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) pin FASTAPI_COMMON_REF to 1.2 in the caller, not just the Dockerfile ([`cfc0c13`](https://github.com/OpenG2P/master-data-service/commit/cfc0c13dfd0dcc3ed058494e24ba953a3abf1094))

<a id="v-0-0-0-develop-67"></a>

## master-data-service — develop 0.0.0-develop.67 (2026-08-28)

_commit `135b60c` · changes since 0.0.0-develop.66_
<!-- build:0.0.0-develop.67 revision:135b60cb76c53759802f82e5707e74cce76225e7 ts:1787914056 -->

**Chart:** [openg2p-master-data 0.0.0-develop.67](https://openg2p.github.io/openg2p-helm/openg2p-master-data-0.0.0-develop.67.tgz)

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) pin fastapi-common to 1.2 to match iam-core 1.4 ([`135b60c`](https://github.com/OpenG2P/master-data-service/commit/135b60cb76c53759802f82e5707e74cce76225e7))

<a id="v-0-0-0-develop-66"></a>

## master-data-service — develop 0.0.0-develop.66 (2026-08-28)

_commit `0bba3c9` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.66 revision:0bba3c9f46465a104bb7d60c092e1739c9e0c7be ts:1787885132 -->

**Chart:** [openg2p-master-data 0.0.0-develop.66](https://openg2p.github.io/openg2p-helm/openg2p-master-data-0.0.0-develop.66.tgz)

### Summary

- **Major:** Migration improvements: adjusted migration logic to ensure proper sequencing and prevent failures by waiting on the completion of critical tables.
- Feature enhancements: added geo level and attribute management, including new dialogs, localization updates, and support for data policies; introduced initial seed data for G2P attributes and values.
- UI updates: initialized the master-data-ui project with Next.js, added configuration for deployment, and enhanced geo locations and reference data management.
- Dependency management: pinned keycloak-init to a specific version and updated IAM service references from GitHub to GitLab, including version number adjustments.
- Code quality: applied pre-commit formatting across the repository, ensuring consistency without functional changes; fixed issues with pod selector conflicts and SQL codelist handling.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Pin keycloak-init to a version published on GitHub ([`0bba3c9`](https://github.com/OpenG2P/master-data-service/commit/0bba3c9f46465a104bb7d60c092e1739c9e0c7be))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`96f630f`](https://github.com/OpenG2P/master-data-service/commit/96f630f2f64cef0d06fe1c539ecb718542e01970))
- Apply pre-commit formatting across the repo (black line-length reflow in master-data-api, trailing whitespace in codelist SQL seeds, missing final newlines in UI files, README and .gitignore); formatting only, no functional change ([`b423005`](https://github.com/OpenG2P/master-data-service/commit/b42300512c21c72c41d0b71421003b5d7c3798aa))
- 67c4be5  [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`16a0d36`](https://github.com/OpenG2P/master-data-service/commit/16a0d36d8480be8f5e64f8ab33b08ab0459f0795))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on master-data-service ([`179581b`](https://github.com/OpenG2P/master-data-service/commit/179581b5a781d7afd23b09885f53de2df95abd8f))
- Fix for clashing pod selector. ([`4de586a`](https://github.com/OpenG2P/master-data-service/commit/4de586a941563743442d88e0892d57b7da15a089))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise national IDs when loading a country pack ([`fe9ce25`](https://github.com/OpenG2P/master-data-service/commit/fe9ce25ea14949d869a2e81723bc86aa8b193248))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`446b691`](https://github.com/OpenG2P/master-data-service/commit/446b69150b93586b240be875353126203426f2b8))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update version numbers and pin IAM service reference to 1.4 ([`5efbd59`](https://github.com/OpenG2P/master-data-service/commit/5efbd59651052e0e20f025268f248f3ed2842464))
- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Carry the pack's birth_date through to the sample individuals table. The API builds these tables with create_all, which never adds a column to an existing one, so the seed job adds the column itself before inserting rather than failing on an environment seeded before this field existed. ([`4f29f7a`](https://github.com/OpenG2P/master-data-service/commit/4f29f7af99ef270f51386a709ff4032ae474aeab))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add configuration for Master Data UI deployment ([`86144ee`](https://github.com/OpenG2P/master-data-service/commit/86144ee891938e0d97537e471e0aa00536345320))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Update SQL codelists to handle conflicts and enhance Docker configurations ([`968c6fb`](https://github.com/OpenG2P/master-data-service/commit/968c6fb2693c947b7764baa9f1887b2d2461ef0e))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Add initial seed data for G2P attributes and values ([`a10123b`](https://github.com/OpenG2P/master-data-service/commit/a10123ba53ecf75d4cc2e8663b19d217851fd135))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`67c4be5`](https://github.com/OpenG2P/master-data-service/commit/67c4be52fe8bee62f65899917dea73d83a83a19c))
- [G2P-5458](https://openg2p.atlassian.net/browse/G2P-5458) feat: add attribute and geo level management ([`6bad7a4`](https://github.com/OpenG2P/master-data-service/commit/6bad7a4ce930de29f4da8e416f224f896d23ef89))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat: enhance geo management with new dialogs and localization updates ([`1e95c1a`](https://github.com/OpenG2P/master-data-service/commit/1e95c1a9b16943ea1e1b31fd20e97d0b6bfb9664))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add geo locations and reference data management ([`275bf51`](https://github.com/OpenG2P/master-data-service/commit/275bf51a08c07871b47f4a4e2f804a68ab9d4406))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456): initialize master-data-ui project with Next.js setup ([`876a1f4`](https://github.com/OpenG2P/master-data-service/commit/876a1f434b8ef207f39b826002b6dbcb47623baa))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Wait on the last table the migration creates, not the first. g2p_geo_levels is created before g2p_attributes and the sample tables, so gating on it proved only that the migration had started — wide enough for the loader to finish geo and then die on g2p_sample_households, which is the failure the guard exists to prevent. Waiting on g2p_sample_households proves the whole migration finished, since the creates are sequential and awaited. Also bounds the pg_isready loop, which could otherwise hang the init container indefinitely against an unreachable database. ([`a31a52b`](https://github.com/OpenG2P/master-data-service/commit/a31a52beab36324e77efd5dd96c74fc89c1f6c06))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Keep XKM as the chart default, and seed the whole pack rather than geography alone. Geography by itself leaves registries on their extension's own code lists, with no semantic role tags at all and no sample people — not a working default for anything downstream. The country itself stays a deployment decision: an install nobody configured must not attach invented figures to a real country's name or pick up a licence obligation by accident. ([`2476e12`](https://github.com/OpenG2P/master-data-service/commit/2476e12ba8ec64d515c5a35178661fc990be43b5))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
