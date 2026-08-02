# master-data-service

_Published automatically._

**Repository:** [gitlab.com/openg2p/master-data-service](https://gitlab.com/openg2p/master-data-service) · **Container images:** [Container Registry](https://gitlab.com/openg2p/master-data-service/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.38`](#v-0-0-0-develop-38) | 2026-08-02 | develop |
| [`0.0.0-develop.37`](#v-0-0-0-develop-37) | 2026-08-01 | develop |
| [`0.0.0-develop.36`](#v-0-0-0-develop-36) | 2026-08-01 | develop |
| [`0.0.0-develop.35`](#v-0-0-0-develop-35) | 2026-08-01 | develop |
| [`0.0.0-develop.34`](#v-0-0-0-develop-34) | 2026-08-01 | develop |
| [`0.0.0-develop.32`](#v-0-0-0-develop-32) | 2026-07-30 | develop |
| [`0.0.0-develop.31`](#v-0-0-0-develop-31) | 2026-07-29 | develop |
| [`0.0.0-develop.30`](#v-0-0-0-develop-30) | 2026-07-28 | develop |
| [`0.0.0-develop.29`](#v-0-0-0-develop-29) | 2026-07-28 | develop |
| [`0.0.0-develop.27`](#v-0-0-0-develop-27) | 2026-07-23 | develop |

# Develop builds

<a id="v-0-0-0-develop-38"></a>

## master-data-service — develop 0.0.0-develop.38 (2026-08-02)

_commit `e319189` · changes since 0.0.0-develop.37_
<!-- build:0.0.0-develop.38 revision:e319189f19fab97a0855c3e2165f9e78ccff4efb ts:1785674332 -->

### Changes since 0.0.0-develop.37

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Surface the country pack in questions.yaml. None of the geo-seed options were in the Rancher form, so the one place a deployment declares its country was reachable only by hand-editing values — an installer had no way to know the choice existed, and every install silently took the fictitious default. ([`e319189`](https://gitlab.com/openg2p/master-data-service/-/commit/e319189f19fab97a0855c3e2165f9e78ccff4efb))

<a id="v-0-0-0-develop-37"></a>

## master-data-service — develop 0.0.0-develop.37 (2026-08-01)

_commit `83bfaee` · changes since 0.0.0-develop.36_
<!-- build:0.0.0-develop.37 revision:83bfaee9ae49249adb12589b0da1a290bf02f9fa ts:1785578161 -->

### Changes since 0.0.0-develop.36

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Lowercase the geo-seed Job name. This template renders at the chart root, where .Chart.Name is the vendored subchart name — the commons-services umbrella carries it as `masterData`, so the Job came out as commons-services-masterData-geo-seed, which Kubernetes rejects. The hook failed, no geography or code lists were seeded, and the whole commons-services release went to `failed`. The API templates were unaffected because they render against a scoped context whose nameOverride is already lowercase. ([`83bfaee`](https://gitlab.com/openg2p/master-data-service/-/commit/83bfaee9ae49249adb12589b0da1a290bf02f9fa))

<a id="v-0-0-0-develop-36"></a>

## master-data-service — develop 0.0.0-develop.36 (2026-08-01)

_commit `ebb8bb5` · changes since 0.0.0-develop.35_
<!-- build:0.0.0-develop.36 revision:ebb8bb50042d370fd70970a7a82be987b862d508 ts:1785558178 -->

### Changes since 0.0.0-develop.35

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add an Ethiopia overlay for the master-data chart. Kept separate from values.yaml so the chart keeps defaulting to the fictitious Kamuntu pack: an install nobody configured must not attach invented figures to a real country's name, and turning codelists and samples on by default would change what an existing deployment gets on upgrade. ([`ebb8bb5`](https://gitlab.com/openg2p/master-data-service/-/commit/ebb8bb50042d370fd70970a7a82be987b862d508))

<a id="v-0-0-0-develop-35"></a>

## master-data-service — develop 0.0.0-develop.35 (2026-08-01)

_commit `3b681c3` · changes since 0.0.0-develop.34_
<!-- build:0.0.0-develop.35 revision:3b681c3e560b1140f53937ffecd9afb1c8bb797e ts:1785557574 -->

### Changes since 0.0.0-develop.34

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Implement --load samples, and stop geo lookups failing silently. The loader advertised a samples section that nothing implemented; sample people now live beside the geography they reference, in the one place the country is declared. get_g2p_geo_level_values also accepts a level's name, not just its lN id, and no longer filters a non-root level on "parent is null" — which matches nothing once the country is itself a level, so a form's first dropdown came back empty and an empty dropdown reads as a country with no regions. ([`3b681c3`](https://gitlab.com/openg2p/master-data-service/-/commit/3b681c3e560b1140f53937ffecd9afb1c8bb797e))

<a id="v-0-0-0-develop-34"></a>

## master-data-service — develop 0.0.0-develop.34 (2026-08-01)

_commit `be4c622` · changes since 0.0.0-develop.32_
<!-- build:0.0.0-develop.34 revision:be4c6225d780928c0436aef94ca674afb08dbdca ts:1785548354 -->

### Summary

- New feature: Introduced country-pack code lists served over the `/attributes` endpoint, with a new router and tables created conditionally based on deployment configuration.
- Data handling: Implemented an opt-in switch for loading country-pack code lists into the Master Data Service (MDS), maintaining existing behavior for upgrades while allowing environment-specific configurations.
- Unauthenticated access: Endpoints for country-pack code lists are accessible without user authentication, designed for registry install-time seeds.
- Domain exclusions: Default behavior excludes domain lists from social registries, ensuring irrelevant data is not loaded.

### Changes since 0.0.0-develop.32

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Serve country-pack code lists over /attributes. Additive: new router, new tables, and no existing route changes shape. Tables are created unconditionally but stay empty unless the seed Job was told to load code lists, so the endpoints answer "this country defines no such list" rather than erroring on a deployment that has not opted in. Unauthenticated like the geo hierarchy routes, since the caller is a registry install-time seed with no user token. Domain lists are excluded by default — a social registry has no use for crop types. ([`be4c622`](https://gitlab.com/openg2p/master-data-service/-/commit/be4c6225d780928c0436aef94ca674afb08dbdca))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Load country-pack code lists into MDS behind an opt-in switch. --load defaults to "geo", so an existing deployment upgrading sees byte-for-byte today's behaviour; codelists and domain subtrees are enabled per environment. Values carry their semantic roles. Uses a composite (attribute_id, value_id) key because value_id is not globally unique — OTHER appears in 13 of Ethiopia's lists, which is why Farmer prefixes every value and NSR does not. ([`bd89c01`](https://gitlab.com/openg2p/master-data-service/-/commit/bd89c01539238bc37ac427c94bef3f02f26e419f))

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
