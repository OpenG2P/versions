# platform-services/master-data-service

_Published automatically._

**Repository:** [gitlab.com/openg2p/platform-services/master-data-service](https://gitlab.com/openg2p/platform-services/master-data-service) · **Container images:** [Container Registry](https://gitlab.com/openg2p/platform-services/master-data-service/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.62`](#v-0-0-0-develop-62) | 2026-08-26 | develop |
| [`0.0.0-develop.60`](#v-0-0-0-develop-60) | 2026-08-24 | develop |

# Develop builds

<a id="v-0-0-0-develop-62"></a>

## platform-services/master-data-service — develop 0.0.0-develop.62 (2026-08-26)

_commit `b423005` · changes since 0.0.0-develop.60_
<!-- build:0.0.0-develop.62 revision:b42300512c21c72c41d0b71421003b5d7c3798aa ts:1787719268 -->

**Chart:** [openg2p-master-data 0.0.0-develop.62](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-0.0.0-develop.62.tgz)

### Summary

- Data management enhancement: improved geo level value management with data policy support.
- Code quality: applied pre-commit formatting across the repository, including black line-length reflow and whitespace corrections.

### Changes

- Apply pre-commit formatting across the repo (black line-length reflow in master-data-api, trailing whitespace in codelist SQL seeds, missing final newlines in UI files, README and .gitignore); formatting only, no functional change ([`b423005`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/b42300512c21c72c41d0b71421003b5d7c3798aa))
- 67c4be5  [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`16a0d36`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/16a0d36d8480be8f5e64f8ab33b08ab0459f0795))

<a id="v-0-0-0-develop-60"></a>

## platform-services/master-data-service — develop 0.0.0-develop.60 (2026-08-24)

_commit `179581b` · changes since the start_
<!-- build:0.0.0-develop.60 revision:179581b5a781d7afd23b09885f53de2df95abd8f ts:1787594551 -->

**Chart:** [openg2p-master-data 0.0.0-develop.60](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-master-data-0.0.0-develop.60.tgz)

### Summary

- **Major:** Migration to GitLab CI, dropping GitHub Actions; includes new CI configurations and builds for geo db-seed images.
- API enhancements: Added `get_all_g2p_geo_levels` endpoint, improved registry database integration, and IAM support; fixed boot crash by migrating to iam-core 1.3.
- Data management improvements: Normalized national IDs, enhanced geo level value management with data policy support, and added initial seed data for G2P attributes.
- Master Data UI updates: Introduced configuration for deployment, added geo locations and reference data management, and initialized the project with Next.js setup.
- Docker and deployment fixes: Resolved clashing pod selectors, improved Docker configurations, and fixed issues with database seeding and initialization.
- Codebase cleanup: Removed unused db-seed Dockerfile and Kubernetes job configurations; consolidated repositories and fixed pre-commit errors.

### Changes

- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on master-data-service ([`179581b`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/179581b5a781d7afd23b09885f53de2df95abd8f))
- Fix for clashing pod selector. ([`4de586a`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/4de586a941563743442d88e0892d57b7da15a089))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise national IDs when loading a country pack ([`fe9ce25`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/fe9ce25ea14949d869a2e81723bc86aa8b193248))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`446b691`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/446b69150b93586b240be875353126203426f2b8))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update version numbers and pin IAM service reference to 1.4 ([`5efbd59`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/5efbd59651052e0e20f025268f248f3ed2842464))
- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Carry the pack's birth_date through to the sample individuals table. The API builds these tables with create_all, which never adds a column to an existing one, so the seed job adds the column itself before inserting rather than failing on an environment seeded before this field existed. ([`4f29f7a`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/4f29f7af99ef270f51386a709ff4032ae474aeab))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add configuration for Master Data UI deployment ([`86144ee`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/86144ee891938e0d97537e471e0aa00536345320))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Update SQL codelists to handle conflicts and enhance Docker configurations ([`968c6fb`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/968c6fb2693c947b7764baa9f1887b2d2461ef0e))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Add initial seed data for G2P attributes and values ([`a10123b`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/a10123ba53ecf75d4cc2e8663b19d217851fd135))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`67c4be5`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/67c4be52fe8bee62f65899917dea73d83a83a19c))
- [G2P-5458](https://openg2p.atlassian.net/browse/G2P-5458) feat: add attribute and geo level management ([`6bad7a4`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/6bad7a4ce930de29f4da8e416f224f896d23ef89))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat: enhance geo management with new dialogs and localization updates ([`1e95c1a`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/1e95c1a9b16943ea1e1b31fd20e97d0b6bfb9664))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add geo locations and reference data management ([`275bf51`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/275bf51a08c07871b47f4a4e2f804a68ab9d4406))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456): initialize master-data-ui project with Next.js setup ([`876a1f4`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/876a1f434b8ef207f39b826002b6dbcb47623baa))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Wait on the last table the migration creates, not the first. g2p_geo_levels is created before g2p_attributes and the sample tables, so gating on it proved only that the migration had started — wide enough for the loader to finish geo and then die on g2p_sample_households, which is the failure the guard exists to prevent. Waiting on g2p_sample_households proves the whole migration finished, since the creates are sequential and awaited. Also bounds the pg_isready loop, which could otherwise hang the init container indefinitely against an unreachable database. ([`a31a52b`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/a31a52beab36324e77efd5dd96c74fc89c1f6c06))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Keep XKM as the chart default, and seed the whole pack rather than geography alone. Geography by itself leaves registries on their extension's own code lists, with no semantic role tags at all and no sample people — not a working default for anything downstream. The country itself stays a deployment decision: an install nobody configured must not attach invented figures to a real country's name or pick up a licence obligation by accident. ([`2476e12`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/2476e12ba8ec64d515c5a35178661fc990be43b5))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Surface the country pack in questions.yaml. None of the geo-seed options were in the Rancher form, so the one place a deployment declares its country was reachable only by hand-editing values — an installer had no way to know the choice existed, and every install silently took the fictitious default. ([`e319189`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/e319189f19fab97a0855c3e2165f9e78ccff4efb))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Lowercase the geo-seed Job name. This template renders at the chart root, where .Chart.Name is the vendored subchart name — the commons-services umbrella carries it as `masterData`, so the Job came out as commons-services-masterData-geo-seed, which Kubernetes rejects. The hook failed, no geography or code lists were seeded, and the whole commons-services release went to `failed`. The API templates were unaffected because they render against a scoped context whose nameOverride is already lowercase. ([`83bfaee`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/83bfaee9ae49249adb12589b0da1a290bf02f9fa))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add an Ethiopia overlay for the master-data chart. Kept separate from values.yaml so the chart keeps defaulting to the fictitious Kamuntu pack: an install nobody configured must not attach invented figures to a real country's name, and turning codelists and samples on by default would change what an existing deployment gets on upgrade. ([`ebb8bb5`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/ebb8bb50042d370fd70970a7a82be987b862d508))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Implement --load samples, and stop geo lookups failing silently. The loader advertised a samples section that nothing implemented; sample people now live beside the geography they reference, in the one place the country is declared. get_g2p_geo_level_values also accepts a level's name, not just its lN id, and no longer filters a non-root level on "parent is null" — which matches nothing once the country is itself a level, so a form's first dropdown came back empty and an empty dropdown reads as a country with no regions. ([`3b681c3`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/3b681c3e560b1140f53937ffecd9afb1c8bb797e))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Serve country-pack code lists over /attributes. Additive: new router, new tables, and no existing route changes shape. Tables are created unconditionally but stay empty unless the seed Job was told to load code lists, so the endpoints answer "this country defines no such list" rather than erroring on a deployment that has not opted in. Unauthenticated like the geo hierarchy routes, since the caller is a registry install-time seed with no user token. Domain lists are excluded by default — a social registry has no use for crop types. ([`be4c622`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/be4c6225d780928c0436aef94ca674afb08dbdca))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Load country-pack code lists into MDS behind an opt-in switch. --load defaults to "geo", so an existing deployment upgrading sees byte-for-byte today's behaviour; codelists and domain subtrees are enabled per environment. Values carry their semantic roles. Uses a composite (attribute_id, value_id) key because value_id is not globally unique — OTHER appears in 13 of Ethiopia's lists, which is why Farmer prefixes every value and NSR does not. ([`bd89c01`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/bd89c01539238bc37ac427c94bef3f02f26e419f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Default geoSeed to the fictitious Kamuntu pack (XKM) so a fresh install never puts invented figures against a real country, with real packs one value away. Point packRoot at openg2p-data/packs after the reorg, prefer the pack manifest's explicit `version`, and log licence/synthetic provenance at seed time. ([`576ffe0`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/576ffe074d1f8b6ed15f7e795fb862e2cc5a99de))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Build the geo db-seed image in CI and publish to the GitLab registry. ([`5474754`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/5474754ff138a7924a63bc9e2dd2b933d027a22f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add db-seed image for country-pack geo seeding. ([`05620b1`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/05620b125edef8fede35e77f6f21063c5fd2bc4e))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add geoSeed job and country-pack selection to the MDS chart. ([`2369c61`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/2369c615e71280ea67dcbefc7788979a3ffd0cb2))
- Seed MDS geography from a country pack. ([`83d4e0a`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/83d4e0af3a615b230792b4149191dd82dc807f2d))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Added pcode, boundary references, localised labels and effective-dating to the geo hierarchy, with migration SQL for existing deployments. ([`851d8ba`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/851d8bac29719d5d2de80867a6a566a40d17d529))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`6daf634`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/6daf634a199e62ecf99338f1e024b1f71474f026))
- [G2P-5341](https://openg2p.atlassian.net/browse/G2P-5341) Fix master-data-api boot crash: source keycloak_client_id from iam-core auth config ([`815addd`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/815addd771c33c9821b793076a77e77a17a80e8f))
- [G2P-5341](https://openg2p.atlassian.net/browse/G2P-5341): Clean up registry DB and data policy codechanges in data policy handling. ([`2253343`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/225334332fbdeffbc3a45243e6f8c56177f4508e))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`54307f3`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/54307f32726d73c3bd1d0f0995ebe4c4b89e3038))
- Fix API boot crash: migrate to iam-core 1.3 auth API; use fastapi-common develop ([`81e48ae`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/81e48ae613337c5368bd11eaccc44dfb3400382a))
- Fix for pre-commit error. ([`ead069c`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/ead069c724d157407402408a27eb28915a9e0f1a))
- 0.0.0-develop.N versioning implemented. Postgres init helm fixed. ([`48a5039`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/48a5039f389038749d3d024fe608a6d8edc3e3ab))
- pre-commit fix ([`c3c4d0b`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/c3c4d0b230f1dd8714771b466c09cb7182043f1f))
- [G2P-5268](https://openg2p.atlassian.net/browse/G2P-5268): Enhance master-data API with registry database integration and IAM support ([`192f442`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/192f44229deb652fbdf34f7e21f44b360feb95a3))
- [G2P-5264](https://openg2p.atlassian.net/browse/G2P-5264): Add get_all_g2p_geo_levels API endpoint and response handling ([`2dbea0e`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/2dbea0e341ad2bd58c0c3d7d24f4d4aab07fc6dd))
- Remove db-seed Dockerfile, entrypoint script, and related Kubernetes job configuration from the repository. ([`9533157`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/9533157fe193a4b382410ffcc5ae99e5df793365))
- Refactor geo data loading to use a single denormalized CSV. Update logic to derive hierarchy and path IDs for geo levels and values. Adjusted database insertion methods for idempotency and clarified uniqueness constraints in the model. ([`0995a76`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/0995a769d0e8e0890635c508cc2b1ac7bbd6d87b))
- Fix docker issue ([`8b478f6`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/8b478f66ea306c738d305859bc8bcd1fd0883a0c))
- Remove unique constraint ([`ccdfff4`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/ccdfff41e5260f71220cac4c2350f3702581a3b4))
- [G2P-4934](https://openg2p.atlassian.net/browse/G2P-4934) - master-data seeding + docker ([`b464953`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/b46495387e48070d947ca2565ed5baa2c5f8e1b1))
- [G2P-5144](https://openg2p.atlassian.net/browse/G2P-5144) Pre-commit errors fixed. ([`2ac3823`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/2ac3823aeb99baa0c6d91360058109992d8fc8ff))
- [G2P-5144](https://openg2p.atlassian.net/browse/G2P-5144) Consolidated all repos. Initial version. ([`c65eddc`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/c65eddc91987bb69c5a51093f9ab93b12b264aa4))
- Initial commit ([`4fa6336`](https://gitlab.com/openg2p/platform-services/master-data-service/-/commit/4fa63366263b94176bd2c4de25c10f079fb63eec))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
