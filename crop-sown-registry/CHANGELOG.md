# crop-sown-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/crop-sown-registry](https://github.com/OpenG2P/crop-sown-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.21`](#v-0-0-0-develop-21) | 2026-10-02 | develop |  |
| [`0.0.0-develop.17`](#v-0-0-0-develop-17) | 2026-10-01 | develop |  |
| [`0.0.0-develop.11`](#v-0-0-0-develop-11) | 2026-09-29 | develop |  |
| [`0.0.0-develop.9`](#v-0-0-0-develop-9) | 2026-09-28 | develop |  |
| [`0.0.0-develop.6`](#v-0-0-0-develop-6) | 2026-09-28 | develop |  |
| [`0.0.0-develop.5`](#v-0-0-0-develop-5) | 2026-09-27 | develop |  |
| [`0.0.0-develop.4`](#v-0-0-0-develop-4) | 2026-09-27 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-21"></a>

## crop-sown-registry — develop 0.0.0-develop.21 (2026-10-02)

_commit `b580a2e` · changes since 0.0.0-develop.17_
<!-- build:0.0.0-develop.21 revision:b580a2e01771b4e00a1c1066fae4389eb233d630 ts:1790900560 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.21](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.21.tgz)

### Summary

- New feature: Linked farmer ID to Fayda FAN for consent checks and implemented final summaries for farmer season data, including period locking and validation tests.
- Data integrity: Introduced context fields and UI hints to prevent corrections from altering crop season data, with associated tests to ensure compliance.
- Version update: Bumped RP version to 0.0.0-develop.453.

### Changes

- Bumped up RP version to 0.0.0-develop.453. ([`b580a2e`](https://github.com/OpenG2P/crop-sown-registry/commit/b580a2e01771b4e00a1c1066fae4389eb233d630))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Link farmer ID to Fayda FAN for consent checks (subject_id_fields); tests ([`34842c0`](https://github.com/OpenG2P/crop-sown-registry/commit/34842c0405bb09a0c668b7f462f2fe5e4038ad1d))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Farmer season summary final on period lock (is_final in DCI); tests for final summaries and searches across farmers ([`9e65500`](https://github.com/OpenG2P/crop-sown-registry/commit/9e6550049415f556c052d62db01fc99debfe6d37))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Declare context fields and UI hints; test that a correction can't change the crop season ([`b66b6de`](https://github.com/OpenG2P/crop-sown-registry/commit/b66b6dedafe14d50dbb126bf842a63b43268fa2c))

<a id="v-0-0-0-develop-17"></a>

## crop-sown-registry — develop 0.0.0-develop.17 (2026-10-01)

_commit `93648c6` · changes since 0.0.0-develop.11_
<!-- build:0.0.0-develop.17 revision:93648c6adce9c604f35ddbf70dc11491447d7aac ts:1790829951 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.17](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.17.tgz)

### Summary

- **Major:** Introduced CSR phase 1 features including cluster entity registration with AWE approval, typed participant roles, and crop-change links, along with enhancements to DCI and reporting views.
- Geography enhancements: Required plot woreda for planning/sowing, new indicators and reporting views by region/zone/woreda, and improved farmer summary with season windows and shared locations.
- Testing improvements: Added DCI per-farmer queries for season summaries and filtered activities, along with documentation clarifying that developer tools like activity_definitions.py and build_seed_sql.py are not included in production.
- Helm configuration update: Sample data loading is now off by default, with an option to load sample crop seasons when enabled.

### Changes

- Bumped up RP version to 0.0.0-develop.448 ([`93648c6`](https://github.com/OpenG2P/crop-sown-registry/commit/93648c6adce9c604f35ddbf70dc11491447d7aac))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) test: DCI per-farmer queries (season summary, crop seasons, filtered and latest activities) ([`3bf8283`](https://github.com/OpenG2P/crop-sown-registry/commit/3bf82832b3d8c9078f589396833a2ecca57a4b91))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) helm: sample data off by default; Rancher question to load sample crop seasons (shown when Load Sample Data is on) ([`749f4e7`](https://github.com/OpenG2P/crop-sown-registry/commit/749f4e7d12328ee72a047b3510e3a2173c652952))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) CSR phase 1: Cluster entity register with AWE approval and sample clusters, typed participant roles, entities first (no temporary plot IDs), crop-change link, harvest_verified and replacement links in DCI and reporting view, sample crop seasons from Master Data people, partner correction in smoke test, tests ([`2691049`](https://github.com/OpenG2P/crop-sown-registry/commit/26910499217589065515b43cbf7b58d8ccc6e3c5))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Geography: plot woreda required when planning/sowing, indicators and reporting views by region/zone/woreda; season windows and shared location in the farmer summary; DCI crop-season and aggregate records on CSR's consent scopes ([`7900fe1`](https://github.com/OpenG2P/crop-sown-registry/commit/7900fe13028d2e77cc431f977f69c4f50b916b64))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Document that activity_definitions.py/build_seed_sql.py are developer tools; only the generated SQL ships ([`b16381f`](https://github.com/OpenG2P/crop-sown-registry/commit/b16381f4c0de412ff1a8add571a10b1c5fc79c2a))

<a id="v-0-0-0-develop-11"></a>

## crop-sown-registry — develop 0.0.0-develop.11 (2026-09-29)

_commit `393f014` · changes since 0.0.0-develop.9_
<!-- build:0.0.0-develop.11 revision:393f0146b22f583f85ae4849e5a995b6c25e8254 ts:1790646685 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.11](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.11.tgz)

### Summary

- **Major:** Introduced uninstall-registry.sh for streamlined removal of the registry, tailored for this release's persistent volumes.
- Version bump to RP 0.0.0-develop.444, indicating ongoing development and updates.

### Changes

- Bumped up RP version to 0.0.0-develop.444 ([`393f014`](https://github.com/OpenG2P/crop-sown-registry/commit/393f0146b22f583f85ae4849e5a995b6c25e8254))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Add uninstall-registry.sh (adapted from FR; no Superset step; only this release's PVs) ([`4cfd71a`](https://github.com/OpenG2P/crop-sown-registry/commit/4cfd71ab7ea66cd4e38c3cf59e0aa24ff4aeaa71))

<a id="v-0-0-0-develop-9"></a>

## crop-sown-registry — develop 0.0.0-develop.9 (2026-09-28)

_commit `525af83` · changes since 0.0.0-develop.6_
<!-- build:0.0.0-develop.9 revision:525af83ab52079d3e9639a605dd69f6cd96dd4a6 ts:1790616352 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.9](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.9.tgz)

### Summary

- Version update: bumped RP version to 0.0.0-develop.441.
- Testing enhancements: enabled sanity tests to improve reliability.
- Feature addition: implemented farmer season summary as an activity aggregate.

### Changes

- Bumped up RP version to 0.0.0-develop.441 ([`525af83`](https://github.com/OpenG2P/crop-sown-registry/commit/525af83ab52079d3e9639a605dd69f6cd96dd4a6))
- Sanity test enabled. ([`63649c4`](https://github.com/OpenG2P/crop-sown-registry/commit/63649c4dfd3a14e4f67a16538edf65d24e59bd4a))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Farmer season summary as an activity aggregate ([`8b54199`](https://github.com/OpenG2P/crop-sown-registry/commit/8b54199173d4d8d57bdfddc7103f5357075c7290))

<a id="v-0-0-0-develop-6"></a>

## crop-sown-registry — develop 0.0.0-develop.6 (2026-09-28)

_commit `4534b35` · changes since 0.0.0-develop.5_
<!-- build:0.0.0-develop.6 revision:4534b35ce82f69825a43546640bf47ba1606b2cd ts:1790561390 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.6](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.6.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Fix Helm form: questions.own.yaml must be a bare list so the inherited registry questions (images etc.) are kept; add ODK URL question ([`4534b35`](https://github.com/OpenG2P/crop-sown-registry/commit/4534b35ce82f69825a43546640bf47ba1606b2cd))

<a id="v-0-0-0-develop-5"></a>

## crop-sown-registry — develop 0.0.0-develop.5 (2026-09-27)

_commit `e3b9c2f` · changes since 0.0.0-develop.4_
<!-- build:0.0.0-develop.5 revision:e3b9c2f9b8005ab0846c573ff1975177e4305c82 ts:1790525469 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.5](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.5.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Read all code lists live from Master Data (ETH pack agriculture domain); drop CS_* lookup data; pin RP 0.0.0-develop.439 ([`e3b9c2f`](https://github.com/OpenG2P/crop-sown-registry/commit/e3b9c2f9b8005ab0846c573ff1975177e4305c82))

<a id="v-0-0-0-develop-4"></a>

## crop-sown-registry — develop 0.0.0-develop.4 (2026-09-27)

_commit `158ae4a` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.4 revision:158ae4ae07b780e21b1a5fd2d41bed0b9a6346ef ts:1790476942 -->

**Chart:** [openg2p-crop-sown-registry 0.0.0-develop.4](https://openg2p.github.io/openg2p-helm/openg2p-crop-sown-registry-0.0.0-develop.4.tgz)

### Summary

- **Major:** Introduced the Crop Sown Registry, enabling activity registration of crop seasons on the registry platform.
- Dependency management: pinned Crop Sown Registry to registry-platform version 0.0.0-develop.438 and updated the bump script to prevent generation of Chart.lock and chart tgz files.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Stop tracking generated Chart.lock and chart tgz; bump script no longer generates them ([`158ae4a`](https://github.com/OpenG2P/crop-sown-registry/commit/158ae4ae07b780e21b1a5fd2d41bed0b9a6346ef))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Pin Crop Sown Registry to registry-platform 0.0.0-develop.438; fix bump-rp-version.sh repo refresh ([`589961c`](https://github.com/OpenG2P/crop-sown-registry/commit/589961cb20df2b0cb0972f8ae2db1305971c1488))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Add Crop Sown Registry: activity register of crop seasons on the registry platform ([`a0340ba`](https://github.com/OpenG2P/crop-sown-registry/commit/a0340ba73fe7adce60273010a54d6e937193cc33))
- Initial commit ([`69aec11`](https://github.com/OpenG2P/crop-sown-registry/commit/69aec119f90d6158e856092197f5638fa5c52588))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
