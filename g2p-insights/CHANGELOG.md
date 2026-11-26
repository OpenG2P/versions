# g2p-insights

_Published automatically._

**Repository:** [github.com/OpenG2P/g2p-insights](https://github.com/OpenG2P/g2p-insights) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.24`](#v-0-0-0-develop-24) | 2026-11-26 | develop |  |
| [`0.0.0-develop.23`](#v-0-0-0-develop-23) | 2026-11-25 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-24"></a>

## g2p-insights — develop 0.0.0-develop.24 (2026-11-26)

_commit `25a5ef9` · changes since 0.0.0-develop.23_
<!-- build:0.0.0-develop.24 revision:25a5ef9257f5f46e2c70d56b6e746b4693369ce6 ts:1795657155 -->

**Chart:** [openg2p-insights 0.0.0-develop.24](https://openg2p.github.io/openg2p-helm/openg2p-insights-0.0.0-develop.24.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Rancher form: Superset service-account Secret named for registry.dashboards as well ([`25a5ef9`](https://github.com/OpenG2P/g2p-insights/commit/25a5ef9257f5f46e2c70d56b6e746b4693369ce6))

<a id="v-0-0-0-develop-23"></a>

## g2p-insights — develop 0.0.0-develop.23 (2026-11-25)

_commit `0f0bf36` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.23 revision:0f0bf36a646217aa0c472dd75e01d210cd5657c1 ts:1795572411 -->

**Chart:** [openg2p-insights 0.0.0-develop.23](https://openg2p.github.io/openg2p-helm/openg2p-insights-0.0.0-develop.23.tgz)

### Summary

- **Major:** Migration of g2p-insights from GitLab to GitHub, including the introduction of a dedicated Dockerfile for the evidence builder and default activation of INSTALL_AI.
- Dashboard updates and several bug fixes enhance overall functionality and user experience.
- Improvements to SQL resolution by the LLM and enhancements to the onboarding scripts streamline database integration and extension checks.
- Integration enhancements with Superset, including local integration and various feature additions, improve data visualization capabilities.
- New script added for onboarding new databases, specifically for creating materialized views, enhancing data handling.
- Expert Lab now includes pre-built common statistical functions, expanding analytical capabilities.
- Documentation has been significantly enhanced to improve clarity and usability.

### Changes

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Move g2p-insights from GitLab to GitHub: publish images and chart through openg2p-packaging, with the evidence builder in its own Dockerfile and INSTALL_AI on by default. ([`0f0bf36`](https://github.com/OpenG2P/g2p-insights/commit/0f0bf36a646217aa0c472dd75e01d210cd5657c1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Dashboard update. ([`3d6870c`](https://github.com/OpenG2P/g2p-insights/commit/3d6870c14be04c6d4975180247620cf0b6109f1c))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several fixes. ([`dc72aea`](https://github.com/OpenG2P/g2p-insights/commit/dc72aeaca60f25fffbd917e85b2be64852d20c96))
-  [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several improvements to get better SQL resolution by the LLM. ([`f5839f8`](https://github.com/OpenG2P/g2p-insights/commit/f5839f8984563f3a3cb2b52521b64b1e173492e4))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Doc enhanced ([`fbb8c40`](https://github.com/OpenG2P/g2p-insights/commit/fbb8c4020f48dbbb95eda7b595b0e801cca28337))
-  [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Doc enhanced ([`b755a55`](https://github.com/OpenG2P/g2p-insights/commit/b755a55c9509cf58ae5cddf1fd5370e940bd5845))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Onboarding scripts enhanced to look at DB and extensions both. ([`94f26eb`](https://github.com/OpenG2P/g2p-insights/commit/94f26eb4b5700f050fdd1d398807dd4c4cc78ee3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Onboarding scripts enhanced to look at DB and extensions both. ([`ad3a1b7`](https://github.com/OpenG2P/g2p-insights/commit/ad3a1b7e65df02367b19651f841dacbff6182b74))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Onboarding scripts enhanced. ([`89b2448`](https://github.com/OpenG2P/g2p-insights/commit/89b2448228f1bd109c7d2899ba14e92f35a4e557))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several enhancements for superset. ([`9e83b2e`](https://github.com/OpenG2P/g2p-insights/commit/9e83b2e2b005f28505197a8f4c19eed3080ff94f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several enhancements for superset. ([`5166862`](https://github.com/OpenG2P/g2p-insights/commit/5166862b4c4b1f4aaf803918de0e225481620db1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Superset integration related changes. ([`d1392d2`](https://github.com/OpenG2P/g2p-insights/commit/d1392d2b16bb43134c28ece39f2cb7d6646ab689))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Decimals reduced. ([`7103bdc`](https://github.com/OpenG2P/g2p-insights/commit/7103bdc7aa8de8c5b28fd85069251304ee9071b3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Script to onboard new database added - to create materialized views. ([`a20216e`](https://github.com/OpenG2P/g2p-insights/commit/a20216e8a37489dd64b3502e16c9e5a62ad3dfb7))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) More context sent to LLM under Ask. Few fixes. ([`73bbb1b`](https://github.com/OpenG2P/g2p-insights/commit/73bbb1bb9d806932fcb310efc96d96076db06c9e))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Expert Lab enhanced by adding pre-built common statistical functions. ([`c7e462d`](https://github.com/OpenG2P/g2p-insights/commit/c7e462df2234afd91c7ac7e61e6a9cb9ab17a7d8))
-  [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fixes, enhancements. ([`8e3a355`](https://github.com/OpenG2P/g2p-insights/commit/8e3a35584f4ec15cecef46d0b265419420285c85))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several additions. ([`838f445`](https://github.com/OpenG2P/g2p-insights/commit/838f445b9f151d2797833bd76b47ac2fd4247d95))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Integration with local superset. ([`13a3365`](https://github.com/OpenG2P/g2p-insights/commit/13a33656d15364598b1c2f2cd3198216f237e6d3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fixed few issues. ([`c904390`](https://github.com/OpenG2P/g2p-insights/commit/c904390eb078edb94672806332f919fc3ed3a8cf))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
