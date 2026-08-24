# registry/farmer-registry

_Published automatically._

**Repository:** [gitlab.com/openg2p/registry/farmer-registry](https://gitlab.com/openg2p/registry/farmer-registry) · **Container images:** [Container Registry](https://gitlab.com/openg2p/registry/farmer-registry/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.191`](#v-0-0-0-develop-191) | 2026-08-24 | develop |
| [`0.0.0-develop.190`](#v-0-0-0-develop-190) | 2026-08-24 | develop |
| [`0.0.0-develop.189`](#v-0-0-0-develop-189) | 2026-08-23 | develop |
| [`0.0.0-develop.187`](#v-0-0-0-develop-187) | 2026-08-23 | develop |
| [`0.0.0-develop.186`](#v-0-0-0-develop-186) | 2026-08-23 | develop |
| [`0.0.0-develop.185`](#v-0-0-0-develop-185) | 2026-08-22 | develop |
| [`0.0.0-develop.183`](#v-0-0-0-develop-183) | 2026-08-22 | develop |
| [`0.0.0-develop.182`](#v-0-0-0-develop-182) | 2026-08-22 | develop |
| [`1.2.1-rc.154`](#v-1-2-1-rc-154) | 2026-08-21 | release candidate |
| [`0.0.0-develop.177`](#v-0-0-0-develop-177) | 2026-08-21 | develop |
| [`0.0.0-develop.176`](#v-0-0-0-develop-176) | 2026-08-21 | develop |
| [`1.2.1-rc.144`](#v-1-2-1-rc-144) | 2026-08-20 | release candidate |
| [`0.0.0-develop.173`](#v-0-0-0-develop-173) | 2026-08-20 | develop |
| [`0.0.0-develop.171`](#v-0-0-0-develop-171) | 2026-08-20 | develop |
| [`0.0.0-develop.170`](#v-0-0-0-develop-170) | 2026-08-20 | develop |
| [`1.2.1-rc.142`](#v-1-2-1-rc-142) | 2026-08-19 | release candidate |
| [`1.2.1-rc.139`](#v-1-2-1-rc-139) | 2026-08-14 | release candidate |
| [`0.0.0-develop.168`](#v-0-0-0-develop-168) | 2026-08-14 | develop |
| [`0.0.0-develop.166`](#v-0-0-0-develop-166) | 2026-08-14 | develop |
| [`0.0.0-develop.163`](#v-0-0-0-develop-163) | 2026-08-11 | develop |
| [`0.0.0-develop.161`](#v-0-0-0-develop-161) | 2026-08-10 | develop |
| [`0.0.0-develop.159`](#v-0-0-0-develop-159) | 2026-08-09 | develop |
| [`0.0.0-develop.154`](#v-0-0-0-develop-154) | 2026-08-07 | develop |
| [`0.0.0-develop.153`](#v-0-0-0-develop-153) | 2026-08-06 | develop |
| [`1.3.0`](#v-1-3-0) | 2026-08-06 | release |
| [`1.3.0-rc.151`](#v-1-3-0-rc-151) | 2026-08-06 | release candidate |

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

<a id="v-1-2-1-rc-154"></a>

## registry/farmer-registry 1.2.1-rc.154 — 2026-08-21

_commit `00f26e1` · changes since 1.2.1-rc.144_
<!-- build:1.2.1-rc.154 revision:00f26e15208d5d6346053b621e5a4a70eae33b35 ts:1787303681 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.154](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-1.2.1-rc.154.tgz)

### Summary

- **Major:** Updated Dockerfiles and Chart.yaml to version 1.2.0-rc.419 and switched to GitLab registry paths.
- Data management enhancements: Added seeding functionality for data insertion via intake form and introduced a script for uploading farmer data and images to MinIO.
- Schema updates: Implemented changes in UI schema and domain translation.
- Functional ID generation: Enabled generation for farmer and household entities.
- Cleanup: Removed obsolete SQL files related to attributes.

### Changes

- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update Dockerfiles and Chart.yaml to use GitLab registry paths ([`212e9e1`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/212e9e18e588fc59ba7971ab5fbdea4168d21761))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update Dockerfiles and Chart.yaml to version 1.2.0-rc.419 ([`7db5915`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/7db5915d453697b102133539c5643b2bbe0303be))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Add seeding to insert data via intake form ([`8dd6d6a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/8dd6d6acbcd37be76cd024d1295b2b3f4f09da7c))
- Change in Ui schema and domain translation ([`75f1c68`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/75f1c685deccc29c8b3d137164ffe35e644c1302))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Add script to upload farmer data and images to MinIO ([`81610dd`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/81610dd3ffad426f1b9d59a4ee012b8aeffa3ecf))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enable functional_id generation for farmer and household ([`99cf568`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/99cf5686d7e32376143ce9b34c9ad1e65ddaf4a5))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Delete attribute sql files ([`ddb078f`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ddb078f07fb67d41bf746da66c87857f37f6e614))

<a id="v-1-2-1-rc-144"></a>

## registry/farmer-registry 1.2.1-rc.144 — 2026-08-20

_commit `19d6b89` · changes since 1.2.1-rc.142_
<!-- build:1.2.1-rc.144 revision:19d6b89cf52c62ecf9ebcc93540961f95ce578a8 ts:1787222397 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.144](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-1.2.1-rc.144.tgz)

### Changes

- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): update SQL insert statements for crops, livestocks, and farminputs sections ([`6c6dff7`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/6c6dff730553ca98dba1aa14482b267540936604))

<a id="v-1-2-1-rc-142"></a>

## registry/farmer-registry 1.2.1-rc.142 — 2026-08-19

_commit `0b5014f` · changes since 1.2.1-rc.139_
<!-- build:1.2.1-rc.142 revision:0b5014f127e0b079592a7fb05963e2dd317e91ea ts:1787121281 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.142](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-1.2.1-rc.142.tgz)

### Summary

- **Major:** Data model update: changed `land_size` field type from string to float in the land model and schema.
- Domain registration optimization: removed `G2PRegisterDomainFactory` and related files to streamline the domain registration process, resulting in significant codebase reduction.

### Changes

- [G2P-5480](https://openg2p.atlassian.net/browse/G2P-5480) Change land_size field type from string to float in land model and schema ([`161821a`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/161821a2b04d18095df90277d5f7404b1994cca0))
- [G2P-5524](https://openg2p.atlassian.net/browse/G2P-5524) refactor: remove G2PRegisterDomainFactory and related files to streamline domain registration process ([`ef21f34`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ef21f346f57e7a358f18b5109cc8fcaf1649ebc4))

<a id="v-1-2-1-rc-139"></a>

## registry/farmer-registry 1.2.1-rc.139 — 2026-08-14

_commit `cda0496` · changes since 1.2.0_
<!-- build:1.2.1-rc.139 revision:cda04961495a1f80105d19eb61d53ddf3bf31b66 ts:1786703967 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.139](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-1.2.1-rc.139.tgz)

### Summary

- **Major:** CI transition to GitLab CI, removing GitHub Actions for build and publish processes.
- Data model updates: corrected field names in the household information section and enhanced SQL insert statements for `g2p_register_sections` and `registry_languages` with additional metadata and widget configurations.
- Repository cleanup: removed redundant entries in `values.yaml` for `openg2p-farmer-registry`.

### Changes since 1.2.0

- [G2P-5519](https://openg2p.atlassian.net/browse/G2P-5519) remove redundant repository entries in values.yaml for openg2p-farmer-registry ([`9d9ba7b`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/9d9ba7b48356181140821ef3ba9d1ea076ce429e))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): Correct field names in household information section ([`675cf2e`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/675cf2e87eb1bfc8a057f89d0a73ff821857946f))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`37c1731`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/37c17318828fbcb4274b33e2eb7b649ee77f5f15))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: enhance SQL insert statements for g2p_register_sections with additional metadata and widget configurations for livestock and household member sections ([`ab6c0db`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ab6c0db73d01620066ba6d3c745b219f42cb230b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`1062700`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/1062700737b8129d66fcc363c7d3809863d0cefb))

# Develop builds

<a id="v-0-0-0-develop-191"></a>

## registry/farmer-registry — develop 0.0.0-develop.191 (2026-08-24)

_commit `9ce672b` · changes since 0.0.0-develop.190_
<!-- build:0.0.0-develop.191 revision:9ce672bded8ff68a18e77df2f91c92726e329eeb ts:1787547967 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.191](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.191.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.414 ([`9ce672b`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/9ce672bded8ff68a18e77df2f91c92726e329eeb))

<a id="v-0-0-0-develop-190"></a>

## registry/farmer-registry — develop 0.0.0-develop.190 (2026-08-24)

_commit `2b0ed75` · changes since 0.0.0-develop.189_
<!-- build:0.0.0-develop.190 revision:2b0ed755c6d3457ca85679cba7fc74196570e857 ts:1787540100 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.190](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.190.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.411 ([`2b0ed75`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/2b0ed755c6d3457ca85679cba7fc74196570e857))

<a id="v-0-0-0-develop-189"></a>

## registry/farmer-registry — develop 0.0.0-develop.189 (2026-08-23)

_commit `605343d` · changes since 0.0.0-develop.187_
<!-- build:0.0.0-develop.189 revision:605343dae8893675263558be8775978424027260 ts:1787473237 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.189](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.189.tgz)

### Summary

- **Major:** Updated RP version to 0.0.0-develop.409, reflecting significant changes in the project.
- New feature: Developed a farmer agent-portal-api image that integrates with the farmer register model, enhancing the system's capabilities.

### Changes

- Bumped up RP version to 0.0.0-develop.409 ([`605343d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/605343dae8893675263558be8775978424027260))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Build a farmer agent-portal-api image so it maps the farmer register model. Bumped up RP version. ([`e0dae0b`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/e0dae0bb54567b257263414ea49501c441ab2e4b))

<a id="v-0-0-0-develop-187"></a>

## registry/farmer-registry — develop 0.0.0-develop.187 (2026-08-23)

_commit `dd71272` · changes since 0.0.0-develop.186_
<!-- build:0.0.0-develop.187 revision:dd7127209ae96e8186d1f83ea05f46903394d5a5 ts:1787462709 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.187](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.187.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.408. ([`dd71272`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/dd7127209ae96e8186d1f83ea05f46903394d5a5))

<a id="v-0-0-0-develop-186"></a>

## registry/farmer-registry — develop 0.0.0-develop.186 (2026-08-23)

_commit `8022dfc` · changes since 0.0.0-develop.185_
<!-- build:0.0.0-develop.186 revision:8022dfcbcb92bd39b81682a6024997b3274004a1 ts:1787447477 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.186](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.186.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.406 ([`8022dfc`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/8022dfcbcb92bd39b81682a6024997b3274004a1))

<a id="v-0-0-0-develop-185"></a>

## registry/farmer-registry — develop 0.0.0-develop.185 (2026-08-22)

_commit `6e3a1f8` · changes since 0.0.0-develop.183_
<!-- build:0.0.0-develop.185 revision:6e3a1f8ad8348e6cb082aa15b8b111306ec7ed87 ts:1787401948 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.185](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.185.tgz)

### Summary

- Version update: bumped RP version to 0.0.0-develop.404.
- Configuration change: updated master data database credentials to point at the renamed secret.

### Changes

- Bumped up RP version to 0.0.0-develop.404 ([`6e3a1f8`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/6e3a1f8ad8348e6cb082aa15b8b111306ec7ed87))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Point master data DB credentials at the renamed secret ([`ffcc9e7`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ffcc9e7f39b441d6e532b2199275427a4ffa1f16))

<a id="v-0-0-0-develop-183"></a>

## registry/farmer-registry — develop 0.0.0-develop.183 (2026-08-22)

_commit `9c608d9` · changes since 0.0.0-develop.182_
<!-- build:0.0.0-develop.183 revision:9c608d91cdce3713f79c40220fd738c2d3426f60 ts:1787381122 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.183](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.183.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.403 ([`9c608d9`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/9c608d91cdce3713f79c40220fd738c2d3426f60))

<a id="v-0-0-0-develop-182"></a>

## registry/farmer-registry — develop 0.0.0-develop.182 (2026-08-22)

_commit `ffb2c75` · changes since 0.0.0-develop.177_
<!-- build:0.0.0-develop.182 revision:ffb2c759bf707fd02b6f760f9839eab21e8f653c ts:1787373547 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.182](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.182.tgz)

### Summary

- **Major:** Introduced claim-169 QR configuration requiring registrant authentication, enhancing security for claims.
- VC issuance is now enabled by default, streamlining the process for users.
- Normalised foundational ID and corrected full name spacing in both the VC view and farmer VC view for improved clarity and consistency.
- Updated RP version to 0.0.0-develop.402, reflecting ongoing development progress.

### Changes

- Bumped up RP version to 0.0.0-develop.402 ([`ffb2c75`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ffb2c759bf707fd02b6f760f9839eab21e8f653c))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ship the claim-169 QR config and require registrant authentication ([`acecdce`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/acecdcedc1261127d012eaca9a5268feaa849e58))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable VC issuance by default ([`7484b69`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/7484b69721348a1dc415d9a9e1a28b74ee4edd1f))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise foundational ID and fix full name spacing in the VC view ([`f6d4c53`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/f6d4c53dea0db69353e9493117ec1b431bc32c13))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix full name spacing in the farmer VC view ([`fbf66e2`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/fbf66e28522d5981bf82a0ad99478f7846682f42))

<a id="v-0-0-0-develop-177"></a>

## registry/farmer-registry — develop 0.0.0-develop.177 (2026-08-21)

_commit `4196dd6` · changes since 0.0.0-develop.176_
<!-- build:0.0.0-develop.177 revision:4196dd6d0c95e79c00e14b5afd04557003f0dcd3 ts:1787295510 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.177](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.177.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.392 ([`4196dd6`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/4196dd6d0c95e79c00e14b5afd04557003f0dcd3))

<a id="v-0-0-0-develop-176"></a>

## registry/farmer-registry — develop 0.0.0-develop.176 (2026-08-21)

_commit `1762516` · changes since 0.0.0-develop.173_
<!-- build:0.0.0-develop.176 revision:1762516054f3fc491d42cb2e885819f4f99dddf7 ts:1787276497 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.176](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.176.tgz)

### Summary

- **Major:** Updated RP version to 0.0.0-develop.391, marking a significant development milestone.
- Data handling enhancement: Seeded the pack's real birth date for sample farmers, improving accuracy while maintaining fallback for older packs.
- Deployment improvement: Automated creation of the VC card ConfigMap during agent portal deployment, streamlining setup processes.

### Changes

- Bumped up RP version to 0.0.0-develop.391 ([`1762516`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/1762516054f3fc491d42cb2e885819f4f99dddf7))
- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Seed the pack's real birth date instead of inventing 1 January. The pack carried only a year, so every sample farmer in the country shared a birthday; older packs still fall back, since a date column cannot hold a year. ([`a74feca`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/a74fecacc096f7a06ff97c70dc951e2545ec7540))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Create the VC card ConfigMap whenever the agent portal is deployed ([`94abb14`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/94abb142887918217bf503ad12eabe3e0555d1d7))

<a id="v-0-0-0-develop-173"></a>

## registry/farmer-registry — develop 0.0.0-develop.173 (2026-08-20)

_commit `1b1a77b` · changes since 0.0.0-develop.171_
<!-- build:0.0.0-develop.173 revision:1b1a77b3e9612b95e9f5f79247c733b42cd81c61 ts:1787217291 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.173](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.173.tgz)

### Summary

- **Major:** Enabled the agent portal by default, enhancing accessibility for users.
- Bumped RP version to 0.0.0-develop.389, indicating ongoing development and updates.

### Changes

- Bumped up RP version to 0.0.0-develop.389 ([`1b1a77b`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/1b1a77b3e9612b95e9f5f79247c733b42cd81c61))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal by default ([`ca4d6ee`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/ca4d6ee1061b1cc59874c5edf0b33f04b1882c42))

<a id="v-0-0-0-develop-171"></a>

## registry/farmer-registry — develop 0.0.0-develop.171 (2026-08-20)

_commit `dfe77b7` · changes since 0.0.0-develop.170_
<!-- build:0.0.0-develop.171 revision:dfe77b79d88e9bb50b55ffea5fbb6309316e11f1 ts:1787215083 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.171](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.171.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.388 ([`dfe77b7`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/dfe77b79d88e9bb50b55ffea5fbb6309316e11f1))

<a id="v-0-0-0-develop-170"></a>

## registry/farmer-registry — develop 0.0.0-develop.170 (2026-08-20)

_commit `a29871f` · changes since 0.0.0-develop.168_
<!-- build:0.0.0-develop.170 revision:a29871fe6a6052c530afa250176172a7e3ee0955 ts:1787213001 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.170](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.170.tgz)

### Summary

- **Major:** Introduced a new feature for farmer credential issuance, which is disabled by default to allow for controlled rollout.
- Cleanup: Removed duplicated VC questions from the registry subchart and updated the RP version to streamline the codebase.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Drop duplicated VC questions inherited from the registry subchart. Bumped up RP version. ([`a29871f`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/a29871fe6a6052c530afa250176172a7e3ee0955))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add farmer credential issuance behind a disabled-by-default switch ([`95e4214`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/95e42143af43a28e72b33f6c4b7855adefd5d415))

<a id="v-0-0-0-develop-168"></a>

## registry/farmer-registry — develop 0.0.0-develop.168 (2026-08-14)

_commit `55f8c65` · changes since 0.0.0-develop.166_
<!-- build:0.0.0-develop.168 revision:55f8c658ff1ec64fe7816f73afe13ac575abba90 ts:1786692965 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.168](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.168.tgz)

### Changes since 0.0.0-develop.166

- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): Correct field names in household information section ([`8599e27`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/8599e272b4ff53ece192c92f60f6eca9cd4fb16a))

<a id="v-0-0-0-develop-166"></a>

## registry/farmer-registry — develop 0.0.0-develop.166 (2026-08-14)

_commit `019012a` · changes since 0.0.0-develop.163_
<!-- build:0.0.0-develop.166 revision:019012a4db73def5084f7b8bf7842fec35ec4cdb ts:1786674098 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.166](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.166.tgz)

### Summary

- Version bump: updated RP version to 0.0.0-develop.384.
- Documentation: made minor corrections in Helm comments for clarity.

### Changes since 0.0.0-develop.163

- Bumped up RP version to 0.0.0-develop.384 ([`98180a1`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/98180a19c65cec2c7bc486a44c9dbc5a2f6d0a97))
- Minor correction in helm comments. ([`835646d`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/835646d64ea4220110d6b6b6f1171faff3b4c2cb))

<a id="v-0-0-0-develop-163"></a>

## registry/farmer-registry — develop 0.0.0-develop.163 (2026-08-11)

_commit `0ba140d` · changes since 0.0.0-develop.161_
<!-- build:0.0.0-develop.163 revision:0ba140d519d364f55ab28b0ce8b95f25ab7c50d4 ts:1786445658 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.163](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.163.tgz)

### Changes since 0.0.0-develop.161

- Add seed manifest generation and remove obsolete performance templates ([`bee2c80`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/bee2c80bda0d7c178d97c2c177c5db7250ea12ab))

<a id="v-0-0-0-develop-161"></a>

## registry/farmer-registry — develop 0.0.0-develop.161 (2026-08-10)

_commit `f8ee93c` · changes since 0.0.0-develop.159_
<!-- build:0.0.0-develop.161 revision:f8ee93c268f93f166d8d605491488a8c57b2300a ts:1786350857 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.161](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-farmer-registry-0.0.0-develop.161.tgz)

### Changes since 0.0.0-develop.159

- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`b2cda40`](https://gitlab.com/openg2p/registry/farmer-registry/-/commit/b2cda40ae3ff83f6b189a43fd8c160bed6dda398))

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

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
