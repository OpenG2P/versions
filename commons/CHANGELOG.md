# commons

_Published automatically._

**Repository:** [gitlab.com/openg2p/commons](https://gitlab.com/openg2p/commons)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.200`](#v-0-0-0-develop-200) | 2026-08-07 | develop |
| [`0.0.0-develop.199`](#v-0-0-0-develop-199) | 2026-08-06 | develop |
| [`2.2.1`](#v-2-2-1) | 2026-08-06 | release |
| [`0.0.0-develop.198`](#v-0-0-0-develop-198) | 2026-08-04 | develop |

# Releases

<a id="v-2-2-1"></a>

## commons 2.2.1 — 2026-08-06

<!-- build:2.2.1 revision:310bf240b836a50aac0757736e12d75df18b9b6e ts:1785994111 -->

_commit `310bf24` · changes since release 2.2.0_

### Release notes

Creating new Tag 2.2.1

### Summary

- **Major:** CI transition to GitLab, replacing GitHub Actions for build and publish processes.
- MinIO integration: added configuration to `values.yaml`, including secret references and read-only user setup.

### Changes

- [G2P-5451](https://openg2p.atlassian.net/browse/G2P-5451) Add MinIO configuration to values.yaml, including existing secret reference and read-only user creation ([`7f68072`](https://gitlab.com/openg2p/commons/-/commit/7f68072ad6599bb8c95c3f992fcf11a244ed0ebe))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`0988f9b`](https://gitlab.com/openg2p/commons/-/commit/0988f9b3c5af0b70f362e672975d99e25646b27e))

# Develop builds

<a id="v-0-0-0-develop-200"></a>

## commons — develop 0.0.0-develop.200 (2026-08-07)

_commit `95dd6fb` · changes since 0.0.0-develop.199_
<!-- build:0.0.0-develop.200 revision:95dd6fb73644da82b38e34662261fb1718463e72 ts:1786082259 -->

### Changes since 0.0.0-develop.199

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Enable EMBEDDED_SUPERSET. Insights loads /embedded/<uuid> in an iframe, a route Superset only registers with this flag — without it the embedded UUID and guest token are both issued successfully and only the iframe 404s, which reads as a broken client rather than a missing feature flag. ([`95dd6fb`](https://gitlab.com/openg2p/commons/-/commit/95dd6fb73644da82b38e34662261fb1718463e72))

<a id="v-0-0-0-develop-199"></a>

## commons — develop 0.0.0-develop.199 (2026-08-06)

_commit `53f78f2` · changes since 0.0.0-develop.198_
<!-- build:0.0.0-develop.199 revision:53f78f2a6050d361055ad476f49a5d2edbbc1afc ts:1786009812 -->

### Changes since 0.0.0-develop.198

- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) CI: refuse to run in forks (namespace guard) ([`53f78f2`](https://gitlab.com/openg2p/commons/-/commit/53f78f2a6050d361055ad476f49a5d2edbbc1afc))

<a id="v-0-0-0-develop-198"></a>

## commons — develop 0.0.0-develop.198 (2026-08-04)

_commit `b5b90d8` · changes since 2.2.0_
<!-- build:0.0.0-develop.198 revision:b5b90d8db9ccb37bb3ae0e7da82a7a29d14c2ea1 ts:1785826767 -->

### Summary

- CI/CD transition: switched from GitHub Actions to GitLab CI for build and publish processes.
- Configuration updates: added MinIO configuration to `values.yaml`, including secret references and read-only user creation; set default `baseDomain` to `{{ .Release.Namespace }}.openg2p.org` across commons charts.
- Country specification: declared Ethiopia as the country for the commons environment, integrating it into the form for better registry management.
- Helm version updates: bumped consent manager Helm version and multiple updates to Master Data Service versions, including to 0.0.0-develop.38.
- Job management improvement: enhanced superset `init-db` hook to ensure successful job cleanup, preventing stale pods from affecting release health.

### Changes since 2.2.0

- Just to trigger a build. No changes ([`b5b90d8`](https://gitlab.com/openg2p/commons/-/commit/b5b90d8db9ccb37bb3ae0e7da82a7a29d14c2ea1))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`2c340a3`](https://gitlab.com/openg2p/commons/-/commit/2c340a346f2f39ab5c54a94bd299f27466a37497))
- [G2P-5451](https://openg2p.atlassian.net/browse/G2P-5451) Add MinIO configuration to values.yaml, including existing secret reference and read-only user creation ([`b766eea`](https://gitlab.com/openg2p/commons/-/commit/b766eead30783b6e1f531e27937ecde1998e6cb1))
- Default baseDomain to {{ .Release.Namespace }}.openg2p.org in both commons charts, and make every consumer tpl it (29 values refs plus the keycloak gateway/virtualservice templates) since a single tpl pass does not evaluate a template nested inside a value and would otherwise emit the literal {{ .Release.Namespace }} into hostnames ([`adc388c`](https://gitlab.com/openg2p/commons/-/commit/adc388c5082613e409edcf1f70d56087d98136e3))
- Bumped up MDS version ([`ae68cf6`](https://gitlab.com/openg2p/commons/-/commit/ae68cf6a73d50925ee101d6192722cfecfa36edb))
- Bumped up MDS version. ([`d39f5eb`](https://gitlab.com/openg2p/commons/-/commit/d39f5eb17054534cff3ea552ce48e67386584c05))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare Ethiopia as the country for the commons environment, and surface the choice in the form. This is the one place an environment names its country — registries read the geography, code lists and sample people from Master Data and name none of their own, which is what lets one registry image serve any country. Master Data is installed from here, so the country pack, the code-list and sample switches, and the domain lists are all questions on this chart rather than values only reachable by hand-editing a subchart. ([`e9fba97`](https://gitlab.com/openg2p/commons/-/commit/e9fba97bf72a08e44bb6ec62890758a917ab511f))
- Add hook-succeeded to superset init-db hook-delete-policy so the Job and its pods (including a first-attempt deadlock retry) are removed once it succeeds, instead of a stale Error pod making a healthy release look failed; restate the hook keys explicitly since jobAnnotations {} never cleared the subchart defaults. Bumped up consent manager Helm version. ([`e862fe0`](https://gitlab.com/openg2p/commons/-/commit/e862fe0ef3db49cdf4863270990d4a83064bdedb))
- Bumped up MDS version to 0.0.0-develop.38 ([`fcd382e`](https://gitlab.com/openg2p/commons/-/commit/fcd382efa84535d8037d3afc5ff510a3deb3c485))
- Bumped up MDS version to 0.0.0-develop.36 ([`e77c23a`](https://gitlab.com/openg2p/commons/-/commit/e77c23ab167cd469a4da463c04fa3befe79af849))
- Bumped up Master Data Service version to 0.0.0-develop.31 ([`ab1f277`](https://gitlab.com/openg2p/commons/-/commit/ab1f2779a2549309c037007fbe4bf7739db657cc))
- Bumped up master data chart to 0.0.0-develop.30 ([`cf8be83`](https://gitlab.com/openg2p/commons/-/commit/cf8be838ab40c768a5a002d62dd47616c0562fa9))
- Bumped up Master Data Service version. ([`0e52ebf`](https://gitlab.com/openg2p/commons/-/commit/0e52ebf19de3fd2ac8af3c4dd128e0f2857f7162))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
