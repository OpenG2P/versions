# master-data-service

_Published automatically._

**Repository:** [github.com/OpenG2P/master-data-service](https://github.com/OpenG2P/master-data-service) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.66`](#v-0-0-0-develop-66) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-66"></a>

## master-data-service — develop 0.0.0-develop.66 (2026-08-28)

_commit `0bba3c9` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.66 revision:0bba3c9f46465a104bb7d60c092e1739c9e0c7be ts:1787885132 -->

**Chart:** [openg2p-master-data 0.0.0-develop.66](https://openg2p.github.io/openg2p-helm/openg2p-master-data-0.0.0-develop.66.tgz)

### Summary

- **Major:** Migration improvements: adjusted migration logic to ensure proper sequencing and prevent failures by waiting on the completion of critical tables.
- Feature enhancements: added geo level and attribute management, including new dialogs, localization updates, and support for data policies; introduced initial seed data for G2P attributes and values.
- UI updates: initialized the master-data-ui project with Next.js, added configuration for deployment, and enhanced geo locations and reference data management.
- Dependency management: pinned keycloak-init to a specific version and updated IAM service references from GitHub to GitLab, including version number adjustments.
- Code quality: applied pre-commit formatting across the repository, ensuring consistency without functional changes; fixed issues with pod selector conflicts and SQL codelist handling.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Pin keycloak-init to a version published on GitHub ([`0bba3c9`](https://github.com/OpenG2P/master-data-service/commit/0bba3c9f46465a104bb7d60c092e1739c9e0c7be))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`96f630f`](https://github.com/OpenG2P/master-data-service/commit/96f630f2f64cef0d06fe1c539ecb718542e01970))
- Apply pre-commit formatting across the repo (black line-length reflow in master-data-api, trailing whitespace in codelist SQL seeds, missing final newlines in UI files, README and .gitignore); formatting only, no functional change ([`b423005`](https://github.com/OpenG2P/master-data-service/commit/b42300512c21c72c41d0b71421003b5d7c3798aa))
- 67c4be5  [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`16a0d36`](https://github.com/OpenG2P/master-data-service/commit/16a0d36d8480be8f5e64f8ab33b08ab0459f0795))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on master-data-service ([`179581b`](https://github.com/OpenG2P/master-data-service/commit/179581b5a781d7afd23b09885f53de2df95abd8f))
- Fix for clashing pod selector. ([`4de586a`](https://github.com/OpenG2P/master-data-service/commit/4de586a941563743442d88e0892d57b7da15a089))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise national IDs when loading a country pack ([`fe9ce25`](https://github.com/OpenG2P/master-data-service/commit/fe9ce25ea14949d869a2e81723bc86aa8b193248))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update IAM service repository reference from GitHub to GitLab ([`446b691`](https://github.com/OpenG2P/master-data-service/commit/446b69150b93586b240be875353126203426f2b8))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update version numbers and pin IAM service reference to 1.4 ([`5efbd59`](https://github.com/OpenG2P/master-data-service/commit/5efbd59651052e0e20f025268f248f3ed2842464))
- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Carry the pack's birth_date through to the sample individuals table. The API builds these tables with create_all, which never adds a column to an existing one, so the seed job adds the column itself before inserting rather than failing on an environment seeded before this field existed. ([`4f29f7a`](https://github.com/OpenG2P/master-data-service/commit/4f29f7af99ef270f51386a709ff4032ae474aeab))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add configuration for Master Data UI deployment ([`86144ee`](https://github.com/OpenG2P/master-data-service/commit/86144ee891938e0d97537e471e0aa00536345320))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Update SQL codelists to handle conflicts and enhance Docker configurations ([`968c6fb`](https://github.com/OpenG2P/master-data-service/commit/968c6fb2693c947b7764baa9f1887b2d2461ef0e))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Add initial seed data for G2P attributes and values ([`a10123b`](https://github.com/OpenG2P/master-data-service/commit/a10123ba53ecf75d4cc2e8663b19d217851fd135))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enhance geo level value management with data policy support ([`67c4be5`](https://github.com/OpenG2P/master-data-service/commit/67c4be52fe8bee62f65899917dea73d83a83a19c))
- [G2P-5458](https://openg2p.atlassian.net/browse/G2P-5458) feat: add attribute and geo level management ([`6bad7a4`](https://github.com/OpenG2P/master-data-service/commit/6bad7a4ce930de29f4da8e416f224f896d23ef89))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat: enhance geo management with new dialogs and localization updates ([`1e95c1a`](https://github.com/OpenG2P/master-data-service/commit/1e95c1a9b16943ea1e1b31fd20e97d0b6bfb9664))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456) feat(master-data-ui): add geo locations and reference data management ([`275bf51`](https://github.com/OpenG2P/master-data-service/commit/275bf51a08c07871b47f4a4e2f804a68ab9d4406))
- [G2P-5456](https://openg2p.atlassian.net/browse/G2P-5456): initialize master-data-ui project with Next.js setup ([`876a1f4`](https://github.com/OpenG2P/master-data-service/commit/876a1f434b8ef207f39b826002b6dbcb47623baa))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Wait on the last table the migration creates, not the first. g2p_geo_levels is created before g2p_attributes and the sample tables, so gating on it proved only that the migration had started — wide enough for the loader to finish geo and then die on g2p_sample_households, which is the failure the guard exists to prevent. Waiting on g2p_sample_households proves the whole migration finished, since the creates are sequential and awaited. Also bounds the pg_isready loop, which could otherwise hang the init container indefinitely against an unreachable database. ([`a31a52b`](https://github.com/OpenG2P/master-data-service/commit/a31a52beab36324e77efd5dd96c74fc89c1f6c06))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Keep XKM as the chart default, and seed the whole pack rather than geography alone. Geography by itself leaves registries on their extension's own code lists, with no semantic role tags at all and no sample people — not a working default for anything downstream. The country itself stays a deployment decision: an install nobody configured must not attach invented figures to a real country's name or pick up a licence obligation by accident. ([`2476e12`](https://github.com/OpenG2P/master-data-service/commit/2476e12ba8ec64d515c5a35178661fc990be43b5))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
