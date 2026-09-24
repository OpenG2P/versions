# openg2p-registry-dr-hh-extensions

_Published automatically._

**Repository:** [github.com/OpenG2P/openg2p-registry-dr-hh-extensions](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.32`](#v-0-0-0-develop-32) | 2026-09-24 | develop |  |
| [`0.0.0-develop.29`](#v-0-0-0-develop-29) | 2026-09-24 | develop |  |
| [`0.0.0-develop.26`](#v-0-0-0-develop-26) | 2026-09-17 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-32"></a>

## openg2p-registry-dr-hh-extensions — develop 0.0.0-develop.32 (2026-09-24)

_commit `06bd805` · changes since 0.0.0-develop.29_
<!-- build:0.0.0-develop.32 revision:06bd805c94cb3cd27b66b4bcc9c0c3e6220aaa64 ts:1790247633 -->

**Chart:** [dom-household-registry 0.0.0-develop.32](https://openg2p.github.io/openg2p-helm/dom-household-registry-0.0.0-develop.32.tgz)

### Summary

_AI summary unavailable — re-run the workflow with `changelog_regenerate=0.0.0-develop.32` to generate it._

### Changes

- Add Dominican Republic geo hierarchy and update intake form definitions ([`10ea12b`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/10ea12b5411a6450fa1a5791510892cdbdf22a35))
- Enhance household registry extension: update PMT score computation, add new household fields, and restructure SQL schemas for improved data handling ([`0fdb273`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/0fdb273efde63b8db1e6ec562538fce4a1df2917))

<a id="v-0-0-0-develop-29"></a>

## openg2p-registry-dr-hh-extensions — develop 0.0.0-develop.29 (2026-09-24)

_commit `bdd6bbf` · changes since 0.0.0-develop.26_
<!-- build:0.0.0-develop.29 revision:bdd6bbf7ded71e0ef80c6397f9bc00ee29fdd51e ts:1790220340 -->

**Chart:** [dom-household-registry 0.0.0-develop.29](https://openg2p.github.io/openg2p-helm/dom-household-registry-0.0.0-develop.29.tgz)

### Summary

_AI summary unavailable — re-run the workflow with `changelog_regenerate=0.0.0-develop.29` to generate it._

### Changes

- Fix SQL syntax in theme values and themes configuration files ([`45f825c`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/45f825c983c532ce6907befb7d71859085919fa2))
- Household registry extension: PMT score computation, ingestion enrichers, sample data and metadata updates; remove geo lookup seed SQL ([`355bb79`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/355bb7912b2d65042a378909ab98f3aca74945c7))

<a id="v-0-0-0-develop-26"></a>

## openg2p-registry-dr-hh-extensions — develop 0.0.0-develop.26 (2026-09-17)

_commit `9dacfb7` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.26 revision:9dacfb713dba29abc950e29267b07ca0e2508d2e ts:1789651094 -->

**Chart:** [dom-household-registry 0.0.0-develop.26](https://openg2p.github.io/openg2p-helm/dom-household-registry-0.0.0-develop.26.tgz)

### Summary

_AI summary unavailable — re-run the workflow with `changelog_regenerate=0.0.0-develop.26` to generate it._

### Changes

- Update Helm chart values to use 'develop' tag for all APIs and workers ([`9dacfb7`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/9dacfb713dba29abc950e29267b07ca0e2508d2e))
- Update household registry extension: replace sections implementation, add Helm chart, AWE integration, master data, updated build tooling, and local dev test script ([`71b664f`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/71b664ff023f543fc9a6ff030695e6c07922add1))
- Replace register-metadata with new household sections (identity, address, dwelling, services, assets_and_risks, scores_and_eligibility, household_members), removing old form-version entries ([`fd2f977`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/fd2f9772fab82060310a8585b17a067429caa7ec))
- Wire up identity, address, dwelling, services, assets_and_risks, scores_and_eligibility, and household_members sections; fix broken imports in models/schemas init and household schema ([`925d242`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/925d242ff5b949bbe88aa904dca55be5b910ad12))
- feat: Enhance translation label insertion with distinct selection and priority ordering ([`49d9990`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/49d99901e6a360d3d381b926c8ee326aaf658676))
- translations ([`6a937ff`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/6a937ff46d2e178462d5f13a898e6651e45fe5a2))
- ui dividsion ([`b2505c0`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/b2505c04b5e90610fad26edb36c6aeb3ddae18d9))
- Translation ([`202ff80`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/202ff80747c7683fcd143e095a94ddf8573ee0ac))
- feat: Add household_id column and update related fields in household data scripts ([`446f024`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/446f0249866fe5d02c531cd21d4bfba3bd614c5c))
- feat: Enhance individual and household schemas with additional attributes ([`e06c3ed`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/e06c3edd4c827f7d651a71485e0f8d21b3cda870))
- added search,and fields ([`7bbc905`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/7bbc90582f4547f7ed639915ef66d4de91d8a9d5))
- [G2P-4936](https://openg2p.atlassian.net/browse/G2P-4936) Refactor PMT score computation logic and update scoring criteria ([`7e64bb8`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/7e64bb8c39c9d5480d37766c04938b9bfef8b9c1))
- docker files ([`7baf630`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/7baf6306526c73c243299bc2eb1403c7f062fd47))
- Technical names change ([`a2b682e`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/a2b682e2fc630ee7ee92fef7a3e56a8f2500af7a))
- intial ([`c5e3e81`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/c5e3e81a563f19538c44824a2f6bf222c0a1dbee))
- Initial commit ([`53f88b6`](https://github.com/OpenG2P/openg2p-registry-dr-hh-extensions/commit/53f88b6789765b709192fcf111b4ad2f116a6c17))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
