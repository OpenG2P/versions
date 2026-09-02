# farmer-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/farmer-registry](https://github.com/OpenG2P/farmer-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.203`](#v-0-0-0-develop-203) | 2026-09-02 | develop |  |
| [`0.0.0-develop.201`](#v-0-0-0-develop-201) | 2026-09-01 | develop |  |
| [`0.0.0-develop.198`](#v-0-0-0-develop-198) | 2026-09-01 | develop |  |
| [`1.2.1-rc.159`](#v-1-2-1-rc-159) | 2026-08-28 | release candidate |  |
| [`0.0.0-develop.196`](#v-0-0-0-develop-196) | 2026-08-28 | develop | **Intermediate Stable Version**. Installs fine after moving back to GitHub. Has Verifiable Credentials (Basic) integrated. Compatible with 0.0.0-develop.235 of commons. |
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

<a id="v-1-2-1-rc-159"></a>

## farmer-registry 1.2.1-rc.159 — 2026-08-28

_commit `448e66e` · changes since 1.2.0_
<!-- build:1.2.1-rc.159 revision:448e66e023a1dfc38f17486804b8a7fdb711ebd6 ts:1787898576 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.159](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.159.tgz)

### Summary

- **Major:** CI transition to GitLab with removal of GitHub Actions for build and publish processes.
- Docker updates: modified Dockerfiles and Chart.yaml to utilize GitLab registry paths and version 1.2.0-rc.419.
- Data model changes: changed land_size field type from string to float, refactored enums, and updated SQL insert statements for crops, livestock, and household sections.
- Record management: reduced record seeding count from 50 to 25 and added seeding functionality for data insertion via intake forms.
- Domain simplification: removed G2PRegisterDomainFactory and related files to streamline the domain registration process.
- Functional enhancements: enabled functional_id generation for farmers and households, and added a script for uploading farmer data and images to MinIO.
- Schema adjustments: updated UI schema and corrected field names in household information sections.

### Changes

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

# Develop builds

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

<a id="v-0-0-0-develop-196"></a>

## farmer-registry — develop 0.0.0-develop.196 (2026-08-28)

> **Note** — **Intermediate Stable Version**. Installs fine after moving back to GitHub. Has Verifiable Credentials (Basic) integrated. Compatible with 0.0.0-develop.235 of commons.

_commit `07f0237` · changes since 1.3.0_
<!-- build:0.0.0-develop.196 revision:07f02374a8d7d6de89c0261f785a0740c4f16818 ts:1787884394 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.196](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.196.tgz)

### Summary

- **Major:** Migration to GitLab for the farmer registry repository, with GitHub build/publish disabled.
- Version updates: Incremented RP version multiple times, culminating in 0.0.0-develop.417.
- Feature enhancements: Enabled VC issuance and agent portal by default, added farmer credential issuance behind a disabled switch, and shipped claim-169 QR config requiring registrant authentication.
- Data handling improvements: Normalised foundational ID, fixed full name spacing in VC views, and seeded the pack's real birth date instead of a default.
- Reporting updates: Declared scores against both farmer and household, generated fr_rpt_crop from declarations, and refreshed reporting views on a schedule.
- Configuration adjustments: Created VC card ConfigMap on agent portal deployment and corrected field names in household information.
- Cleanup: Removed obsolete performance templates and dropped duplicated VC questions inherited from the registry subchart.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`07f0237`](https://github.com/OpenG2P/farmer-registry/commit/07f02374a8d7d6de89c0261f785a0740c4f16818))
- Bumped up RP version to 0.0.0-develop.417 ([`777b647`](https://github.com/OpenG2P/farmer-registry/commit/777b647680dcce77e351c4bea6a0eebf88387623))
- Bumped up RP version to 0.0.0-develop.415 ([`2855ab9`](https://github.com/OpenG2P/farmer-registry/commit/2855ab96152250e47cc8554c2496172b2ad8816f))
- Bumped up RP version to 0.0.0-develop.414 ([`9ce672b`](https://github.com/OpenG2P/farmer-registry/commit/9ce672bded8ff68a18e77df2f91c92726e329eeb))
- Bumped up RP version to 0.0.0-develop.411 ([`2b0ed75`](https://github.com/OpenG2P/farmer-registry/commit/2b0ed755c6d3457ca85679cba7fc74196570e857))
- Bumped up RP version to 0.0.0-develop.409 ([`605343d`](https://github.com/OpenG2P/farmer-registry/commit/605343dae8893675263558be8775978424027260))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Build a farmer agent-portal-api image so it maps the farmer register model. Bumped up RP version. ([`e0dae0b`](https://github.com/OpenG2P/farmer-registry/commit/e0dae0bb54567b257263414ea49501c441ab2e4b))
- Bumped up RP version to 0.0.0-develop.408. ([`dd71272`](https://github.com/OpenG2P/farmer-registry/commit/dd7127209ae96e8186d1f83ea05f46903394d5a5))
- Bumped up RP version to 0.0.0-develop.406 ([`8022dfc`](https://github.com/OpenG2P/farmer-registry/commit/8022dfcbcb92bd39b81682a6024997b3274004a1))
- Bumped up RP version to 0.0.0-develop.404 ([`6e3a1f8`](https://github.com/OpenG2P/farmer-registry/commit/6e3a1f8ad8348e6cb082aa15b8b111306ec7ed87))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Point master data DB credentials at the renamed secret ([`ffcc9e7`](https://github.com/OpenG2P/farmer-registry/commit/ffcc9e7f39b441d6e532b2199275427a4ffa1f16))
- Bumped up RP version to 0.0.0-develop.403 ([`9c608d9`](https://github.com/OpenG2P/farmer-registry/commit/9c608d91cdce3713f79c40220fd738c2d3426f60))
- Bumped up RP version to 0.0.0-develop.402 ([`ffb2c75`](https://github.com/OpenG2P/farmer-registry/commit/ffb2c759bf707fd02b6f760f9839eab21e8f653c))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ship the claim-169 QR config and require registrant authentication ([`acecdce`](https://github.com/OpenG2P/farmer-registry/commit/acecdcedc1261127d012eaca9a5268feaa849e58))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable VC issuance by default ([`7484b69`](https://github.com/OpenG2P/farmer-registry/commit/7484b69721348a1dc415d9a9e1a28b74ee4edd1f))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise foundational ID and fix full name spacing in the VC view ([`f6d4c53`](https://github.com/OpenG2P/farmer-registry/commit/f6d4c53dea0db69353e9493117ec1b431bc32c13))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix full name spacing in the farmer VC view ([`fbf66e2`](https://github.com/OpenG2P/farmer-registry/commit/fbf66e28522d5981bf82a0ad99478f7846682f42))
- Bumped up RP version to 0.0.0-develop.392 ([`4196dd6`](https://github.com/OpenG2P/farmer-registry/commit/4196dd6d0c95e79c00e14b5afd04557003f0dcd3))
- Bumped up RP version to 0.0.0-develop.391 ([`1762516`](https://github.com/OpenG2P/farmer-registry/commit/1762516054f3fc491d42cb2e885819f4f99dddf7))
- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Seed the pack's real birth date instead of inventing 1 January. The pack carried only a year, so every sample farmer in the country shared a birthday; older packs still fall back, since a date column cannot hold a year. ([`a74feca`](https://github.com/OpenG2P/farmer-registry/commit/a74fecacc096f7a06ff97c70dc951e2545ec7540))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Create the VC card ConfigMap whenever the agent portal is deployed ([`94abb14`](https://github.com/OpenG2P/farmer-registry/commit/94abb142887918217bf503ad12eabe3e0555d1d7))
- Bumped up RP version to 0.0.0-develop.389 ([`1b1a77b`](https://github.com/OpenG2P/farmer-registry/commit/1b1a77b3e9612b95e9f5f79247c733b42cd81c61))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal by default ([`ca4d6ee`](https://github.com/OpenG2P/farmer-registry/commit/ca4d6ee1061b1cc59874c5edf0b33f04b1882c42))
- Bumped up RP version to 0.0.0-develop.388 ([`dfe77b7`](https://github.com/OpenG2P/farmer-registry/commit/dfe77b79d88e9bb50b55ffea5fbb6309316e11f1))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Drop duplicated VC questions inherited from the registry subchart. Bumped up RP version. ([`a29871f`](https://github.com/OpenG2P/farmer-registry/commit/a29871fe6a6052c530afa250176172a7e3ee0955))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add farmer credential issuance behind a disabled-by-default switch ([`95e4214`](https://github.com/OpenG2P/farmer-registry/commit/95e42143af43a28e72b33f6c4b7855adefd5d415))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): Correct field names in household information section ([`8599e27`](https://github.com/OpenG2P/farmer-registry/commit/8599e272b4ff53ece192c92f60f6eca9cd4fb16a))
- Bumped up RP version to 0.0.0-develop.384 ([`98180a1`](https://github.com/OpenG2P/farmer-registry/commit/98180a19c65cec2c7bc486a44c9dbc5a2f6d0a97))
- Minor correction in helm comments. ([`835646d`](https://github.com/OpenG2P/farmer-registry/commit/835646d64ea4220110d6b6b6f1171faff3b4c2cb))
- Add seed manifest generation and remove obsolete performance templates ([`bee2c80`](https://github.com/OpenG2P/farmer-registry/commit/bee2c80bda0d7c178d97c2c177c5db7250ea12ab))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`b2cda40`](https://github.com/OpenG2P/farmer-registry/commit/b2cda40ae3ff83f6b189a43fd8c160bed6dda398))
- Bumped up RP version to 0.0.0-develop.383 ([`ec8828c`](https://github.com/OpenG2P/farmer-registry/commit/ec8828c439ff33ac65bfb502bdb3bad5358c14d1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare score against both farmer and household. A single install carries both — the bulk generator attaches scores to farmers and the sample loader to households, 5,671 and 6 on a reference install — so naming one parent silently stripped the id and the geography from every row of the other. ([`40556c9`](https://github.com/OpenG2P/farmer-registry/commit/40556c9a6b4ea4f0791f3a2e30a8fbaa428c85ef))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate fr_rpt_crop from declarations instead of hand-written SQL. Verified byte-identical to the previous definition across all seventeen shared columns and 757 rows before the SQL was removed; it keeps its materialization and indexes, and additionally carries the geo pcodes and workflow columns the hand-written version omitted. ([`699b3a2`](https://github.com/OpenG2P/farmer-registry/commit/699b3a283105c25a82b7c87608afb18a1d28a61f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare the household member age bands, matching fr_rpt_farmer's edges. The generator derives an age wherever it withholds a birth date, but where the bands fall is policy, and defining them twice with different edges is how two charts come to disagree about how many people are under 25. ([`6daa47a`](https://github.com/OpenG2P/farmer-registry/commit/6daa47af0c0b0abd14b6b4b701db197ac6fd2839))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the mechanical reporting views from the platform generator. reporting.yaml declares the entity tree, names farmer/land/crop as hand-written and marks the cooperative name columns as organisations rather than people; the generated ten add livestock, inputs, membership, scores, households, members, change requests, record history and geo_levels, which used to be derived from registered rows and so was empty on a production install. ([`11e3b8b`](https://github.com/OpenG2P/farmer-registry/commit/11e3b8beb7368af5e1dbf8bb6810c6ef08238a18))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Refresh the reporting views on a schedule, instead of relying on Insights to do it. They are materialized, so they held whatever the install produced and every farmer registered afterwards was invisible with no error anywhere; a CronJob now rebuilds them in dependency order resolved from pg_depend, on analytics.reportingViews.refreshSchedule. ([`8f93c33`](https://github.com/OpenG2P/farmer-registry/commit/8f93c337cbc07bcef9de94f12633572297c92e9f))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) fix: correct ui configuration for multiple sections and add dedicated parent lookup sections for crop intake and crop register ([`2f172d4`](https://github.com/OpenG2P/farmer-registry/commit/2f172d4848fecc02c08f9c5a9e83edb76888ba53))
- Moved to GitLab: openg2p/registry/farmer-registry (read-only; build/publish disabled) ([`fab0037`](https://github.com/OpenG2P/farmer-registry/commit/fab003727dda0013ca27f315dd967537756b6171))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
