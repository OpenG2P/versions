# commons

_Published automatically._

**Repository:** [gitlab.com/openg2p/commons](https://gitlab.com/openg2p/commons)

| Version | Date | Type |
| --- | --- | --- |
| [`2.2.2-rc.214`](#v-2-2-2-rc-214) | 2026-08-24 | release candidate |
| [`0.0.0-develop.210`](#v-0-0-0-develop-210) | 2026-08-22 | develop |
| [`0.0.0-develop.209`](#v-0-0-0-develop-209) | 2026-08-21 | develop |
| [`0.0.0-develop.207`](#v-0-0-0-develop-207) | 2026-08-21 | develop |
| [`0.0.0-develop.206`](#v-0-0-0-develop-206) | 2026-08-21 | develop |
| [`0.0.0-develop.205`](#v-0-0-0-develop-205) | 2026-08-20 | develop |
| [`0.0.0-develop.204`](#v-0-0-0-develop-204) | 2026-08-20 | develop |
| [`0.0.0-develop.203`](#v-0-0-0-develop-203) | 2026-08-19 | develop |
| [`0.0.0-develop.202`](#v-0-0-0-develop-202) | 2026-08-14 | develop |
| [`0.0.0-develop.201`](#v-0-0-0-develop-201) | 2026-08-09 | develop |
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

# Release candidates

<a id="v-2-2-2-rc-214"></a>

## commons 2.2.2-rc.214 — 2026-08-24

_commit `623204a` · changes since 0.0.0-develop.210_
<!-- build:2.2.2-rc.214 revision:623204a94d0306d55434ae9ade1615d4135f548f ts:1787546739 -->

### Summary

- **Major:** Migration to GitLab CI for continuous integration, removing GitHub Actions for build and publish processes.
- Configuration updates: Added MinIO configuration to `values.yaml`, including secret references and read-only user creation.

### Changes

- [G2P-5451](https://openg2p.atlassian.net/browse/G2P-5451) Add MinIO configuration to values.yaml, including existing secret reference and read-only user creation ([`7f68072`](https://gitlab.com/openg2p/commons/-/commit/7f68072ad6599bb8c95c3f992fcf11a244ed0ebe))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`0988f9b`](https://gitlab.com/openg2p/commons/-/commit/0988f9b3c5af0b70f362e672975d99e25646b27e))

# Develop builds

<a id="v-0-0-0-develop-210"></a>

## commons — develop 0.0.0-develop.210 (2026-08-22)

_commit `9fad89d` · changes since 0.0.0-develop.209_
<!-- build:0.0.0-develop.210 revision:9fad89dd4dcef322cd12cf598dd625b4f7c99656 ts:1787361567 -->

### Changes

- Add --reset-keymanager to the commons-services uninstall: esignet and mock-identity run PKCS11, so their key material sits in softhsm while their key_alias rows sit in base-owned DBs that the uninstall deliberately keeps, and resetting softhsm alone leaves the aliases pointing at HSM keys that no longer exist so both fail at keymanager init on reinstall; the flag truncates just key_alias+key_store so keys regenerate, leaving application data intact ([`9fad89d`](https://gitlab.com/openg2p/commons/-/commit/9fad89dd4dcef322cd12cf598dd625b4f7c99656))

<a id="v-0-0-0-develop-209"></a>

## commons — develop 0.0.0-develop.209 (2026-08-21)

_commit `8082046` · changes since 0.0.0-develop.207_
<!-- build:0.0.0-develop.209 revision:8082046bc21c8cb5a2b1379f57a7105f17a640aa ts:1787321448 -->

### Changes

- Bump openg2p-master-data to 1.1.0-rc.55 and openg2p-iam-service to 1.4.0-rc.90 ([`8832184`](https://gitlab.com/openg2p/commons/-/commit/8832184f8053e10de50da41c1fa1c09b19e08ce2))

<a id="v-0-0-0-develop-207"></a>

## commons — develop 0.0.0-develop.207 (2026-08-21)

_commit `1653fdb` · changes since 0.0.0-develop.206_
<!-- build:0.0.0-develop.207 revision:1653fdb1a3acb423062ce0976f6efe10d052aaa9 ts:1787293936 -->

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ship Inji Certify with commons-services, enabled by default ([`1653fdb`](https://gitlab.com/openg2p/commons/-/commit/1653fdb1a3acb423062ce0976f6efe10d052aaa9))

<a id="v-0-0-0-develop-206"></a>

## commons — develop 0.0.0-develop.206 (2026-08-21)

_commit `460d8e4` · changes since 0.0.0-develop.205_
<!-- build:0.0.0-develop.206 revision:460d8e43e9ab293283c659eb22ad99fe65e34327 ts:1787287508 -->

### Changes

- Versions of MDS, Mock ID, IAM bumped up. ([`460d8e4`](https://gitlab.com/openg2p/commons/-/commit/460d8e43e9ab293283c659eb22ad99fe65e34327))

<a id="v-0-0-0-develop-205"></a>

## commons — develop 0.0.0-develop.205 (2026-08-20)

_commit `2515d20` · changes since 0.0.0-develop.204_
<!-- build:0.0.0-develop.205 revision:2515d20da59deafcf282ce79a9e539f4c6f2e887 ts:1787223518 -->

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add agent portal API overrides so its Keycloak URL and redirect resolve ([`2515d20`](https://gitlab.com/openg2p/commons/-/commit/2515d20da59deafcf282ce79a9e539f4c6f2e887))

<a id="v-0-0-0-develop-204"></a>

## commons — develop 0.0.0-develop.204 (2026-08-20)

_commit `fa817d9` · changes since 0.0.0-develop.203_
<!-- build:0.0.0-develop.204 revision:fa817d9d98a8748b20ac4b40fef85384e2b7fb26 ts:1787217613 -->

### Changes

- Bumped up version of IAM, and changed its location to Gitlab. ([`fa817d9`](https://gitlab.com/openg2p/commons/-/commit/fa817d9d98a8748b20ac4b40fef85384e2b7fb26))

<a id="v-0-0-0-develop-203"></a>

## commons — develop 0.0.0-develop.203 (2026-08-19)

_commit `9850037` · changes since 0.0.0-develop.202_
<!-- build:0.0.0-develop.203 revision:985003774f36a2041ff2f9af465f03c5236d19b3 ts:1787100806 -->

### Changes since 0.0.0-develop.202

- Bumped up AWE version to 0.0.0-develop.70 ([`9850037`](https://gitlab.com/openg2p/commons/-/commit/985003774f36a2041ff2f9af465f03c5236d19b3))

<a id="v-0-0-0-develop-202"></a>

## commons — develop 0.0.0-develop.202 (2026-08-14)

_commit `055b4d6` · changes since 0.0.0-develop.201_
<!-- build:0.0.0-develop.202 revision:055b4d69b5149dad32eb9321e6dd02b5bd5c3a5e ts:1786684414 -->

### Changes since 0.0.0-develop.201

- Fix IAM keycloak base URL in commons-services: set IAM_STAFF_KEYCLOAK_BASE_URL directly under iamStaffPortalApi.envVars with an explicit tpl call, since the subchart's indirection gets only one tpl pass and was emitting the unresolved 'https://keycloak.{{ tpl .Values.global.baseDomain $ }}' into the pod; drop the hardcoded qa keycloakBaseUrl which was dead anyway because a subchart-scoped global loses to the top-level one ([`055b4d6`](https://gitlab.com/openg2p/commons/-/commit/055b4d69b5149dad32eb9321e6dd02b5bd5c3a5e))

<a id="v-0-0-0-develop-201"></a>

## commons — develop 0.0.0-develop.201 (2026-08-09)

_commit `2cabc9c` · changes since 0.0.0-develop.200_
<!-- build:0.0.0-develop.201 revision:2cabc9c5aba91fa5b18ec9fbff2506d5bd44bc6f ts:1786255114 -->

### Changes since 0.0.0-develop.200

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Make the country pack a free-text field with short form guidance. The two-value enum let an environment pick only ETH or XKM, so a country adding its own pack to openg2p-data could not select it; the Rancher description now says where to find the directory name and the provenance notes move to values.yaml. ([`2cabc9c`](https://gitlab.com/openg2p/commons/-/commit/2cabc9c5aba91fa5b18ec9fbff2506d5bd44bc6f))

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
