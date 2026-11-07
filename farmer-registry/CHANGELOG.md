# farmer-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/farmer-registry](https://github.com/OpenG2P/farmer-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.283`](#v-0-0-0-develop-283) | 2026-11-07 | develop |  |
| [`1.2.1-rc.326`](#v-1-2-1-rc-326) | 2026-11-04 | release candidate |  |
| [`1.2.1-rc.210`](#v-1-2-1-rc-210) | 2026-10-30 | release candidate |  |
| [`0.0.0-develop.282`](#v-0-0-0-develop-282) | 2026-10-28 | develop |  |
| [`1.2.1-rc.199`](#v-1-2-1-rc-199) | 2026-10-27 | release candidate |  |
| [`1.2.1-rc.194`](#v-1-2-1-rc-194) | 2026-10-26 | release candidate |  |
| [`1.2.1-rc.192`](#v-1-2-1-rc-192) | 2026-10-23 | release candidate |  |
| [`0.0.0-develop.280`](#v-0-0-0-develop-280) | 2026-10-21 | develop |  |
| [`0.0.0-develop.278`](#v-0-0-0-develop-278) | 2026-10-19 | develop |  |
| [`1.2.1-rc.190`](#v-1-2-1-rc-190) | 2026-10-14 | release candidate |  |
| [`1.2.1-rc.188`](#v-1-2-1-rc-188) | 2026-10-14 | release candidate |  |
| [`0.0.0-develop.276`](#v-0-0-0-develop-276) | 2026-10-08 | develop |  |
| [`0.0.0-develop.275`](#v-0-0-0-develop-275) | 2026-10-08 | develop |  |
| [`0.0.0-develop.273`](#v-0-0-0-develop-273) | 2026-10-07 | develop |  |
| [`0.0.0-develop.272`](#v-0-0-0-develop-272) | 2026-10-07 | develop |  |
| [`1.2.1-rc.182`](#v-1-2-1-rc-182) | 2026-10-06 | release candidate |  |
| [`1.2.1-rc.180`](#v-1-2-1-rc-180) | 2026-10-05 | release candidate |  |
| [`1.2.1-rc.179`](#v-1-2-1-rc-179) | 2026-10-05 | release candidate |  |
| [`0.0.0-develop.271`](#v-0-0-0-develop-271) | 2026-10-05 | develop |  |
| [`0.0.0-develop.221`](#v-0-0-0-develop-221) | 2026-10-03 | develop |  |
| [`0.0.0-develop.218`](#v-0-0-0-develop-218) | 2026-10-02 | develop |  |
| [`0.0.0-develop.215`](#v-0-0-0-develop-215) | 2026-10-01 | develop |  |
| [`0.0.0-develop.211`](#v-0-0-0-develop-211) | 2026-09-27 | develop |  |
| [`0.0.0-develop.209`](#v-0-0-0-develop-209) | 2026-09-23 | develop |  |
| [`0.0.0-develop.207`](#v-0-0-0-develop-207) | 2026-09-12 | develop |  |
| [`0.0.0-develop.206`](#v-0-0-0-develop-206) | 2026-09-03 | develop | **Intermediate Stable Version**. VC issuance and verification both working fine. Compatible with commons 0.0.0-develop.243. |
| [`0.0.0-develop.205`](#v-0-0-0-develop-205) | 2026-09-02 | develop |  |
| [`0.0.0-develop.203`](#v-0-0-0-develop-203) | 2026-09-02 | develop |  |
| [`0.0.0-develop.201`](#v-0-0-0-develop-201) | 2026-09-01 | develop |  |
| [`0.0.0-develop.198`](#v-0-0-0-develop-198) | 2026-09-01 | develop |  |
| [`1.3.0`](#v-1-3-0) | 2026-08-06 | release |  |
| [`1.2.0`](#v-1-2-0) | 2026-07-25 | release |  |

# Releases

<a id="v-1-3-0"></a>

## farmer-registry 1.3.0 — 2026-08-06

<!-- build:1.3.0 revision:d39deba138813845cc34ea701b885ed763833836 ts:1786007784 -->

_commit `d39deba` · changes since release 1.2.0_

**Chart:** [openg2p-farmer-registry 1.3.0](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.3.0.tgz)

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

<a id="v-1-2-0"></a>

## farmer-registry 1.2.0 — 2026-07-25

<!-- build:1.2.0 revision:7055a710a25bca297f8a1cbd6c2cb64664840b20 ts:1784886389 -->

_commit `7055a71` · first release_

**Chart:** [openg2p-farmer-registry 1.2.0](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.0.tgz)

### Summary

- **Major:** Updated openg2p-registry pin to 0.0.0-develop.295 across all Dockerfiles and Helm charts, ensuring lockstep alignment and introducing a CI guard against version mismatches.
- Production hardening: implemented resource limits, fixed HPA bugs, and ensured Docker containers run as non-root users.
- Security enhancements: added CSRF validation for staff-portal-api requests, enabled partner signature validation and consent enforcement by default, and updated IAM permissions for metadata API access.
- CI improvements: migrated to a central build-publish CI model, fixed Dockerfile pin/build-arg mismatches, and tidied up CI migration leftovers.
- Sanity testing: added a comprehensive e2e test suite, improved retry logic for DCI searches, and ensured tests pass end-to-end on live clusters.
- Chart updates: fixed inert db-seed loaders, declared farmer idTypes explicitly, and inherited Rancher questions.yaml from the pinned openg2p-registry dependency.
- Data seeding enhancements: updated seeding models for score attributes, added support for loading geo reference data, and enhanced SQL templates for farmer extension.
- Dependency management: bumped various dependencies to their latest versions and ensured compatibility with the latest Docker images.
- Refactoring: improved clarity in naming conventions, removed obsolete models, and updated SQL data models for consistency and accuracy.

### Changes

- Bumped up RP version ([`7055a71`](https://github.com/OpenG2P/farmer-registry/commit/7055a710a25bca297f8a1cbd6c2cb64664840b20))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Tooling: add scripts/bump-rp-version.sh (with -n dry-run and -h help) to move the openg2p-registry pin — Dockerfiles + chart dependency together — to the latest version published in BOTH the Helm index and Docker Hub, plus a CI lockstep guard (test/test_rp_pin_lockstep.py + checks.yml) that fails the build if the pins ever split ([`90ec640`](https://github.com/OpenG2P/farmer-registry/commit/90ec64034ee4bea339f9109dd8ee6cb388a8bc76))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Tooling: add scripts/bump-rp-version.sh to move the openg2p-registry pin (Dockerfiles + chart dependency) atomically to the latest version published in both the Helm index and Docker Hub, plus a CI lockstep guard (test/test_rp_pin_lockstep.py + checks.yml) that fails the build if the pins ever split ([`d4770e3`](https://github.com/OpenG2P/farmer-registry/commit/d4770e3a3c9b6fe250d2ab5b17be1d3c6ca393d3))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Bump openg2p-registry pin to 0.0.0-develop.295 in all Dockerfiles and the chart dependency (kept in lockstep) ([`30ca665`](https://github.com/OpenG2P/farmer-registry/commit/30ca665d81fa44184f5eaac869ad9956c462bec3))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Align RP_VERSION in all Dockerfiles with the chart dependency at 0.0.0-develop.294 — the chart had been bumped but the images were still built FROM .288, so the sanity overlay imported post_search from a harness that predated it ([`f4ad365`](https://github.com/OpenG2P/farmer-registry/commit/f4ad365cb12d27dad053909817a3b3572b59f276))
- Bumped up registry platform version. ([`2997fcf`](https://github.com/OpenG2P/farmer-registry/commit/2997fcfa364644d36ba8e20af6127c8fbe1127b2))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: retry a DCI search only when a dependency returns 5xx (e.g. Consent Manager stale-connection 500) — a genuine policy denial is never retried, so fail-closed behaviour is still asserted ([`88f13ce`](https://github.com/OpenG2P/farmer-registry/commit/88f13ce4b289b7ff318eca18d87ee9c1598f87a1))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) FR: align RP_VERSION in all Dockerfiles with the chart dependency at 0.0.0-develop.291,and refresh the chart lock so the sanity job renders again ([`c797983`](https://github.com/OpenG2P/farmer-registry/commit/c79798339e983f011699ca50ea9794eb0b6fdef7))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Chart: declare farmer idTypes and the IAM application description explicitly, now that the platform chart defaults to the reference registry's individual+household pools and a neutral tile name ([`390dde1`](https://github.com/OpenG2P/farmer-registry/commit/390dde136ea7f1399e263f0defdbea3d0a915191))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Chart: fix inert db-seed loaders — move loadGeoData/loadSampleData/loadImages/loadTemplates from global.* to registry.dbSeed.* (the db-seed Job reads .Values.dbSeed.load* and has no global fallback, so sample/geo/image data was never loaded) ([`5b8df23`](https://github.com/OpenG2P/farmer-registry/commit/5b8df236df3191c71d7f1e1f4181a30894043927))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Chart: inherit Rancher questions.yaml from the pinned openg2p-registry dependency at package time (chart-inherit-questions) instead of duplicating it; gitignore the generated file ([`3687050`](https://github.com/OpenG2P/farmer-registry/commit/3687050e50b54c9fcf69df857ee7b1506b1c2a71))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) FR as thin extension: add openg2p-farmer-registry wrapper chart (openg2p-registry dep pinned 0.0.0-develop.286), pin RP_VERSION in thin dockers, reduce sanity to farmer field tests (Set 2) FROM openg2p-registry-sanity-tests, rename staff-portal-api→staff-api & sanity→sanity-tests, drop deployment/values.yaml ([`9cf5ec7`](https://github.com/OpenG2P/farmer-registry/commit/9cf5ec777f072b489d064887ea99e555a3530d95))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) values.yaml added. ([`00d4026`](https://github.com/OpenG2P/farmer-registry/commit/00d40265792971d2d9701a7759740c90ae86d746))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Updates. ([`4a0cfb8`](https://github.com/OpenG2P/farmer-registry/commit/4a0cfb8241641a504ad36722353fb03c81d6b233))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Registry platform docker version corrected. ([`80ac54c`](https://github.com/OpenG2P/farmer-registry/commit/80ac54cda79f3a48c3c9bd9ed13e98e31ef921e9))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Invert build model: registry-platform publishes base images + Helm chart, farmer-registry extends ([`08b194a`](https://github.com/OpenG2P/farmer-registry/commit/08b194a23b8b09c1c236e7c3064243a7e1ceb6c0))
- [G2P-5380](https://openg2p.atlassian.net/browse/G2P-5380) fix(seed): update seeding model for score attributes and minor chart refactor ([`cf54dde`](https://github.com/OpenG2P/farmer-registry/commit/cf54dde8dad18462f2925b6c05aeb847ceb0fd7a))
- Just to trigger build to use latest registry-platform. Otherwise, no changes in the code. ([`03eb3ca`](https://github.com/OpenG2P/farmer-registry/commit/03eb3cad247750a8f7881beefb88105ebde0c9bd))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) id-generator moved to Gitlab. Changed the reference in Chart.yaml ([`fd9bbda`](https://github.com/OpenG2P/farmer-registry/commit/fd9bbdabcd1a08eb1a0b1208f32e2cd7edead188))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix sanity DCI e2e after change-request test: chart searchText must be the farmer's functional_record_id (SANITY-FARMER-0001), not the SANITYE2E marker — the CR approval regenerates search_text via the ORM and drops the manual marker, so a DCI search for it returns nothing; functional_record_id is a real search field and survives (reproduced and verified against live trial) ([`3ef95ed`](https://github.com/OpenG2P/farmer-registry/commit/3ef95eddd980976f198bc3594a288076eb02038b))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix sanity e2e install-time 403s: run the sanity test Job at hook-weight 25 so it executes AFTER iam-register (weight 20) pushes the registry's roles→permissions catalog to IAM — the change-request tests were running at weight 15, before IAM knew the registry roles, causing 'Insufficient resource_access roles' ([`540f176`](https://github.com/OpenG2P/farmer-registry/commit/540f1767d159309560970440cae7b4e794494698))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Make sanity e2e survive install-time startup race: retry create_change_request on 403 (permission path warms up after staff-portal-api is reachable) with a fresh token up to authReadyTimeout=120s, and wait for staff-portal-api readiness in the entrypoint — the 4 CR tests were failing only because the Job ran ~2min into a fresh install. ([`345fc57`](https://github.com/OpenG2P/farmer-registry/commit/345fc579a35e7bb4d36c0f51b88e5685527cf78f))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix sanity audit-DB wiring: auditDbSecret/key were audit-manager-db-user / audit-manager-db-user-password; the real Secret is audit-manager / audit-manager-db-user (as the auditmanager deployment mounts) — the in-cluster audit test would otherwise fail ([`e286919`](https://github.com/OpenG2P/farmer-registry/commit/e286919fca9c753c7dc3dd61f06d63b0307c9f1d))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Make change-request e2e pass end-to-end on a live cluster: grant the sanity user AWE_ADMIN and approve every task on the request (shipped stages are mode='all' with demo approvers); poll for the async history row; key the audit assertion on actor_id (events carry no resource_id); add tab_id to get_number_of_versions; fix teardown to key on internal_record_id (CR/history are stamped with the display name) ([`14ec94c`](https://github.com/OpenG2P/farmer-registry/commit/14ec94c2ed2a4cd436ffec2f087e1833b6fd3ff3))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Docs: add Farmer Registry sanity-testing page (tests, DCI + change-request flow diagrams, seeding & markers, install packaging, run-local procedure, gates/e2e-off behavior, teardown); link from deployment README, helm-chart and SUMMARY ([`347f7bf`](https://github.com/OpenG2P/farmer-registry/commit/347f7bf4da3cf6c4b2214197e804737053acf106))
- Fail closed by default: enable partner signature validation and consent enforcement (matching the registry platform defaults, which the chart inverted); keep sanity e2e off by default; fix stale audit comment; record the consent/signature posture as a perf-testing variable ([`331ab43`](https://github.com/OpenG2P/farmer-registry/commit/331ab43be49d4f800bd6552fbbcabddfc1b45681))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) E2e sanity test suite added with 2 power e2e tests. ([`85b60d1`](https://github.com/OpenG2P/farmer-registry/commit/85b60d11a4628ec7a18322a21de3878a09ba940d))
- [G2P-5333](https://openg2p.atlassian.net/browse/G2P-5333) Update permission-to-role mappings ([`fceb436`](https://github.com/OpenG2P/farmer-registry/commit/fceb436fe895c2c6927169a2007ba77fd0cc418f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Tidy CI-migration leftovers in farmer: drop dead develop.txt specs, repoint Chart.yaml comment and celery README to build-publish.yml/Dockerfile ([`6e15b11`](https://github.com/OpenG2P/farmer-registry/commit/6e15b117626e7c8abc678f71c3a3b87148c604b1))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix pin/build-arg repo mismatch: install iam-core from openg2p/iam-service (was openg2p-iam-service, which lacks the resolved SHA), and fetch openg2p-data by ref via git fetch+checkout so db-seed accepts a pinned commit SHA (git clone -b takes only a branch/tag name) ([`1f22275`](https://github.com/OpenG2P/farmer-registry/commit/1f22275da0bce42cb361e9792db8d45e9d31d044))
- IAM service repo renamed. ([`ce226a5`](https://github.com/OpenG2P/farmer-registry/commit/ce226a56f6bf9d282ca1c224d1c00fbf30b129ba))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Move to central build-publish CI; self-contained pinned Dockerfiles ([`84ad210`](https://github.com/OpenG2P/farmer-registry/commit/84ad2101e3f730e62dfb55b844f199e386b13ec8))
- [G2P-5342](https://openg2p.atlassian.net/browse/G2P-5342): Update develop.txt files to replace references to 'openg2p-iam-service' with 'iam-service' ([`8e68be8`](https://github.com/OpenG2P/farmer-registry/commit/8e68be8e828c4f135a333353a436e33d8105c8b4))
- [G2P-5308](https://openg2p.atlassian.net/browse/G2P-5308) refactor(data): update incoming and outgoing templates structure ([`25137a1`](https://github.com/OpenG2P/farmer-registry/commit/25137a195a76d622f4e6908eca36edb736c82726))
- [G2P-5319](https://openg2p.atlassian.net/browse/G2P-5319) Production hardening. Resource limits fixed. HPA bug fixed. Dockers run as non-root. ([`41ea585`](https://github.com/OpenG2P/farmer-registry/commit/41ea5851217bf2b8e29b5ea9c03113ab967d629c))
- [G2P-5318](https://openg2p.atlassian.net/browse/G2P-5318) Sync operational role IAM permissions for register metadata API access ([`e5c879b`](https://github.com/OpenG2P/farmer-registry/commit/e5c879b1c2cff372b2fcc14bbac53fb027f70834))
- [G2P-5255](https://openg2p.atlassian.net/browse/G2P-5255) Add CSRF validation configuration for staff-portal-api requests ([`5b00de3`](https://github.com/OpenG2P/farmer-registry/commit/5b00de3d9da0875353112159c0437877c8e753b1))
- [G2P-5221](https://openg2p.atlassian.net/browse/G2P-5221) Add IAM public URL configuration for Staff Portal UI ([`97ec733`](https://github.com/OpenG2P/farmer-registry/commit/97ec7336b313921b73ef1293d7522e79ab958dc0))
- [G2P-5226](https://openg2p.atlassian.net/browse/G2P-5226) Add Redis configuration for staff-portal-api authentication ([`26383d9`](https://github.com/OpenG2P/farmer-registry/commit/26383d9f0e7753fa0686e1d1d7feb3bf3aa135c6))
- [G2P-5221](https://openg2p.atlassian.net/browse/G2P-5221) Update AWE approver user password and add first/last names for new users in keycloak-init ([`9f768e0`](https://github.com/OpenG2P/farmer-registry/commit/9f768e0366be56a65bac49b3d6bb2da1b8aaba08))
- G2P5221 Add CSP configuration for profile/document images from MinIO ([`499f66a`](https://github.com/OpenG2P/farmer-registry/commit/499f66ad0e265499f137542bc1cfd53db8693c57))
- G2P5221 Add AWE_CALLBACK_CALLER_SERVICE to db-seed and update SQL template ([`9888832`](https://github.com/OpenG2P/farmer-registry/commit/9888832206278d1baea75aed1401b95175a94a9a))
- [G2P-5221](https://openg2p.atlassian.net/browse/G2P-5221) Remove unused verification permissions from payload.json ([`53a2d5f`](https://github.com/OpenG2P/farmer-registry/commit/53a2d5fb8bc1f64dfde7cabba45e8193863d32af))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) URL of CM updated as it is not installed via commons-services. ([`3a76763`](https://github.com/OpenG2P/farmer-registry/commit/3a76763315a054d949ba23e8384cb4a3d3dd0638))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Harden helm-publish workflow against gh-pages push races: add concurrency group + rebase-pull before commit. ([`70c8859`](https://github.com/OpenG2P/farmer-registry/commit/70c88596ad1a9b87c4605fd1a62428e1840d3e6d))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Repoint Partner Management to commons-services and align PM-seed auth to the g2p-bridge pmSeedClientId pattern. ([`6da7b1c`](https://github.com/OpenG2P/farmer-registry/commit/6da7b1c8888ae07a6b48bbf4985cebd99652d35d))
-  [G2P-5299](https://openg2p.atlassian.net/browse/G2P-5299)  Url for PM updated. ([`724f07a`](https://github.com/OpenG2P/farmer-registry/commit/724f07a9c16239ad5a7c0ad971d9ece620f3b340))
- [G2P-5299](https://openg2p.atlassian.net/browse/G2P-5299) Ports corrected. ([`79a6cf2`](https://github.com/OpenG2P/farmer-registry/commit/79a6cf269d22c20ada488c1e09823075df46310f))
- [G2P-5299](https://openg2p.atlassian.net/browse/G2P-5299) questions.yaml updated. ([`b5ebd05`](https://github.com/OpenG2P/farmer-registry/commit/b5ebd0522e17a61f1666d46f7e8302f0791676cf))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Sanity tests added. ([`d3d47bd`](https://github.com/OpenG2P/farmer-registry/commit/d3d47bd85fc15fbce068d03f095d8337cf7263bb))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Enhancement for consent, partner management, WJS. ([`984d6a9`](https://github.com/OpenG2P/farmer-registry/commit/984d6a93d2317c936c9565607b59894cc61cd874))
- Versions updated to 'develop' ([`24a4f82`](https://github.com/OpenG2P/farmer-registry/commit/24a4f82147e1ea2e6e736968ad86c3fcf1f16ae3))
- Fix for db seed docker failing. ([`55a08c8`](https://github.com/OpenG2P/farmer-registry/commit/55a08c88d93c1840f9a5de53bc7c36be28cabdc7))
- [G2P-5207](https://openg2p.atlassian.net/browse/G2P-5207): update SQL insert statements for g2p_register_sections ([`1c9bd2d`](https://github.com/OpenG2P/farmer-registry/commit/1c9bd2d2a3d19df9902ae143c00596213d291b32))
- [G2P-5260](https://openg2p.atlassian.net/browse/G2P-5260) AWE removed from here. Commons AWE used. ([`6b302cd`](https://github.com/OpenG2P/farmer-registry/commit/6b302cd1ccf4a54b9afe742c954f4eef54ac4a78))
- db-seed functionality: Added support for loading geo reference data into the master_data database. ([`7d9f06b`](https://github.com/OpenG2P/farmer-registry/commit/7d9f06b7f93350de0b6f0110578a379cde4b6b96))
- AWE version frozen. ([`9562666`](https://github.com/OpenG2P/farmer-registry/commit/95626664d8ec5e879f4a718589a8a7858e367b3c))
- [G2P-5207](https://openg2p.atlassian.net/browse/G2P-5207) fix: translations and UI schema seeding ([`057c447`](https://github.com/OpenG2P/farmer-registry/commit/057c447d82b1481216b9ebf2cd22f84828e9bc2f))
- [G2P-5202](https://openg2p.atlassian.net/browse/G2P-5202) Bump dependencies and update image tags to latest versions ([`7fdcded`](https://github.com/OpenG2P/farmer-registry/commit/7fdcded62d2089655064a34e551e983e1f2dfb95))
- postgres-init version changed to frozen version ([`42bb8eb`](https://github.com/OpenG2P/farmer-registry/commit/42bb8eba6c19d850a2aee9dd06dea030854f820a))
- [G2P-5187](https://openg2p.atlassian.net/browse/G2P-5187) Develop versioning updated with 0.0.0-develop.N convention ([`c5da4e7`](https://github.com/OpenG2P/farmer-registry/commit/c5da4e76859a54d47793a81547faaad67e41f447))
- Enhance data seeding scripts: Introduced geo hierarchy functions in load_sample_data.py, updated crop and farm input JSON files with new records and modified existing entries, and corrected link IDs in household members and lands JSON files. Adjusted livestock records to reflect accurate types and counts. Updated membership details with new member entries and corrected associations. ([`4f1f54f`](https://github.com/OpenG2P/farmer-registry/commit/4f1f54fd32d9f4ba9ad99c3e1534c0ea57dd4bfc))
- [G2P-5174](https://openg2p.atlassian.net/browse/G2P-5174) Performance test suit added. Still WIP. ([`0d881c9`](https://github.com/OpenG2P/farmer-registry/commit/0d881c9faf7ed5e1a207d5adcf2ad49257be57c0))
- [G2P-5186](https://openg2p.atlassian.net/browse/G2P-5186) Duplicate jobs with same name removed. ([`795d50f`](https://github.com/OpenG2P/farmer-registry/commit/795d50f281c6cfab686c25b9f571cc20ffe0e2e3))
- [G2P-4904](https://openg2p.atlassian.net/browse/G2P-4904) - Farmer data seeding ([`2e124bd`](https://github.com/OpenG2P/farmer-registry/commit/2e124bd979298447502a8c0aaf64bb61755ae56e))
- [G2P-5143](https://openg2p.atlassian.net/browse/G2P-5143) IAM traces removed with uninstall. ([`14d0804`](https://github.com/OpenG2P/farmer-registry/commit/14d08042bccd4323f5eb1d6dbcd32b6d9dfb38ef))
- [G2P-5143](https://openg2p.atlassian.net/browse/G2P-5143) Calling IAM endpoint to register. ([`65f5f8b`](https://github.com/OpenG2P/farmer-registry/commit/65f5f8b48e8bc19ce65f7229c78068289ea086dc))
- [G2P-5142](https://openg2p.atlassian.net/browse/G2P-5142) update language data seeding: add new field and remove obsolete field ([`13ad7de`](https://github.com/OpenG2P/farmer-registry/commit/13ad7dea9bebfe5562dfca89d546f5767e412820))
- Postgres version corrected. ([`9f936f3`](https://github.com/OpenG2P/farmer-registry/commit/9f936f3bc99651e83fd1c79ff495be7f68295681))
- [G2P-5103](https://openg2p.atlassian.net/browse/G2P-5103) Changes in AWE configs such that multiple registries can be installed in an env. ([`097746f`](https://github.com/OpenG2P/farmer-registry/commit/097746f38c213d4f7165c3b5c65ad09af254196a))
- Readme cleaned up. ([`62cb828`](https://github.com/OpenG2P/farmer-registry/commit/62cb8285604c6945be9118423b278e2b80059eb7))
- Temp version to fix the harcoded chart name issue. ([`82d5288`](https://github.com/OpenG2P/farmer-registry/commit/82d52880b49ab91cf92aff102f9f3e613fd04d43))
- Version changed 0.0.1 as the previous issue is still there. ([`8533435`](https://github.com/OpenG2P/farmer-registry/commit/85334351785b9129cb9207be67c82495411e313f))
- Changed the version number to fix the problem of fixed chart name appearing while installing with Rancher. ([`3728628`](https://github.com/OpenG2P/farmer-registry/commit/372862881d8d303ad53a3bac825870dc2b4133d7))
- [G2P-5125](https://openg2p.atlassian.net/browse/G2P-5125) Legacy logging removed, changes synced with latest NSR. ([`1a2fbac`](https://github.com/OpenG2P/farmer-registry/commit/1a2fbaca558d6f1f9548616cdf5a05359df43770))
- [G2P-5125](https://openg2p.atlassian.net/browse/G2P-5125) Consolidated helm chart with dockers built using libs from registry-platform. Just like we did for NSR. ([`1b6b457`](https://github.com/OpenG2P/farmer-registry/commit/1b6b457ec6bf89016dcd183f105a9c5fb4d960be))
- [G2P-4924](https://openg2p.atlassian.net/browse/G2P-4924) Seed AWE approval policies for Farmer Registry ([`3134a03`](https://github.com/OpenG2P/farmer-registry/commit/3134a03dc3ac925c4b28e771bdc5b1f374b453ae))
- [G2P-5028](https://openg2p.atlassian.net/browse/G2P-5028) feat(services): implement domain validation utilities for various services ([`e79ad62`](https://github.com/OpenG2P/farmer-registry/commit/e79ad6217157667b9165ab50bcb580acc6276618))
- [G2P-4932](https://openg2p.atlassian.net/browse/G2P-4932) feat(db-seed): enhance Docker setup for template uploads ([`0757a8f`](https://github.com/OpenG2P/farmer-registry/commit/0757a8f8e1c40e8a109a5b5cbedd61fdabddd150))
- [G2P-4932](https://openg2p.atlassian.net/browse/G2P-4932) feat(data): update SQL data models and templates for farmer extension ([`92529eb`](https://github.com/OpenG2P/farmer-registry/commit/92529eb9ac452186cd511926513d40d7c7b827a4))
- refactor(data): update SQL data models and templates for farmer extension ([`1115ab1`](https://github.com/OpenG2P/farmer-registry/commit/1115ab1180ae43a47121657331bd1222629f5781))
- Update SQL data for farmer extension: modify incoming model semantic patterns and enhance g2p register scores ([`d61f6c8`](https://github.com/OpenG2P/farmer-registry/commit/d61f6c8548ad877a97c611a58248666b2aec62ac))
- fix(docker): update Staff Portal UI version in configuration file to 1.1.0 ([`4f2b43f`](https://github.com/OpenG2P/farmer-registry/commit/4f2b43f39a4acfc206d86f0c396da1968df5b1bf))
- build: add Docker configuration files for version 1.1.0 of Celery, Partner API, and Staff Portal API ([`4ac52dc`](https://github.com/OpenG2P/farmer-registry/commit/4ac52dcd7b89b249bc014a60576046a39e8b51a0))
- [G2P-4695](https://openg2p.atlassian.net/browse/G2P-4695) refactor(app): remove poverty score models from initialization process ([`94507ea`](https://github.com/OpenG2P/farmer-registry/commit/94507ea741d1c338c3b736d4b29e946c75ee692d))
- feat(data): add new Jinja2 templates for DCI response and farmer data processing ([`5e2c270`](https://github.com/OpenG2P/farmer-registry/commit/5e2c270178a6067942859ad97eac475961418de4))
- [G2P-4695](https://openg2p.atlassian.net/browse/G2P-4695) refactor(data): update SQL data models and templates for farmer extension ([`ae5987e`](https://github.com/OpenG2P/farmer-registry/commit/ae5987e3bc3e409b0c964de669494fc85e34a2be))
- refactor(id_generator): update farmer ID prefix from 'FAR-' to 'FR-' for consistency ([`e0009b8`](https://github.com/OpenG2P/farmer-registry/commit/e0009b8ec967bd1c170510e652ab5e2135dc4cfa))
- refactor(poverty): rename internal_record_id to link_internal_record_id for clarity ([`b67217f`](https://github.com/OpenG2P/farmer-registry/commit/b67217f0591800ef7ba8cd61f9e03e619b8e462a))
- refactor(models): remove poverty score model and update enums to use StrEnum ([`a002e32`](https://github.com/OpenG2P/farmer-registry/commit/a002e32acc0494e8c3d9f2a11763d3587678fa97))
- refactor(score_compute): replace PMT score computation with new poverty score service ([`f5b6641`](https://github.com/OpenG2P/farmer-registry/commit/f5b66410954cd34d482a480b33ecc5bbfc19959c))
- Renaming configurations to meta_data. ([`9416a3b`](https://github.com/OpenG2P/farmer-registry/commit/9416a3baa69f05deb42736535d1fc94cc79a897f))
- fix(docker): update git branch URL for staff portal UI ([`c3da205`](https://github.com/OpenG2P/farmer-registry/commit/c3da2052525d961b49e4a046814677610cf3b3d5))
- build(docker): update image tag to use 'develop' branch ([`791b3f4`](https://github.com/OpenG2P/farmer-registry/commit/791b3f4b0476ccde04e40cf0b027b814f66c13bc))
- build(docker): update dependencies to use 'develop' branch ([`82fec0f`](https://github.com/OpenG2P/farmer-registry/commit/82fec0fc75f87919053f69c1d548dd34aa0c0a30))
- feat(metadata): add SQL seed data for farmer intake forms and templates ([`167fd06`](https://github.com/OpenG2P/farmer-registry/commit/167fd060ef1e77ab33d4bd2c5c462c901647e7f0))
- [G2P-4694](https://openg2p.atlassian.net/browse/G2P-4694)  feat(models): add async method to link internal record ID ([`17ff7c6`](https://github.com/OpenG2P/farmer-registry/commit/17ff7c6a5009fbe98b0a93248da9dbd7863d587c))
- [G2P-4692](https://openg2p.atlassian.net/browse/G2P-4692) Added. ([`c5e4dfa`](https://github.com/OpenG2P/farmer-registry/commit/c5e4dfa9caa5338ea31f80ff250b96965bbd66cd))
- Initial commit ([`6e3cf83`](https://github.com/OpenG2P/farmer-registry/commit/6e3cf838809c5522a8b0cda15b87f726683ec175))

# Release candidates

<a id="v-1-2-1-rc-326"></a>

## farmer-registry 1.2.1-rc.326 — 2026-11-04

_commit `20a17e4` · changes since 1.2.1-rc.210_
<!-- build:1.2.1-rc.326 revision:20a17e4d9f56bd3df2c4159c041e95e3a00df510 ts:1793780280 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.326](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.326.tgz)

### Summary

- Performance testing enhancements: Added comprehensive performance data collection for async partner search, birth-date range queries, and Celery worker performance, including detailed results and documentation for various test scenarios.
- Documentation overhaul: Significant updates to performance testing documentation, including new reports for partner API and Celery, and restructuring of existing materials for clarity and accessibility.
- CI/CD migration: Transitioned CI from GitHub Actions to GitLab, streamlining build and publish processes while addressing issues with configuration and dependencies.
- Data integrity improvements: Resolved issues with bulk-sample ID collisions and improved handling of geo dropdowns, ensuring accurate data seeding and API interactions.
- Code refactoring: Removed unused async methods across several models to enhance maintainability and streamline codebase.
- Dependency updates: Adjusted dependency manifests for performance testing scripts and related components, ensuring compatibility and stability across the project.

### Changes

- partner-api perf test measurements ([`2ef9506`](https://github.com/OpenG2P/farmer-registry/commit/2ef95067000ebd7f56be4e882347b6dadab0bb74))
- Add performance data for async partner search ([`cf8f02a`](https://github.com/OpenG2P/farmer-registry/commit/cf8f02a117e5730c5d305bbb53cad269c00552d3))
- [G2P-5839](https://openg2p.atlassian.net/browse/G2P-5839) Collected birth-date range query performance data for expression, predicate, and GraphQL searches at page sizes 100 ([`c853a69`](https://github.com/OpenG2P/farmer-registry/commit/c853a693ce93b388814865801e6aa8ee581b9160))
- Collect performance data for async search ([`fd10b10`](https://github.com/OpenG2P/farmer-registry/commit/fd10b1003f398104468e6c03af92d088bffe0383))
- Add performance testing results ([`1eb2b4e`](https://github.com/OpenG2P/farmer-registry/commit/1eb2b4e090a4ff53250738714957168be48446fb))
- [G2P-5826](https://openg2p.atlassian.net/browse/G2P-5826) Collect ingest data and add scripts for performance testing ([`42e27ec`](https://github.com/OpenG2P/farmer-registry/commit/42e27ec34f6627455655a1a6186b55a9be838cae))
- [G2P-5810](https://openg2p.atlassian.net/browse/G2P-5810) Add partner ingest performance test script ([`364265d`](https://github.com/OpenG2P/farmer-registry/commit/364265db6b829af6dec24d4a3ba250a193aeab64))
- Added links to actual github files for index and table sizes in storage measurements ([`c39ace1`](https://github.com/OpenG2P/farmer-registry/commit/c39ace1f4227f549f28d6a594ca266826c94d559))
- Celery - final measurements ([`86d5355`](https://github.com/OpenG2P/farmer-registry/commit/86d5355db50ba8e24f7927505b630d6ed37aa205))
- Add performance test result images for worker pods in blend scenario ([`3fcdda2`](https://github.com/OpenG2P/farmer-registry/commit/3fcdda279aacaa4e8a17483c9679b8553f7d0ba0))
- Collect deduplication case data and analyze Celery Beat and worker performance ([`7964688`](https://github.com/OpenG2P/farmer-registry/commit/7964688224234702358ce2c6241d8a2ea27bac47))
- Created Celery Documentation for Performance Test ([`eee7f03`](https://github.com/OpenG2P/farmer-registry/commit/eee7f03909b599d38840d1bb6cc615ec15639495))
- [G2P-5765](https://openg2p.atlassian.net/browse/G2P-5765) Record Celery import progress by CSV row and build outgest and import backlogs in the populate scripts ([`d853df2`](https://github.com/OpenG2P/farmer-registry/commit/d853df22671da676dd9debee28f57facf802bd8b))
- Refactor poverty score computation to use contributing attribute configuration and update performance testing documentation with new scenarios and results. ([`705b7c6`](https://github.com/OpenG2P/farmer-registry/commit/705b7c61292f43bf2e527dc1581e1c94622c264b))
- Add result files and images for pods 1-3 ([`4db782b`](https://github.com/OpenG2P/farmer-registry/commit/4db782beb88b5233913ff68c3e776d6316277671))
- Reworked documentation ([`500e285`](https://github.com/OpenG2P/farmer-registry/commit/500e285d18d0bc775f1cee83e8671b0fff12304a))
- [G2P-5735](https://openg2p.atlassian.net/browse/G2P-5735) Collected data for farmer poverty score completion and validated score computation. ([`4671cb7`](https://github.com/OpenG2P/farmer-registry/commit/4671cb7cab547e897465069bfc9d3743599d3b33))
- [G2P-5728](https://openg2p.atlassian.net/browse/G2P-5728) Add performance testing scripts for Celery backlog observation and Kubernetes case execution, with SQL, preflight checks, and dependency updates. ([`9e044f4`](https://github.com/OpenG2P/farmer-registry/commit/9e044f4ad4016afb7e5b9884341bab0d3ffb9624))
- [G2P-5713](https://openg2p.atlassian.net/browse/G2P-5713) Add in-cluster performance metrics ([`1bf24e0`](https://github.com/OpenG2P/farmer-registry/commit/1bf24e0fa66c8b75b52f3f8754e727005caa205e))
- [G2P-5713](https://openg2p.atlassian.net/browse/G2P-5713) Add performance metrics for 50M data volume ([`e61374e`](https://github.com/OpenG2P/farmer-registry/commit/e61374e04dd631e15af7e6a9a694cfa9f61ca6cf))
- Add table and index sizes for 50M ([`9656be7`](https://github.com/OpenG2P/farmer-registry/commit/9656be726a03cd90ac5c83a1db1f4197dcc789c7))
- Update rebuild-indexes job configuration and enhance index rebuilding script ([`406a45d`](https://github.com/OpenG2P/farmer-registry/commit/406a45d9a73b5a4b501af23eee268d812c4c621c))
- More changes to documentation ([`af50147`](https://github.com/OpenG2P/farmer-registry/commit/af50147d2ed3d828cae4f6c3578be3ac750a28a8))
- [G2P-5693](https://openg2p.atlassian.net/browse/G2P-5693) Add configurable 50M farmer seeding setup ([`f088407`](https://github.com/OpenG2P/farmer-registry/commit/f088407840b9b123a6934b625741c33e8d0ceb0e))
- Edited seeding-design and environment-topology - corrections ([`690108f`](https://github.com/OpenG2P/farmer-registry/commit/690108ff0572f20db986e4a8ff1da00278bb277d))
- brought back documentation for WIP ([`4bac2b2`](https://github.com/OpenG2P/farmer-registry/commit/4bac2b2928a90487fc5f96004b8f010bba36066d))
- moved documentation to openg2p-documentation ([`aa179d6`](https://github.com/OpenG2P/farmer-registry/commit/aa179d6f52b787f1f497e029b979d010cd5683ff))
- [G2P-5690](https://openg2p.atlassian.net/browse/G2P-5690) Add soak test performance data ([`8d4a37f`](https://github.com/OpenG2P/farmer-registry/commit/8d4a37fb99dd9d8aa635aa6651e1a40b403f18be))
- Add results from in-cluster performance tests ([`c164da5`](https://github.com/OpenG2P/farmer-registry/commit/c164da5989ee3daf2c0095194b65ff5e5a6892d8))
- Changes to documentation ([`814559c`](https://github.com/OpenG2P/farmer-registry/commit/814559cd453f71abe0b0a76ade2316604fbc52de))
- [G2P-5689](https://openg2p.atlassian.net/browse/G2P-5689) Implemented in-cluster soak testing ([`ea63109`](https://github.com/OpenG2P/farmer-registry/commit/ea631099cf784a44485f2b0d2b29781f43c1b6ac))
- [G2P-5681](https://openg2p.atlassian.net/browse/G2P-5681) Add performance test data for blend scenario primary volume ([`9fd4e79`](https://github.com/OpenG2P/farmer-registry/commit/9fd4e796086dd9feabd618da2b739f3775fee359))
- [G2P-5681](https://openg2p.atlassian.net/browse/G2P-5681) Add performance test data to Pod 3 primary volume ([`2701c7a`](https://github.com/OpenG2P/farmer-registry/commit/2701c7a3245d5b7d4f34908cf22ab1c5326d378f))
- [G2P-5681](https://openg2p.atlassian.net/browse/G2P-5681) Add performance test data to Pod 2 primary volume ([`2f9d904`](https://github.com/OpenG2P/farmer-registry/commit/2f9d904b8574f3c1ade7290c7b40ed05fb27488d))
- [G2P-5681](https://openg2p.atlassian.net/browse/G2P-5681) Add performance test data to Pod 1 primary volume ([`4d0f580`](https://github.com/OpenG2P/farmer-registry/commit/4d0f5807d3defc0e97fa9b2caa79aa22bb027728))
- [G2P-5678](https://openg2p.atlassian.net/browse/G2P-5678)  Add CPU monitoring and SLO adjustments ([`1352f32`](https://github.com/OpenG2P/farmer-registry/commit/1352f32b6ee85e8cbab7500e26d220bc60ee6897))
- Add results for primary volume ([`0520f97`](https://github.com/OpenG2P/farmer-registry/commit/0520f9783aa8029b3b5955a329200a1a934088c3))
- Add table_sizes.txt to document primary volume table sizes and row counts ([`d19df56`](https://github.com/OpenG2P/farmer-registry/commit/d19df5605605cb3b51c263479a8e9ab1e40709cd))
- [G2P-5669](https://openg2p.atlassian.net/browse/G2P-5669) Add rebuild indexes job and script for missing live indexes ([`02ac515`](https://github.com/OpenG2P/farmer-registry/commit/02ac515d3b293eb80eb5cdbaf5feceda701a7620))
- worked on final-report for realistic user modeling ([`0a893aa`](https://github.com/OpenG2P/farmer-registry/commit/0a893aa12c2580eeb3214eb4d4b109af909ffb41))
- Enhance performance testing seeding configuration ([`b66236a`](https://github.com/OpenG2P/farmer-registry/commit/b66236af113f4d759a4c4ee42b0cec7e044f98cb))
- [G2P-5668](https://openg2p.atlassian.net/browse/G2P-5668) Add Kubernetes job generation and seeding scripts ([`eb68120`](https://github.com/OpenG2P/farmer-registry/commit/eb681205c0a292bdc8cee40e464789b3c48af829))
- update final-report.md -- performance testing ([`28c0c4a`](https://github.com/OpenG2P/farmer-registry/commit/28c0c4ae430dd857f6b6a68253fc74bbb01cd29a))
- Added performance data for all testcases ([`142e256`](https://github.com/OpenG2P/farmer-registry/commit/142e256a0c249ffe8ea72e05862db87d493884fc))
- Collect performance data for all test cases with a 3 pod ([`28f92d7`](https://github.com/OpenG2P/farmer-registry/commit/28f92d722e3b864a2c35d640046c2820ca61a551))
- Collect performance data for all test cases with a 3 pod ([`2a2a8c0`](https://github.com/OpenG2P/farmer-registry/commit/2a2a8c0b00fd681df9cabf06d5658a1b2deec25d))
- Collect performance data for all test cases with a 2 pod ([`764d798`](https://github.com/OpenG2P/farmer-registry/commit/764d798fe54934cf5c3eef3fd8538a9068bb7467))
- Collect performance data for all test cases with a single pod ([`06f8097`](https://github.com/OpenG2P/farmer-registry/commit/06f80979cca8249c3252a620e66508b75aad9e5e))
- Refactor performance testing scripts for change request and intake approval flows ([`a88a4f7`](https://github.com/OpenG2P/farmer-registry/commit/a88a4f7b721f7aba8dd8daabb2d429d3a7e1245c))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Fix the base images: they come from registry-platform, not this repo ([`49756e3`](https://github.com/OpenG2P/farmer-registry/commit/49756e3f90755e25a349015d946beaf777afec99))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the performance-test branch with GitHub ([`f904a69`](https://github.com/OpenG2P/farmer-registry/commit/f904a6950d24c7a469ca3a8687c7d5d4b5922a53))
- [G2P-5520](https://openg2p.atlassian.net/browse/G2P-5520) Enhanced performance testing for intake and change request flows with realistic search scenarios, warmup-aware ramping, improved change request tracking and approval ordering, and support for both successful and intentional miss scenarios. ([`416f48b`](https://github.com/OpenG2P/farmer-registry/commit/416f48b5ad97d05a8c87239bdbfc091bb22d1371))
- Failures should not affect ramp up logic. Only SLOs influence Ramp up ([`31350c2`](https://github.com/OpenG2P/farmer-registry/commit/31350c27db728a653ff02b6d1e44147d755aea81))
- Modified the test harness to run for 15 minutes at top users and not break at first failure ([`bdb20b7`](https://github.com/OpenG2P/farmer-registry/commit/bdb20b7fe2802730aabd0df1185d98b8c08ec546))
- Updated seed_manifest.json ([`69da4ff`](https://github.com/OpenG2P/farmer-registry/commit/69da4ffd25d7cddcd92865fcba1ab7534a15d630))
- Add AWE integration in change request and intake approval processes ([`b3de289`](https://github.com/OpenG2P/farmer-registry/commit/b3de28908c572afa12980a2171c203749eeb547b))
- Add seed manifest generation and remove obsolete performance templates ([`bee2c80`](https://github.com/OpenG2P/farmer-registry/commit/bee2c80bda0d7c178d97c2c177c5db7250ea12ab))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`b2cda40`](https://github.com/OpenG2P/farmer-registry/commit/b2cda40ae3ff83f6b189a43fd8c160bed6dda398))
- Bumped up RP version to 0.0.0-develop.383 ([`ec8828c`](https://github.com/OpenG2P/farmer-registry/commit/ec8828c439ff33ac65bfb502bdb3bad5358c14d1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare score against both farmer and household. A single install carries both — the bulk generator attaches scores to farmers and the sample loader to households, 5,671 and 6 on a reference install — so naming one parent silently stripped the id and the geography from every row of the other. ([`40556c9`](https://github.com/OpenG2P/farmer-registry/commit/40556c9a6b4ea4f0791f3a2e30a8fbaa428c85ef))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate fr_rpt_crop from declarations instead of hand-written SQL. Verified byte-identical to the previous definition across all seventeen shared columns and 757 rows before the SQL was removed; it keeps its materialization and indexes, and additionally carries the geo pcodes and workflow columns the hand-written version omitted. ([`699b3a2`](https://github.com/OpenG2P/farmer-registry/commit/699b3a283105c25a82b7c87608afb18a1d28a61f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare the household member age bands, matching fr_rpt_farmer's edges. The generator derives an age wherever it withholds a birth date, but where the bands fall is policy, and defining them twice with different edges is how two charts come to disagree about how many people are under 25. ([`6daa47a`](https://github.com/OpenG2P/farmer-registry/commit/6daa47af0c0b0abd14b6b4b701db197ac6fd2839))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the mechanical reporting views from the platform generator. reporting.yaml declares the entity tree, names farmer/land/crop as hand-written and marks the cooperative name columns as organisations rather than people; the generated ten add livestock, inputs, membership, scores, households, members, change requests, record history and geo_levels, which used to be derived from registered rows and so was empty on a production install. ([`11e3b8b`](https://github.com/OpenG2P/farmer-registry/commit/11e3b8beb7368af5e1dbf8bb6810c6ef08238a18))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Refresh the reporting views on a schedule, instead of relying on Insights to do it. They are materialized, so they held whatever the install produced and every farmer registered afterwards was invisible with no error anywhere; a CronJob now rebuilds them in dependency order resolved from pg_depend, on analytics.reportingViews.refreshSchedule. ([`8f93c33`](https://github.com/OpenG2P/farmer-registry/commit/8f93c337cbc07bcef9de94f12633572297c92e9f))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) fix: correct ui configuration for multiple sections and add dedicated parent lookup sections for crop intake and crop register ([`2f172d4`](https://github.com/OpenG2P/farmer-registry/commit/2f172d4848fecc02c08f9c5a9e83edb76888ba53))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix bulk-sample id collisions: sub-table functional ids were uuid[:8], which collides by the birthday bound (100k farmers died at ~39k crops on ix_g2p_register_crops_functional_record_id) — use sequential counters like the farmer ids already do ([`d39deba`](https://github.com/OpenG2P/farmer-registry/commit/d39deba138813845cc34ea701b885ed763833836))
- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) Fix AWE seed aborting on shared-DB policy_key clash: untargeted ON CONFLICT DO NOTHING (uq_policy_key_version was unguarded by the id-targeted clause) plus FK-orphan filters on stages/rules, so a policy another registry already owns no longer takes the whole batch — and the farmer policy — down with it ([`43afe27`](https://github.com/OpenG2P/farmer-registry/commit/43afe27ad81c2fedd13e22c35d1d1029c78882ae))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fall back to this registry's own Superset connection name when the release is gone. The name was only ever read from `helm get values`, so uninstalling from Rancher — or running helm uninstall first — skipped the dashboard cleanup with a quiet warning and left the dashboards, charts, datasets and connection in the shared Superset, where the next install adopted them by UUID. ([`a445d51`](https://github.com/OpenG2P/farmer-registry/commit/a445d51fc54913d9fd0127e138f3213d748b4410))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Skip the dashboard import when Superset is absent instead of failing the install. Superset is a separate release and analytics is optional, but the gate exited 1 after waiting, so a registry installed without a reporting stack failed outright. The gate is checked in the init container AND the main one, because an init container exiting 0 does not stop the pod; set analytics.dashboards.superset.required=true where a silent skip would be worse. ([`2e3a06a`](https://github.com/OpenG2P/farmer-registry/commit/2e3a06a243dc3a44d8485622deae1b9f4d07aa25))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add the maps content and publish it as an image. Insights draws maps from a registry-specific image; without one, FR installs fell back to the reference content, which queries nsr_rpt_* and poverty measures FR does not have. Queries plot land tenure, input use and cooperative membership from fr_rpt_farmer/fr_rpt_crop, and are validated against a live FR database. ([`6aac6b7`](https://github.com/OpenG2P/farmer-registry/commit/6aac6b7b128d3ed896c70cae283af39cd25a49ac))
- Fixes in data seeding. ([`7af358a`](https://github.com/OpenG2P/farmer-registry/commit/7af358afa6577cce069d120c54b7cc2f892e94fe))
- Bumped up RP version to 0.0.0-develop.346 ([`f19c12d`](https://github.com/OpenG2P/farmer-registry/commit/f19c12dd57340798ff7de921c17ebb179eb4fc3a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) DB-seed: take ownership of load_sample_data.py and upload_images.py from the platform image ([`003ac5d`](https://github.com/OpenG2P/farmer-registry/commit/003ac5de37ee21bb695b23bc492248c0b68d5f6a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Analytics: add FR reporting views, bulk sample generator, Superset bundle (5 dashboards/45 charts) and the analytics Jobs; declare the DB globals the wrapper's own templates need ([`932aa5a`](https://github.com/OpenG2P/farmer-registry/commit/932aa5a4ddf7b9c9a0ebb4b30096ad67c22758df))
- [G2P-2804](https://openg2p.atlassian.net/browse/G2P-2804) Analytics: add FR reporting layer (fr_rpt_farmer, fr_rpt_land, fr_rpt_geo_levels) — area normalised to hectares, crops/livestock/inputs rolled off the land grain ([`30672a4`](https://github.com/OpenG2P/farmer-registry/commit/30672a410c1fc942b9bdd1e4b544ab337e507436))
- questions.yaml copied during CI ([`ae32039`](https://github.com/OpenG2P/farmer-registry/commit/ae32039b18158b8ade948311e02681bc6442dadd))
- Bumped up RP version ([`5cae5e3`](https://github.com/OpenG2P/farmer-registry/commit/5cae5e38b01f7c598811f49f7451bd30d4ea50d1))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Chart: fix values.yaml clobbered by the CI migration (yq line offset; staffApi/partnerApi pointed at the wrong images); take registry-platform 0.0.0-develop.343 from the GitLab charts registry ([`c989a9d`](https://github.com/OpenG2P/farmer-registry/commit/c989a9db99f52fb64fa871219abd7adde8222ea4))
- Data related changes. ([`d66f1a6`](https://github.com/OpenG2P/farmer-registry/commit/d66f1a697e05a5b78b9c6b9a4eddc72b727354be))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Enable the Master Data path and stop seeding a second geography. loadGeoData was still true, which runs the legacy slug-path loader over the hierarchy master-data already holds from its country pack — two hierarchies, one of which joins to nothing. Also enables loadAttributes with the agriculture domain, and syncGeoWidgets. ([`e2d45bc`](https://github.com/OpenG2P/farmer-registry/commit/e2d45bc2153058f54bd5a0f13f4ac49394827f15))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`1cc19d0`](https://github.com/OpenG2P/farmer-registry/commit/1cc19d0410a71c7c7d45ae5458d64519a1457c47))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix the two geo dropdowns. They carried a hardcoded dev-environment URL and no service/endpoint, so the widget layer bailed before making the request and the dropdowns never populated. Now resolved through master-data like every other api widget, with levels that match the default country pack. ([`79edff5`](https://github.com/OpenG2P/farmer-registry/commit/79edff5679c097d400c4ce645f28b383ceae32cc))
- [G2P-5412](https://openg2p.atlassian.net/browse/G2P-5412) Refactor: Remove unused async methods for linking internal record IDs in various models (crop, farm inputs, farmer, household member, land, livestock, membership details) to streamline code and improve maintainability. ([`c5ab693`](https://github.com/OpenG2P/farmer-registry/commit/c5ab69323dd7435a93ae3572213fd5dfdec6a71f))

<a id="v-1-2-1-rc-210"></a>

## farmer-registry 1.2.1-rc.210 — 2026-10-30

_commit `4166d39` · changes since 1.2.1-rc.199_
<!-- build:1.2.1-rc.210 revision:4166d399c10ff8b94dba5dba7f55fccdc9d654df ts:1793352490 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.210](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.210.tgz)

### Summary

- **Major:** Refactor SQL insert statements for G2P registry and intake forms, reintroducing household farmer personal identification and socio-economic sections, while removing household intake.
- Version updates: Bumped RP_VERSION to 1.2.2-rc.625 and 1.2.2-rc.557 in Dockerfiles and Chart.yaml, and updated Docker images for celery, partner-api, and staff-api.
- Feature enhancements: Added validation for household state and farmer household status during intake submission.
- SQL updates: Revised section order for farmer intake forms and added new SQL entries for household and outgoing templates.

### Changes

- Update Dockerfiles to use new image names for celery and partner-api; reintroduce SQL insert statements for household farmer personal identification and socio-economic sections in metadata. ([`8334bb3`](https://github.com/OpenG2P/farmer-registry/commit/8334bb31f158dee56c15c1f41b59829c57a70641))
- Bump RP_VERSION to 1.2.2-rc.625 in Dockerfiles and Chart.yaml; update SQL tab section order for farmer intake forms. ([`4063159`](https://github.com/OpenG2P/farmer-registry/commit/40631593f890e117b93b40374d9dc1810e881fa2))
- [G2P-5849](https://openg2p.atlassian.net/browse/G2P-5849) Refactor SQL insert statements for G2P registry and intake forms and remove household intake ([`c13dd55`](https://github.com/OpenG2P/farmer-registry/commit/c13dd55c2cd8d0c000d20b7137c983dcce99f85b))
- Bump RP_VERSION to 1.2.2-rc.557 in Dockerfiles for celery, partner-api, and staff-api ([`3e2b0f5`](https://github.com/OpenG2P/farmer-registry/commit/3e2b0f5b2a431f6778e59457295cdc87e3597212))
- [G2P-5821](https://openg2p.atlassian.net/browse/G2P-5821) feat(intake): validate household state on submit ([`8ae2f70`](https://github.com/OpenG2P/farmer-registry/commit/8ae2f70e9454f41d4ec3d211356488161511a79f))
- [G2P-5821](https://openg2p.atlassian.net/browse/G2P-5821) feat(intake): validate farmer household status ([`9b1afd8`](https://github.com/OpenG2P/farmer-registry/commit/9b1afd8691a3a6a1d7011a978dfc0330b362aba2))
- Update Dockerfiles to use version 1.2.0-rc.434 and refactor image names; add new SQL entries for household and outgoing templates. ([`fb3edf6`](https://github.com/OpenG2P/farmer-registry/commit/fb3edf6bfb8fc13a4f46ad122d69190ee0591cc9))

<a id="v-1-2-1-rc-199"></a>

## farmer-registry 1.2.1-rc.199 — 2026-10-27

_commit `e144e71` · changes since 1.2.1-rc.194_
<!-- build:1.2.1-rc.199 revision:e144e71e1a2e47552bd983af8d11f9c94b120f7c ts:1793104323 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.199](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.199.tgz)

### Summary

- Version update: upgraded RP from 1.2.2-rc.557 to 1.2.2-rc.593 in Dockerfiles and Chart.yaml.
- Data integrity enhancements: added field validation for Farmer Registry section widgets and restricted duplicate values in list sections for land, crop, livestock, and farm input.

### Changes

- Version of RP from 1.2.2-rc.557 to 1.2.2-rc.593 in Dockerfiles and Chart.yaml ([`5782d66`](https://github.com/OpenG2P/farmer-registry/commit/5782d6618f25b9bcc2a089a840a965bebd924e7c))
- [G2P-5841](https://openg2p.atlassian.net/browse/G2P-5841) Add field validation to Farmer Registry section widgets ([`2c04ad9`](https://github.com/OpenG2P/farmer-registry/commit/2c04ad96e768bcb0df5ff4af433ea48b9a6e6b57))
- [G2P-5816](https://openg2p.atlassian.net/browse/G2P-5816) - Restrict duplicate values in list sections such as land, crop, livestock and farm input ([`a91e605`](https://github.com/OpenG2P/farmer-registry/commit/a91e6058e228fefdfbe4b0269e9a0eebc1a5d448))

<a id="v-1-2-1-rc-194"></a>

## farmer-registry 1.2.1-rc.194 — 2026-10-26

_commit `414a62b` · changes since 1.2.1-rc.192_
<!-- build:1.2.1-rc.194 revision:414a62bc65e7280ffdec2dc266ab0b54af066392 ts:1793005546 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.194](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.194.tgz)

### Changes

- [G2P-5835](https://openg2p.atlassian.net/browse/G2P-5835) Integrate staff-ui into Farmer Registry build and configuration ([`a7c6671`](https://github.com/OpenG2P/farmer-registry/commit/a7c6671a7a501d250127358d77fc37700270e4db))

<a id="v-1-2-1-rc-192"></a>

## farmer-registry 1.2.1-rc.192 — 2026-10-23

_commit `ed1e70c` · changes since 1.2.1-rc.190_
<!-- build:1.2.1-rc.192 revision:ed1e70ccf18df5476fa404ed8018e12d55e418fa ts:1792751536 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.192](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.192.tgz)

### Changes

- [G2P-5769](https://openg2p.atlassian.net/browse/G2P-5769): Add staff-ui extensibility support to Farmer Registry ([`0e4af4e`](https://github.com/OpenG2P/farmer-registry/commit/0e4af4e79a0d356f09cf6438f84636cf2e8d9e22))

<a id="v-1-2-1-rc-190"></a>

## farmer-registry 1.2.1-rc.190 — 2026-10-14

_commit `48ddb80` · changes since 1.2.1-rc.188_
<!-- build:1.2.1-rc.190 revision:48ddb804e8c5ab73c98f32d7f3719928a30ee4ea ts:1791978720 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.190](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.190.tgz)

### Changes

- Bump version of RP to 1.2.2-rc.557 in Dockerfiles and Chart.yaml ([`3ecf1ee`](https://github.com/OpenG2P/farmer-registry/commit/3ecf1eec0a93618050f94b869b3c60e76233f6e9))

<a id="v-1-2-1-rc-188"></a>

## farmer-registry 1.2.1-rc.188 — 2026-10-14

_commit `7d86b26` · changes since 1.2.1-rc.182_
<!-- build:1.2.1-rc.188 revision:7d86b2671045f44b26e34d6658cdef6adf3a2c3c ts:1791972342 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.188](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.188.tgz)

### Summary

- Data model updates: revised section identifiers for farmer crop, input, and livestock details in Python and SQL files; changed crop season designation from SUMMER to MEHER.
- Validation improvements: added validation for household data to enhance data integrity.
- UI enhancements: improved dropdown field widgets and made the relationship to head field conditional, with Primary Cooperative Member or Cooperative Union Member status now also conditional.
- Migration updates: modified four migration scripts related to metadata and registry configurations, ensuring alignment with the new data model changes.
- Testing additions: introduced a new test file for dependent field clearing to bolster test coverage.

### Changes

- Update section identifiers in Python and SQL files for farmer crop, input, and livestock details ([`19597f7`](https://github.com/OpenG2P/farmer-registry/commit/19597f7c15e13adf93ce85a630bede8a8826b84e))
- Add validation for household ([`39d3dfa`](https://github.com/OpenG2P/farmer-registry/commit/39d3dfa9798ff1ce6df91c6258822334eec5ca8a))
- [G2P-5791](https://openg2p.atlassian.net/browse/G2P-5791) [G2P-5595](https://openg2p.atlassian.net/browse/G2P-5595) - Update section identifiers in SQL and Python files for farmer crop, input, and livestock details; change crop season from SUMMER to MEHER. ([`3ea84d8`](https://github.com/OpenG2P/farmer-registry/commit/3ea84d831bebf8c1def1c2efd691011aa4cddcb3))
- [G2P-5776](https://openg2p.atlassian.net/browse/G2P-5776) Enhanced widget for dropdown fields ([`f9de3e5`](https://github.com/OpenG2P/farmer-registry/commit/f9de3e57ad11c88bcb330632cbc9359299413e13))
- [G2P-5783](https://openg2p.atlassian.net/browse/G2P-5783) [G2P-5778](https://openg2p.atlassian.net/browse/G2P-5778) - relationship to head field make it conditional and Primary Cooperative Member or Cooperative Union Member is now conditional ([`51cf1ec`](https://github.com/OpenG2P/farmer-registry/commit/51cf1ec24850f8a455960927b9cb04ffff2f961d))

<a id="v-1-2-1-rc-182"></a>

## farmer-registry 1.2.1-rc.182 — 2026-10-06

_commit `94a6152` · changes since 1.2.1-rc.180_
<!-- build:1.2.1-rc.182 revision:94a615273562abc4a3a8269a7baffbda47fe536d ts:1791262209 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.182](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.182.tgz)

### Changes

- Bump version of RP to 1.2.2-rc.536 in Dockerfiles and Chart.yaml ([`1f0d126`](https://github.com/OpenG2P/farmer-registry/commit/1f0d12691d840db2da3c19d24c115cc556613e5f))

<a id="v-1-2-1-rc-180"></a>

## farmer-registry 1.2.1-rc.180 — 2026-10-05

_commit `37670a7` · changes since 1.2.1-rc.179_
<!-- build:1.2.1-rc.180 revision:37670a713aebcb2b9d4da9f050be91fd538c76ad ts:1791181700 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.180](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.180.tgz)

### Changes

- Bump version of RP to 1.2.2-rc.534 ([`37670a7`](https://github.com/OpenG2P/farmer-registry/commit/37670a713aebcb2b9d4da9f050be91fd538c76ad))

<a id="v-1-2-1-rc-179"></a>

## farmer-registry 1.2.1-rc.179 — 2026-10-05

_commit `e5d1fa6` · changes since 1.2.1-rc.178_
<!-- build:1.2.1-rc.179 revision:e5d1fa6a63ba1d24ab716f620a097da916c06271 ts:1791177086 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.179](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.179.tgz)

### Changes

- Bump version of RP to 1.2.2-rc.515 ([`e5d1fa6`](https://github.com/OpenG2P/farmer-registry/commit/e5d1fa6a63ba1d24ab716f620a097da916c06271))

# Develop builds

<a id="v-0-0-0-develop-283"></a>

## farmer-registry — develop 0.0.0-develop.283 (2026-11-07)

_commit `fad6a40` · changes since 0.0.0-develop.282_
<!-- build:0.0.0-develop.283 revision:fad6a40bc2bbda64c1584151e6e0542a2fbc9539 ts:1794010765 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.283](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.283.tgz)

### Changes

- Bumped up RP to 0.0.0-develop.716 ([`fad6a40`](https://github.com/OpenG2P/farmer-registry/commit/fad6a40bc2bbda64c1584151e6e0542a2fbc9539))

<a id="v-0-0-0-develop-282"></a>

## farmer-registry — develop 0.0.0-develop.282 (2026-10-28)

_commit `4fd95fe` · changes since 0.0.0-develop.280_
<!-- build:0.0.0-develop.282 revision:4fd95fed12667819bfc3d40bc7ae5cce2bd597b7 ts:1793152526 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.282](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.282.tgz)

### Summary

- Dependency update: bumped RP to version 0.0.0-develop.625.
- Data model change: updated consent lookup from UIN to FAYDA_FAN for consentSubjectIdTypes.

### Changes

- Bumped up RP to 0.0.0-develop.625 ([`4fd95fe`](https://github.com/OpenG2P/farmer-registry/commit/4fd95fed12667819bfc3d40bc7ae5cce2bd597b7))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Chart: consentSubjectIdTypes UIN → FAYDA_FAN for consent lookup ([`1898811`](https://github.com/OpenG2P/farmer-registry/commit/18988112f4a82578803345b1b094f30158af82e5))

<a id="v-0-0-0-develop-280"></a>

## farmer-registry — develop 0.0.0-develop.280 (2026-10-21)

_commit `3df7c16` · changes since 0.0.0-develop.278_
<!-- build:0.0.0-develop.280 revision:3df7c16309ce1a02c0e4f1f80cc648b43206aab5 ts:1792544115 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.280](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.280.tgz)

### Summary

- Policy management enhancement: introduced data-scope text and updated documentation for Partner Management, including an uninstall note.
- Version bump: updated RP to 0.0.0-develop.621, reflecting ongoing development progress.

### Changes

- Bumped up RP to 0.0.0-develop.621 ([`3df7c16`](https://github.com/OpenG2P/farmer-registry/commit/3df7c16309ce1a02c0e4f1f80cc648b43206aab5))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Policies are in Partner Management: data-scope text, sanity docs and uninstall note ([`93c80f6`](https://github.com/OpenG2P/farmer-registry/commit/93c80f607c7b2ac740e3f3a1e2a292f980723bb1))

<a id="v-0-0-0-develop-278"></a>

## farmer-registry — develop 0.0.0-develop.278 (2026-10-19)

_commit `57111fc` · changes since 0.0.0-develop.276_
<!-- build:0.0.0-develop.278 revision:57111fc95d4ab4458b6c9065aac18749c8dcff8d ts:1792408006 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.278](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.278.tgz)

### Summary

- **Major:** Updated RP version to 0.0.0-develop.615, indicating a significant development milestone.
- Data model changes: Retired CROP_WHEAT in the ETH pack and replaced it with CROP_BREAD_WHEAT for improved clarity in crop categorization.

### Changes

- Bumped up RP version to 0.0.0-develop.615 ([`57111fc`](https://github.com/OpenG2P/farmer-registry/commit/57111fc95d4ab4458b6c9065aac18749c8dcff8d))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) sample crop CROP_WHEAT -&gt; CROP_BREAD_WHEAT (CROP_WHEAT retired in the ETH pack) ([`67b5f21`](https://github.com/OpenG2P/farmer-registry/commit/67b5f218617c279a06a2ae13c720f0b9e4bcd85b))

<a id="v-0-0-0-develop-276"></a>

## farmer-registry — develop 0.0.0-develop.276 (2026-10-08)

_commit `5babaca` · changes since 0.0.0-develop.275_
<!-- build:0.0.0-develop.276 revision:5babaca7d513cf94a7cc6f366b19964f2c021913 ts:1791428709 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.276](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.276.tgz)

### Changes

-  Bumped up RP version to 0.0.0-develop.613 ([`5babaca`](https://github.com/OpenG2P/farmer-registry/commit/5babaca7d513cf94a7cc6f366b19964f2c021913))

<a id="v-0-0-0-develop-275"></a>

## farmer-registry — develop 0.0.0-develop.275 (2026-10-08)

_commit `0c43737` · changes since 0.0.0-develop.273_
<!-- build:0.0.0-develop.275 revision:0c4373721aad868f3c39375ce138897a1ee2cc2a ts:1791424357 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.275](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.275.tgz)

### Summary

- **Major:** Updated RP version to 0.0.0-develop.613 and corrected uninstall script to enhance deployment reliability.
- Helm configuration: Changed IAM registration to use `iamRegister.runAsHook: false`, eliminating warnings related to table overwrites.

### Changes

- Bumped up RP version to 0.0.0-develop.613.  Corrected uninstall script. ([`0c43737`](https://github.com/OpenG2P/farmer-registry/commit/0c4373721aad868f3c39375ce138897a1ee2cc2a))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Helm: IAM registration via iamRegister.runAsHook: false instead of null annotations (removes the "cannot overwrite table with non table" warning) ([`952d06b`](https://github.com/OpenG2P/farmer-registry/commit/952d06b1feef2ee3e6ae50039f51a08184ed22f3))

<a id="v-0-0-0-develop-273"></a>

## farmer-registry — develop 0.0.0-develop.273 (2026-10-07)

_commit `5436422` · changes since 0.0.0-develop.272_
<!-- build:0.0.0-develop.273 revision:5436422bdb048407fa58677877ff34159571cbd0 ts:1791358772 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.273](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.273.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.611 ([`5436422`](https://github.com/OpenG2P/farmer-registry/commit/5436422bdb048407fa58677877ff34159571cbd0))

<a id="v-0-0-0-develop-272"></a>

## farmer-registry — develop 0.0.0-develop.272 (2026-10-07)

_commit `6d6cf31` · changes since 0.0.0-develop.271_
<!-- build:0.0.0-develop.272 revision:6d6cf31ebccf5145c946be72188fb785d3e2dedd ts:1791338063 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.272](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.272.tgz)

### Changes

- Bumped up RP to 0.0.0-develop.608 ([`6d6cf31`](https://github.com/OpenG2P/farmer-registry/commit/6d6cf31ebccf5145c946be72188fb785d3e2dedd))

<a id="v-0-0-0-develop-271"></a>

## farmer-registry — develop 0.0.0-develop.271 (2026-10-05)

_commit `d67f189` · changes since 0.0.0-develop.221_
<!-- build:0.0.0-develop.271 revision:d67f189acf34ec81befdbcb27a94856b8e718ca2 ts:1791165956 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.271](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.271.tgz)

### Summary

- **Major:** CI transition to GitLab, removing GitHub Actions for build and publish processes.
- Data model enhancements: introduced named data scopes for various farmer attributes, improved household member data model and validation, and added null annotations for Rancher compatibility.
- Database improvements: fixed ID authentication widget SQL, updated SQL insert statements for crops and livestock, and corrected field names in household information.
- Docker and Helm updates: aligned Dockerfile versions with registry platform, pointed object store to in-cluster commons Garage, and updated paths in Dockerfiles and Chart.yaml.
- Seeding and data handling: fixed db-seed for fresh deployments, added functionality for data insertion via intake forms, and reduced record seeding count.
- UI and widget improvements: enhanced table cell handling for decimals, improved child change request inheritance, and streamlined domain registration process by removing redundant files.

### Changes

- Bumped up RP version to 0.0.0-develop.604 ([`d67f189`](https://github.com/OpenG2P/farmer-registry/commit/d67f189acf34ec81befdbcb27a94856b8e718ca2))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Data scopes: named scope catalogue (farmer_identifiers, personal_details, contact, location, main_crops, socio_economic_and_health, land, land_location, livestock, farm_inputs, memberships, household, household_location, household_members, poverty_score; no default section scopes); sanity dataScopes/deniedScopes and DCI e2e use scope IDs; test publishes the catalogue and renders a filtered farmer record ([`b63a79e`](https://github.com/OpenG2P/farmer-registry/commit/b63a79ea7ace0ab64b7133d3c40a16a880462ace))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Helm: point the object store at the in-cluster commons Garage (global.minioHost commons-garage:3900, minioSecure false) ([`76ef5db`](https://github.com/OpenG2P/farmer-registry/commit/76ef5db0d57031f002a279214fb59624979a5591))
- Fix db-seed on a fresh deployment: give celery-beat a consumed queue, report why the seed fails ([`46527b5`](https://github.com/OpenG2P/farmer-registry/commit/46527b5db1d7ea81831cf06907416ab6b680457f))
- [G2P-5703](https://openg2p.atlassian.net/browse/G2P-5703) Add null annotations for Rancher compatibility in values.yaml ([`bae8577`](https://github.com/OpenG2P/farmer-registry/commit/bae85776f8f7f1d6cd07217c563ad8a891f1e3a6))
- fix: align openg2p-registry version pins to 1.2.2-rc.489 ([`b009442`](https://github.com/OpenG2P/farmer-registry/commit/b0094425c32195b621e50c087986fd88ede3eba5))
- [G2P-5695](https://openg2p.atlassian.net/browse/G2P-5695) Fix ID authentication widget SQL ([`1c7a311`](https://github.com/OpenG2P/farmer-registry/commit/1c7a3113d0af9638311b2e7e3cc31a1608defa3e))
- Bump version 1.2.2-rc.489 of registry platform in Dockerfile ([`498ffa8`](https://github.com/OpenG2P/farmer-registry/commit/498ffa8e6fc7bfa84d05b88551fdd53a60566ba1))
- Bump version 1.2.2-rc.487 of registry platform in Dockerfile ([`fb6cd5d`](https://github.com/OpenG2P/farmer-registry/commit/fb6cd5d764013c99ee4a26e82884f99ddfa2b2a4))
- Image issues ([`ea5e3fd`](https://github.com/OpenG2P/farmer-registry/commit/ea5e3fda595a607b90289ed497982ba0ab854c3d))
- [G2P-5680](https://openg2p.atlassian.net/browse/G2P-5680) [G2P-5676](https://openg2p.atlassian.net/browse/G2P-5676) ui-widgets decimals in table cells, child change requests inherit the subject record name, partner-api and db-seed fixes ([`73e3037`](https://github.com/OpenG2P/farmer-registry/commit/73e30377460db8762d66e3d33468a319aa1d979f))
- [G2P-5604](https://openg2p.atlassian.net/browse/G2P-5604) Enhance domain services for household and household members ([`5805d9d`](https://github.com/OpenG2P/farmer-registry/commit/5805d9d1147757658e6376b4fb7d1dcbe57e98f1))
- [G2P-5607](https://openg2p.atlassian.net/browse/G2P-5607): include is_head and relationship_to_head in members table configuration ([`407bb1c`](https://github.com/OpenG2P/farmer-registry/commit/407bb1c76e788650fe1b72e1628ae6f1f77738b3))
- [G2P-5616](https://openg2p.atlassian.net/browse/G2P-5616) Enhance household member data model and validation ([`552ec3c`](https://github.com/OpenG2P/farmer-registry/commit/552ec3c4ea0c716b1019e613cb302ba3e4381c42))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Fix the base images: they come from registry-platform, not this repo ([`448e66e`](https://github.com/OpenG2P/farmer-registry/commit/448e66e023a1dfc38f17486804b8a7fdb711ebd6))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.2 release line with GitHub ([`b740b81`](https://github.com/OpenG2P/farmer-registry/commit/b740b8138e502451b11bb2b5cd026dbb2dcf74e9))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Refactor enums and update source of income references ([`6dff669`](https://github.com/OpenG2P/farmer-registry/commit/6dff669117c19d9dc6eb84a3b23fd8643fb8c85d))
- [G2P-5574](https://openg2p.atlassian.net/browse/G2P-5574) Reduce record seeding count from 50 to 25 ([`d33c743`](https://github.com/OpenG2P/farmer-registry/commit/d33c743097d2acd59a25f38199e3c3ba7daaf200))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update Dockerfiles and Chart.yaml to use GitLab registry paths ([`212e9e1`](https://github.com/OpenG2P/farmer-registry/commit/212e9e18e588fc59ba7971ab5fbdea4168d21761))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update Dockerfiles and Chart.yaml to version 1.2.0-rc.419 ([`7db5915`](https://github.com/OpenG2P/farmer-registry/commit/7db5915d453697b102133539c5643b2bbe0303be))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Add seeding to insert data via intake form ([`8dd6d6a`](https://github.com/OpenG2P/farmer-registry/commit/8dd6d6acbcd37be76cd024d1295b2b3f4f09da7c))
- Change in Ui schema and domain translation ([`75f1c68`](https://github.com/OpenG2P/farmer-registry/commit/75f1c685deccc29c8b3d137164ffe35e644c1302))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Add script to upload farmer data and images to MinIO ([`81610dd`](https://github.com/OpenG2P/farmer-registry/commit/81610dd3ffad426f1b9d59a4ee012b8aeffa3ecf))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enable functional_id generation for farmer and household ([`99cf568`](https://github.com/OpenG2P/farmer-registry/commit/99cf5686d7e32376143ce9b34c9ad1e65ddaf4a5))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Delete attribute sql files ([`ddb078f`](https://github.com/OpenG2P/farmer-registry/commit/ddb078f07fb67d41bf746da66c87857f37f6e614))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): update SQL insert statements for crops, livestocks, and farminputs sections ([`6c6dff7`](https://github.com/OpenG2P/farmer-registry/commit/6c6dff730553ca98dba1aa14482b267540936604))
- [G2P-5480](https://openg2p.atlassian.net/browse/G2P-5480) Change land_size field type from string to float in land model and schema ([`161821a`](https://github.com/OpenG2P/farmer-registry/commit/161821a2b04d18095df90277d5f7404b1994cca0))
- [G2P-5524](https://openg2p.atlassian.net/browse/G2P-5524) refactor: remove G2PRegisterDomainFactory and related files to streamline domain registration process ([`ef21f34`](https://github.com/OpenG2P/farmer-registry/commit/ef21f346f57e7a358f18b5109cc8fcaf1649ebc4))
- [G2P-5519](https://openg2p.atlassian.net/browse/G2P-5519) remove redundant repository entries in values.yaml for openg2p-farmer-registry ([`9d9ba7b`](https://github.com/OpenG2P/farmer-registry/commit/9d9ba7b48356181140821ef3ba9d1ea076ce429e))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): Correct field names in household information section ([`675cf2e`](https://github.com/OpenG2P/farmer-registry/commit/675cf2e87eb1bfc8a057f89d0a73ff821857946f))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`37c1731`](https://github.com/OpenG2P/farmer-registry/commit/37c17318828fbcb4274b33e2eb7b649ee77f5f15))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: enhance SQL insert statements for g2p_register_sections with additional metadata and widget configurations for livestock and household member sections ([`ab6c0db`](https://github.com/OpenG2P/farmer-registry/commit/ab6c0db73d01620066ba6d3c745b219f42cb230b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`1062700`](https://github.com/OpenG2P/farmer-registry/commit/1062700737b8129d66fcc363c7d3809863d0cefb))

<a id="v-0-0-0-develop-221"></a>

## farmer-registry — develop 0.0.0-develop.221 (2026-10-03)

_commit `2b3cb0e` · changes since 0.0.0-develop.218_
<!-- build:0.0.0-develop.221 revision:2b3cb0e6f5d4c2f4432bb81b44e303b5d5524f0c ts:1791021149 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.221](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.221.tgz)

### Summary

- **Major:** Transitioned registries to exclusively interact with MDS via its API, removing direct database access and eliminating loadGeoData/syncGeoWidgets functions.
- Reporting enhancement: Large reports over 500 KB are now compressed into a zip file with a summary page for GitBook integration.
- Version bump to RP 0.0.0-develop.599, indicating ongoing development updates.

### Changes

- Bumped up RP version to 0.0.0-develop.599 ([`2b3cb0e`](https://github.com/OpenG2P/farmer-registry/commit/2b3cb0e6f5d4c2f4432bb81b44e303b5d5524f0c))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Registries never touch MDS's database: drop loadGeoData/syncGeoWidgets, seed scripts and analytics Jobs read MDS via its API (mds_client) ([`f44d04b`](https://github.com/OpenG2P/farmer-registry/commit/f44d04b94681efc19c4182f27675e23ed37ba080))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) create_raw_report.py: reports over 500 KB go to a zip with a short summary page for GitBook ([`74be0a9`](https://github.com/OpenG2P/farmer-registry/commit/74be0a94c8c0237b39a98a6cf032e6dee7d6f9f4))

<a id="v-0-0-0-develop-218"></a>

## farmer-registry — develop 0.0.0-develop.218 (2026-10-02)

_commit `ed73955` · changes since 0.0.0-develop.215_
<!-- build:0.0.0-develop.218 revision:ed73955e7f6e0706bdcbcbd819d169935f032161 ts:1790900606 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.218](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.218.tgz)

### Summary

- **Major:** Replaced the Crops tab with a new CROP_COMMODITY multi-select for declared main crops on the farmer, retiring crop register metadata and updating related sample data, DCI, reporting, and dashboards.
- Data model updates: Introduced platform-neutral naming conventions for sanity overlay, including RECORD_* and record_seeded identifiers.
- Version bump: Updated RP version to 0.0.0-develop.453.

### Changes

- Bumped up RP version to 0.0.0-develop.453 ([`ed73955`](https://github.com/OpenG2P/farmer-registry/commit/ed73955e7f6e0706bdcbcbd819d169935f032161))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Sanity overlay: use the platform's neutral names (RECORD_*, record_seeded, cfg.register_id, sanity.registerId); ([`8eeb6c5`](https://github.com/OpenG2P/farmer-registry/commit/8eeb6c59ace1748f0830806b28987c276d6fa3c1))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Replace Crops tab with declared main crops on the farmer (CROP_COMMODITY multi-select); retire crop register metadata on upgrade; main-crop sample data, DCI, reporting and dashboards ([`ee93733`](https://github.com/OpenG2P/farmer-registry/commit/ee93733bcc0b5e39b75eda1e8b5bd36209ff0191))

<a id="v-0-0-0-develop-215"></a>

## farmer-registry — develop 0.0.0-develop.215 (2026-10-01)

_commit `060e2e5` · changes since 0.0.0-develop.211_
<!-- build:0.0.0-develop.215 revision:060e2e5590efac9a4d69f560e5b2a22ca4a19c52 ts:1790829884 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.215](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.215.tgz)

### Summary

- **Major:** Introduced FARMER_ID in farmer records for enhanced identification alongside Fayda UIN.
- New features: Added "Generate bulk demo data" and "Bulk demo farmers" options in the Rancher form, with sample data and images set to default OFF.
- Enhanced DCI functionality: Implemented Cluster entity registration with AWE approval, typed participant roles, and integrated crop-change links, along with sample crop seasons.
- Testing improvements: Updated smoke tests to include partner corrections and added comprehensive tests for new features.

### Changes

- Bumped up RP version to 0.0.0-develop.448 ([`060e2e5`](https://github.com/OpenG2P/farmer-registry/commit/060e2e5590efac9a4d69f560e5b2a22ca4a19c52))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) DCI: farmer record carries FARMER_ID alongside the Fayda UIN ([`12476c1`](https://github.com/OpenG2P/farmer-registry/commit/12476c1f1b016287e390e33a174a26399bf56962))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) FR chart: sample data, sample images and bulk demo data default OFF; add "Generate bulk demo data" and "Bulk demo farmers" to the Rancher form (Analytics), separate from reporting views, which install either way ([`d9b5b11`](https://github.com/OpenG2P/farmer-registry/commit/d9b5b11bedc46017492cc83c430a5dbb489837d3))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) CSR phase 1: Cluster entity register with AWE approval and sample clusters, typed participant roles, entities first (no temporary plot IDs), crop-change link, harvest_verified and replacement links in DCI and reporting view, sample crop seasons from Master Data people, partner correction in smoke test, tests ([`93eef0a`](https://github.com/OpenG2P/farmer-registry/commit/93eef0acda07eb5b6525c9f07653c27abe0dca7f))

<a id="v-0-0-0-develop-211"></a>

## farmer-registry — develop 0.0.0-develop.211 (2026-09-27)

_commit `336e09b` · changes since 0.0.0-develop.209_
<!-- build:0.0.0-develop.211 revision:336e09be2b136bc9f46f04a43c5d47bf95d88642 ts:1790524042 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.211](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.211.tgz)

### Summary

- **Major:** Transition to Master Data 1.1 for live code lists, replacing 12 coded dropdowns with MDS attributes and aligning gender, income, education, and disability codes across various components including enums and templates.
- Code cleanup: Removed lookup-data and streamlined sample and bulk data handling, enhancing search filters and translations.
- Version bump: Updated RP version to 0.0.0-develop.439.

### Changes

- Bumped up RP verison to 0.0.0-develop.439 ([`336e09b`](https://github.com/OpenG2P/farmer-registry/commit/336e09be2b136bc9f46f04a43c5d47bf95d88642))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Read code lists live from Master Data 1.1: switch the 12 coded dropdowns to MDS attributes, drop lookup-data, align gender/income/education/disability codes with MDS across enums, DCI template, sample and bulk data, search filter, translations and perf generators ([`43a8198`](https://github.com/OpenG2P/farmer-registry/commit/43a819885cc7fcf9b914b369c6b3680c28d079e3))

<a id="v-0-0-0-develop-209"></a>

## farmer-registry — develop 0.0.0-develop.209 (2026-09-23)

_commit `84e6d1e` · changes since 0.0.0-develop.207_
<!-- build:0.0.0-develop.209 revision:84e6d1e5eaebda06fe83702a0398f8fb7c06bffc ts:1790150578 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.209](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.209.tgz)

### Summary

- Feature enhancement: Each wallet offer now includes a unique transaction code and a scannable QR code for improved user interaction.
- Version update: The RP version has been incremented to 0.0.0-develop.435, reflecting ongoing development progress.

### Changes

- Bumped up RP version to 0.0.0-develop.435 ([`84e6d1e`](https://github.com/OpenG2P/farmer-registry/commit/84e6d1e5eaebda06fe83702a0398f8fb7c06bffc))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Give each wallet offer its own transaction code and a scannable QR ([`ce9fa75`](https://github.com/OpenG2P/farmer-registry/commit/ce9fa7505c3663166c827463e8d150e78bd4cc0c))

<a id="v-0-0-0-develop-207"></a>

## farmer-registry — develop 0.0.0-develop.207 (2026-09-12)

_commit `8387808` · changes since 0.0.0-develop.206_
<!-- build:0.0.0-develop.207 revision:8387808ba50182ec6e2ae8389ae55ebdcce36356 ts:1789175674 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.207](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.207.tgz)

### Changes

- Bumped up RP version to develop 0.0.0-develop.432 ([`8387808`](https://github.com/OpenG2P/farmer-registry/commit/8387808ba50182ec6e2ae8389ae55ebdcce36356))

<a id="v-0-0-0-develop-206"></a>

## farmer-registry — develop 0.0.0-develop.206 (2026-09-03)

> **Note** — **Intermediate Stable Version**. VC issuance and verification both working fine. Compatible with commons 0.0.0-develop.243.

_commit `fa11515` · changes since 0.0.0-develop.205_
<!-- build:0.0.0-develop.206 revision:fa1151506041d30b5a4ca0242e99c19da19b07f7 ts:1788434449 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.206](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.206.tgz)

### Changes

- Bumped up RP version to 0.0.0-develop.430 ([`fa11515`](https://github.com/OpenG2P/farmer-registry/commit/fa1151506041d30b5a4ca0242e99c19da19b07f7))

<a id="v-0-0-0-develop-205"></a>

## farmer-registry — develop 0.0.0-develop.205 (2026-09-02)

_commit `ce948e3` · changes since 0.0.0-develop.203_
<!-- build:0.0.0-develop.205 revision:ce948e3f695f66ab088fff7d54f7cf7be8e2189e ts:1788339305 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.205](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.205.tgz)

### Summary

- Domain management: transitioned to deriving all hostnames from `baseDomain`, eliminating hardcoded domains for improved flexibility.
- Versioning: updated RP version to 0.0.0-develop.429, reflecting ongoing development progress.

### Changes

- Bumped up RP version to 0.0.0-develop.429 ([`ce948e3`](https://github.com/OpenG2P/farmer-registry/commit/ce948e3f695f66ab088fff7d54f7cf7be8e2189e))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Derive every hostname from baseDomain instead of hardcoding the domain ([`3315fc1`](https://github.com/OpenG2P/farmer-registry/commit/3315fc15b7a96d2435195f87297613b9eea6813b))

<a id="v-0-0-0-develop-203"></a>

## farmer-registry — develop 0.0.0-develop.203 (2026-09-02)

_commit `b0705ee` · changes since 0.0.0-develop.201_
<!-- build:0.0.0-develop.203 revision:b0705ee67c5fdc8b706267b52c2c52e536b27b44 ts:1788310982 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.203](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.203.tgz)

### Summary

- **Major:** Dropped the claim-169 Data issuer key, resolving an issue with overwriting Language.
- Version bump to RP 0.0.0-develop.428.

### Changes

- Bumped up RP version to 0.0.0-develop.428 ([`b0705ee`](https://github.com/OpenG2P/farmer-registry/commit/b0705ee67c5fdc8b706267b52c2c52e536b27b44))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Drop the claim-169 Data issuer key that overwrote Language ([`c977a89`](https://github.com/OpenG2P/farmer-registry/commit/c977a89db98d36299af770ed4cb3ab3d15d746a8))

<a id="v-0-0-0-develop-201"></a>

## farmer-registry — develop 0.0.0-develop.201 (2026-09-01)

_commit `c0f00c4` · changes since 0.0.0-develop.198_
<!-- build:0.0.0-develop.201 revision:c0f00c4c60bdf61adab8aac05f111fc315e19d50 ts:1788242760 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.201](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.201.tgz)

### Summary

- User interface updates: implemented Roboto font across the agent portal and included Farmer ID in QR codes.
- Credential verification enhancements: added visibility and audit capabilities for the checks performed during credential verification.
- Version bump: updated RP version to 0.0.0-develop.426.

### Changes

- Bumped up RP version to 0.0.0-develop.426 ([`c0f00c4`](https://github.com/OpenG2P/farmer-registry/commit/c0f00c4c60bdf61adab8aac05f111fc315e19d50))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Use Roboto throughout the agent portal and carry the Farmer ID in the QR ([`1d92a57`](https://github.com/OpenG2P/farmer-registry/commit/1d92a57e1089c5e08ed7e94a3caec29968423eb0))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Show and audit what a credential verification actually checked ([`fb85c12`](https://github.com/OpenG2P/farmer-registry/commit/fb85c12af40542f5688d6868c173f9db2ad31a43))

<a id="v-0-0-0-develop-198"></a>

## farmer-registry — develop 0.0.0-develop.198 (2026-09-01)

_commit `a68e552` · changes since 0.0.0-develop.196_
<!-- build:0.0.0-develop.198 revision:a68e552aa9bc35a24975f3d57ba7acf196b23fd5 ts:1788224900 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.198](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.198.tgz)

### Summary

- **Major:** Upgraded RP version to 0.0.0-develop.424, introducing significant changes in the development branch.
- New feature: Added a credential-verification switch to enhance security and control over user authentication processes.

### Changes

- Bumped up RP version to 0.0.0-develop.424 ([`a68e552`](https://github.com/OpenG2P/farmer-registry/commit/a68e552aa9bc35a24975f3d57ba7acf196b23fd5))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add the credential-verification switch ([`1cad544`](https://github.com/OpenG2P/farmer-registry/commit/1cad54408cf651a9d31768e3a1e98a0df2512e59))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
