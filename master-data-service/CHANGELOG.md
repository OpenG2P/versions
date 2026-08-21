# master-data-service

_Published automatically._

**Repository:** [gitlab.com/openg2p/master-data-service](https://gitlab.com/openg2p/master-data-service) · **Container images:** [Container Registry](https://gitlab.com/openg2p/master-data-service/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.47`](#v-0-0-0-develop-47) | 2026-08-21 | develop |
| [`1.1.0-rc.55`](#v-1-1-0-rc-55) | 2026-08-21 | release candidate |
| [`0.0.0-develop.46`](#v-0-0-0-develop-46) | 2026-08-21 | develop |
| [`1.1.0-rc.51`](#v-1-1-0-rc-51) | 2026-08-20 | release candidate |
| [`1.1.0-rc.49`](#v-1-1-0-rc-49) | 2026-08-20 | release candidate |
| [`0.0.0-develop.40`](#v-0-0-0-develop-40) | 2026-08-03 | develop |
| [`0.0.0-develop.39`](#v-0-0-0-develop-39) | 2026-08-03 | develop |
| [`0.0.0-develop.38`](#v-0-0-0-develop-38) | 2026-08-02 | develop |
| [`0.0.0-develop.37`](#v-0-0-0-develop-37) | 2026-08-01 | develop |
| [`0.0.0-develop.36`](#v-0-0-0-develop-36) | 2026-08-01 | develop |
| [`0.0.0-develop.35`](#v-0-0-0-develop-35) | 2026-08-01 | develop |
| [`0.0.0-develop.34`](#v-0-0-0-develop-34) | 2026-08-01 | develop |
| [`0.0.0-develop.32`](#v-0-0-0-develop-32) | 2026-07-30 | develop |
| [`0.0.0-develop.31`](#v-0-0-0-develop-31) | 2026-07-29 | develop |
| [`0.0.0-develop.30`](#v-0-0-0-develop-30) | 2026-07-28 | develop |

# Release candidates

<a id="v-1-1-0-rc-55"></a>

## master-data-service 1.1.0-rc.55 — 2026-08-21

_commit `3a65680` · changes since 1.1.0-rc.51_
<!-- build:1.1.0-rc.55 revision:3a65680ca0a709da57a9fad44959b7fb83d59a46 ts:1787301498 -->

**Chart:** [openg2p-master-data 1.1.0-rc.55](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-1.1.0-rc.55.tgz)

### Summary

- Dependency updates: Updated IAM service reference from GitHub to GitLab and pinned to version 1.4, along with changes to dependency manifests in `package-lock.json` and `package.json`.
- Docker configuration: Minor adjustments made to Docker setup, reflecting changes in dependencies.

### Changes

- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`446b691`](https://gitlab.com/openg2p/master-data-service/-/commit/446b69150b93586b240be875353126203426f2b8))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update version numbers and pin IAM service reference to 1.4 ([`5efbd59`](https://gitlab.com/openg2p/master-data-service/-/commit/5efbd59651052e0e20f025268f248f3ed2842464))

<a id="v-1-1-0-rc-51"></a>

## master-data-service 1.1.0-rc.51 — 2026-08-20

_commit `f6ce705` · changes since 1.1.0-rc.49_
<!-- build:1.1.0-rc.51 revision:f6ce705bfb39e2d9a6de740caf63f3a1c51fe7ad ts:1787222768 -->

**Chart:** [openg2p-master-data 1.1.0-rc.51](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-1.1.0-rc.51.tgz)

### Changes

- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add configuration for Master Data UI deployment ([`86144ee`](https://gitlab.com/openg2p/master-data-service/-/commit/86144ee891938e0d97537e471e0aa00536345320))

<a id="v-1-1-0-rc-49"></a>

## master-data-service 1.1.0-rc.49 — 2026-08-20

_commit `03ffe82` · changes since 0.0.0-develop.40_
<!-- build:1.1.0-rc.49 revision:03ffe82c443c21e26f3f84ec93902118894a2b48 ts:1787222174 -->

**Chart:** [openg2p-master-data 1.1.0-rc.49](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-1.1.0-rc.49.tgz)

### Summary

- **Major:** Initialization of the master-data-ui project with Next.js setup, enabling modern web development practices.
- Feature enhancements: Added geo locations and reference data management, improved geo management with new dialogs and localization updates, and introduced attribute and geo level management with data policy support.
- Data management improvements: Updated SQL codelists to handle conflicts and added initial seed data for G2P attributes and values, enhancing overall data integrity and usability.
- Docker configuration enhancements to streamline development and deployment processes.

### Changes

- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Update SQL codelists to handle conflicts and enhance Docker configurations ([`968c6fb`](https://gitlab.com/openg2p/master-data-service/-/commit/968c6fb2693c947b7764baa9f1887b2d2461ef0e))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Add initial seed data for G2P attributes and values ([`a10123b`](https://gitlab.com/openg2p/master-data-service/-/commit/a10123ba53ecf75d4cc2e8663b19d217851fd135))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`67c4be5`](https://gitlab.com/openg2p/master-data-service/-/commit/67c4be52fe8bee62f65899917dea73d83a83a19c))
- [G2P-5458](https://openg2p.atlassian.net/browse/G2P-5458) feat: add attribute and geo level management ([`6bad7a4`](https://gitlab.com/openg2p/master-data-service/-/commit/6bad7a4ce930de29f4da8e416f224f896d23ef89))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat: enhance geo management with new dialogs and localization updates ([`1e95c1a`](https://gitlab.com/openg2p/master-data-service/-/commit/1e95c1a9b16943ea1e1b31fd20e97d0b6bfb9664))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add geo locations and reference data management ([`275bf51`](https://gitlab.com/openg2p/master-data-service/-/commit/275bf51a08c07871b47f4a4e2f804a68ab9d4406))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456): initialize master-data-ui project with Next.js setup ([`876a1f4`](https://gitlab.com/openg2p/master-data-service/-/commit/876a1f434b8ef207f39b826002b6dbcb47623baa))

# Develop builds

<a id="v-0-0-0-develop-47"></a>

## master-data-service — develop 0.0.0-develop.47 (2026-08-21)

_commit `fe9ce25` · changes since 0.0.0-develop.46_
<!-- build:0.0.0-develop.47 revision:fe9ce25ea14949d869a2e81723bc86aa8b193248 ts:1787307348 -->

**Chart:** [openg2p-master-data 0.0.0-develop.47](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-0.0.0-develop.47.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise national IDs when loading a country pack ([`fe9ce25`](https://gitlab.com/openg2p/master-data-service/-/commit/fe9ce25ea14949d869a2e81723bc86aa8b193248))

<a id="v-0-0-0-develop-46"></a>

## master-data-service — develop 0.0.0-develop.46 (2026-08-21)

_commit `4f29f7a` · changes since 0.0.0-develop.40_
<!-- build:0.0.0-develop.46 revision:4f29f7af99ef270f51386a709ff4032ae474aeab ts:1787276348 -->

**Chart:** [openg2p-master-data 0.0.0-develop.46](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-0.0.0-develop.46.tgz)

### Summary

- **Major:** New master-data-ui project initialized with Next.js, including essential configuration files and localization support.
- Feature enhancements: Added geo management capabilities with new dialogs, reference data management, and attribute/geo level management.
- Database schema update: Introduced `birth_date` column to the sample individuals table, with a seed job to handle pre-existing environments.
- Dependency updates: Updated package manifests for master-data-ui, reflecting new dependencies and configurations.

### Changes

- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Carry the pack's birth_date through to the sample individuals table. The API builds these tables with create_all, which never adds a column to an existing one, so the seed job adds the column itself before inserting rather than failing on an environment seeded before this field existed. ([`4f29f7a`](https://gitlab.com/openg2p/master-data-service/-/commit/4f29f7af99ef270f51386a709ff4032ae474aeab))
- [G2P-5458](https://openg2p.atlassian.net/browse/G2P-5458) feat: add attribute and geo level management ([`6bad7a4`](https://gitlab.com/openg2p/master-data-service/-/commit/6bad7a4ce930de29f4da8e416f224f896d23ef89))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat: enhance geo management with new dialogs and localization updates ([`1e95c1a`](https://gitlab.com/openg2p/master-data-service/-/commit/1e95c1a9b16943ea1e1b31fd20e97d0b6bfb9664))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add geo locations and reference data management ([`275bf51`](https://gitlab.com/openg2p/master-data-service/-/commit/275bf51a08c07871b47f4a4e2f804a68ab9d4406))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456): initialize master-data-ui project with Next.js setup ([`876a1f4`](https://gitlab.com/openg2p/master-data-service/-/commit/876a1f434b8ef207f39b826002b6dbcb47623baa))

<a id="v-0-0-0-develop-40"></a>

## master-data-service — develop 0.0.0-develop.40 (2026-08-03)

_commit `a31a52b` · changes since 0.0.0-develop.39_
<!-- build:0.0.0-develop.40 revision:a31a52beab36324e77efd5dd96c74fc89c1f6c06 ts:1785722945 -->

### Changes since 0.0.0-develop.39

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Wait on the last table the migration creates, not the first. g2p_geo_levels is created before g2p_attributes and the sample tables, so gating on it proved only that the migration had started — wide enough for the loader to finish geo and then die on g2p_sample_households, which is the failure the guard exists to prevent. Waiting on g2p_sample_households proves the whole migration finished, since the creates are sequential and awaited. Also bounds the pg_isready loop, which could otherwise hang the init container indefinitely against an unreachable database. ([`a31a52b`](https://gitlab.com/openg2p/master-data-service/-/commit/a31a52beab36324e77efd5dd96c74fc89c1f6c06))

<a id="v-0-0-0-develop-39"></a>

## master-data-service — develop 0.0.0-develop.39 (2026-08-03)

_commit `2476e12` · changes since 0.0.0-develop.38_
<!-- build:0.0.0-develop.39 revision:2476e12ba8ec64d515c5a35178661fc990be43b5 ts:1785720916 -->

### Changes since 0.0.0-develop.38

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Keep XKM as the chart default, and seed the whole pack rather than geography alone. Geography by itself leaves registries on their extension's own code lists, with no semantic role tags at all and no sample people — not a working default for anything downstream. The country itself stays a deployment decision: an install nobody configured must not attach invented figures to a real country's name or pick up a licence obligation by accident. ([`2476e12`](https://gitlab.com/openg2p/master-data-service/-/commit/2476e12ba8ec64d515c5a35178661fc990be43b5))

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

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
