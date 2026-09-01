# consent-manager

_Published automatically._

**Repository:** [github.com/OpenG2P/consent-manager](https://github.com/OpenG2P/consent-manager) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.0.2-rc.61`](#v-1-0-2-rc-61) | 2026-09-01 | release candidate |  |
| [`1.0.1`](#v-1-0-1) | 2026-09-01 | release |  |
| [`1.0.1-rc.59`](#v-1-0-1-rc-59) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.58`](#v-0-0-0-develop-58) | 2026-09-01 | develop |  |
| [`1.0.1-rc.58`](#v-1-0-1-rc-58) | 2026-09-01 | release candidate |  |
| [`1.0.0`](#v-1-0-0) | 2026-09-01 | release |  |
| [`1.0.0-rc.57`](#v-1-0-0-rc-57) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.57`](#v-0-0-0-develop-57) | 2026-08-28 | develop |  |

# Releases

<a id="v-1-0-1"></a>

## consent-manager 1.0.1 — 2026-09-01

<!-- build:1.0.1 revision:c84a6ddeec6dcac06c9ef19ae18aa32ff81971dd ts:1788255147 -->

_commit `c84a6dd` · changes since release 1.0.0_

**Same artifact as [`1.0.1-rc.59`](#v-1-0-1-rc-59)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-consent-manager 1.0.1](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-1.0.1.tgz)

### Release notes

**Updated**
 - keycloak-init version to 1.2.0
 - fastapi-common version set to 1.2.0

### Summary

- Dependency updates: upgraded FASTAPI_COMMON_REF and keycloak-init to version 1.2.0, ensuring compatibility with the latest features and fixes.

### Changes

- Update FASTAPI_COMMON_REF to version 1.2.0 ([`c84a6dd`](https://github.com/OpenG2P/consent-manager/commit/c84a6ddeec6dcac06c9ef19ae18aa32ff81971dd))
- Update keycloak-init version to 1.2.0 ([`167a49e`](https://github.com/OpenG2P/consent-manager/commit/167a49ec5e708856651a8145b73b527ad910f76e))

<a id="v-1-0-0"></a>

## consent-manager 1.0.0 — 2026-09-01

<!-- build:1.0.0 revision:c67030b14e70decb46d2ebdbba07e4c9e63def7f ts:1787881677 -->

_commit `c67030b` · first release_

**Same artifact as [`1.0.0-rc.57`](#v-1-0-0-rc-57)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-consent-manager 1.0.0](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-1.0.0.tgz)

### Release notes

**Consent Manager 1.0.0**
First production-ready release of the OpenG2P Consent Manager (CM): a dedicated Policy Decision Point for outbound data sharing.

No personal data leaves a registry (or any other data-holding module) without a positive CM decision. The registry stays a Policy Enforcement Point — it never interprets consent, never holds partner signing keys, and never evaluates policy.

One CM instance is shared across modules (registry, PBMS, and others). Partner identity and keys live in Partner Management; CM holds only a thin policy binding.

Documentation: [docs.openg2p.org → Consent Management](https://docs.openg2p.org/platform/platform-services/consent-management)

**Highlights**

- Verify & enforce — partners embed a compact JWS consent object; CM verifies the signature against Partner Management keys, evaluates the partner’s data-share policy, and returns the effective fields the PEP may release (consent ∩ policy).
- Cryptographic proof — partner-signed consent objects; CM-signed Kantara/ISO 27560-aligned receipts published at /.well-known/jwks.json.
- Versioned partner policy — allowed fields, purposes, subject ID types, signing algorithms, validity ceiling, and fetch semantics. Policy widening can be gated by the Approval Workflow Engine (AWE).
- Consent origination — request → OIDC authenticate → approve/deny → artefact + receipt, plus revocation and scheduled expiry.
- Staff console — partner policy bindings, an AWE approvals inbox, and an immutable decision log.
- Platform-ready deploy — Helm chart with staff + partner APIs (beneficiary API scaffolded), Keycloak and Postgres init, Istio routing, HPA, signing-key Secret, expiry CronJob, and a release-blocking sanity Job.
-

Links

- Source: https://github.com/OpenG2P/consent-manager
- Design & API: https://docs.openg2p.org/platform/platform-services/consent-management
- License: Mozilla Public License 2.0

### Summary

- **Major:** Migration to GitLab: repository moved from GitHub, with updated README to reflect the change and disabled auto build/publish on GitHub.
- CI/CD enhancements: replaced docker-build and helm-publish with a centralized build-publish workflow, and published consent-manager images and charts exclusively to GitLab.
- Job configuration fixes: resolved duplicate environment variable issues in the cm-sanity Job and added nameOverride for better alignment with renamed API components.
- Keycloak updates: new location and version adjustments implemented for Keycloak initialization.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`c67030b`](https://github.com/OpenG2P/consent-manager/commit/c67030b14e70decb46d2ebdbba07e4c9e63def7f))
- Keycloak-init new location and version updated. ([`a434f9b`](https://github.com/OpenG2P/consent-manager/commit/a434f9b73a744aaa2687aa6917e39de3f514ebd4))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Point image source and project URLs at the new GitLab location (openg2p/platform-services/consent-manager). ([`81e8fd6`](https://github.com/OpenG2P/consent-manager/commit/81e8fd6f8a0bd1bcdc53ea83ae474abaa1bebe2c))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on consent-manager ([`9b09d4c`](https://github.com/OpenG2P/consent-manager/commit/9b09d4c655eaab0d52f456d9e07ed316736f0a94))
- Fix duplicate SANITY_VERIFY_TLS env in the cm-sanity Job (emitted both inline and via the shared pmSeedEnv helper), which made server-side apply reject the Job with "duplicate entries for key" and fail the release ([`a9f7c06`](https://github.com/OpenG2P/consent-manager/commit/a9f7c0684d3c0eb3286da61d81ed6f3343c6915b))
- The sanity and pm-seed Jobs hardcoded &lt;release&gt;-sanity / &lt;release&gt;-pm-seed, so when the API components are renamed via nameOverride the sanity Job name no longer lines up with them. Add sanity.nameOverride (default "" = no change) inserted as an infix: e.g. "cm" -&gt; &lt;release&gt;-cm-sanity / &lt;release&gt;-cm-pm-seed. ([`954ee5f`](https://github.com/OpenG2P/consent-manager/commit/954ee5f21b87245c3c5dfc2583552881f23d4f77))
- Minor edit to just stimulate helm publish. ([`64fa696`](https://github.com/OpenG2P/consent-manager/commit/64fa6965a4a6dcd68af70ba02290271a59deff09))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Freeze GitHub repo: add "moved to GitLab" README notice and disable auto build/publish (remove push/tag triggers). ([`d826db5`](https://github.com/OpenG2P/consent-manager/commit/d826db55ac86bac7cd3e6c70b55540bce3caeaf6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Re-run GitLab pipeline with fixed chart job ([`51fd07c`](https://github.com/OpenG2P/consent-manager/commit/51fd07c2a7e90c6ccd76436172f331ae373f023d))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Minor edit of README. ([`58f81a4`](https://github.com/OpenG2P/consent-manager/commit/58f81a4a14490f5d5edefde87efbdfc35b376f9f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Minor edit of README. ([`f87a6ea`](https://github.com/OpenG2P/consent-manager/commit/f87a6eaea7eda4839134990bc82c6a1da88e3a98))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Moved repo from Github as is. ([`8bf5787`](https://github.com/OpenG2P/consent-manager/commit/8bf57873609d7fafd1030d7d91b40f02fab4852b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Grant packages: write in caller to satisfy reusable workflow (fix startup failure) ([`88041e0`](https://github.com/OpenG2P/consent-manager/commit/88041e0bb0e001338e2ccdded9eb334108c614d3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish consent-manager images and chart to GitLab; drop GHCR ([`b38f1e7`](https://github.com/OpenG2P/consent-manager/commit/b38f1e7e9691d25f6e50ebcdd6d882412dcb0a3c))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) consent-manager: publish images + chart to GHCR (chart under charts/ to avoid image name clash) ([`b736910`](https://github.com/OpenG2P/consent-manager/commit/b73691010948b6fb58607aef4825f28b4f23ae3b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish images + chart to GHCR only (OCI), values to ghcr.io ([`6f7508a`](https://github.com/OpenG2P/consent-manager/commit/6f7508aa35737986fec55598e0a692384da7bf63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) clarify changelog workflow_dispatch input descriptions ([`326edee`](https://github.com/OpenG2P/consent-manager/commit/326edeebd7ca9b5284da5991f14b571046442ce6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) forward changelog dispatch inputs to central workflow ([`75b649f`](https://github.com/OpenG2P/consent-manager/commit/75b649f3ceafb79f250ea20d8464e94323d56d63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix in publish. ([`9ff69b6`](https://github.com/OpenG2P/consent-manager/commit/9ff69b6b74defc2d7f51095bd9504db1f108f95b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) ci: replace docker-build + helm-publish with central build-publish workflow ([`0a508a6`](https://github.com/OpenG2P/consent-manager/commit/0a508a6e8ecbbb33d5b1d6ad898c28e409c051b1))

# Release candidates

<a id="v-1-0-2-rc-61"></a>

## consent-manager 1.0.2-rc.61 — 2026-09-01

_commit `52bb1b0` · changes since 0.0.0-develop.57_
<!-- build:1.0.2-rc.61 revision:52bb1b021c3efd61103db332d7b1cc748cef9a30 ts:1788261125 -->

**Chart:** [openg2p-consent-manager 1.0.2-rc.61](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-1.0.2-rc.61.tgz)

### Summary

- Dependency updates: upgraded image tags to version 1.0.2, FASTAPI_COMMON_REF to version 1.2.0, and keycloak-init to version 1.2.0.

### Changes

- Update image tags to version 1.0.2 ([`8bce8bc`](https://github.com/OpenG2P/consent-manager/commit/8bce8bc5b544efd2a468c0f801d63273419be706))
- Update FASTAPI_COMMON_REF to version 1.2.0 ([`c84a6dd`](https://github.com/OpenG2P/consent-manager/commit/c84a6ddeec6dcac06c9ef19ae18aa32ff81971dd))
- Update keycloak-init version to 1.2.0 ([`167a49e`](https://github.com/OpenG2P/consent-manager/commit/167a49ec5e708856651a8145b73b527ad910f76e))

<a id="v-1-0-1-rc-59"></a>

## consent-manager 1.0.1-rc.59 — 2026-09-01

_commit `c84a6dd` · changes since 1.0.1-rc.58_
<!-- build:1.0.1-rc.59 revision:c84a6ddeec6dcac06c9ef19ae18aa32ff81971dd ts:1788255147 -->

**Chart:** [openg2p-consent-manager 1.0.1-rc.59](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-1.0.1-rc.59.tgz)

### Changes

- Update FASTAPI_COMMON_REF to version 1.2.0 ([`c84a6dd`](https://github.com/OpenG2P/consent-manager/commit/c84a6ddeec6dcac06c9ef19ae18aa32ff81971dd))

<a id="v-1-0-1-rc-58"></a>

## consent-manager 1.0.1-rc.58 — 2026-09-01

_commit `167a49e` · changes since 0.0.0-develop.57_
<!-- build:1.0.1-rc.58 revision:167a49ec5e708856651a8145b73b527ad910f76e ts:1788254415 -->

**Chart:** [openg2p-consent-manager 1.0.1-rc.58](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-1.0.1-rc.58.tgz)

### Changes

- Update keycloak-init version to 1.2.0 ([`167a49e`](https://github.com/OpenG2P/consent-manager/commit/167a49ec5e708856651a8145b73b527ad910f76e))

<a id="v-1-0-0-rc-57"></a>

## consent-manager 1.0.0-rc.57 — 2026-09-01

_commit `c67030b` · changes since 0.0.0-develop.57_
<!-- build:1.0.0-rc.57 revision:c67030b14e70decb46d2ebdbba07e4c9e63def7f ts:1787881677 -->

**Chart:** [openg2p-consent-manager 1.0.0-rc.57](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-1.0.0-rc.57.tgz)

### Changes

_No new commits since 0.0.0-develop.57._

# Develop builds

<a id="v-0-0-0-develop-58"></a>

## consent-manager — develop 0.0.0-develop.58 (2026-09-01)

_commit `5361069` · changes since 0.0.0-develop.57_
<!-- build:0.0.0-develop.58 revision:536106974a7f6d67501a45dfc02cb9da95348f37 ts:1788255124 -->

**Chart:** [openg2p-consent-manager 0.0.0-develop.58](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-0.0.0-develop.58.tgz)

### Changes

- Change FASTAPI_COMMON_REF to version 1.2.0 ([`5361069`](https://github.com/OpenG2P/consent-manager/commit/536106974a7f6d67501a45dfc02cb9da95348f37))

<a id="v-0-0-0-develop-57"></a>

## consent-manager — develop 0.0.0-develop.57 (2026-08-28)

_commit `c67030b` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.57 revision:c67030b14e70decb46d2ebdbba07e4c9e63def7f ts:1787881677 -->

**Chart:** [openg2p-consent-manager 0.0.0-develop.57](https://openg2p.github.io/openg2p-helm/openg2p-consent-manager-0.0.0-develop.57.tgz)

### Summary

- **Major:** Migration to GitLab: repository moved from GitHub, with updated README to reflect the change and disabled auto build/publish on GitHub.
- CI/CD enhancements: implemented a central build-publish workflow, replacing the previous docker-build and helm-publish processes; fixed chart job in GitLab pipeline.
- Image and chart publishing: consent-manager images and charts are now published exclusively to GitLab, with adjustments to avoid name clashes and ensure proper versioning.
- Environment variable fix: resolved duplicate SANITY_VERIFY_TLS environment variable issue in the cm-sanity Job, preventing job failures.
- Job name alignment: introduced sanity.nameOverride to ensure consistency in job naming when API components are renamed.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`c67030b`](https://github.com/OpenG2P/consent-manager/commit/c67030b14e70decb46d2ebdbba07e4c9e63def7f))
- Keycloak-init new location and version updated. ([`a434f9b`](https://github.com/OpenG2P/consent-manager/commit/a434f9b73a744aaa2687aa6917e39de3f514ebd4))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Point image source and project URLs at the new GitLab location (openg2p/platform-services/consent-manager). ([`81e8fd6`](https://github.com/OpenG2P/consent-manager/commit/81e8fd6f8a0bd1bcdc53ea83ae474abaa1bebe2c))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on consent-manager ([`9b09d4c`](https://github.com/OpenG2P/consent-manager/commit/9b09d4c655eaab0d52f456d9e07ed316736f0a94))
- Fix duplicate SANITY_VERIFY_TLS env in the cm-sanity Job (emitted both inline and via the shared pmSeedEnv helper), which made server-side apply reject the Job with "duplicate entries for key" and fail the release ([`a9f7c06`](https://github.com/OpenG2P/consent-manager/commit/a9f7c0684d3c0eb3286da61d81ed6f3343c6915b))
- The sanity and pm-seed Jobs hardcoded &lt;release&gt;-sanity / &lt;release&gt;-pm-seed, so when the API components are renamed via nameOverride the sanity Job name no longer lines up with them. Add sanity.nameOverride (default "" = no change) inserted as an infix: e.g. "cm" -&gt; &lt;release&gt;-cm-sanity / &lt;release&gt;-cm-pm-seed. ([`954ee5f`](https://github.com/OpenG2P/consent-manager/commit/954ee5f21b87245c3c5dfc2583552881f23d4f77))
- Minor edit to just stimulate helm publish. ([`64fa696`](https://github.com/OpenG2P/consent-manager/commit/64fa6965a4a6dcd68af70ba02290271a59deff09))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Freeze GitHub repo: add "moved to GitLab" README notice and disable auto build/publish (remove push/tag triggers). ([`d826db5`](https://github.com/OpenG2P/consent-manager/commit/d826db55ac86bac7cd3e6c70b55540bce3caeaf6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Re-run GitLab pipeline with fixed chart job ([`51fd07c`](https://github.com/OpenG2P/consent-manager/commit/51fd07c2a7e90c6ccd76436172f331ae373f023d))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Minor edit of README. ([`58f81a4`](https://github.com/OpenG2P/consent-manager/commit/58f81a4a14490f5d5edefde87efbdfc35b376f9f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Minor edit of README. ([`f87a6ea`](https://github.com/OpenG2P/consent-manager/commit/f87a6eaea7eda4839134990bc82c6a1da88e3a98))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Moved repo from Github as is. ([`8bf5787`](https://github.com/OpenG2P/consent-manager/commit/8bf57873609d7fafd1030d7d91b40f02fab4852b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Grant packages: write in caller to satisfy reusable workflow (fix startup failure) ([`88041e0`](https://github.com/OpenG2P/consent-manager/commit/88041e0bb0e001338e2ccdded9eb334108c614d3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish consent-manager images and chart to GitLab; drop GHCR ([`b38f1e7`](https://github.com/OpenG2P/consent-manager/commit/b38f1e7e9691d25f6e50ebcdd6d882412dcb0a3c))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) consent-manager: publish images + chart to GHCR (chart under charts/ to avoid image name clash) ([`b736910`](https://github.com/OpenG2P/consent-manager/commit/b73691010948b6fb58607aef4825f28b4f23ae3b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish images + chart to GHCR only (OCI), values to ghcr.io ([`6f7508a`](https://github.com/OpenG2P/consent-manager/commit/6f7508aa35737986fec55598e0a692384da7bf63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) clarify changelog workflow_dispatch input descriptions ([`326edee`](https://github.com/OpenG2P/consent-manager/commit/326edeebd7ca9b5284da5991f14b571046442ce6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) forward changelog dispatch inputs to central workflow ([`75b649f`](https://github.com/OpenG2P/consent-manager/commit/75b649f3ceafb79f250ea20d8464e94323d56d63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix in publish. ([`9ff69b6`](https://github.com/OpenG2P/consent-manager/commit/9ff69b6b74defc2d7f51095bd9504db1f108f95b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) ci: replace docker-build + helm-publish with central build-publish workflow ([`0a508a6`](https://github.com/OpenG2P/consent-manager/commit/0a508a6e8ecbbb33d5b1d6ad898c28e409c051b1))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
