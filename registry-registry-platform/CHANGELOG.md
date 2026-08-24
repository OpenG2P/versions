# registry/registry-platform

_Published automatically._

**Repository:** [gitlab.com/openg2p/registry/registry-platform](https://gitlab.com/openg2p/registry/registry-platform) · **Container images:** [Container Registry](https://gitlab.com/openg2p/registry/registry-platform/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.415`](#v-0-0-0-develop-415) | 2026-08-24 | develop |
| [`0.0.0-develop.414`](#v-0-0-0-develop-414) | 2026-08-24 | develop |
| [`0.0.0-develop.411`](#v-0-0-0-develop-411) | 2026-08-24 | develop |
| [`0.0.0-develop.409`](#v-0-0-0-develop-409) | 2026-08-23 | develop |
| [`0.0.0-develop.408`](#v-0-0-0-develop-408) | 2026-08-23 | develop |
| [`0.0.0-develop.407`](#v-0-0-0-develop-407) | 2026-08-23 | develop |
| [`0.0.0-develop.406`](#v-0-0-0-develop-406) | 2026-08-23 | develop |
| [`0.0.0-develop.404`](#v-0-0-0-develop-404) | 2026-08-22 | develop |
| [`0.0.0-develop.403`](#v-0-0-0-develop-403) | 2026-08-22 | develop |
| [`0.0.0-develop.402`](#v-0-0-0-develop-402) | 2026-08-22 | develop |
| [`1.2.0-rc.419`](#v-1-2-0-rc-419) | 2026-08-21 | release candidate |
| [`1.2.0-rc.411`](#v-1-2-0-rc-411) | 2026-08-21 | release candidate |
| [`0.0.0-develop.392`](#v-0-0-0-develop-392) | 2026-08-21 | develop |
| [`1.2.0-rc.410`](#v-1-2-0-rc-410) | 2026-08-21 | release candidate |
| [`0.0.0-develop.391`](#v-0-0-0-develop-391) | 2026-08-21 | develop |
| [`0.0.0-develop.390`](#v-0-0-0-develop-390) | 2026-08-21 | develop |
| [`1.2.0-rc.408`](#v-1-2-0-rc-408) | 2026-08-20 | release candidate |
| [`1.2.0-rc.407`](#v-1-2-0-rc-407) | 2026-08-20 | release candidate |
| [`1.2.0-rc.402`](#v-1-2-0-rc-402) | 2026-08-20 | release candidate |
| [`0.0.0-develop.389`](#v-0-0-0-develop-389) | 2026-08-20 | develop |
| [`0.0.0-develop.388`](#v-0-0-0-develop-388) | 2026-08-20 | develop |
| [`0.0.0-develop.387`](#v-0-0-0-develop-387) | 2026-08-20 | develop |
| [`1.2.0-rc.399`](#v-1-2-0-rc-399) | 2026-08-19 | release candidate |
| [`1.2.0-rc.397`](#v-1-2-0-rc-397) | 2026-08-18 | release candidate |
| [`1.2.0-rc.396`](#v-1-2-0-rc-396) | 2026-08-14 | release candidate |
| [`1.2.0-rc.393`](#v-1-2-0-rc-393) | 2026-08-14 | release candidate |
| [`0.0.0-develop.384`](#v-0-0-0-develop-384) | 2026-08-14 | develop |
| [`0.0.0-develop.383`](#v-0-0-0-develop-383) | 2026-08-09 | develop |
| [`0.0.0-develop.379`](#v-0-0-0-develop-379) | 2026-08-07 | develop |
| [`0.0.0-develop.378`](#v-0-0-0-develop-378) | 2026-08-06 | develop |

# Release candidates

<a id="v-1-2-0-rc-419"></a>

## registry/registry-platform 1.2.0-rc.419 — 2026-08-21

_commit `67ec038` · changes since 1.2.0-rc.411_
<!-- build:1.2.0-rc.419 revision:67ec038e21114ac2c7e44c4a4bb90fb8659cd118 ts:1787301550 -->

**Chart:** [openg2p-registry 1.2.0-rc.419](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.419.tgz)

### Summary

- **Major:** Updated IAM service repository reference from GitHub to GitLab and incremented IAM_CORE_REF to version 1.4, along with version number updates to 1.2.0 across multiple APIs.
- Enhanced IAM registration: added APP_API_URL environment variable and refactored data policy request helper, improving db-seed job configuration.
- Refactored UI components: removed functional id and tab id from useBreadcrumb, and implemented G2PIntakeRegisterSectionMapService with updates to related services and improved UI version history handling.

### Changes

- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`c2a1198`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c2a1198696cb9e72dfb7e7e4f834ae7f97cf2a99))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM_CORE_REF to version 1.4 and increment version numbers to 1.2.0 across multiple APIs; refactor data policy request helper and enhance db-seed job configuration. ([`66b2eac`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/66b2eac2547aac03b7d2a86b0902df507ee2526d))
- Refactor useBreadcrumb: remove functional id and tab id ([`0495193`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/04951937ca7e37283b7cbcfaa70b7373dfc4f48a))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Add APP_API_URL environment variable for IAM registration job ([`d77fd84`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/d77fd84fa9989ecc5cda2160f4bdc9b5aa71c26c))
- [G2P-5544](https://openg2p.atlassian.net/browse/G2P-5544) Implement G2PIntakeRegisterSectionMapService, update related services/components, and improve UI version history handling. ([`1f2ab43`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1f2ab43ea9141e37d8daad210d7565edff588173))

<a id="v-1-2-0-rc-411"></a>

## registry/registry-platform 1.2.0-rc.411 — 2026-08-21

_commit `f95c4fd` · changes since 1.2.0-rc.410_
<!-- build:1.2.0-rc.411 revision:f95c4fd2f121f3e0cd0c2a9a3fbc9a10b97f525a ts:1787294279 -->

**Chart:** [openg2p-registry 1.2.0-rc.411](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.411.tgz)

### Changes

- Published widget version 1.1.6-dev.6 and updated the ui for the same ([`f95c4fd`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f95c4fd2f121f3e0cd0c2a9a3fbc9a10b97f525a))

<a id="v-1-2-0-rc-410"></a>

## registry/registry-platform 1.2.0-rc.410 — 2026-08-21

_commit `a312a3e` · changes since 1.2.0-rc.408_
<!-- build:1.2.0-rc.410 revision:a312a3e6d7685b2e01b7a7dace01422b5885954c ts:1787292563 -->

**Chart:** [openg2p-registry 1.2.0-rc.410](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.410.tgz)

### Changes

- [G2P-5457](https://openg2p.atlassian.net/browse/G2P-5457) refactor: include all records with modified and new rows in diffTableRows ([`e7d2668`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/e7d2668c4c979a6a9c8c8735df13d0dd4aed098b))

<a id="v-1-2-0-rc-408"></a>

## registry/registry-platform 1.2.0-rc.408 — 2026-08-20

_commit `6028e77` · changes since 1.2.0-rc.407_
<!-- build:1.2.0-rc.408 revision:6028e771b07b44f7a8e8eea6a80c7233b61cd115 ts:1787227462 -->

**Chart:** [openg2p-registry 1.2.0-rc.408](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.408.tgz)

### Changes

- Published widget version 1.1.6-dev.5 and updated the ui for the same ([`6028e77`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/6028e771b07b44f7a8e8eea6a80c7233b61cd115))

<a id="v-1-2-0-rc-407"></a>

## registry/registry-platform 1.2.0-rc.407 — 2026-08-20

_commit `1e7a4a2` · changes since 1.2.0-rc.402_
<!-- build:1.2.0-rc.407 revision:1e7a4a22a8d067efdb5ee59f2cda613420dc8103 ts:1787222831 -->

**Chart:** [openg2p-registry 1.2.0-rc.407](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.407.tgz)

### Summary

- **Major:** Removal of attributes configuration and related components from the staff UI, including layout, pages, modals, and API routes, with sidebar options updated accordingly.
- UI enhancements: Added record table view functionality for record lists and refactored the intake form and task UI, along with the change request UI.
- Significant codebase changes: 111 files modified, with 2571 lines added and 2885 lines removed, indicating a substantial overhaul of the UI and API components.
- New components introduced: Added multiple shared entity list components, including CompactCard, DataTable, and StackedCard, enhancing the UI's modularity and functionality.

### Changes

- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): add record table view functionality for record list ([`66734c1`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/66734c1ce865055c4b1e018dea1415b8ee35fb73))
- [G2P-5546](https://openg2p.atlassian.net/browse/G2P-5546) refactor intake form and task ui ([`c6c852d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c6c852d9e356a65fb60510cade8e0b5d1f4aef0c))
- [G2P-5545](https://openg2p.atlassian.net/browse/G2P-5545): refactor change request ui ([`df686ef`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/df686ef2cf1cd85b5097e01c58d50f4d602e5f5a))
- [G2P-5457](https://openg2p.atlassian.net/browse/G2P-5457) Remove attributes configuration and related components from staff UI, including layout, pages, modals, and API routes. Update sidebar options to exclude attributes section. ([`650b158`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/650b158f2f9c46ca6cb399bd0e3a7d5fed179c75))

<a id="v-1-2-0-rc-402"></a>

## registry/registry-platform 1.2.0-rc.402 — 2026-08-20

_commit `0cfb813` · changes since 1.2.0-rc.399_
<!-- build:1.2.0-rc.402 revision:0cfb81321103be6a09da273cb51fa0c9a13bc919 ts:1787221025 -->

**Chart:** [openg2p-registry 1.2.0-rc.402](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-1.2.0-rc.402.tgz)

### Summary

- Change API enhancements: updated `sor_by` convention for change request searches and added unit tests for parsing sort parameters; included `register_mnemonic` and `tab_label` in change request data.
- Testing improvements: added new test files for change request data fields and search sort functionality, enhancing overall test coverage.

### Changes

- [G2P-5553](https://openg2p.atlassian.net/browse/G2P-5553) feat(change-api): update sor_by convention for change request searches and add unit tests for parsing sort parameters ([`0ac64f6`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0ac64f68b2bffad3c7152043d6e5885ae71cb1c8))
- [G2P-5541](https://openg2p.atlassian.net/browse/G2P-5541) fix(change-api): add register_mnemonic and tab_label in change request data ([`183b842`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/183b8429a115e10d76d05c73e0eac03e161502ef))

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

# Develop builds

<a id="v-0-0-0-develop-415"></a>

## registry/registry-platform — develop 0.0.0-develop.415 (2026-08-24)

_commit `779926e` · changes since 0.0.0-develop.414_
<!-- build:0.0.0-develop.415 revision:779926e73f2618800697c71153a86416e16a4247 ts:1787569778 -->

**Chart:** [openg2p-registry 0.0.0-develop.415](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.415.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Pull iam-core from GitLab instead of the frozen GitHub mirror ([`779926e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/779926e73f2618800697c71153a86416e16a4247))

<a id="v-0-0-0-develop-414"></a>

## registry/registry-platform — develop 0.0.0-develop.414 (2026-08-24)

_commit `746ac03` · changes since 0.0.0-develop.411_
<!-- build:0.0.0-develop.414 revision:746ac031c147116295edac7af8c7c950f425c565 ts:1787546954 -->

**Chart:** [openg2p-registry 0.0.0-develop.414](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.414.tgz)

### Summary

- User interface enhancement: introduced a landing page for the agent portal's tasks and aligned agent permissions with the staff portal's approach.
- Dependency update: bumped Keycloak-init version to improve authentication management.

### Changes

- Keycloak-init version bumped up. ([`746ac03`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/746ac031c147116295edac7af8c7c950f425c565))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Put the agent portal's tasks behind a landing page ([`0137024`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/01370249f8100c19e8be997cca797c0194e69362))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Resolve agent permissions the way the staff portal does ([`0db58a4`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0db58a45b91d6fe298f12e56c6116109ed3197e1))

<a id="v-0-0-0-develop-411"></a>

## registry/registry-platform — develop 0.0.0-develop.411 (2026-08-24)

_commit `bc49a26` · changes since 0.0.0-develop.409_
<!-- build:0.0.0-develop.411 revision:bc49a2655658fe3688caf8b9641db03b5bd3e83a ts:1787484876 -->

**Chart:** [openg2p-registry 0.0.0-develop.411](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.411.tgz)

### Summary

- **Major:** Rebuilt the agent portal UI using the Next.js BFF model from the staff portal, enhancing the overall architecture and user experience.
- Implemented reading of prefixed authentication cookies for the agent portal, improving session management and security.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Rebuild the agent portal UI on the staff portal's Next.js BFF model ([`bc49a26`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/bc49a2655658fe3688caf8b9641db03b5bd3e83a))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Read the agent portal's prefixed auth cookies ([`136f938`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/136f93812278ded5664dd7a3ab689a2e613d48ce))

<a id="v-0-0-0-develop-409"></a>

## registry/registry-platform — develop 0.0.0-develop.409 (2026-08-23)

_commit `cbbec9c` · changes since 0.0.0-develop.408_
<!-- build:0.0.0-develop.409 revision:cbbec9c34ab229b59bc0c7278e08f4cc39a49cce ts:1787466489 -->

**Chart:** [openg2p-registry 0.0.0-develop.409](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.409.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fail the credential-config job when Certify registration does not succeed ([`cbbec9c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/cbbec9c34ab229b59bc0c7278e08f4cc39a49cce))

<a id="v-0-0-0-develop-408"></a>

## registry/registry-platform — develop 0.0.0-develop.408 (2026-08-23)

_commit `65186d5` · changes since 0.0.0-develop.407_
<!-- build:0.0.0-develop.408 revision:65186d5a99fda5f381160b6975bb4342c29f1c52 ts:1787449885 -->

**Chart:** [openg2p-registry 0.0.0-develop.408](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.408.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix the provider-row SQL quoting so the bootstrap job can run unattended ([`65186d5`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/65186d5a99fda5f381160b6975bb4342c29f1c52))

<a id="v-0-0-0-develop-407"></a>

## registry/registry-platform — develop 0.0.0-develop.407 (2026-08-23)

_commit `32e978e` · changes since 0.0.0-develop.406_
<!-- build:0.0.0-develop.407 revision:32e978e0713fa6d9b58229664ecb78b68ed1ad4c ts:1787449553 -->

**Chart:** [openg2p-registry 0.0.0-develop.407](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.407.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Feed the provider-row SQL through stdin so psql interpolates the key ([`32e978e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/32e978e0713fa6d9b58229664ecb78b68ed1ad4c))

<a id="v-0-0-0-develop-406"></a>

## registry/registry-platform — develop 0.0.0-develop.406 (2026-08-23)

_commit `51d8ab2` · changes since 0.0.0-develop.404_
<!-- build:0.0.0-develop.406 revision:51d8ab20dd96e46bbc69ce9fb5d99382a12ce98d ts:1787446963 -->

**Chart:** [openg2p-registry 0.0.0-develop.406](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.406.tgz)

### Summary

- **Major:** Migration of Keycloak-init to GitLab with the latest version referenced in Chart.yaml, enhancing deployment and version management.
- Improved data seeding process by preventing failure when Master Data code lists are unavailable, increasing robustness during initialization.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Don't fail the whole seed when Master Data code lists are unavailable ([`51d8ab2`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/51d8ab20dd96e46bbc69ce9fb5d99382a12ce98d))
- Keycloak-init moved to Gitlab, and its latest version referenced in Chart.yaml. ([`efce0ec`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/efce0eca7248df624299e48124d7a5ddd75459d9))

<a id="v-0-0-0-develop-404"></a>

## registry/registry-platform — develop 0.0.0-develop.404 (2026-08-22)

_commit `1e269ad` · changes since 0.0.0-develop.403_
<!-- build:0.0.0-develop.404 revision:1e269ad1b31ad37306b3cc393294aba976f4358a ts:1787395282 -->

**Chart:** [openg2p-registry 0.0.0-develop.404](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.404.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Point master data DB credentials at the renamed secret ([`1e269ad`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/1e269ad1b31ad37306b3cc393294aba976f4358a))

<a id="v-0-0-0-develop-403"></a>

## registry/registry-platform — develop 0.0.0-develop.403 (2026-08-22)

_commit `4a98d83` · changes since 0.0.0-develop.402_
<!-- build:0.0.0-develop.403 revision:4a98d83b3a01bc7d71c69fdc68e69647239ec476 ts:1787374571 -->

**Chart:** [openg2p-registry 0.0.0-develop.403](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.403.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Use an image that actually provides openssl for keypair generation ([`4a98d83`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/4a98d83b3a01bc7d71c69fdc68e69647239ec476))

<a id="v-0-0-0-develop-402"></a>

## registry/registry-platform — develop 0.0.0-develop.402 (2026-08-22)

_commit `0b1e48d` · changes since 0.0.0-develop.392_
<!-- build:0.0.0-develop.402 revision:0b1e48dfb82e93a9bc7c300f10fb4fcbbf626989 ts:1787363335 -->

**Chart:** [openg2p-registry 0.0.0-develop.402](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.402.tgz)

### Summary

- **Major:** Bootstrap of the beneficiary-authentication setup and default issuer DID for clean VC issuance installation.
- Agent enhancements: Each registry now has its own Keycloak client, and a dedicated Keycloak realm with a unique hostname for the agent UI.
- Security improvements: Audit of agent portal actions to reject unresolved credential template placeholders.
- Fixes: Resolved issues with registrant authentication, agent UI API routing, and token fallback, ensuring proper session sharing and unblocking of the agent portal.
- Credential handling: Unwrapped the credential envelope and corrected the Certify proof audience.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Bootstrap the beneficiary-authentication setup from the chart ([`0b1e48d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/0b1e48dfb82e93a9bc7c300f10fb4fcbbf626989))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Default the issuer DID so a registry with VC issuance installs cleanly ([`625036c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/625036ca73d7fac5788afe92322b3a4cd31a978d))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Give each registry its own agent Keycloak clients ([`c383a49`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/c383a491645a36655db7ba2cd0ea608d4d648d73))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Audit agent portal actions and reject unresolved credential template placeholders ([`fa0e22b`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/fa0e22bfc9dbe3c3b386c20f7679392c184c1713))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Unwrap the credential envelope and fix the Certify proof audience ([`581952c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/581952ccdea751fe0808dd9d3e54d5b6f88d91c8))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix registrant authentication, agent UI API routing and token fallback ([`da26791`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/da26791645233b16ee3327618cadc4133197e3ae))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix registrant authentication and route the agent UI to its API ([`3bbf8a8`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/3bbf8a867680498bccc60b056589f29ea83580e4))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix registrant authentication: resolve the register model, share the session store, unblock the agent portal ([`f9f8e63`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f9f8e63fe30a7ecbf8707f64ab0f848c1f272227))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Create the agent Keycloak realm and give the agent UI its own hostname ([`61f85b1`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/61f85b1f9196f14578759b7822f12c25b7516a34))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Serve the agent UI on nginx's port instead of the Next.js port ([`b5cad3c`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/b5cad3c6971145be7ecdae78017f14d5021975ff))

<a id="v-0-0-0-develop-392"></a>

## registry/registry-platform — develop 0.0.0-develop.392 (2026-08-21)

_commit `f59189d` · changes since 0.0.0-develop.391_
<!-- build:0.0.0-develop.392 revision:f59189d8ab845936152b210834afccbd6824b22a ts:1787294219 -->

**Chart:** [openg2p-registry 0.0.0-develop.392](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.392.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Derive the Certify audience from a hostname instead of a hardcoded URL ([`f59189d`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/f59189d8ab845936152b210834afccbd6824b22a))

<a id="v-0-0-0-develop-391"></a>

## registry/registry-platform — develop 0.0.0-develop.391 (2026-08-21)

_commit `655590e` · changes since 0.0.0-develop.390_
<!-- build:0.0.0-develop.391 revision:655590e57fa15a2159bcceee5b717e5b65a02777 ts:1787274965 -->

**Chart:** [openg2p-registry 0.0.0-develop.391](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.391.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Harden the agent portal authentication popup to match the registry widget ([`655590e`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/655590e57fa15a2159bcceee5b717e5b65a02777))

<a id="v-0-0-0-develop-390"></a>

## registry/registry-platform — develop 0.0.0-develop.390 (2026-08-21)

_commit `22f62e7` · changes since 0.0.0-develop.389_
<!-- build:0.0.0-develop.390 revision:22f62e76542c3510e4be6dc238fd6bb4c71588ec ts:1787273161 -->

**Chart:** [openg2p-registry 0.0.0-develop.390](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.390.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Make the agent portal card volume optional so a missing ConfigMap cannot block startup ([`22f62e7`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/22f62e76542c3510e4be6dc238fd6bb4c71588ec))

<a id="v-0-0-0-develop-389"></a>

## registry/registry-platform — develop 0.0.0-develop.389 (2026-08-20)

_commit `7055e57` · changes since 0.0.0-develop.388_
<!-- build:0.0.0-develop.389 revision:7055e578d71eb89a14b359088f53a03a8e8344c6 ts:1787215823 -->

**Chart:** [openg2p-registry 0.0.0-develop.389](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.389.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix mangled show_if conditions and surface the VC master switch ([`7055e57`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/7055e578d71eb89a14b359088f53a03a8e8344c6))

<a id="v-0-0-0-develop-388"></a>

## registry/registry-platform — develop 0.0.0-develop.388 (2026-08-20)

_commit `12f3b99` · changes since 0.0.0-develop.387_
<!-- build:0.0.0-develop.388 revision:12f3b99826f263a96e2f54e203264716da42fd2e ts:1787213367 -->

**Chart:** [openg2p-registry 0.0.0-develop.388](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-registry-0.0.0-develop.388.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Surface the Certify base URL and proof audience in the install form ([`12f3b99`](https://gitlab.com/openg2p/registry/registry-platform/-/commit/12f3b99826f263a96e2f54e203264716da42fd2e))

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

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
