# commons

_Published automatically._

**Repository:** [github.com/OpenG2P/commons](https://github.com/OpenG2P/commons)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.233`](#v-0-0-0-develop-233) | 2026-08-28 | develop |  |
| [`0.0.0-develop.232`](#v-0-0-0-develop-232) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-233"></a>

## commons — develop 0.0.0-develop.233 (2026-08-28)

_commit `8defb45` · changes since 0.0.0-develop.232_
<!-- build:0.0.0-develop.233 revision:8defb450c9546d840cf1862100caff901d330de1 ts:1787908180 -->

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) publish the commons charts to the Rancher index too ([`8defb45`](https://github.com/OpenG2P/commons/commit/8defb450c9546d840cf1862100caff901d330de1))

<a id="v-0-0-0-develop-232"></a>

## commons — develop 0.0.0-develop.232 (2026-08-28)

_commit `9385c3a` · changes since 2.2.1_
<!-- build:0.0.0-develop.232 revision:9385c3a573c0fac9dfff34009adba14dfa3ba63b ts:1787893825 -->

### Summary

- **Major:** CI/CD overhaul: switched from GitHub Actions to GitLab CI, enforcing namespace guards to prevent execution in forks.
- Dependency updates: multiple services, including IAM and Master Data Service, have been upgraded to their latest versions, with specific version bumps noted for openg2p-master-data and openg2p-iam-service.
- Keycloak integration improvements: fixed IAM Keycloak base URL configuration and enhanced agent portal API overrides for Keycloak URL resolution.
- Security enhancements: moved eSignet and mock identity to PKCS12 keystores, dropping SoftHSM, and added a reset option for key management during commons-services uninstallation to prevent orphaned key references.
- Configuration updates: added MinIO configuration to values.yaml, updated IAM image references post-repo migration, and set default baseDomain for commons charts.
- Feature additions: enabled EMBEDDED_SUPERSET for Insights and shipped Inji Certify with commons-services, now enabled by default.
- Miscellaneous fixes: corrected Keycloak init job name and made SoftHSM environment references optional.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub ([`9385c3a`](https://github.com/OpenG2P/commons/commit/9385c3a573c0fac9dfff34009adba14dfa3ba63b))
- Versions updated. ([`48411db`](https://github.com/OpenG2P/commons/commit/48411dbca27820b38839960dc9140e2eb351fe7d))
- Updated several services to latest versions. ([`327340b`](https://github.com/OpenG2P/commons/commit/327340b6c679c90c18ecb43e194505f3018c9a61))
- Bug fix on Keycloak init job name ([`ca12014`](https://github.com/OpenG2P/commons/commit/ca1201496762ae937b08b2b67ba55647eb5a20ad))
- Updated versions related to recent moving of repos to platform-services group on Gitlab. ([`b8dc4e5`](https://github.com/OpenG2P/commons/commit/b8dc4e50096a5188dcbf7fc4d04d99d9fec03c9e))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Give the agent realm the OpenG2P theme ([`447ff13`](https://github.com/OpenG2P/commons/commit/447ff1352b8210c1d2c5f14feafdea9629633459))
- Point the IAM staff-portal-api image at registry.gitlab.com/openg2p/platform-services/iam/ after the move of iam, awe, master-data-service, audit-manager, partner-management and consent-manager into the platform-services group; this is the only GitLab image commons pins directly, the rest are set in their own subcharts and must be updated there ([`fd0b779`](https://github.com/OpenG2P/commons/commit/fd0b779f7ef3a353c59b23c4ff553456c07e50c5))
- Update of versions of several services. Fixes for IAM docker path. ([`87d2a48`](https://github.com/OpenG2P/commons/commit/87d2a48b1e2b25929935cf38a7bc5c33e038b19b))
- Move image and env config to IAM Helm chart ([`ba9633d`](https://github.com/OpenG2P/commons/commit/ba9633d03e2ffe2e5db10125e4f0dbeee99c5570))
- Deleted ([`3ff3fee`](https://github.com/OpenG2P/commons/commit/3ff3fee5759a1b00a06ff30de22278a5ff8d4864))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Own the agent realm and its confidential client alongside staff ([`59ec665`](https://github.com/OpenG2P/commons/commit/59ec665f86242ba005d8331bc198c371b0035d05))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Mark the SoftHSM env references optional instead of blanking them ([`81fa10c`](https://github.com/OpenG2P/commons/commit/81fa10c17a8cc8bcb7099be0192355c2ab39a6f1))
- [G2P-5573](https://openg2p.atlassian.net/browse/G2P-5573) Move eSignet and mock identity to PKCS12 keystores and drop SoftHSM ([`ffcf083`](https://github.com/OpenG2P/commons/commit/ffcf083f03f59d8d2b430e13c44fe92ff36fc765))
- Complete the commons-services uninstall: add the missing inji_certify DB/role, and make --reset-keymanager purge the softhsm key objects as well as truncating key_alias/key_store, since esignet and mock-identity keep their key references in base-owned DBs and their key material in the shared softhsm and clearing only one half leaves the other stale (orphan HSM objects accumulate duplicate CKA_LABELs and crash-loop both services) ([`b9e65c4`](https://github.com/OpenG2P/commons/commit/b9e65c481a7bd76d5bf26a06d61fd06194127597))
- Add --reset-keymanager to the commons-services uninstall: esignet and mock-identity run PKCS11, so their key material sits in softhsm while their key_alias rows sit in base-owned DBs that the uninstall deliberately keeps, and resetting softhsm alone leaves the aliases pointing at HSM keys that no longer exist so both fail at keymanager init on reinstall; the flag truncates just key_alias+key_store so keys regenerate, leaving application data intact ([`9fad89d`](https://github.com/OpenG2P/commons/commit/9fad89dd4dcef322cd12cf598dd625b4f7c99656))
- Bump openg2p-master-data to 1.1.0-rc.55 and openg2p-iam-service to 1.4.0-rc.90 ([`8832184`](https://github.com/OpenG2P/commons/commit/8832184f8053e10de50da41c1fa1c09b19e08ce2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ship Inji Certify with commons-services, enabled by default ([`1653fdb`](https://github.com/OpenG2P/commons/commit/1653fdb1a3acb423062ce0976f6efe10d052aaa9))
- Versions of MDS, Mock ID, IAM bumped up. ([`460d8e4`](https://github.com/OpenG2P/commons/commit/460d8e43e9ab293283c659eb22ad99fe65e34327))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add agent portal API overrides so its Keycloak URL and redirect resolve ([`2515d20`](https://github.com/OpenG2P/commons/commit/2515d20da59deafcf282ce79a9e539f4c6f2e887))
- Bumped up version of IAM, and changed its location to Gitlab. ([`fa817d9`](https://github.com/OpenG2P/commons/commit/fa817d9d98a8748b20ac4b40fef85384e2b7fb26))
- Bumped up AWE version to 0.0.0-develop.70 ([`9850037`](https://github.com/OpenG2P/commons/commit/985003774f36a2041ff2f9af465f03c5236d19b3))
- Fix IAM keycloak base URL in commons-services: set IAM_STAFF_KEYCLOAK_BASE_URL directly under iamStaffPortalApi.envVars with an explicit tpl call, since the subchart's indirection gets only one tpl pass and was emitting the unresolved 'https://keycloak.{{ tpl .Values.global.baseDomain $ }}' into the pod; drop the hardcoded qa keycloakBaseUrl which was dead anyway because a subchart-scoped global loses to the top-level one ([`055b4d6`](https://github.com/OpenG2P/commons/commit/055b4d69b5149dad32eb9321e6dd02b5bd5c3a5e))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Make the country pack a free-text field with short form guidance. The two-value enum let an environment pick only ETH or XKM, so a country adding its own pack to openg2p-data could not select it; the Rancher description now says where to find the directory name and the provenance notes move to values.yaml. ([`2cabc9c`](https://github.com/OpenG2P/commons/commit/2cabc9c5aba91fa5b18ec9fbff2506d5bd44bc6f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Enable EMBEDDED_SUPERSET. Insights loads /embedded/&lt;uuid&gt; in an iframe, a route Superset only registers with this flag — without it the embedded UUID and guest token are both issued successfully and only the iframe 404s, which reads as a broken client rather than a missing feature flag. ([`95dd6fb`](https://github.com/OpenG2P/commons/commit/95dd6fb73644da82b38e34662261fb1718463e72))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) CI: refuse to run in forks (namespace guard) ([`53f78f2`](https://github.com/OpenG2P/commons/commit/53f78f2a6050d361055ad476f49a5d2edbbc1afc))
- Just to trigger a build. No changes ([`b5b90d8`](https://github.com/OpenG2P/commons/commit/b5b90d8db9ccb37bb3ae0e7da82a7a29d14c2ea1))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`2c340a3`](https://github.com/OpenG2P/commons/commit/2c340a346f2f39ab5c54a94bd299f27466a37497))
- [G2P-5451](https://openg2p.atlassian.net/browse/G2P-5451) Add MinIO configuration to values.yaml, including existing secret reference and read-only user creation ([`b766eea`](https://github.com/OpenG2P/commons/commit/b766eead30783b6e1f531e27937ecde1998e6cb1))
- Default baseDomain to {{ .Release.Namespace }}.openg2p.org in both commons charts, and make every consumer tpl it (29 values refs plus the keycloak gateway/virtualservice templates) since a single tpl pass does not evaluate a template nested inside a value and would otherwise emit the literal {{ .Release.Namespace }} into hostnames ([`adc388c`](https://github.com/OpenG2P/commons/commit/adc388c5082613e409edcf1f70d56087d98136e3))
- Bumped up MDS version ([`ae68cf6`](https://github.com/OpenG2P/commons/commit/ae68cf6a73d50925ee101d6192722cfecfa36edb))
- Bumped up MDS version. ([`d39f5eb`](https://github.com/OpenG2P/commons/commit/d39f5eb17054534cff3ea552ce48e67386584c05))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare Ethiopia as the country for the commons environment, and surface the choice in the form. This is the one place an environment names its country — registries read the geography, code lists and sample people from Master Data and name none of their own, which is what lets one registry image serve any country. Master Data is installed from here, so the country pack, the code-list and sample switches, and the domain lists are all questions on this chart rather than values only reachable by hand-editing a subchart. ([`e9fba97`](https://github.com/OpenG2P/commons/commit/e9fba97bf72a08e44bb6ec62890758a917ab511f))
- Add hook-succeeded to superset init-db hook-delete-policy so the Job and its pods (including a first-attempt deadlock retry) are removed once it succeeds, instead of a stale Error pod making a healthy release look failed; restate the hook keys explicitly since jobAnnotations {} never cleared the subchart defaults. Bumped up consent manager Helm version. ([`e862fe0`](https://github.com/OpenG2P/commons/commit/e862fe0ef3db49cdf4863270990d4a83064bdedb))
- Bumped up MDS version to 0.0.0-develop.38 ([`fcd382e`](https://github.com/OpenG2P/commons/commit/fcd382efa84535d8037d3afc5ff510a3deb3c485))
- Bumped up MDS version to 0.0.0-develop.36 ([`e77c23a`](https://github.com/OpenG2P/commons/commit/e77c23ab167cd469a4da463c04fa3befe79af849))
- Bumped up Master Data Service version to 0.0.0-develop.31 ([`ab1f277`](https://github.com/OpenG2P/commons/commit/ab1f2779a2549309c037007fbe4bf7739db657cc))
- Bumped up master data chart to 0.0.0-develop.30 ([`cf8be83`](https://github.com/OpenG2P/commons/commit/cf8be838ab40c768a5a002d62dd47616c0562fa9))
- Bumped up Master Data Service version. ([`0e52ebf`](https://github.com/OpenG2P/commons/commit/0e52ebf19de3fd2ac8af3c4dd128e0f2857f7162))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
