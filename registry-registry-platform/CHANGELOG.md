# registry/registry-platform

_Published automatically._

**Repository:** [gitlab.com/openg2p/registry/registry-platform](https://gitlab.com/openg2p/registry/registry-platform) · **Container images:** [Container Registry](https://gitlab.com/openg2p/registry/registry-platform/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.387`](#v-0-0-0-develop-387) | 2026-08-20 | develop |
| [`1.2.0-rc.399`](#v-1-2-0-rc-399) | 2026-08-19 | release candidate |
| [`1.2.0-rc.397`](#v-1-2-0-rc-397) | 2026-08-18 | release candidate |
| [`1.2.0-rc.396`](#v-1-2-0-rc-396) | 2026-08-14 | release candidate |
| [`1.2.0-rc.393`](#v-1-2-0-rc-393) | 2026-08-14 | release candidate |
| [`1.2.0-rc.391`](#v-1-2-0-rc-391) | 2026-08-14 | release candidate |
| [`1.2.0-rc.389`](#v-1-2-0-rc-389) | 2026-08-14 | release candidate |
| [`0.0.0-develop.384`](#v-0-0-0-develop-384) | 2026-08-14 | develop |
| [`1.2.0-rc.387`](#v-1-2-0-rc-387) | 2026-08-13 | release candidate |
| [`1.2.0-rc.384`](#v-1-2-0-rc-384) | 2026-08-10 | release candidate |
| [`0.0.0-develop.383`](#v-0-0-0-develop-383) | 2026-08-09 | develop |
| [`1.2.0-rc.381`](#v-1-2-0-rc-381) | 2026-08-07 | release candidate |
| [`0.0.0-develop.379`](#v-0-0-0-develop-379) | 2026-08-07 | develop |
| [`1.2.0-rc.380`](#v-1-2-0-rc-380) | 2026-08-07 | release candidate |
| [`0.0.0-develop.378`](#v-0-0-0-develop-378) | 2026-08-06 | develop |
| [`0.0.0-develop.374`](#v-0-0-0-develop-374) | 2026-08-06 | develop |
| [`0.0.0-develop.353`](#v-0-0-0-develop-353) | 2026-08-06 | develop |
| [`0.0.0-develop.346`](#v-0-0-0-develop-346) | 2026-08-05 | develop |
| [`0.0.0-develop.345`](#v-0-0-0-develop-345) | 2026-08-04 | develop |
| [`0.0.0-develop.343`](#v-0-0-0-develop-343) | 2026-08-04 | develop |

# Release candidates

<a id="v-1-2-0-rc-399"></a>

## registry/registry-platform 1.2.0-rc.399 — 2026-08-19

_commit `cf61f52` · changes since 1.2.0-rc.397_
<!-- build:1.2.0-rc.399 revision:cf61f52be64fe41362e0c9862013e7b6b32ab3f6 ts:1787121259 -->

**Chart:** [openg2p-registry 1.2.0-rc.399](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.399.tgz)

### Changes

- [G2P-4786](https://openg2p.atlassian.net/browse/G2P-4786) refactor: move G2PRegisterDomainFactory and G2PIdGeneratorFactory to core interfaces, removing dependencies from extensions ([`929a1f3`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/929a1f38b5f3eda56905fe4caa886bc0d50b9370))

<a id="v-1-2-0-rc-397"></a>

## registry/registry-platform 1.2.0-rc.397 — 2026-08-18

_commit `0524935` · changes since 1.2.0-rc.396_
<!-- build:1.2.0-rc.397 revision:052493500f69964f1b646186eb1c36ba5e2d3151 ts:1787053503 -->

**Chart:** [openg2p-registry 1.2.0-rc.397](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.397.tgz)

### Changes since 1.2.0-rc.396

- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Refactored registry code list handling and API endpoints by removing attribute seeding, deleting related SQL/defaults, linking local ui-widgets, updating geo-level API routes, and optimizing attribute-value pagination defaults. ([`0524935`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/052493500f69964f1b646186eb1c36ba5e2d3151))

<a id="v-1-2-0-rc-396"></a>

## registry/registry-platform 1.2.0-rc.396 — 2026-08-14

_commit `de4ce53` · changes since 1.2.0-rc.393_
<!-- build:1.2.0-rc.396 revision:de4ce533b916ab67104dbda1b6a432155b73bacf ts:1786692907 -->

**Chart:** [openg2p-registry 1.2.0-rc.396](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.396.tgz)

### Changes since 1.2.0-rc.393

- [G2P-5369](https://openg2p.atlassian.net/browse/G2P-5369): Enhance GeoHierarchy functionality and validation ([`a533082`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/a53308284603cf91b473cbf8d365c630a78ed923))

<a id="v-1-2-0-rc-393"></a>

## registry/registry-platform 1.2.0-rc.393 — 2026-08-14

_commit `6020cb0` · changes since 1.2.0-rc.391_
<!-- build:1.2.0-rc.393 revision:6020cb08062d4f4b7ecf3e137aba300e404df32e ts:1786692549 -->

**Chart:** [openg2p-registry 1.2.0-rc.393](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.393.tgz)

### Changes since 1.2.0-rc.391

- [G2P-5493](https://openg2p.atlassian.net/browse/G2P-5493) refactor change request handling and remove unused staff-portal-ui folder ([`34d861b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/34d861b53e08918c8b30a2ac5edf72ee1d0e2162))

<a id="v-1-2-0-rc-391"></a>

## registry/registry-platform 1.2.0-rc.391 — 2026-08-14

_commit `9d10448` · changes since 1.2.0-rc.389_
<!-- build:1.2.0-rc.391 revision:9d1044817c1be37d1fb503ee3dd4acd48085263a ts:1786681006 -->

**Chart:** [openg2p-registry 1.2.0-rc.391](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.391.tgz)

### Changes since 1.2.0-rc.389

- [G2P-5500](https://openg2p.atlassian.net/browse/G2P-5500) Enhance G2PIntakeFormDataService to validate only surviving records during intake form processing. Introduced a new method to filter out records marked for deletion before validation, ensuring data integrity in the upsert operation. ([`08ea139`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/08ea13972db6ed1a633cd0d497beda7e3e980f21))

<a id="v-1-2-0-rc-389"></a>

## registry/registry-platform 1.2.0-rc.389 — 2026-08-14

_commit `3e0e2b2` · changes since 1.2.0-rc.387_
<!-- build:1.2.0-rc.389 revision:3e0e2b28c6614806c243474bd5c895ce497197af ts:1786680992 -->

**Chart:** [openg2p-registry 1.2.0-rc.389](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.389.tgz)

### Changes since 1.2.0-rc.387

- [G2P-5516](https://openg2p.atlassian.net/browse/G2P-5516) refactor: G2PGeo model and schema to use float type for latitude, longitude, and altitude fields ([`7d05211`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7d05211c359e88992b446a4ff028c2a9b0343be5))

<a id="v-1-2-0-rc-387"></a>

## registry/registry-platform 1.2.0-rc.387 — 2026-08-13

_commit `e601367` · changes since 1.2.0-rc.384_
<!-- build:1.2.0-rc.387 revision:e601367a1cf206f8a2fd58b7fe82f420bd2f7764 ts:1786602457 -->

**Chart:** [openg2p-registry 1.2.0-rc.387](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.387.tgz)

### Summary

- New feature: introduced `G2PChangeRequestSectionPayloadService` for enhanced change request processing and added validation to ensure only one active change request section per record.
- Testing improvements: added unit tests for the new change request section payload service, enhancing overall test coverage.

### Changes since 1.2.0-rc.384

- [G2P-5497](https://openg2p.atlassian.net/browse/G2P-5497) feat(cr): add G2PChangeRequestSectionPayloadService and integrate validation in change request processing ([`bc7091c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/bc7091c2a36f62ef80c449d77816b66507aea54f))
- [G2P-5492](https://openg2p.atlassian.net/browse/G2P-5492) feat(cr): add validation to enforce single section active crs for a record ([`3d14b54`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3d14b54b27741b7f2989936139a175103d090fe1))

<a id="v-1-2-0-rc-384"></a>

## registry/registry-platform 1.2.0-rc.384 — 2026-08-10

_commit `129dae1` · changes since 0.0.0-develop.374_
<!-- build:1.2.0-rc.384 revision:129dae1695398c120577c4145a9c9431e1545308 ts:1786352962 -->

**Chart:** [openg2p-registry 1.2.0-rc.384](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.384.tgz)

### Summary

- Performance optimization: streamlined policy condition handling in G2PIntakeFormDataService and G2PRegisterService to eliminate unnecessary await calls.
- IAM integration: added IAM admin user to Keycloak for enhanced access management.
- Dockerfile cleanup: removed redundant sharp installation and chown layers to improve build efficiency.
- Partner and consent management: reapplied enhancements and realigned configurations to improve integration with commons-services and the g2p-bridge pmSeedClientId pattern.

### Changes since 0.0.0-develop.374

- Optimize policy condition handling in G2PIntakeFormDataService to avoid unnecessary await ([`a76dbaa`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/a76dbaa68d9f0a35dfd8e13992a8d8e65c4d6bba))
- Refactor policy condition handling in G2PRegisterService to avoid unnecessary await ([`4552894`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/45528947f52b9b3be91a29ff5485283a11f784d3))
- [G2P-5495](https://openg2p.atlassian.net/browse/G2P-5495) Add IAM admin user to keycloak-init ([`816cfdf`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/816cfdf8d4963b49b2f2bb9f2ae6bf0e738b7202))
- [G2P-5489](https://openg2p.atlassian.net/browse/G2P-5489) Remove redundant sharp install and chown layers from Dockerfile ([`34eb393`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/34eb39345707ba11e4bd63f5ce236eda6659fea0))
- Reapply "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Repoint Partner Management to commons-services and align PM-seed auth to the g2p-bridge pmSeedClientId pattern." ([`ff1f9c8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/ff1f9c8fe8e61e5717cf65e2f1363f8f51df7da0))
- Reapply "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Consent and partner management related." ([`e378ecb`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/e378ecbac8108749766d0ae0fc5fed197e517a4e))
- Reapply "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Enhancements for consent management, partner management and WJS support." ([`eabfb80`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/eabfb8096865dca361b8a4f48d8d9d4551bc86d1))

<a id="v-1-2-0-rc-381"></a>

## registry/registry-platform 1.2.0-rc.381 — 2026-08-07

_commit `4bbd6f7` · changes since 1.2.0-rc.380_
<!-- build:1.2.0-rc.381 revision:4bbd6f79d5fffdde52b4e2f42feed380a18a4e14 ts:1786103120 -->

**Chart:** [openg2p-registry 1.2.0-rc.381](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.381.tgz)

### Changes since 1.2.0-rc.380

- [G2P-5492](https://openg2p.atlassian.net/browse/G2P-5492) feat(cr): add validation to enforce single section active crs for a record ([`4bbd6f7`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/4bbd6f79d5fffdde52b4e2f42feed380a18a4e14))

<a id="v-1-2-0-rc-380"></a>

## registry/registry-platform 1.2.0-rc.380 — 2026-08-07

_commit `0cc8ad4` · changes since 1.2.0-rc.378_
<!-- build:1.2.0-rc.380 revision:0cc8ad40379860bf6928e0528f4367c87fe4c614 ts:1786097032 -->

**Chart:** [openg2p-registry 1.2.0-rc.380](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.380.tgz)

### Changes since 1.2.0-rc.378

- [G2P-5489](https://openg2p.atlassian.net/browse/G2P-5489) Remove redundant sharp install and chown layers from Dockerfile ([`34eb393`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/34eb39345707ba11e4bd63f5ce236eda6659fea0))

# Develop builds

<a id="v-0-0-0-develop-387"></a>

## registry/registry-platform — develop 0.0.0-develop.387 (2026-08-20)

_commit `e25bd6b` · changes since 0.0.0-develop.384_
<!-- build:0.0.0-develop.387 revision:e25bd6be076e4fef8441397429528693619d4aa8 ts:1787200740 -->

**Chart:** [openg2p-registry 0.0.0-develop.387](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.387.tgz)

### Summary

- Security and authentication: Registered credential configurations with Certify, aligned agent Keycloak clients with IAM, and documented the agent realm recipe.
- Feature addition: Introduced agent portal VC issuance to the Registry Platform, available behind a disabled-by-default switch.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Register credential configs with Certify and align agent Keycloak clients ([`e25bd6b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/e25bd6be076e4fef8441397429528693619d4aa8))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Align agent Keycloak clients with IAM and document the agent realm recipe ([`43439a8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/43439a8f812f0defadaac7ea2bdc103ec8f3cda7))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add agent portal VC issuance to Registry Platform behind a disabled-by-default switch ([`09543b3`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/09543b36ab66f225f03a4f014078768735c075a6))

<a id="v-0-0-0-develop-384"></a>

## registry/registry-platform — develop 0.0.0-develop.384 (2026-08-14)

_commit `5a51c9e` · changes since 0.0.0-develop.383_
<!-- build:0.0.0-develop.384 revision:5a51c9e032fe68c393782156e8fda1ae555a9c78 ts:1786672977 -->

**Chart:** [openg2p-registry 0.0.0-develop.384](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.384.tgz)

### Changes since 0.0.0-develop.383

- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Remove dead staff-api imports from registry-core controller services. get_data_policies and get_data_policy_mnemonics were imported in four files and never called, but registry-core ships in every image while only staff-api installs openg2p_registry_staff_api — so partner-api and any non-staff image crashed at import. Also correct the ID-types note in questions.yaml. ([`5a51c9e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5a51c9e032fe68c393782156e8fda1ae555a9c78))

<a id="v-0-0-0-develop-383"></a>

## registry/registry-platform — develop 0.0.0-develop.383 (2026-08-09)

_commit `50804dd` · changes since 0.0.0-develop.379_
<!-- build:0.0.0-develop.383 revision:50804dde517f49b57693d1e7d6bdc41b35ef97c3 ts:1786191874 -->

**Chart:** [openg2p-registry 0.0.0-develop.383](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.383.tgz)

### Summary

- **Major:** Enhanced registry functionality: introduced the ability to declare inherited parent attributes, derived columns, and row filters, enabling more expressive semantic views and automated reporting without manual SQL.
- Improved reporting: generated mechanical reporting views directly from the registry schema, ensuring consistency and coverage based on actual data rather than manual entries, while enforcing personal data safeguards.
- PII compliance: refined handling of inherited columns to apply explicit PII rules, ensuring derived columns are exempt from certain validations to prevent build failures.
- Dependency updates: modified the dependency manifest for the db-seed Docker component, reflecting changes necessary for the new reporting generation functionality.

### Changes since 0.0.0-develop.379

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Apply only the explicit PII rules to an inherited column. verify() exempted derived columns but not inherited ones, so five age_band columns inherited from NSR's individual view failed the build as unbounded free text; the deny-list and patterns still apply to them, since a hand-written parent could expose a name, but the free-text heuristic must not re-judge a column whose meaning the parent already declared. ([`50804dd`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/50804dde517f49b57693d1e7d6bdc41b35ef97c3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Let a registry declare inherited parent attributes and a row filter. Without them the vocabulary could not express even the simplest semantic view — a crop needs its parcel's tenure on the row, and RP marks superseded records rather than deleting them, so an unfiltered view counts a corrected parcel twice. ([`fa1af5d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fa1af5d54a7d372651f3b3bb22ba23316ef4ea4f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Let a registry declare derived columns, roll-ups and which views are materialized. Without these the generator could only emit raw record-grain views, so anything a country computes — age bands, parcels per farmer, whether a holding is titled — still needed hand-written SQL; derived expressions are wrapped around the PII-free base select so they cannot reach a withheld column, and roll-ups read the child's base table so parent and child views never reference each other. ([`4c70842`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/4c70842d80bde1d311ce5546e501aeb3d761e3e9))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate the mechanical reporting views from the registry's own schema. Each registry hand-wrote them, so coverage was whatever somebody remembered — FR gave livestock a boolean and no view while the register held 132,824 rows — and the geo block had already drifted between FR and NSR; the generator takes hierarchy depth and labels from Master Data and the entity tree from reporting.yaml, so the output depends on the install rather than on what has been registered, and it fails the job if personal data reaches a generated view. Also ignores __pycache__, which the db-seed scripts now produce. ([`9b7c74b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/9b7c74ba033b38fb985d20a17c709852cd268441))

<a id="v-0-0-0-develop-379"></a>

## registry/registry-platform — develop 0.0.0-develop.379 (2026-08-07)

_commit `d23682b` · changes since 0.0.0-develop.378_
<!-- build:0.0.0-develop.379 revision:d23682b28ab7a009da724e871190277c9a3229b4 ts:1786100775 -->

**Chart:** [openg2p-registry 0.0.0-develop.379](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.379.tgz)

### Changes since 0.0.0-develop.378

- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Enable BUILD_CACHE for registry-platform builds ([`d23682b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d23682b28ab7a009da724e871190277c9a3229b4))

<a id="v-0-0-0-develop-378"></a>

## registry/registry-platform — develop 0.0.0-develop.378 (2026-08-06)

_commit `b0eca4d` · changes since 0.0.0-develop.374_
<!-- build:0.0.0-develop.378 revision:b0eca4d20214b20ad38fc8adb9fa1018dd9e9b24 ts:1786012597 -->

### Summary

- Partner management overhaul: Repointed to commons-services, aligning PM-seed authentication with the g2p-bridge pmSeedClientId pattern, and enhanced consent management and partner management functionalities.
- New functionality: Introduced a consent helper in the partner API to streamline consent-related operations.
- Dependency update: Modified dependency manifests in the partner API to reflect the latest requirements.

### Changes since 0.0.0-develop.374

- Reapply "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Repoint Partner Management to commons-services and align PM-seed auth to the g2p-bridge pmSeedClientId pattern." ([`a5ade5e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/a5ade5e1fc966262a9188e4f05a8c22dbe2f20b2))
- Reapply "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Consent and partner management related." ([`63f2385`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/63f2385601b71e657458eb23767d0807584bfc4b))
- Reapply "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Enhancements for consent management, partner management and WJS support." ([`c6b51a0`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c6b51a040e0f3d1b43f73f284da1aadb3166b264))

<a id="v-0-0-0-develop-374"></a>

## registry/registry-platform — develop 0.0.0-develop.374 (2026-08-06)

_commit `bf59097` · changes since 0.0.0-develop.353_
<!-- build:0.0.0-develop.374 revision:bf590976e1a19296dbf35fe797cb22b3ed34a408 ts:1786000316 -->

### Summary

- **Major:** Reverted multiple enhancements related to consent and partner management, including changes to partner management alignment and consent helper functionality.
- Feature enhancements: Implemented internal record ID resolution in intake form processing, improved intake form components with submission context, and added a new parent lookup widget.
- UI improvements: Enhanced MinIO configuration for read access, improved localization and panel navigation, and fixed boolean value preservation in select options.
- Dependency updates: Upgraded ui-widget version and modified dependency manifests for both API and UI components.
- Error handling improvements: Enhanced overall error handling mechanisms across the application.

### Changes since 0.0.0-develop.353

- [G2P-5466](https://openg2p.atlassian.net/browse/G2P-5466) Implement subject internal record ID resolution in intake form processing ([`ba5d9f0`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/ba5d9f0973f350293c8a114890605dc3ca39cf3d))
- [G2P-5478](https://openg2p.atlassian.net/browse/G2P-5478) fix(vc-configuration): update service with pagination and additional parameters ([`36d59d5`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/36d59d5cf62b1c8b0daf5675210c8ff2bf8ea10d))
- [G2P-5451](https://openg2p.atlassian.net/browse/G2P-5451) feat(document): enhance MinIO configuration for read access in environment files and core components ([`5c15f30`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5c15f3031b04dc3b645271b4aaa9caebec187694))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): improve localization and panel toggle navigation ([`7dbaaad`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7dbaaada4af5af4d37d7cc893c57cf4e8e821972))
- ui-wdget version upgraded ([`dab5529`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/dab5529e3b3fbe2677e4044dde245635451a0439))
- Revert "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Enhancements for consent management, partner management and WJS support." ([`7b60b8a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7b60b8a6c494e48483edad37975b4aaa1e9b3775))
- Revert "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Consent and partner management related." ([`5b12f1b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5b12f1b45efc998d257f047a4a2684ad43f343f5))
- Revert "[G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Repoint Partner Management to commons-services and align PM-seed auth to the g2p-bridge pmSeedClientId pattern." ([`b12884d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b12884d133ba9348575c63cfcffb8ff26f594ef9))
- [G2P-5429](https://openg2p.atlassian.net/browse/G2P-5429) feat(IntakeForm): enhance intake form components with submission and registration context ([`f20eed8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f20eed896514f51bb85da3cf73d93b37ebabe080))
- [G2P-5429](https://openg2p.atlassian.net/browse/G2P-5429) feat(ParentLookupWidget): add new parent lookup widget and update related components ([`fd4681f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fd4681fc8e706b3270c49cd2420dadc8c33898ec))
- [G2P-5408](https://openg2p.atlassian.net/browse/G2P-5408) Fix SelectWidget to preserve boolean values for select options ([`fa7b925`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fa7b9254baf81aa0fc0a8f71e04a0bbc3318a437))
- G2P-[G2P-5389](https://openg2p.atlassian.net/browse/G2P-5389) improve error handling ([`40c729f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/40c729feb6b8f2b5fe697527fd5dd1ef378ece61))

<a id="v-0-0-0-develop-353"></a>

## registry/registry-platform — develop 0.0.0-develop.353 (2026-08-06)

_commit `b203acd` · changes since 0.0.0-develop.346_
<!-- build:0.0.0-develop.353 revision:b203acd4ceeb48f52b6f1ffd56e2153d52591c99 ts:1785996427 -->

### Summary

- **Major:** Removal of the data policies feature and all associated components across the API and UI, resulting in significant codebase reduction (3572 deletions).
- Refactoring: Cleaned up service methods by removing unused request parameters and debug print statements, and updated hierarchy path building.
- Fixes: Corrected import paths for data policy request helpers to ensure proper functionality post-removal.
- General cleanup: A total of 57 files were modified, with a focus on streamlining the codebase and enhancing maintainability.

### Changes since 0.0.0-develop.346

- Remove data policies feature and related components ([`71309a2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/71309a23899cdf56be97ddf7bcebda6efc0b43af))
- Refactor: remove unused request parameters from service methods ([`daa4521`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/daa4521aa15f9374bd16070c351a847bf7ee6825))
- Refactor: update hierarchy path building and remove debug print statements ([`36584d1`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/36584d1b5f124b62db13cb084efa540b98ba3dd6))
- Fix: update import paths for data policy request helper ([`b087344`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b087344a1b2225a11a74427b2e83cad4ea5dbbaa))
- Fix: update import paths for data policy request helper ([`4c7c7c9`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/4c7c7c9db4d10e1556369f9412106ff623e2bd9e))
- Refactor data policy handling across services ([`c61a9db`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c61a9dbdba1ea0726d458cef2f7fc2ae9ab6e4bb))

<a id="v-0-0-0-develop-346"></a>

## registry/registry-platform — develop 0.0.0-develop.346 (2026-08-05)

_commit `ab38f08` · changes since 0.0.0-develop.345_
<!-- build:0.0.0-develop.346 revision:ab38f087fff9b48a928843a029b015822a7df606 ts:1785892510 -->

### Changes since 0.0.0-develop.345

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) DB-seed: move the farmer-shaped sample loaders out of the platform image — load_sample_data.py/upload_images.py write farmer-extension tables and read farmer seed JSON, so they belong to the variant; the entrypoint keeps the hook and errors clearly without one ([`ab38f08`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/ab38f087fff9b48a928843a029b015822a7df606))

<a id="v-0-0-0-develop-345"></a>

## registry/registry-platform — develop 0.0.0-develop.345 (2026-08-04)

_commit `2759d58` · changes since 0.0.0-develop.343_
<!-- build:0.0.0-develop.345 revision:2759d587c57b8325a82873cebb8fa6c65b1aecda ts:1785842393 -->

### Summary

- Testing enhancements: smoke suite now runs by default, and Sanity questions expanded from 4 to 11.
- Migration improvements: chart-inherit-questions migrated from GitHub caller to maintain Rancher form in wrapper charts.
- Fixture updates: removed farmer naming from platform's fixtures for clarity.

### Changes since 0.0.0-develop.343

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Sanity: run the smoke suite by default (questions.yaml already said so) and drop the farmer naming from the platform's fixtures; expand the Sanity questions from 4 to 11 ([`2759d58`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/2759d587c57b8325a82873cebb8fa6c65b1aecda))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Migrate: carry chart-inherit-questions across from the GitHub caller, so wrapper charts keep their Rancher form ([`95ca561`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/95ca561599df62d3b8c754d109a29da03d5a8e71))

<a id="v-0-0-0-develop-343"></a>

## registry/registry-platform — develop 0.0.0-develop.343 (2026-08-04)

_commit `39e4c2c` · changes since v1.0.0_
<!-- build:0.0.0-develop.343 revision:39e4c2c7f148f5b0674b20fb0b3ab2618cb98cb2 ts:1785808984 -->

### Summary

- **Major:** CI transition to GitLab with removal of GitHub Actions; new build-publish workflow consolidates all images and charts.
- Security enhancements: added CSRF validation for staff-portal-api requests and client-side CSRF token handling.
- Data management improvements: introduced read-only user access for Minio client, enhanced file validation and upload profiles, and added configurable reference generator for intake forms.
- Feature updates: added unsaved changes warning for intake forms, new endpoint for retrieving allowed parents, and support for logo and favicon in registry settings.
- Refactoring efforts: streamlined document handling across various components, removed deprecated methods, and improved attribute value fetching and geo hierarchy handling.
- Bug fixes: resolved issues with geo hierarchy service absence, corrected variable names in controllers, and ensured proper handling of approval status and document uploads.
- Dependency updates: upgraded ui-widgets version and synchronized with staff-portal-ui, ensuring compatibility across modules.

### Changes since v1.0.0

- Just to trigger a build. No change otherwie ([`39e4c2c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/39e4c2c7f148f5b0674b20fb0b3ab2618cb98cb2))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`f5aa8eb`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f5aa8ebb74e8b89c3e7f10dc37818285f76a30d8))
- [G2P-5451](https://openg2p.atlassian.net/browse/G2P-5451) feat(document):  add read only user access for minio client ([`da42213`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/da42213bf2512603a4cbfd3747fc9382dc5e01c8))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Surface the country pack in questions.yaml. None of the geo-seed options were in the Rancher form, so the one place a deployment declares its country was reachable only by hand-editing values — an installer had no way to know the choice existed, and every install silently took the fictitious default. ([`b890549`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b890549d41cb2e9fdba8eb811291594a6f6c74dd))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Correct the loadGeoData comment. It still described the old direction, where the registry pushed geo into master-data because master-data shipped none — so it read as though the flag were needed for sample data. Master Data seeds its own geography from a country pack now, and enabling this writes a second, five-level slug-path hierarchy over it. ([`495542f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/495542f02dbafc3b3cc7159d428b6597b01e6222))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Read code-list dropdowns from the database instead of the widget, in the reference extension, and stop truncating them. The attributes route defaulted to page_size 20, so a longer list rendered 20 options with nothing to indicate the rest existed and the missing values simply could not be chosen. ([`22c1d78`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/22c1d78693bae934355b57868858e7132f939f0f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Attach the sub-table fixtures to whoever was actually loaded. They link to the demography CSV's id space, so once people come from a country pack every land parcel, crop, housing and programme row pointed at a record that does not exist — and with no foreign key to violate they landed as orphans, leaving farmers who own nothing and households with no housing data. Links are remapped onto the loaded records, cycling when a pack carries fewer samples than the fixtures assume, and a table that had one row per record keeps one. Links pointing within the fixture set — a crop's parcel — are left alone. No-op when the ids already match. ([`cd8845f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/cd8845ff72c92519207b3a23eeea948c0adfb82f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Supply head_individual_id, headship_type and adult/elderly counts with the master-data samples. Registries differ in what they record about a household and NSR needs these four; supplying the union costs nothing since each loader takes only the keys it asks for. ([`35bf698`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/35bf698cfd4cd9afcd8b635c3c308e5d8797d49d))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the country out of sample seeding and the geo widgets. load_sample_data no longer assumes five levels called country..village — that describes Kamuntu and nothing else, and Ethiopia has four ending at woreda; people and their whole ancestry now come from Master Data, with the CSV as fallback. New sync_geo_widgets step (SYNC_GEO_WIDGETS, default false) matches a register's geo dropdowns to the hierarchy actually loaded, since an extension's hardcoded level names produce dropdowns that silently return nothing against a country that names them differently. Labels are left alone but reported when they name the wrong level. ([`782fa19`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/782fa19fafd11251d7fd737058e14b3834667862))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Validate coded values against the seeded country lists, behind registry_core_validate_attribute_values (default false). This is the check the compiled enums do today, and it is what lets them be deleted: an enum is fixed at image build time, so a registry validating against one can only serve the country it was built for. Fields map to lists by convention — 30 of Ethiopia's 34 already match a column name — with a field_map for the few that don't. Applied on both the change-request and intake-form paths. Also resolve sample-data geo ids against master-data instead of computing slug-paths, which match nothing once master-data is seeded from a P-coded pack; slug-paths remain the fallback and the outcome is always reported. ([`b806b8a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b806b8aee6845b8cf0594e40634542ffb710feb5))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Seed registry code lists from Master Data, behind LOAD_ATTRIBUTES (default false). The registry copies the country pack's lists into its own tables at install and validates against that copy after, so MDS is an install-time dependency, not a runtime one. Roles go in a new table, not a new column: create_all never adds columns to existing tables, so a column would be declared by the ORM and missing from every upgraded database. Where an extension fixture and the pack define the same list, the pack replaces it — merging left PROGRAM_NAME with 18 values and a dropdown showing every programme twice — and each replaced value is logged. ([`62dee1a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/62dee1a537ef6ccc6303c21219c755368d7281ae))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Correct the geo-join comment in load_sample_data.py. It claimed the slug-path id keeps the registry<->master-data join working, but master data is now seeded from P-coded country packs, so demography-seeded records carry ids MDS has never heard of and never appear on a map. Documents the mismatch and the two-part fix. ([`ed1d67a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/ed1d67a83ef73da194289862a47d61662724c3c1))
- chore(ui-widgets): version for npm next publish, sync staff-portal-ui @1.1.6-dev.3 [skip ci] ([`0169c66`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0169c661a768770067d044ae1d3b67acdfd741cc))
- [G2P-5412](https://openg2p.atlassian.net/browse/G2P-5412) refactor(models): remove unused async methods and clean imports ([`0b777ad`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0b777ade7a8ccd158ad16ca59503667d4b4e1dcf))
- [G2P-5411](https://openg2p.atlassian.net/browse/G2P-5411) feat(celery): register new services for intake form management ([`2d3eea1`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/2d3eea1146572a4c61d61eef8694a0a4cf7c842b))
- [G2P-5411](https://openg2p.atlassian.net/browse/G2P-5411) feat(intake-form): add endpoint to retrieve allowed parents for intake forms ([`6d02119`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/6d0211985c9ed0c8b42341b6dde67a16245116e3))
- Just to take latest version of openg2p-data ([`525b84f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/525b84f27a6029cc6882a208a98b154e35271a37))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Pin the db-seed image to openg2p-data develop in CI. ([`80e5002`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/80e5002bdd7cf922b118aeed74b479e6a3d9fdbe))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Track openg2p-data develop for the db-seed image. ([`dc2dc8d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/dc2dc8d64a905b3b632139aa99b7660420acc4b4))
- [G2P-5400](https://openg2p.atlassian.net/browse/G2P-5400) refactor(ui-routes): Remove deprecated tab and section routes ([`574c372`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/574c372ce3497ad3abdae962a1b0dfa32ebbfc33))
- [G2P-5400](https://openg2p.atlassian.net/browse/G2P-5400) refactor (staff-api): Remove legacy tab and section CRUD routes ([`de2db46`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/de2db4656099d3927004a7f7ae7496f4ae776553))
- [G2P-5400](https://openg2p.atlassian.net/browse/G2P-5400) fix(register): align tab/section service with current ORM columns ([`9bb223b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/9bb223be957d852468e87d8edfe2de3975ce1f24))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) db-seed: make sample-data loading idempotent — add ON CONFLICT (internal_record_id) DO NOTHING to the register/sub-table inserts so a re-install over an already-seeded database is a no-op instead of failing on g2p_register_*_pkey ([`6ec5f56`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/6ec5f56c97c3744ac71f6bb0594db12d864203a1))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: make the DCI overlay tolerant of an older pinned harness — probe for post_search and fall back to a plain POST instead of failing collection with ImportError ([`c5214fc`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c5214fc0ea55c590df3599b2b82c7245ac967417))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: retry a DCI search only when a dependency returns 5xx (e.g. Consent Manager stale-connection 500) — a genuine policy denial is never retried, so fail-closed behaviour is still asserted ([`9ded7ac`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/9ded7ac1e08c7fba279ff4b8cb71e844fd4bc7a2))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: add a contract test asserting a variant's fixtures overlay satisfies every fixtures.<SYMBOL> the inherited harness imports — renaming a symbol in an overlay silently breaks sanity/dci.py and friends at collection time ([`23c58b3`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/23c58b3fb72a204db6a6694142b34005e7918f02))
- [G2P-5365](https://openg2p.atlassian.net/browse/G2P-5365) refactor(useCrViewData): fix audit details in table widget ([`a71fb67`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/a71fb679b913cabf8988c5b4f568f61b8feaf939))
- [G2P-5382](https://openg2p.atlassian.net/browse/G2P-5382) refactor(VersionHistoryPage): recreate widget store on version change to prevent stale data ([`b622225`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b6222259a0c84b503b85467f78fa503bb8238455))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: fail instead of silently passing — default SANITY_FAIL_ON_ERROR/failOnError to true so a failing suite fails the Job and the install, and make fixtures FAIL when a dependency is configured but broken (unconfigured dependencies still skip), so a run cannot go green having dropped every consent and signature test ([`dd25651`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/dd256515449c69dd3290db2d9ddbc2f9c9fefbea))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: fix PM partner seeding — Partner Management returns HTTP 400 with body code PM-PRT-409 for an already-onboarded partner, so the status_code==409 branch never fired and every consent/signature test silently SKIPPED; also surface the response body on failure ([`112378f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/112378f8f3edd5c16060b079b35551ce1f20129f))
- chore(ui-widgets): version for npm next publish, sync staff-portal-ui @1.1.6-dev.2 [skip ci] ([`7b30e97`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7b30e979cbc9e443e8dadce4a61a5f97dc19b6c2))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Chart: make the IAM tile name values-driven (iamRegister.applicationDescription via __APPLICATION_DESCRIPTION__) so a wrapper chart can set it, and fix the reference registry's id-generator idTypes (farmer -> individual) so its Individual register actually gets a functional-ID pool ([`01ce237`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/01ce237388d7e036eb9492d6c08e581bd485cb9f))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Fix ui-widgets npm-publish drift+race: self-heal dev version from npm 'next' dist-tag, retry the just-published widget install for registry propagation so commit-back lands; realign develop to 1.1.6-dev.1 ([`688ec49`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/688ec4941c3b085d75217f077c495949888fc531))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Fix ui-widgets npm publish collision: bump develop version 1.1.4-dev.3 → 1.1.6-dev.0 (ahead of released 1.1.5) so the dev prerelease no longer republishes an existing version ([`bc4a341`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/bc4a341cd8f862cd71bddd985ec0d86f66b1902f))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) CI: stop build-publish on Dependabot branches (exclude !dependabot/**); add lightweight ui-ci PR check (npm type-check+build, no publish) for the UI packages ([`0364f07`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0364f0759eb6097e95ce888256b4f8bdba6212cd))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) CI: single build-publish workflow for all images+chart at one locked version — fold staff-ui in (own context), add staffUi+sanity to chart-image-paths, drop separate docker-staff-portal-ui.yml ([`aebd339`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/aebd3399642c4b65bd90c9e354c3d374bc60974b))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Reference registry cleanup: remove broken/unused inbound message-rule seed, de-NSR (templates→individual_to_dci, registry name, master-data URLs), correct Dockerfile/README comments to the runnable reference-registry + Option-C model ([`d7139ea`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d7139ea1bb36a12681daa5805cfb16a80d747d50))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity e2e logs: clean titled per-test banner + timestamped step lines + RESULT footer; suppress httpx and pytest live-log noise (drop log_cli, run with -s) ([`c72eb16`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c72eb16907af882b891ecb4866e46c744faaf2b0))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: history test reads g2p_register_history_individuals (last farmer-table ref); reference e2e now fully green (DCI + change-request/AWE) ([`d424e68`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d424e68853f2359035aaed506a8e9d1a60229a46))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity: fix ScopeMismatch — use a plain logger (not the function-scoped step fixture) inside the module-scoped change_request fixture ([`d6399e7`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d6399e79eacebe7e4bfcc3148aa8427928af12b4))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Reference AWE seed collision-tolerant: split individual vs household groups with ON CONFLICT DO NOTHING so the individual change_request policy+stages always seed even when a shared AWE DB already has registry.change_request.household from another registry ([`b15861f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b15861f3b494ebca04d26a97b3994fbb3aa67689))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Reference DCI seed to core schema (documents/data_models/outgoing_templates) so DCI search resolves the Individual template; add timestamped per-test step logging (DCI + change-request/AWE stages) ([`d171513`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d17151398c368b7dc6394a2f2ec92d549fbc8f8b))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity CR e2e: target reference individual UI tab/section + individuals table for the change-request test ([`749f91f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/749f91ff5b878ccd6b66da446c58489baa0ca805))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity DCI e2e: read name/birth_date directly under demographic_info (reference DCI-standard template shape) ([`877d833`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/877d83337e5961d413578a4a66e7df3619d327f3))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Sanity e2e: point reference sanity suite at individual register (data_seed table, register id, DCI scopes/type) so e2e runs against the reference registry ([`3f8b410`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3f8b410ecb81d896d3172295bed70e642d0cc87b))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Reference registry db-seed green: minimal seed with demo-data loaders (sample/geo/images/templates) defaulted OFF in base chart, farmer overlay re-enables; add openg2p-registry-sanity-tests image + e2e suite + CI entry ([`1476fbb`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1476fbb1dc89769c7139f83324f0ecce95a024e8))
- [G2P-5365](https://openg2p.atlassian.net/browse/G2P-5365) refactor(g2p_register): streamline history field handling - update base fields to exclude from current register data - add last approved by and approved at fields to current register data ([`102b30b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/102b30bf51eb76e73c103af2735138cb6bf83295))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Reference registry + naming cleanup: RP images are runnable reference registries (individual+household from NSR), env-selected extension (Option C), staff-api/bene-api/celery-*/staff-ui rename, single openg2p-registry chart; farmer extends via REGISTRY_EXTENSION_MODULE ([`db42ba2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/db42ba21748d16f714506f157779bd0006c1cba6))
- bumped up the version to 1.1.1 for registry platform ([`6367bae`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/6367bae50d7ef6c6a31700324311620d67c7d44a))
- feat(DataPoliciesListPage): update registry-widgets version and enhance permissions handling ([`aa86b28`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/aa86b28ce26915ac4b8e78695462f15c7917cc58))
- published and updated ui widget version to 1.1.4-dev.4 ([`3abf27c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3abf27c95df473313630476afa24d82e73ff7e1a))
- [G2P-5383](https://openg2p.atlassian.net/browse/G2P-5383) Invert build model: registry-platform publishes base images + Helm chart, farmer-registry extends ([`53d580c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/53d580c0d8e454996e559fb34a7450b4790ba2ae))
- [G2P-5381](https://openg2p.atlassian.net/browse/G2P-5381) feat(intake-form): add unsaved changes warning before submit ([`9b664e1`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/9b664e1fa37246c91e73262a82341ff299d82dfe))
- chore(ui-widgets): version for npm next publish, sync staff-portal-ui @1.1.4-dev.3 [skip ci] ([`4e4548b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/4e4548b3fb2e645191fd660836fd2d7b674097fe))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Grant packages: write in library changelog caller (reusable images/chart jobs require it at startup) ([`c73493f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c73493fd9c9990fe57ee36b28461aba944bcaf17))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Add library changelog tracking (kind: library) ([`532a3f9`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/532a3f96341f56c3438421fa984bbc807292f1dc))
- [G2P-5375](https://openg2p.atlassian.net/browse/G2P-5375) Update @openg2p/registry-widgets version to 1.1.4 ([`c0331db`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c0331db71aa8c9af8fdc38643bcc8e7cc58898b7))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) fix: update buildSectionsDataMap return type - change return type to always return an object ([`b010347`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b010347a6f87170f3975f417e30bdcd7937821ee))
- updating the ui widget develop tag 1.1.4-dev.2 in the staff portal ui ([`08cb976`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/08cb976ce5d3172f4c82a8ac2a5bf5eb75eced47))
- updating the ui widget develop tag in the staff portal ui ([`5bb768f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5bb768fa8c60e7d83e1c9d1019ffe603174f5725))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) refactor: update file rendering for change request header, submission header, and DocsWidget ([`e103a51`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/e103a518aa0ff0d25ee5896b1e9ed6bbe375f9e4))
- [G2P-5347](https://openg2p.atlassian.net/browse/G2P-5347) refactor(intake_form_register): dedupe document ingestion by register - update document retrieval to group by register - adjust document processing to use register-level sections - enhance logging for missing section references ([`5eaaf0c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5eaaf0cb28c6bb165363ede1741a91752bf8fb09))
- [G2P-5347](https://openg2p.atlassian.net/browse/G2P-5347) chore(helper): remove unused MinioClient import ([`93630f0`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/93630f0813c7892332faf88d9f0aaf91eed555f4))
- updating the ui widget tag in the staff portal ui ([`13ca764`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/13ca76482e411b901e97a294e7868bc84f9cb1c6))
- [G2P-5347](https://openg2p.atlassian.net/browse/G2P-5347) fix(enum): restore entry in ChangeRequestSourceEnum ([`4d7ff96`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/4d7ff96e277eef3e77444856a9154f08ac92ec2f))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) refactor(geo-hierarchy): enhance layout and widget handling ([`46317cf`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/46317cf8a7193859eeac8961974935085456857f))
- fix(g2p_register): handle geo hierarchy service absence gracefully ([`9fcf214`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/9fcf214da6ae5b40a706f501a94d249d1776dba5))
- [G2P-5347](https://openg2p.atlassian.net/browse/G2P-5347) refactor(service): streamline document handling on change approval ([`eb99cf3`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/eb99cf322e02386f0b55cf2acd4828ab69d737bf))
- [G2P-5347](https://openg2p.atlassian.net/browse/G2P-5347) fix(service): add record image URLs to change request data ([`860817e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/860817e82a27173ba101a7245c11dc2c70222854))
- [G2P-5330](https://openg2p.atlassian.net/browse/G2P-5330) fix(controller): remove permissions for upload and delete documents ([`ee6528a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/ee6528a6ab92b9992aae536417ec46eb33aef20f))
- [G2P-5307](https://openg2p.atlassian.net/browse/G2P-5307) fix(model): simplify created_at field by removing timezone support and using utcnow ([`fbaae54`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fbaae549dac2aacb3c33b8e484584454cd1ec201))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) fix: preview url issue for HeaderSectionWidget ([`512c3f5`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/512c3f56338338f09a272b4e5f9da370a979de0a))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) fix: refetch approval status after decision and split approval hooks ([`fc0cec9`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fc0cec9c6397df2398232da4297af1e908386a09))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) refactor: update geo hierarchy and document handling ([`91edd25`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/91edd25d5f914b95a705d39d4798c204adef4808))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) refactor: update register and intake form document handling ([`24009ab`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/24009ab9cf81d514b80355557d0e60bf623d75b4))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) refactor: rename template_file_id to template_document_id across the application ([`cf1e75d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/cf1e75df4a98a8281f25d18bbb6fd8689afcb06f))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) fix(model): ensure created_at uses timezone-aware DateTime ([`ed8df39`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/ed8df39a39859cce4b48826afc15b626fc6dc07d))
- [G2P-5238](https://openg2p.atlassian.net/browse/G2P-5238) chore: update ui-widgets to v1.1.3 ([`f8adc49`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f8adc49a10b4ae2ad1e0c154a2630f5f8a41162d))
- [G2P-5275](https://openg2p.atlassian.net/browse/G2P-5275) fix(minio): update bucket handling to use StrEnum directly ([`3140005`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3140005bd027d2d387a673e70bcdbaae275f78d5))
- [G2P-4763](https://openg2p.atlassian.net/browse/G2P-4763) fix(model): update bucket column type to Enum - change bucket column from String to Enum for DocumentBucket - adjust default value for bucket to use Enum directly ([`d9b49b7`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d9b49b7645ed77a75fec0fae2c56893b89544465))
- [G2P-5275](https://openg2p.atlassian.net/browse/G2P-5275) fix(helper): correct import path for DocumentBucket ([`d0359fd`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d0359fd27cf924b3bfcdb437d3007288df544cb3))
- [G2P-5336](https://openg2p.atlassian.net/browse/G2P-5336) fix(controller): unify error response handling for new document controller ([`737c444`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/737c44447b063627e145377e8d8800c17bfd23eb))
- [G2P-5336](https://openg2p.atlassian.net/browse/G2P-5336) fix(errors): update error handling to use new default error code ([`69ad5ee`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/69ad5ee2fad88b69b1b2f1920db9e70b8b2948fb))
- [G2P-5339](https://openg2p.atlassian.net/browse/G2P-5339) refactor: update docs widget configuration to use 'widget-total-docs' and enhance column distribution logic ([`cd85f91`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/cd85f9156c45e66d8c93f78327f218b35711f2b9))
- [G2P-5238](https://openg2p.atlassian.net/browse/G2P-5238) refactor: remove fixed layout configuration from geo hierarchy widget and improve column distribution logic ([`1cb6017`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1cb6017df8a6850b02801a0e8e9df13ee0b78c6b))
- [G2P-5275](https://openg2p.atlassian.net/browse/G2P-5275) refactor(documents): add dashboard image validation profile ([`142b0f2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/142b0f27ca95e5b50bd490f51dbdd33a007ea91a))
- [G2P-5326](https://openg2p.atlassian.net/browse/G2P-5326) feat(documents): enhance file validation and upload profiles ([`1b4581b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1b4581bc20b9a74727ce9ddb165c24f95db18880))
- [G2P-5275](https://openg2p.atlassian.net/browse/G2P-5275) refactor(icons): enhance file validation for uploads ([`d459348`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d459348825030d5b898f489bd6be29c2f586d512))
- [G2P-5334](https://openg2p.atlassian.net/browse/G2P-5334) Remove dash from new intake form breadcrumb ([`3520034`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3520034cf157cfec9e5d7f0497319657d7332309))
- [G2P-5332](https://openg2p.atlassian.net/browse/G2P-5332) add register icon remove button ([`b4a2d47`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b4a2d47725861e6db6a10a4e24786c7f76b464dd))
- [G2P-5339](https://openg2p.atlassian.net/browse/G2P-5339) add docs widget ([`66aed2a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/66aed2a4cf094a820d51ba1bdbf84452678f0252))
- [G2P-5325](https://openg2p.atlassian.net/browse/G2P-5325) refactor(documents): update document handling and request response ([`595e7dc`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/595e7dcf3374fa4b7cad04c3a82738604bc7d779))
- [G2P-5238](https://openg2p.atlassian.net/browse/G2P-5238) refactor: improve geo location, requestDataSourceHandler, and translation handling ([`9117fe8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/9117fe885fcafca9ba7aab3305c21426cc64d8ad))
- [G2P-5326](https://openg2p.atlassian.net/browse/G2P-5326) fix: template file upload size and type ([`8dbcb73`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/8dbcb736bbc42de6c5d159c9b341c891472f8c70))
- [G2P-5275](https://openg2p.atlassian.net/browse/G2P-5275) fix: update 1MB image upload limit for logo, favicon, and register icon ([`fd6a81d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fd6a81de7a737212dd6725b645d04f87cdcbca56))
- [G2P-5325](https://openg2p.atlassian.net/browse/G2P-5325) refactor(documents): update environment variables and streamline document handling ([`b0c2e53`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b0c2e53b0e641f7d082e97acb0bc7507d21d30b4))
- [G2P-5325](https://openg2p.atlassian.net/browse/G2P-5325) refactor(documents): update document handling and configurations for celery queue tasks ([`40fdc64`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/40fdc644350c9959b319594ea4844f2fa3ddef01))
- [G2P-5325](https://openg2p.atlassian.net/browse/G2P-5325) refactor(documents): streamline document handling in apis and remove template file controller ([`fd5666e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fd5666e57c7a88f85b15cadb81016cfb02892c4b))
- [G2P-5307](https://openg2p.atlassian.net/browse/G2P-5307) ([`14ae7bd`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/14ae7bde33b24bd2513e1e68e45f48b585ea2185))
- [G2P-5307](https://openg2p.atlassian.net/browse/G2P-5307) refactor(documents): streamline document handling and update schemas ([`09f5306`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/09f53060963e5f18e09f93d8911b410a0f4d9c0f))
- [G2P-5306](https://openg2p.atlassian.net/browse/G2P-5306) refactor(document): restructure document handling and abstract MinioClient ([`7ba5cbe`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7ba5cbebc018f20091d6b7002e20b7d162ed4f91))
- [G2P-5307](https://openg2p.atlassian.net/browse/G2P-5307) refactor(models): update document handling in data models ([`c20ccd8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c20ccd825362ac9ddc430c20994ebe40d8b3c944))
- [G2P-5319](https://openg2p.atlassian.net/browse/G2P-5319) Permission decorated enabled on one API. ([`e11e8fe`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/e11e8fe14d717636da5cc8cd1c3d16694db57cca))
- [G2P-5318](https://openg2p.atlassian.net/browse/G2P-5318) Restrict config nav to CONFIG_NAV_ACTIONS and guard config sub-pages ([`aaca369`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/aaca36983e9e86dea39674c0167371253006d4ab))
- [G2P-5262](https://openg2p.atlassian.net/browse/G2P-5262) refactor: update attribute value fetching in AttributeValueInput component ([`02ddbfb`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/02ddbfbc08b854a9fe3357a6e1071d6adbfd67f8))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Repoint Partner Management to commons-services and align PM-seed auth to the g2p-bridge pmSeedClientId pattern. ([`7d798a4`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7d798a430fb4ae254fdd749ed06b766bff8f2fc7))
- changed the widget version and published the dev ([`f2ef6ab`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f2ef6ab88262300981abdd7530de65c914f304a8))
- [G2P-5271](https://openg2p.atlassian.net/browse/G2P-5271) Update version to 1.1.0 across all modules ([`60f853d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/60f853de9f4007f98f9e8619e22f8f34804c89fb))
- [G2P-5181](https://openg2p.atlassian.net/browse/G2P-5181): Record Level Access - Approach using BaseRepository with Generics T ([`1ab3f52`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1ab3f527730353e97b6b5657cd51a9c9496db317))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Consent and partner management related. ([`873f96a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/873f96aa7c2624e5bcee3ca51df344d659f6cdd2))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Enhancements for consent management, partner management and WJS support. ([`a9ba084`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/a9ba084b7654de83842e97cbf3c8f4f29ec6edd4))
- 'develop' version was incorrect in init.py. Changed to 0.0.0-dev0 ([`3dd3947`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3dd3947aeb10293855202d76696c408beaa727e3))
- [G2P-5267](https://openg2p.atlassian.net/browse/G2P-5267) rename attribute labels to reference data ([`37aee91`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/37aee9110037cee04cd676cd88211bc4e9a428a3))
- [G2P-5262](https://openg2p.atlassian.net/browse/G2P-5262) feat: add new data policy management features for administrative areas and reference data ([`533420a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/533420afb69b95229ec51ce796ea4d37a2739497))
- [G2P-5265](https://openg2p.atlassian.net/browse/G2P-5265) feat(intake): add configurable reference generator ([`55cf95d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/55cf95dd473eda2885cce6a1a03439b0b6684eba))
- [G2P-5263](https://openg2p.atlassian.net/browse/G2P-5263) Update breadcrumbs for register and intake form pages ([`dad3970`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/dad39709fb54a307b61dbf7f5c58d85412d24b56))
- [G2P-5262](https://openg2p.atlassian.net/browse/G2P-5262) feat: extend data policy to handle new policy target ([`faef96b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/faef96bdd783349c7553b2a77a2d89a9b9f4f65b))
- [G2P-5255](https://openg2p.atlassian.net/browse/G2P-5255) Refactor AWE proxy request handling to support pagination and improve payload resolution ([`364cce2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/364cce2cefd2cd93d50aa4365f0f90ac3e2c5e69))
- [G2P-5122](https://openg2p.atlassian.net/browse/G2P-5122) cleanup: remove unused change request approval code ([`f538140`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f53814018f7158da6f9aec58d2a6a2fbc88cd8be))
- [G2P-5122](https://openg2p.atlassian.net/browse/G2P-5122): add approvals list ([`b64eda0`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b64eda0920c70c29ebaead9eb2a128a66cf82255))
- [G2P-5255](https://openg2p.atlassian.net/browse/G2P-5255) Add CSRF validation configuration for staff-portal-api requests ([`1f8c663`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1f8c663d3a0ded1841efd87e9a1c96ea1be3ecda))
- [G2P-5178](https://openg2p.atlassian.net/browse/G2P-5178) feat(attribute-service): add search functionality for attributes and values ([`78f2d13`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/78f2d1328420dcf731b70ae55dd6e3fd708422e1))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) feat: support logo within text and registry favicon ([`8ba88a2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/8ba88a28e6032f68299432f52d3f8b98285e8935))
- [G2P-5247](https://openg2p.atlassian.net/browse/G2P-5247) Add request_id to VersionForDateData and update G2PRegisterService to populate it from change requests ([`f31d5b8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f31d5b89ea0e5fb954d2f4af871bb5217136e110))
- [G2P-5245](https://openg2p.atlassian.net/browse/G2P-5245) feat(application-reference): add application reference field, its generation, usage and update api ([`a2a9ece`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/a2a9eced23a584ccb43ba87568aa1a961721f162))
- [G2P-5238](https://openg2p.atlassian.net/browse/G2P-5238) refactor: improve UI widgets and add example UI schema reference ([`866ed7a`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/866ed7ace683f1e752d42f5c460e409ffd190ec1))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Add cookieDomain to environment configuration and update auth cookie handling ([`bffa646`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/bffa64684394f29747f74f1722024a479f6d28a2))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Add assignee_name field to ApprovalTask model and update related logic ([`5648eb2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5648eb2f95bb7f5cb59be06a053ce8d45fe5751c))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Add upgrade-insecure-requests to CSP header ([`71c5085`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/71c5085cfc1067bf45bfe3cdd8d9ac61ea241034))
- [G2P-5182](https://openg2p.atlassian.net/browse/G2P-5182) fix: boolean conditional visibility, dialog-table conditions, and attribute API hooks ([`48f4136`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/48f41364aa11ad02e80cbe204f55b82d95af804e))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Fix: rollback CR changes when terminal approval validation fails ([`8868209`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/88682099c356820fa9ab71d1ec9d038b924c3a01))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Add list_tasks_for_request endpoint and related functionality ([`0ac9dce`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0ac9dcee872d2c270f30804d0acc67b2838a1109))
- [G2P-5219](https://openg2p.atlassian.net/browse/G2P-5219) feat(change-request): add pre-approve hook for change requests ([`1f236ae`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1f236ae68f75f6aebf011c910f7a811b09f5f19c))
- fix: correct variable name in G2PRegistrantAuthenticationControllerService ([`20ba84f`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/20ba84fee15e14e4f6d35554430e8ed4ad75a1b1))
- [G2P-5208](https://openg2p.atlassian.net/browse/G2P-5208) refactor(intake-form): simplify submission search logic ([`b7fd7e9`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b7fd7e9aa82ff75c660e747bda6da11ecbb5635b))
- [G2P-5206](https://openg2p.atlassian.net/browse/G2P-5206) refactor(models): remove deprecated G2PIntakeFormSectionPayload class ([`fffbde9`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fffbde9a586f5124b1556876ca6ae315251db39d))
- [G2P-5207](https://openg2p.atlassian.net/browse/G2P-5207) fix: translations and UI schema seeding ([`5e43850`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/5e43850944e58926167dc1282f71cd4be0d40582))
- [G2P-5206](https://openg2p.atlassian.net/browse/G2P-5206) feat: add upsert functionality for submission search text in intake form data service ([`02a7a34`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/02a7a342cc3ea18249202197a2ebb83089f8bfc8))
- [G2P-5194](https://openg2p.atlassian.net/browse/G2P-5194) - changed version to develop in develop branch ([`26a1690`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/26a16900553e77ed314248de8530311b8f61b75c))
- [G2P-5183](https://openg2p.atlassian.net/browse/G2P-5183) Add client-side CSRF token handling ([`e9b48ad`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/e9b48ad4fb1dc808a474b01c5aa09fa70aadeb70))
- [G2P-5154](https://openg2p.atlassian.net/browse/G2P-5154) Update environment variables, and refactor logout handling ([`cbead27`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/cbead274b7c0a43f2e81d7b29c7e8e45a6047c1e))
- [G2P-5153](https://openg2p.atlassian.net/browse/G2P-5153) Refactor IAM permission handling and authentication cookie management ([`8a6abe5`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/8a6abe5de479bf2647f89b31fbfa62989114ef3e))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
