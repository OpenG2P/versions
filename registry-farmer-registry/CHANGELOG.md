# registry/farmer-registry

_Published automatically._

**Repository:** [gitlab.com/openg2p/registry/farmer-registry](https://gitlab.com/openg2p/registry/farmer-registry) · **Container images:** [Container Registry](https://gitlab.com/openg2p/registry/farmer-registry/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.146`](#v-0-0-0-develop-146) | 2026-08-06 | develop |
| [`0.0.0-develop.145`](#v-0-0-0-develop-145) | 2026-08-06 | develop |
| [`0.0.0-develop.144`](#v-0-0-0-develop-144) | 2026-08-05 | develop |
| [`0.0.0-develop.142`](#v-0-0-0-develop-142) | 2026-08-04 | develop |
| [`0.0.0-develop.141`](#v-0-0-0-develop-141) | 2026-08-04 | develop |
| [`0.0.0-develop.140`](#v-0-0-0-develop-140) | 2026-08-04 | develop |

# Develop builds

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
> candidates** per release line. Older develop builds and release candidates
> are pruned as they are superseded, and a release's candidates are removed
> once it ships. Those versions still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
