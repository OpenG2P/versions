# registry/disability-registry

_Published automatically._

**Repository:** [gitlab.com/openg2p/registry/disability-registry](https://gitlab.com/openg2p/registry/disability-registry) · **Container images:** [Container Registry](https://gitlab.com/openg2p/registry/disability-registry/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.7`](#v-0-0-0-develop-7) | 2026-08-19 | develop |
| [`0.0.0-develop.6`](#v-0-0-0-develop-6) | 2026-08-16 | develop |
| [`0.0.0-develop.4`](#v-0-0-0-develop-4) | 2026-08-15 | develop |
| [`0.0.0-develop.3`](#v-0-0-0-develop-3) | 2026-08-13 | develop |

# Develop builds

<a id="v-0-0-0-develop-7"></a>

## registry/disability-registry — develop 0.0.0-develop.7 (2026-08-19)

_commit `358802c` · changes since 0.0.0-develop.6_
<!-- build:0.0.0-develop.7 revision:358802c21d5736a6dd1e26b04097775e159676c6 ts:1787100539 -->

**Chart:** [openg2p-disability-registry 0.0.0-develop.7](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-disability-registry-0.0.0-develop.7.tgz)

### Changes since 0.0.0-develop.6

- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Correct the theme comment: the users are government staff, not the people whose records the registry holds. ([`358802c`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/358802c21d5736a6dd1e26b04097775e159676c6))

<a id="v-0-0-0-develop-6"></a>

## registry/disability-registry — develop 0.0.0-develop.6 (2026-08-16)

_commit `ff74399` · changes since 0.0.0-develop.4_
<!-- build:0.0.0-develop.6 revision:ff743994f3d382b2248b49a771fed4561673cbff ts:1786853384 -->

**Chart:** [openg2p-disability-registry 0.0.0-develop.6](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-disability-registry-0.0.0-develop.6.tgz)

### Summary

- **Major:** Dashboard functionality enabled with the inclusion of the Superset bundle, allowing the import job to run successfully.
- Reporting views job fixed by correcting entity name derivation from table names, ensuring proper parent-child relationships and resolving indexing issues on program enrolment.
- CI improvements: packaged chart files now include necessary components for building dashboards without a database.
- Data integrity enhancements through adjustments in mapping and indexing to comply with PII regulations.

### Changes since 0.0.0-develop.4

- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Enable dashboards and ship the Superset bundle. Reporting views were already on but the bundle was absent, so the import job never ran; CI packages the chart without a database to build one from, so files/dr-dashboards.zip is committed as in FR and NSR. ([`ff74399`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/ff743994f3d382b2248b49a771fed4561673cbff))
- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Fix the reporting views job. The generator derives entity names from table names, and g2p_register_persons_with_disability pluralises the head noun so it never matched the declared tree — every parent link was dropped, costing the children their geography and failing on the geo_1 index. Map it via views:, and stop indexing program_enrolment on program_name, which the pii rules withhold. ([`76890f8`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/76890f82b6daf5aa53aff5e794f156e55d0b98a7))

<a id="v-0-0-0-develop-4"></a>

## registry/disability-registry — develop 0.0.0-develop.4 (2026-08-15)

_commit `975b783` · changes since 0.0.0-develop.3_
<!-- build:0.0.0-develop.4 revision:975b783a217a6def41a56f8d482eab6788b630ea ts:1786787156 -->

**Chart:** [openg2p-disability-registry 0.0.0-develop.4](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-disability-registry-0.0.0-develop.4.tgz)

### Changes since 0.0.0-develop.3

- Bumped up RP version to 0.0.0-develop.384 ([`975b783`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/975b783a217a6def41a56f8d482eab6788b630ea))

<a id="v-0-0-0-develop-3"></a>

## registry/disability-registry — develop 0.0.0-develop.3 (2026-08-13)

_commit `cd0b5a7` · changes since the start_
<!-- build:0.0.0-develop.3 revision:cd0b5a7d1cd84f241d4e1175b9b0017fa5005571 ts:1786615579 -->

**Chart:** [openg2p-disability-registry 0.0.0-develop.3](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-disability-registry-0.0.0-develop.3.tgz)

### Summary

- **Major:** Initial version of the Disability Registry project established with foundational commits.
- Workflow adjustments implemented to enhance functionality and address issues.

### Changes since the start

- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Workflow fix. ([`cd0b5a7`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/cd0b5a7d1cd84f241d4e1175b9b0017fa5005571))
- Initial version. WIP. ([`003c1ea`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/003c1ea8b6c6b1c308b2ab5cb339f12a64fb6c6e))
- Initial commit ([`7e0c0d9`](https://gitlab.com/openg2p/registry/disability-registry/-/commit/7e0c0d97718894e6665695cfbafa05b0b8d18d35))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
