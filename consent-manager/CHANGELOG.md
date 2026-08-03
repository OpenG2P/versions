# consent-manager

_Published automatically._

**Repository:** [gitlab.com/openg2p/consent-manager](https://gitlab.com/openg2p/consent-manager) · **Container images:** [Container Registry](https://gitlab.com/openg2p/consent-manager/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.50`](#v-0-0-0-develop-50) | 2026-08-03 | develop |
| [`0.0.0-develop.49`](#v-0-0-0-develop-49) | 2026-07-18 | develop |

# Develop builds

<a id="v-0-0-0-develop-50"></a>

## consent-manager — develop 0.0.0-develop.50 (2026-08-03)

_commit `a9f7c06` · changes since 0.0.0-develop.49_
<!-- build:0.0.0-develop.50 revision:a9f7c0684d3c0eb3286da61d81ed6f3343c6915b ts:1785719104 -->

### Changes since 0.0.0-develop.49

- Fix duplicate SANITY_VERIFY_TLS env in the cm-sanity Job (emitted both inline and via the shared pmSeedEnv helper), which made server-side apply reject the Job with "duplicate entries for key" and fail the release ([`a9f7c06`](https://gitlab.com/openg2p/consent-manager/-/commit/a9f7c0684d3c0eb3286da61d81ed6f3343c6915b))

<a id="v-0-0-0-develop-49"></a>

## consent-manager — develop 0.0.0-develop.49 (2026-07-18)

_commit `954ee5f` · baseline: release the start_
<!-- build:0.0.0-develop.49 revision:954ee5f21b87245c3c5dfc2583552881f23d4f77 ts:1784349305 -->

### Summary

_All changes since release the start:_

- Major changes related to new Partner Management integration, including proper integration with PM and AWE.
- JWS support added for enhanced security.
- AWE is now deactivated by default; it can be enabled if required, and the sanity test will pass only if it is deactivated.
- Public keys are now stored in the database, with an additional option to query well-known keys.
- Helm chart and consent-manager images are now published to GitLab, dropping support for GitHub Container Registry (GHCR).
- Sanity test job has been added to ensure deployment fails if the test fails.
- Fixed issues with multiple pods being created and race conditions.
- Sanity and pm-seed Jobs now support a configurable nameOverride to align with renamed API components.
- Support for multiple modules using the same Consent Manager has been implemented.
- FastAPI 'develop' version is now used for development purposes.
- Minor edits made to the README and other documentation for clarity.
- Helm chart publish issue has been resolved.

### Since last release (the start)

- The sanity and pm-seed Jobs hardcoded <release>-sanity / <release>-pm-seed, so when the API components are renamed via nameOverride the sanity Job name no longer lines up with them. Add sanity.nameOverride (default "" = no change) inserted as an infix: e.g. "cm" -> <release>-cm-sanity / <release>-cm-pm-seed. ([`954ee5f`](https://gitlab.com/openg2p/consent-manager/-/commit/954ee5f21b87245c3c5dfc2583552881f23d4f77))
- Minor edit to just stimulate helm publish. ([`64fa696`](https://gitlab.com/openg2p/consent-manager/-/commit/64fa6965a4a6dcd68af70ba02290271a59deff09))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Re-run GitLab pipeline with fixed chart job ([`51fd07c`](https://gitlab.com/openg2p/consent-manager/-/commit/51fd07c2a7e90c6ccd76436172f331ae373f023d))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Minor edit of README. ([`58f81a4`](https://gitlab.com/openg2p/consent-manager/-/commit/58f81a4a14490f5d5edefde87efbdfc35b376f9f))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Moved repo from Github as is. ([`8bf5787`](https://gitlab.com/openg2p/consent-manager/-/commit/8bf57873609d7fafd1030d7d91b40f02fab4852b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Grant packages: write in caller to satisfy reusable workflow (fix startup failure) ([`88041e0`](https://gitlab.com/openg2p/consent-manager/-/commit/88041e0bb0e001338e2ccdded9eb334108c614d3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish consent-manager images and chart to GitLab; drop GHCR ([`b38f1e7`](https://gitlab.com/openg2p/consent-manager/-/commit/b38f1e7e9691d25f6e50ebcdd6d882412dcb0a3c))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) consent-manager: publish images + chart to GHCR (chart under charts/ to avoid image name clash) ([`b736910`](https://gitlab.com/openg2p/consent-manager/-/commit/b73691010948b6fb58607aef4825f28b4f23ae3b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Publish images + chart to GHCR only (OCI), values to ghcr.io ([`6f7508a`](https://gitlab.com/openg2p/consent-manager/-/commit/6f7508aa35737986fec55598e0a692384da7bf63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) clarify changelog workflow_dispatch input descriptions ([`326edee`](https://gitlab.com/openg2p/consent-manager/-/commit/326edeebd7ca9b5284da5991f14b571046442ce6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) forward changelog dispatch inputs to central workflow ([`75b649f`](https://gitlab.com/openg2p/consent-manager/-/commit/75b649f3ceafb79f250ea20d8464e94323d56d63))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix in publish. ([`9ff69b6`](https://gitlab.com/openg2p/consent-manager/-/commit/9ff69b6b74defc2d7f51095bd9504db1f108f95b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) ci: replace docker-build + helm-publish with central build-publish workflow ([`0a508a6`](https://gitlab.com/openg2p/consent-manager/-/commit/0a508a6e8ecbbb33d5b1d6ad898c28e409c051b1))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Repoint Partner Management to commons-services and align PM-seed auth to the g2p-bridge pmSeedClientId pattern. ([`4a1970a`](https://gitlab.com/openg2p/consent-manager/-/commit/4a1970a73dd468c6302472ed948dda894fe5bf45))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) PM Url corrected. ([`a6265f7`](https://gitlab.com/openg2p/consent-manager/-/commit/a6265f7b7d1872d34add1d25246d19c40d05ba35))
-  [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) PM Url corrected. ([`9ffcf64`](https://gitlab.com/openg2p/consent-manager/-/commit/9ffcf645f5d78caa6569652f028d3f3d6ed8fbb7))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) JWS support added. ([`b234266`](https://gitlab.com/openg2p/consent-manager/-/commit/b2342667d70a922401a0fac8bc77f1a6367bf2e0))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) UI Docker built. ([`4e6cb62`](https://gitlab.com/openg2p/consent-manager/-/commit/4e6cb62e10e5eaff611ef4975620d51b6deebe4b))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) AWE deactivated by default. Use it if required. Sanity test will pass only if it is deactivated. ([`1be662c`](https://gitlab.com/openg2p/consent-manager/-/commit/1be662c03e9110f60e7399b943951e2421a8feb8))
-  [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) PM client name corrected. ([`32be265`](https://gitlab.com/openg2p/consent-manager/-/commit/32be265106e622724f2a6e93cce98f698eb331df))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Rejig based on staff, partner apis ([`9844b65`](https://gitlab.com/openg2p/consent-manager/-/commit/9844b65751c50305939fa98dad1e41659cbb7e85))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Proper integration with PM and AWE. ([`09dc8b4`](https://gitlab.com/openg2p/consent-manager/-/commit/09dc8b4129b3915a2c3c6ef5fa5602ae8db6b0b2))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Proper integration with PM and AWE. WIP ([`def0cbf`](https://gitlab.com/openg2p/consent-manager/-/commit/def0cbf4a5dfc19949c33633485e792f3d8990a8))
-  [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Proper integration with PM and AWE. WIP ([`30b443c`](https://gitlab.com/openg2p/consent-manager/-/commit/30b443c35f55d0944ed93d6fa6baf2bf86958c5b))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Fix for sanity auth issue ([`a04fd55`](https://gitlab.com/openg2p/consent-manager/-/commit/a04fd55d497a217645e2f6705ff7eac436d6eb6c))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Fix for sanity auth issue ([`27eca21`](https://gitlab.com/openg2p/consent-manager/-/commit/27eca211b9a6b7582ebd53e232228cb266b756f1))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Sanity test job run added. ([`73e11ea`](https://gitlab.com/openg2p/consent-manager/-/commit/73e11ea0d93a5dc164ff686fd6056af8018e9f37))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Major changes -- modifications related to new Partner Management ([`2455380`](https://gitlab.com/openg2p/consent-manager/-/commit/2455380690738eb847d515a9e3c4e559b846e156))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Race condition fix ([`6f3d0f8`](https://gitlab.com/openg2p/consent-manager/-/commit/6f3d0f8f2ae61fb5ed4d1c5c11c95122fa68c244))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Cron job bug fixed ([`1f73a66`](https://gitlab.com/openg2p/consent-manager/-/commit/1f73a66b19ec3a641325a9dbcf67043ffc101e17))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Fix for previous change ([`e5517bb`](https://gitlab.com/openg2p/consent-manager/-/commit/e5517bb9a2765652bca575e72d290a422c663d67))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Fastapi 'develop' version used. ([`dcd84fe`](https://gitlab.com/openg2p/consent-manager/-/commit/dcd84fe4966494a3f3fc0b05beae484a9c0d22a2))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) TODO added for APIs to be done later. ([`500dc6a`](https://gitlab.com/openg2p/consent-manager/-/commit/500dc6a9816504977763e0c3302ddeb37c906677))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) e2e test enabled by default ([`f973d14`](https://gitlab.com/openg2p/consent-manager/-/commit/f973d14078b4b940f6ccdf5f4b572ea48fa9cb70))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Deployment fails if sanity test fail. ([`c1427de`](https://gitlab.com/openg2p/consent-manager/-/commit/c1427def990b7be8e35f581721919355eb61b05d))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Confusing options removed. ([`8726d5b`](https://gitlab.com/openg2p/consent-manager/-/commit/8726d5b809a80b2cc85dcdc0ee4afd85c50b2754))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Ensured sanity test works with external p12 key as well and not just with demo key. ([`0c98672`](https://gitlab.com/openg2p/consent-manager/-/commit/0c9867200b0b63509f97f2978a11a2ba6f2a61a4))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Issue related to multiple pods being created fixed. ([`9c17c43`](https://gitlab.com/openg2p/consent-manager/-/commit/9c17c43656d4772e52d2ea6d1e05fedecb3a40dd))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Public keys stored in DB. and another option to query well known added. ([`c8c1d2c`](https://gitlab.com/openg2p/consent-manager/-/commit/c8c1d2c6054a5f5536321037feb97e59a0e9eeb4))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Sorted out .p12 file issues - the way keys are stored and installed. ([`c5c5f22`](https://gitlab.com/openg2p/consent-manager/-/commit/c5c5f22a0179db982def3d82d8f3234fe21e75a5))
- Cleanup ([`9f0afb9`](https://gitlab.com/openg2p/consent-manager/-/commit/9f0afb9926c68d679d981996bcea42ad31d0c6b2))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Helm chart publish issue fixed. ([`81350da`](https://gitlab.com/openg2p/consent-manager/-/commit/81350da7202ff8e8643c924f988feaf413c2133a))
- publish consent-manager helm chart OpenG2P/consent-manager@0a344ad029cf7b1782dba92a2901958bf68840e0 ([`ee5fa21`](https://gitlab.com/openg2p/consent-manager/-/commit/ee5fa21597673992831990f734826a56b505eecd))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Support for multiple modules using the same CM. ([`0a344ad`](https://gitlab.com/openg2p/consent-manager/-/commit/0a344ad029cf7b1782dba92a2901958bf68840e0))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Minor. ([`9e2bdbd`](https://gitlab.com/openg2p/consent-manager/-/commit/9e2bdbdca1cf59299ab03d8ff7ddca9e9c570c67))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) Helm, docker, auth added. ([`fd3cc33`](https://gitlab.com/openg2p/consent-manager/-/commit/fd3cc33d81541c726fc354c848aef40bd2afc399))
- [G2P-5222](https://openg2p.atlassian.net/browse/G2P-5222) WIP. ([`8ddad02`](https://gitlab.com/openg2p/consent-manager/-/commit/8ddad0276f1880ae7362ffb4efb3e185bd25cdc3))
- Create README.md ([`85a52fe`](https://gitlab.com/openg2p/consent-manager/-/commit/85a52fe6c04a66d43a5985c1930ca206574a4240))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 10 develop builds** and the **latest 10 release
> candidates** per release line. Older develop builds and release candidates
> are pruned as they are superseded, and a release's candidates are removed
> once it ships. Those versions still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
