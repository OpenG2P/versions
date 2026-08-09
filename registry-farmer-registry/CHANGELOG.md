# registry/farmer-registry

_Published automatically._

**Repository:** [gitlab.com/openg2p/registry/farmer-registry](https://gitlab.com/openg2p/registry/farmer-registry) · **Container images:** [Container Registry](https://gitlab.com/openg2p/registry/farmer-registry/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.159`](#v-0-0-0-develop-159) | 2026-08-09 | develop |
| [`0.0.0-develop.154`](#v-0-0-0-develop-154) | 2026-08-07 | develop |
| [`0.0.0-develop.153`](#v-0-0-0-develop-153) | 2026-08-06 | develop |
| [`1.3.0`](#v-1-3-0) | 2026-08-06 | release |
| [`1.3.0-rc.151`](#v-1-3-0-rc-151) | 2026-08-06 | release candidate |
| [`0.0.0-develop.151`](#v-0-0-0-develop-151) | 2026-08-06 | develop |
| [`0.0.0-develop.150`](#v-0-0-0-develop-150) | 2026-08-06 | develop |
| [`0.0.0-develop.148`](#v-0-0-0-develop-148) | 2026-08-06 | develop |
| [`0.0.0-develop.146`](#v-0-0-0-develop-146) | 2026-08-06 | develop |
| [`0.0.0-develop.145`](#v-0-0-0-develop-145) | 2026-08-06 | develop |
| [`0.0.0-develop.144`](#v-0-0-0-develop-144) | 2026-08-05 | develop |
| [`0.0.0-develop.142`](#v-0-0-0-develop-142) | 2026-08-04 | develop |
| [`0.0.0-develop.141`](#v-0-0-0-develop-141) | 2026-08-04 | develop |
| [`0.0.0-develop.140`](#v-0-0-0-develop-140) | 2026-08-04 | develop |

# Releases

<a id="v-1-3-0"></a>

## registry/farmer-registry 1.3.0 — 2026-08-06

<!-- build:1.3.0 revision:d39deba138813845cc34ea701b885ed763833836 ts:1786007784 -->

_commit `d39deba` · changes since release 1.2.0_

**Chart:** [openg2p-farmer-registry 1.3.0](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-1.3.0.tgz)

### Release notes

Intermediate stable version; several enhancements related to country packs, reading geo from MDS, bulk data generation, sample data generation, upload of dashboards in superset; compatible with commons 0.0.0-develop.198

### Summary

- **Major:** Database fixes: resolved bulk-sample ID collisions and policy key clashes to prevent data integrity issues during seeding and AWE operations.
- Analytics enhancements: introduced FR reporting views, a bulk sample generator, and a Superset bundle with multiple dashboards and charts; added maps content as a dedicated image for improved insights.
- CI/CD improvements: transitioned CI to GitLab, replacing GitHub Actions, and fixed values.yaml issues caused by the migration.
- Data management: enabled Master Data path, eliminated redundant geography seeding, and fixed geo dropdowns to ensure proper API integration.
- Code refactoring: removed unused async methods across various models to enhance maintainability and streamline the codebase.

### Changes

- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix bulk-sample id collisions: sub-table functional ids were uuid[:8], which collides by the birthday bound (100k farmers died at ~39k crops on ix_g2p_register_crops_functional_record_id) — use sequential counters like the farmer ids already do ([`d39deba`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/d39deba138813845cc34ea701b885ed763833836))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix AWE seed aborting on shared-DB policy_key clash: untargeted ON CONFLICT DO NOTHING (uq_policy_key_version was unguarded by the id-targeted clause) plus FK-orphan filters on stages/rules, so a policy another registry already owns no longer takes the whole batch — and the farmer policy — down with it ([`43afe27`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/43afe27ad81c2fedd13e22c35d1d1029c78882ae))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fall back to this registry's own Superset connection name when the release is gone. The name was only ever read from `helm get values`, so uninstalling from Rancher — or running helm uninstall first — skipped the dashboard cleanup with a quiet warning and left the dashboards, charts, datasets and connection in the shared Superset, where the next install adopted them by UUID. ([`a445d51`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/a445d51fc54913d9fd0127e138f3213d748b4410))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Skip the dashboard import when Superset is absent instead of failing the install. Superset is a separate release and analytics is optional, but the gate exited 1 after waiting, so a registry installed without a reporting stack failed outright. The gate is checked in the init container AND the main one, because an init container exiting 0 does not stop the pod; set analytics.dashboards.superset.required=true where a silent skip would be worse. ([`2e3a06a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/2e3a06a243dc3a44d8485622deae1b9f4d07aa25))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add the maps content and publish it as an image. Insights draws maps from a registry-specific image; without one, FR installs fell back to the reference content, which queries nsr_rpt_* and poverty measures FR does not have. Queries plot land tenure, input use and cooperative membership from fr_rpt_farmer/fr_rpt_crop, and are validated against a live FR database. ([`6aac6b7`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/6aac6b7b128d3ed896c70cae283af39cd25a49ac))
- Fixes in data seeding. ([`7af358a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/7af358afa6577cce069d120c54b7cc2f892e94fe))
- Bumped up RP version to 0.0.0-develop.346 ([`f19c12d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/f19c12dd57340798ff7de921c17ebb179eb4fc3a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) DB-seed: take ownership of load_sample_data.py and upload_images.py from the platform image ([`003ac5d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/003ac5de37ee21bb695b23bc492248c0b68d5f6a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Analytics: add FR reporting views, bulk sample generator, Superset bundle (5 dashboards/45 charts) and the analytics Jobs; declare the DB globals the wrapper's own templates need ([`932aa5a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/932aa5a4ddf7b9c9a0ebb4b30096ad67c22758df))
- [G2P-2804](https://openg2p.atlassian.net/browse/G2P-2804) Analytics: add FR reporting layer (fr_rpt_farmer, fr_rpt_land, fr_rpt_geo_levels) — area normalised to hectares, crops/livestock/inputs rolled off the land grain ([`30672a4`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/30672a410c1fc942b9bdd1e4b544ab337e507436))
- questions.yaml copied during CI ([`ae32039`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ae32039b18158b8ade948311e02681bc6442dadd))
- Bumped up RP version ([`5cae5e3`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/5cae5e38b01f7c598811f49f7451bd30d4ea50d1))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Chart: fix values.yaml clobbered by the CI migration (yq line offset; staffApi/partnerApi pointed at the wrong images); take registry-platform 0.0.0-develop.343 from the GitLab charts registry ([`c989a9d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/c989a9db99f52fb64fa871219abd7adde8222ea4))
- Data related changes. ([`d66f1a6`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/d66f1a697e05a5b78b9c6b9a4eddc72b727354be))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Enable the Master Data path and stop seeding a second geography. loadGeoData was still true, which runs the legacy slug-path loader over the hierarchy master-data already holds from its country pack — two hierarchies, one of which joins to nothing. Also enables loadAttributes with the agriculture domain, and syncGeoWidgets. ([`e2d45bc`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/e2d45bc2153058f54bd5a0f13f4ac49394827f15))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`1cc19d0`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/1cc19d0410a71c7c7d45ae5458d64519a1457c47))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix the two geo dropdowns. They carried a hardcoded dev-environment URL and no service/endpoint, so the widget layer bailed before making the request and the dropdowns never populated. Now resolved through master-data like every other api widget, with levels that match the default country pack. ([`79edff5`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/79edff5679c097d400c4ce645f28b383ceae32cc))
- [G2P-5412](https://openg2p.atlassian.net/browse/G2P-5412) Refactor: Remove unused async methods for linking internal record IDs in various models (crop, farm inputs, farmer, household member, land, livestock, membership details) to streamline code and improve maintainability. ([`c5ab693`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/c5ab69323dd7435a93ae3572213fd5dfdec6a71f))

# Release candidates

<a id="v-1-3-0-rc-151"></a>

## registry/farmer-registry 1.3.0-rc.151 — 2026-08-06

_commit `d39deba` · changes since 0.0.0-develop.151_
<!-- build:1.3.0-rc.151 revision:d39deba138813845cc34ea701b885ed763833836 ts:1786007784 -->

**Chart:** [openg2p-farmer-registry 1.3.0-rc.151](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-1.3.0-rc.151.tgz)

### Changes since 0.0.0-develop.151

_No new commits since 0.0.0-develop.151._

# Develop builds

<a id="v-0-0-0-develop-159"></a>

## registry/farmer-registry — develop 0.0.0-develop.159 (2026-08-09)

_commit `ec8828c` · changes since 0.0.0-develop.154_
<!-- build:0.0.0-develop.159 revision:ec8828c439ff33ac65bfb502bdb3bad5358c14d1 ts:1786242862 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.159](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.159.tgz)

### Summary

- **Major:** Enhanced data integrity: scores are now declared against both farmers and households, preventing data loss from naming conflicts.
- Reporting improvements: generated `fr_rpt_crop` from declarations, ensuring consistency with previous definitions while adding missing geo pcodes and workflow columns; introduced mechanical reporting views that expand the entity tree with additional data points.
- Policy alignment: defined household member age bands to match farmer reporting, resolving discrepancies in age data across charts.

### Changes since 0.0.0-develop.154

- Bumped up RP version to 0.0.0-develop.383 ([`ec8828c`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ec8828c439ff33ac65bfb502bdb3bad5358c14d1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare score against both farmer and household. A single install carries both — the bulk generator attaches scores to farmers and the sample loader to households, 5,671 and 6 on a reference install — so naming one parent silently stripped the id and the geography from every row of the other. ([`40556c9`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/40556c9a6b4ea4f0791f3a2e30a8fbaa428c85ef))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate fr_rpt_crop from declarations instead of hand-written SQL. Verified byte-identical to the previous definition across all seventeen shared columns and 757 rows before the SQL was removed; it keeps its materialization and indexes, and additionally carries the geo pcodes and workflow columns the hand-written version omitted. ([`699b3a2`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/699b3a283105c25a82b7c87608afb18a1d28a61f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare the household member age bands, matching fr_rpt_farmer's edges. The generator derives an age wherever it withholds a birth date, but where the bands fall is policy, and defining them twice with different edges is how two charts come to disagree about how many people are under 25. ([`6daa47a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/6daa47af0c0b0abd14b6b4b701db197ac6fd2839))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the mechanical reporting views from the platform generator. reporting.yaml declares the entity tree, names farmer/land/crop as hand-written and marks the cooperative name columns as organisations rather than people; the generated ten add livestock, inputs, membership, scores, households, members, change requests, record history and geo_levels, which used to be derived from registered rows and so was empty on a production install. ([`11e3b8b`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/11e3b8beb7368af5e1dbf8bb6810c6ef08238a18))

<a id="v-0-0-0-develop-154"></a>

## registry/farmer-registry — develop 0.0.0-develop.154 (2026-08-07)

_commit `8f93c33` · changes since 0.0.0-develop.153_
<!-- build:0.0.0-develop.154 revision:8f93c337cbc07bcef9de94f12633572297c92e9f ts:1786095224 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.154](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.154.tgz)

### Changes since 0.0.0-develop.153

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Refresh the reporting views on a schedule, instead of relying on Insights to do it. They are materialized, so they held whatever the install produced and every farmer registered afterwards was invisible with no error anywhere; a CronJob now rebuilds them in dependency order resolved from pg_depend, on analytics.reportingViews.refreshSchedule. ([`8f93c33`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/8f93c337cbc07bcef9de94f12633572297c92e9f))

<a id="v-0-0-0-develop-153"></a>

## registry/farmer-registry — develop 0.0.0-develop.153 (2026-08-06)

_commit `3d55dcd` · changes since 0.0.0-develop.151_
<!-- build:0.0.0-develop.153 revision:3d55dcdd76b52fe46426156eaf72e24f26a5888c ts:1786009141 -->

### Changes since 0.0.0-develop.151

- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) fix: correct ui configuration for multiple sections and add dedicated parent lookup sections for crop intake and crop register ([`2f172d4`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/2f172d4848fecc02c08f9c5a9e83edb76888ba53))

<a id="v-0-0-0-develop-151"></a>

## registry/farmer-registry — develop 0.0.0-develop.151 (2026-08-06)

_commit `d39deba` · changes since 0.0.0-develop.150_
<!-- build:0.0.0-develop.151 revision:d39deba138813845cc34ea701b885ed763833836 ts:1786007784 -->

### Changes since 0.0.0-develop.150

- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix bulk-sample id collisions: sub-table functional ids were uuid[:8], which collides by the birthday bound (100k farmers died at ~39k crops on ix_g2p_register_crops_functional_record_id) — use sequential counters like the farmer ids already do ([`d39deba`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/d39deba138813845cc34ea701b885ed763833836))

<a id="v-0-0-0-develop-150"></a>

## registry/farmer-registry — develop 0.0.0-develop.150 (2026-08-06)

_commit `43afe27` · changes since 0.0.0-develop.148_
<!-- build:0.0.0-develop.150 revision:43afe27ad81c2fedd13e22c35d1d1029c78882ae ts:1786005949 -->

### Summary

- **Major:** Database migration updates: modified approval policy, stage, and rule SQL files to enhance data integrity and prevent policy key clashes during shared database operations.
- Policy management improvement: implemented untargeted ON CONFLICT DO NOTHING for policy key version handling, preventing batch failures due to existing policies in other registries.
- Registry connection handling: added fallback mechanism for Superset connection name to ensure proper cleanup and avoid orphaned resources after uninstallation.

### Changes since 0.0.0-develop.148

- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix AWE seed aborting on shared-DB policy_key clash: untargeted ON CONFLICT DO NOTHING (uq_policy_key_version was unguarded by the id-targeted clause) plus FK-orphan filters on stages/rules, so a policy another registry already owns no longer takes the whole batch — and the farmer policy — down with it ([`43afe27`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/43afe27ad81c2fedd13e22c35d1d1029c78882ae))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fall back to this registry's own Superset connection name when the release is gone. The name was only ever read from `helm get values`, so uninstalling from Rancher — or running helm uninstall first — skipped the dashboard cleanup with a quiet warning and left the dashboards, charts, datasets and connection in the shared Superset, where the next install adopted them by UUID. ([`a445d51`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/a445d51fc54913d9fd0127e138f3213d748b4410))

<a id="v-0-0-0-develop-148"></a>

## registry/farmer-registry — develop 0.0.0-develop.148 (2026-08-06)

_commit `2e3a06a` · changes since 0.0.0-develop.146_
<!-- build:0.0.0-develop.148 revision:2e3a06a243dc3a44d8485622deae1b9f4d07aa25 ts:1785996415 -->

### Summary

- Installation improvements: Skip dashboard import when Superset is absent to prevent installation failures; set `analytics.dashboards.superset.required=true` for better handling of optional analytics components.
- New feature: Added maps content published as a registry-specific image to enhance Insights, allowing for accurate queries related to land tenure, input use, and cooperative membership validated against the live FR database.

### Changes since 0.0.0-develop.146

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Skip the dashboard import when Superset is absent instead of failing the install. Superset is a separate release and analytics is optional, but the gate exited 1 after waiting, so a registry installed without a reporting stack failed outright. The gate is checked in the init container AND the main one, because an init container exiting 0 does not stop the pod; set analytics.dashboards.superset.required=true where a silent skip would be worse. ([`2e3a06a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/2e3a06a243dc3a44d8485622deae1b9f4d07aa25))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add the maps content and publish it as an image. Insights draws maps from a registry-specific image; without one, FR installs fell back to the reference content, which queries nsr_rpt_* and poverty measures FR does not have. Queries plot land tenure, input use and cooperative membership from fr_rpt_farmer/fr_rpt_crop, and are validated against a live FR database. ([`6aac6b7`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/6aac6b7b128d3ed896c70cae283af39cd25a49ac))

<a id="v-0-0-0-develop-146"></a>

## registry/farmer-registry — develop 0.0.0-develop.146 (2026-08-06)

_commit `7af358a` · changes since 0.0.0-develop.145_
<!-- build:0.0.0-develop.146 revision:7af358afa6577cce069d120c54b7cc2f892e94fe ts:1785981849 -->

### Changes since 0.0.0-develop.145

- Fixes in data seeding. ([`7af358a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/7af358afa6577cce069d120c54b7cc2f892e94fe))

<a id="v-0-0-0-develop-145"></a>

## registry/farmer-registry — develop 0.0.0-develop.145 (2026-08-06)

_commit `f19c12d` · changes since 0.0.0-develop.144_
<!-- build:0.0.0-develop.145 revision:f19c12dd57340798ff7de921c17ebb179eb4fc3a ts:1785977474 -->

### Changes since 0.0.0-develop.144

- Bumped up RP version to 0.0.0-develop.346 ([`f19c12d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/f19c12dd57340798ff7de921c17ebb179eb4fc3a))

<a id="v-0-0-0-develop-144"></a>

## registry/farmer-registry — develop 0.0.0-develop.144 (2026-08-05)

_commit `003ac5d` · changes since 0.0.0-develop.142_
<!-- build:0.0.0-develop.144 revision:003ac5de37ee21bb695b23bc492248c0b68d5f6a ts:1785892531 -->

### Summary

- **Major:** New analytics features: introduced FR reporting views, a bulk sample generator, and a Superset bundle with 5 dashboards and 45 charts, along with analytics jobs.
- Database enhancements: took ownership of `load_sample_data.py` and `upload_images.py` from the platform image for improved data seeding.

### Changes since 0.0.0-develop.142

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) DB-seed: take ownership of load_sample_data.py and upload_images.py from the platform image ([`003ac5d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/003ac5de37ee21bb695b23bc492248c0b68d5f6a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Analytics: add FR reporting views, bulk sample generator, Superset bundle (5 dashboards/45 charts) and the analytics Jobs; declare the DB globals the wrapper's own templates need ([`932aa5a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/932aa5a4ddf7b9c9a0ebb4b30096ad67c22758df))

<a id="v-0-0-0-develop-142"></a>

## registry/farmer-registry — develop 0.0.0-develop.142 (2026-08-04)

_commit `30672a4` · changes since 0.0.0-develop.141_
<!-- build:0.0.0-develop.142 revision:30672a410c1fc942b9bdd1e4b544ab337e507436 ts:1785831582 -->

### Changes since 0.0.0-develop.141

- [G2P-2804](https://openg2p.atlassian.net/browse/G2P-2804) Analytics: add FR reporting layer (fr_rpt_farmer, fr_rpt_land, fr_rpt_geo_levels) — area normalised to hectares, crops/livestock/inputs rolled off the land grain ([`30672a4`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/30672a410c1fc942b9bdd1e4b544ab337e507436))

<a id="v-0-0-0-develop-141"></a>

## registry/farmer-registry — develop 0.0.0-develop.141 (2026-08-04)

_commit `ae32039` · changes since 0.0.0-develop.140_
<!-- build:0.0.0-develop.141 revision:ae32039b18158b8ade948311e02681bc6442dadd ts:1785820307 -->

### Changes since 0.0.0-develop.140

- questions.yaml copied during CI ([`ae32039`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ae32039b18158b8ade948311e02681bc6442dadd))

<a id="v-0-0-0-develop-140"></a>

## registry/farmer-registry — develop 0.0.0-develop.140 (2026-08-04)

_commit `5cae5e3` · changes since 1.2.0_
<!-- build:0.0.0-develop.140 revision:5cae5e38b01f7c598811f49f7451bd30d4ea50d1 ts:1785816561 -->

### Summary

- **Major:** CI migration to GitLab: switched from GitHub Actions to GitLab CI, updating `.gitlab-ci.yml` and fixing values.yaml issues related to the CI setup.
- Data management enhancements: enabled the Master Data path, stopped seeding a second geography, and fixed geo dropdowns to properly populate from master-data.
- Code refactoring: removed unused async methods across various models (crop, farm inputs, etc.) to streamline code and improve maintainability.
- Dependency updates: bumped the RP version and took the latest registry-platform from the GitLab charts registry.

### Changes since 1.2.0

- Bumped up RP version ([`5cae5e3`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/5cae5e38b01f7c598811f49f7451bd30d4ea50d1))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Chart: fix values.yaml clobbered by the CI migration (yq line offset; staffApi/partnerApi pointed at the wrong images); take registry-platform 0.0.0-develop.343 from the GitLab charts registry ([`c989a9d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/c989a9db99f52fb64fa871219abd7adde8222ea4))
- Data related changes. ([`d66f1a6`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/d66f1a697e05a5b78b9c6b9a4eddc72b727354be))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Enable the Master Data path and stop seeding a second geography. loadGeoData was still true, which runs the legacy slug-path loader over the hierarchy master-data already holds from its country pack — two hierarchies, one of which joins to nothing. Also enables loadAttributes with the agriculture domain, and syncGeoWidgets. ([`e2d45bc`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/e2d45bc2153058f54bd5a0f13f4ac49394827f15))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`1cc19d0`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/1cc19d0410a71c7c7d45ae5458d64519a1457c47))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix the two geo dropdowns. They carried a hardcoded dev-environment URL and no service/endpoint, so the widget layer bailed before making the request and the dropdowns never populated. Now resolved through master-data like every other api widget, with levels that match the default country pack. ([`79edff5`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/79edff5679c097d400c4ce645f28b383ceae32cc))
- [G2P-5412](https://openg2p.atlassian.net/browse/G2P-5412) Refactor: Remove unused async methods for linking internal record IDs in various models (crop, farm inputs, farmer, household member, land, livestock, membership details) to streamline code and improve maintainability. ([`c5ab693`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/c5ab69323dd7435a93ae3572213fd5dfdec6a71f))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
