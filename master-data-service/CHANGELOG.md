# master-data-service

_Published automatically._

**Repository:** [gitlab.com/openg2p/master-data-service](https://gitlab.com/openg2p/master-data-service) · **Container images:** [Container Registry](https://gitlab.com/openg2p/master-data-service/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.32`](#v-0-0-0-develop-32) | 2026-07-30 | develop |
| [`0.0.0-develop.31`](#v-0-0-0-develop-31) | 2026-07-29 | develop |
| [`0.0.0-develop.30`](#v-0-0-0-develop-30) | 2026-07-28 | develop |
| [`0.0.0-develop.29`](#v-0-0-0-develop-29) | 2026-07-28 | develop |
| [`0.0.0-develop.27`](#v-0-0-0-develop-27) | 2026-07-23 | develop |

# Develop builds

<a id="v-0-0-0-develop-32"></a>

## master-data-service — develop 0.0.0-develop.32 (2026-07-30)

_commit `576ffe0` · changes since 0.0.0-develop.31_
<!-- build:0.0.0-develop.32 revision:576ffe074d1f8b6ed15f7e795fb862e2cc5a99de ts:1785382386 -->

### Changes since 0.0.0-develop.31

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Default geoSeed to the fictitious Kamuntu pack (XKM) so a fresh install never puts invented figures against a real country, with real packs one value away. Point packRoot at openg2p-data/packs after the reorg, prefer the pack manifest's explicit `version`, and log licence/synthetic provenance at seed time. ([`576ffe0`](https://gitlab.com/openg2p/master-data-service/-/commit/576ffe074d1f8b6ed15f7e795fb862e2cc5a99de))

<a id="v-0-0-0-develop-31"></a>

## master-data-service — develop 0.0.0-develop.31 (2026-07-29)

_commit `5474754` · changes since 0.0.0-develop.30_
<!-- build:0.0.0-develop.31 revision:5474754ff138a7924a63bc9e2dd2b933d027a22f ts:1785290640 -->

### Changes since 0.0.0-develop.30

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Build the geo db-seed image in CI and publish to the GitLab registry. ([`5474754`](https://gitlab.com/openg2p/master-data-service/-/commit/5474754ff138a7924a63bc9e2dd2b933d027a22f))

<a id="v-0-0-0-develop-30"></a>

## master-data-service — develop 0.0.0-develop.30 (2026-07-28)

_commit `05620b1` · changes since 0.0.0-develop.29_
<!-- build:0.0.0-develop.30 revision:05620b125edef8fede35e77f6f21063c5fd2bc4e ts:1785239243 -->

### Changes since 0.0.0-develop.29

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add db-seed image for country-pack geo seeding. ([`05620b1`](https://gitlab.com/openg2p/master-data-service/-/commit/05620b125edef8fede35e77f6f21063c5fd2bc4e))

<a id="v-0-0-0-develop-29"></a>

## master-data-service — develop 0.0.0-develop.29 (2026-07-28)

_commit `2369c61` · changes since 0.0.0-develop.27_
<!-- build:0.0.0-develop.29 revision:2369c615e71280ea67dcbefc7788979a3ffd0cb2 ts:1785237680 -->

### Summary

- New feature: introduced geoSeed job for seeding MDS geography using country packs, enhancing data management capabilities. 
- Enhancements to MDS chart: added country-pack selection functionality to improve user experience and data accuracy.

### Changes since 0.0.0-develop.27

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add geoSeed job and country-pack selection to the MDS chart. ([`2369c61`](https://gitlab.com/openg2p/master-data-service/-/commit/2369c615e71280ea67dcbefc7788979a3ffd0cb2))
- Seed MDS geography from a country pack. ([`83d4e0a`](https://gitlab.com/openg2p/master-data-service/-/commit/83d4e0af3a615b230792b4149191dd82dc807f2d))

<a id="v-0-0-0-develop-27"></a>

## master-data-service — develop 0.0.0-develop.27 (2026-07-23)

_commit `851d8ba` · baseline: release the start_
<!-- build:0.0.0-develop.27 revision:851d8bac29719d5d2de80867a6a566a40d17d529 ts:1784795007 -->

### Summary

_All changes since release the start:_

- **Major:** Migration of geo hierarchy with pcode, boundary references, localised labels, and effective-dating, including SQL for existing deployments.
- CI/CD overhaul: Transitioned to GitLab CI, removing GitHub Actions, and implemented new CI configurations.
- API stability improvements: Resolved boot crashes by migrating to iam-core 1.3 and sourcing keycloak_client_id from iam-core auth config.
- Database enhancements: Integrated registry database with master-data API, added new API endpoint for geo levels, and refactored geo data loading for improved idempotency and uniqueness.
- Cleanup: Removed db-seed Dockerfile and related Kubernetes configurations, and fixed pre-commit errors across the repository.

### Since last release (the start)

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Added pcode, boundary references, localised labels and effective-dating to the geo hierarchy, with migration SQL for existing deployments. ([`851d8ba`](https://gitlab.com/openg2p/master-data-service/-/commit/851d8bac29719d5d2de80867a6a566a40d17d529))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`6daf634`](https://gitlab.com/openg2p/master-data-service/-/commit/6daf634a199e62ecf99338f1e024b1f71474f026))
- [G2P-5341](https://openg2p.atlassian.net/browse/G2P-5341) Fix master-data-api boot crash: source keycloak_client_id from iam-core auth config ([`815addd`](https://gitlab.com/openg2p/master-data-service/-/commit/815addd771c33c9821b793076a77e77a17a80e8f))
- [G2P-5341](https://openg2p.atlassian.net/browse/G2P-5341): Clean up registry DB and data policy codechanges in data policy handling. ([`2253343`](https://gitlab.com/openg2p/master-data-service/-/commit/225334332fbdeffbc3a45243e6f8c56177f4508e))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`54307f3`](https://gitlab.com/openg2p/master-data-service/-/commit/54307f32726d73c3bd1d0f0995ebe4c4b89e3038))
- Fix API boot crash: migrate to iam-core 1.3 auth API; use fastapi-common develop ([`81e48ae`](https://gitlab.com/openg2p/master-data-service/-/commit/81e48ae613337c5368bd11eaccc44dfb3400382a))
- Fix for pre-commit error. ([`ead069c`](https://gitlab.com/openg2p/master-data-service/-/commit/ead069c724d157407402408a27eb28915a9e0f1a))
- 0.0.0-develop.N versioning implemented. Postgres init helm fixed. ([`48a5039`](https://gitlab.com/openg2p/master-data-service/-/commit/48a5039f389038749d3d024fe608a6d8edc3e3ab))
- pre-commit fix ([`c3c4d0b`](https://gitlab.com/openg2p/master-data-service/-/commit/c3c4d0b230f1dd8714771b466c09cb7182043f1f))
- [G2P-5268](https://openg2p.atlassian.net/browse/G2P-5268): Enhance master-data API with registry database integration and IAM support ([`192f442`](https://gitlab.com/openg2p/master-data-service/-/commit/192f44229deb652fbdf34f7e21f44b360feb95a3))
- [G2P-5264](https://openg2p.atlassian.net/browse/G2P-5264): Add get_all_g2p_geo_levels API endpoint and response handling ([`2dbea0e`](https://gitlab.com/openg2p/master-data-service/-/commit/2dbea0e341ad2bd58c0c3d7d24f4d4aab07fc6dd))
- Remove db-seed Dockerfile, entrypoint script, and related Kubernetes job configuration from the repository. ([`9533157`](https://gitlab.com/openg2p/master-data-service/-/commit/9533157fe193a4b382410ffcc5ae99e5df793365))
- Refactor geo data loading to use a single denormalized CSV. Update logic to derive hierarchy and path IDs for geo levels and values. Adjusted database insertion methods for idempotency and clarified uniqueness constraints in the model. ([`0995a76`](https://gitlab.com/openg2p/master-data-service/-/commit/0995a769d0e8e0890635c508cc2b1ac7bbd6d87b))
- Fix docker issue ([`8b478f6`](https://gitlab.com/openg2p/master-data-service/-/commit/8b478f66ea306c738d305859bc8bcd1fd0883a0c))
- Remove unique constraint ([`ccdfff4`](https://gitlab.com/openg2p/master-data-service/-/commit/ccdfff41e5260f71220cac4c2350f3702581a3b4))
- [G2P-4934](https://openg2p.atlassian.net/browse/G2P-4934) - master-data seeding + docker ([`b464953`](https://gitlab.com/openg2p/master-data-service/-/commit/b46495387e48070d947ca2565ed5baa2c5f8e1b1))
- [G2P-5144](https://openg2p.atlassian.net/browse/G2P-5144) Pre-commit errors fixed. ([`2ac3823`](https://gitlab.com/openg2p/master-data-service/-/commit/2ac3823aeb99baa0c6d91360058109992d8fc8ff))
- [G2P-5144](https://openg2p.atlassian.net/browse/G2P-5144) Consolidated all repos. Initial version. ([`c65eddc`](https://gitlab.com/openg2p/master-data-service/-/commit/c65eddc91987bb69c5a51093f9ab93b12b264aa4))
- Initial commit ([`4fa6336`](https://gitlab.com/openg2p/master-data-service/-/commit/4fa63366263b94176bd2c4de25c10f079fb63eec))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 10 develop builds** and the **latest 10 release
> candidates** per release line. Older develop builds and release candidates
> are pruned as they are superseded, and a release's candidates are removed
> once it ships. Those versions still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
