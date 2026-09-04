# iam

_Published automatically._

**Repository:** [github.com/OpenG2P/iam](https://github.com/OpenG2P/iam) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.4.2-rc.115`](#v-1-4-2-rc-115) | 2026-09-04 | release candidate |  |
| [`1.4.2-rc.113`](#v-1-4-2-rc-113) | 2026-09-04 | release candidate |  |
| [`1.4.1`](#v-1-4-1) | 2026-09-02 | release |  |
| [`1.4.1-rc.111`](#v-1-4-1-rc-111) | 2026-09-02 | release candidate |  |
| [`1.4.0`](#v-1-4-0) | 2026-09-01 | release |  |
| [`1.4.0-rc.101`](#v-1-4-0-rc-101) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.98`](#v-0-0-0-develop-98) | 2026-09-02 | develop |  |
| [`1.4.0-rc.100`](#v-1-4-0-rc-100) | 2026-08-28 | release candidate |  |
| [`0.0.0-develop.97`](#v-0-0-0-develop-97) | 2026-08-28 | develop |  |

# Releases

<a id="v-1-4-1"></a>

## iam 1.4.1 — 2026-09-02

<!-- build:1.4.1 revision:7398f88d3fe3cee5fd26b2bab3b4b54ffa75e560 ts:1788335866 -->

_commit `7398f88` · changes since release 1.4.0_

**Same artifact as [`1.4.1-rc.111`](#v-1-4-1-rc-111)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-iam-service 1.4.1](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.1.tgz)

### Release notes

## What's Changed
- Separate agent vs staff auth cookies (agent- prefix) so shared cookie domains do not overwrite sessions
- Return 401 instead of 500 when a token cannot be verified against this portal’s JWKS
- Agent API auth now matches staff: GET /auth/logout (OIDC end-session), GET /auth/get_logged_in_user
- Enable CSRF on the agent API (the 1.4.0 Helm flag was unused)
- Seed the agent-realm login provider by issuer so agent tokens can be validated
- Seed staff login providers by issuer as well (shared login_providers table)
- Render Keycloak base URL with tpl (1.4.0 left a nested template in the pod env)
- Point the agent application URL at the agent portal host, not the IAM staff UI
- Add global.agentPortalHostname; derive redirect URI and CORS from it
- Remove keycloak-init from this chart (owned by commons)
- Bump image tags to 1.4.1; pin FASTAPI_COMMON_REF to 1.2.0
- Add tests for cookie prefix, agent data loader, and unverifiable-token 401

### Summary

- **Major:** Keycloak integration: configured the agent app to connect to the Keycloak base URL and aligned the agent portal API with the staff portal's authentication surface.
- Security enhancements: separated agent and staff authentication cookies, implemented 401 responses for unverifiable tokens, and seeded the agent realm's login provider for token validation.
- CI improvements: transitioned to a single looping job for pre-commit checks without a local cache and established build and publish processes on GitHub.
- Code quality: applied black formatting across the repository to enforce a consistent 110-column line length.

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Render the Keycloak base URL and point the agent app at the agent portal ([`6ebcbf3`](https://github.com/OpenG2P/iam/commit/6ebcbf3b1b7d03dfa21016e8a47eb611c751ac40))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub ([`8682df5`](https://github.com/OpenG2P/iam/commit/8682df599b0dc919606c8e9f77387d09d0479829))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) applied the platform-service group change on iam service ([`0d0ba76`](https://github.com/OpenG2P/iam/commit/0d0ba7675231135ba843f99eaa598bab9dfdf60a))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Run pre-commit as a single looping job without a runner-local cache ([`4c9d599`](https://github.com/OpenG2P/iam/commit/4c9d599acd40e81a8620243632ea80a86a3b0bd4))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Match the staff portal's auth surface in the agent portal API ([`31250d7`](https://github.com/OpenG2P/iam/commit/31250d7f4207e9d946c1986fa0ea3311d8dbfcce))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Keep agent and staff auth cookies apart and 401 on unverifiable tokens ([`2c74a91`](https://github.com/OpenG2P/iam/commit/2c74a91033590b4355e9d0ce1898adbe900edd14))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Apply black formatting at the repo's 110-column line length ([`29983b7`](https://github.com/OpenG2P/iam/commit/29983b7ccd0e6a9d4ab68ca61e642e13efc129ad))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Seed the agent realm's login provider so agent tokens validate ([`d6ecd80`](https://github.com/OpenG2P/iam/commit/d6ecd80f634a0306d02458a9474144abc24b324f))

<a id="v-1-4-0"></a>

## iam 1.4.0 — 2026-09-01

<!-- build:1.4.0 revision:ebafe2eaeea1e3d69e1760bf60624f76d5162c2a ts:1788258730 -->

_commit `ebafe2e` · changes since release v1.3.0_

**Same artifact as [`1.4.0-rc.101`](#v-1-4-0-rc-101)** — built from the
same commit and *promoted* (retagged), not rebuilt. No code changed between them.

**Chart:** [openg2p-iam-service 1.4.0](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.0.tgz)

### Release notes

**IAM 1.4.0**
OpenG2P Identity and Access Management — first staff admin console, data-policy enforcement, and a production-ready agent portal.

Compared with 1.3.0, this release turns IAM from an auth backend into an operable identity platform: you can manage applications, roles, login providers, and row-level data policies in the UI, and agents get their own Keycloak realm and API.


**Docs**: [Staff portal SSO login flow](https://github.com/OpenG2P/iam/blob/1.4/docs/staff-portal-sso-login-flow.md)

**Highlights**

- IAM Staff UI — new Next.js 16 admin console (applications, roles, permissions, login providers, data policies).
- Data policies — ALLOW/DISALLOW filters on register records, geo, and attributes; published to Keycloak as DP_<mnemonic> client roles; evaluate API for PEPs.
- Application management APIs — CRUD for applications, roles, permissions, role-permission mappings, and login providers; roles sync to Keycloak.
- Agent portal API — shipped in Helm on by default, with an agent realm and agent-portal client (code existed in 1.3.0 but was not deployed).
- openg2p-fastapi-common 1.2.0 — partner JWT verification via CryptoFactory.
- Session TTLs tuned so refresh tokens outlive the access cookie.

### Summary

- **Major:** CI overhaul: migrated from GitHub Actions to GitLab CI, implementing new workflows and dropping outdated configurations.
- Security enhancements: updated FastAPI common library to version 1.2.0, improved JWT validation using CryptoFactory, and added Keycloak initialization configuration.
- Session management improvements: updated Redis token TTLs and cache expiration settings for better performance.
- Feature additions: implemented data policy management and middleware, added roles and permissions management tabs, and enhanced application management with Keycloak integration.
- UI/UX refinements: refactored multiple components for consistency and accessibility, improved modal styling, and added reusable UI components.
- Cleanup and maintenance: removed unused SQL seed scripts and API URLs, fixed templating issues for Keycloak, and updated IAM_STAFF_UI_PERMISSIONS.
- Testing improvements: enhanced unit test coverage for IAM staff portal API components and core functionality, and updated middleware tests for accuracy.

### Changes

- updated fastapi-commons to 1.2.0 ([`ebafe2e`](https://github.com/OpenG2P/iam/commit/ebafe2eaeea1e3d69e1760bf60624f76d5162c2a))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.4 release line with GitHub ([`f8bccfe`](https://github.com/OpenG2P/iam/commit/f8bccfe85f60a9793ff290a785f58e37e0a95927))
- [G2P-5592](https://openg2p.atlassian.net/browse/G2P-5592) Update Redis token TTLs and cache expiration for improved session management ([`1a1ca2b`](https://github.com/OpenG2P/iam/commit/1a1ca2b68810120c30d6f13a2a494b880a2b6dc9))
- [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Refactor GeoLocationPickerModal to use new utility functions for fetching geo levels and improve state management ([`b69ebd6`](https://github.com/OpenG2P/iam/commit/b69ebd628df3aeffa811d8acd0775b73a109adfb))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Update FastAPI common library reference to version 1.2 and add Keycloak initialization configuration ([`bd43783`](https://github.com/OpenG2P/iam/commit/bd43783f8be1d179c58a24aecc47a3a8a2f3babf))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Refactor JWT validation to use CryptoFactory and update tests for component registration ([`9d4d3c1`](https://github.com/OpenG2P/iam/commit/9d4d3c1ce970aca4b51d144ffb9470eb95906a75))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add registration for mds, awe, partner api ([`22af5d6`](https://github.com/OpenG2P/iam/commit/22af5d687c5ff99f03a6adf5ea97e6037b51c04e))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Refactor DataPoliciesTab layout and comment out IconBase64Field in LoginProviderForm ([`6495993`](https://github.com/OpenG2P/iam/commit/649599302609de1af0604741c6fa5a74fe6f8e48))
- Remove include_domains from request payload in attribute API calls ([`dafa801`](https://github.com/OpenG2P/iam/commit/dafa801754b76a0e4591e48da0f47029c4ea4296))
- Fix templating for Keycloak base URL in IAM Staff and Agent APIs ([`ed5741a`](https://github.com/OpenG2P/iam/commit/ed5741a4cac7edafecf79d6f0b132869a605dd18))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Bump version to 1.4.0 and update image tags in values.yaml ([`1eb3a25`](https://github.com/OpenG2P/iam/commit/1eb3a250b00aefbec03aaadf96e2516f4bc07756))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Add iam-staff-ui to the build/publish pipeline and pin its chart image tag ([`d7fdd9c`](https://github.com/OpenG2P/iam/commit/d7fdd9c233643770a9f132d96649ec0ee76f5248))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Fix pre-commit ([`a2157ea`](https://github.com/OpenG2P/iam/commit/a2157eaed5056c130daac1cf760b0e63a8af78fe))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Remove registry API URL from env and add API URL to staff portal application ([`69495bf`](https://github.com/OpenG2P/iam/commit/69495bf53b3fb5b2ef72d4ecf3772017c6d8d3d2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal API by default and fix show_if conditions ([`da9db90`](https://github.com/OpenG2P/iam/commit/da9db90f1c0dd7702b650d205c8535b819a4d6a8))
- [G2P-5537](https://openg2p.atlassian.net/browse/G2P-5537) Port attribute-management API routes and hooks from upstream develop; drop wrongly-ported role-permission caching ([`74c5879`](https://github.com/OpenG2P/iam/commit/74c587992636e1c4fa913457035817272c3e573e))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Complete GitLab migration: port GitHub workflows to CI guards, drop .github, and port pending upstream commits ([`e04966e`](https://github.com/OpenG2P/iam/commit/e04966ec74808402fc600f9f1e936a5c8351595f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`3ed9ea0`](https://github.com/OpenG2P/iam/commit/3ed9ea066ce582c301e59ef4fc01d4b083b42fe2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Wire iam-agent-portal-api into the IAM chart behind a disabled-by-default switch ([`9de210b`](https://github.com/OpenG2P/iam/commit/9de210b49892450a651173bdd85538db21e692b9))
- Remove unused SQL seed script and login providers JSON; update IAM_STAFF_UI_PERMISSIONS to include delete permissions ([`1c5a6a6`](https://github.com/OpenG2P/iam/commit/1c5a6a633a477e72d5d16ff6e67fd97fc0fd39eb))
- Enhance values.yaml: Add backend API URLs for iam-staff-ui and update login provider ID ([`6d1d4f9`](https://github.com/OpenG2P/iam/commit/6d1d4f9d7708a7484dbff19db6fc89ab2cbfac34))
- Refactor: Remove unused use client directives and implement ApplicationsPageClient component ([`a694c5d`](https://github.com/OpenG2P/iam/commit/a694c5d11faf44ea65ea3197bc173ec56486d6f4))
- [G2P-5485](https://openg2p.atlassian.net/browse/G2P-5485) Enhance IconBase64Field with MIME type detection ([`2556ffa`](https://github.com/OpenG2P/iam/commit/2556ffa32f5137038cffca59e9e5deb91e5a82af))
- [G2P-5479](https://openg2p.atlassian.net/browse/G2P-5479) Add policy filter preview and view data policy modal components ([`5234a36`](https://github.com/OpenG2P/iam/commit/5234a3655cc2f27e4bb0471743df402ff66df143))
- Test: Update data policy middleware tests for accuracy and coverage ([`35f3bd9`](https://github.com/OpenG2P/iam/commit/35f3bd9004798e51b97bcdec69528df7cd9e9476))
- Feat: Implement data policy management and middleware ([`8a1c8cd`](https://github.com/OpenG2P/iam/commit/8a1c8cdca49d67828304428cd64f38da89570977))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Enhance application management with Keycloak integration ([`d7b1c7f`](https://github.com/OpenG2P/iam/commit/d7b1c7f348009636a95db8db1d0fd2c060250b12))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor UI components for consistency: update styles, improve accessibility, and enhance user experience across error, button, input, and modal components ([`0c1d936`](https://github.com/OpenG2P/iam/commit/0c1d93694207a526adc4162de79743275c451bde))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Add reusable UI components, improve modal styling, and refactor application and login provider pages ([`12956d8`](https://github.com/OpenG2P/iam/commit/12956d893015c299b7f4057572f7bd9b6f33c6f0))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor application and login provider components ([`b582d6f`](https://github.com/OpenG2P/iam/commit/b582d6fcd7a74a1202f7a642e1fa410c093301ed))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Add Roles, Permissions, and Role-Permissions management tabs with reusable modals, enhanced tables, login provider improvements, and loading skeletons ([`e70231c`](https://github.com/OpenG2P/iam/commit/e70231c8b56f1b0c908f5075025dbc038dc69abf))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor authentication and RBAC contexts, introduce reusable hooks/components, and add typed application and login provider data management ([`7ff270c`](https://github.com/OpenG2P/iam/commit/7ff270cb101d0861b808be879b220880a3c8e5c9))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor ApplicationAccess, Applications, and LoginProviders controllers to use strongly typed response models ([`ab5686d`](https://github.com/OpenG2P/iam/commit/ab5686dd272343ca932825f65a8acbc83da3cbfe))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Implement Application Management module in IAM Staff UI ([`235f138`](https://github.com/OpenG2P/iam/commit/235f138d8a691ee6efb123d4791238748ec74a8e))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix chart-image-paths to .iamStaffPortalApi.image.tag (chart shipped unpinned) ([`947f58f`](https://github.com/OpenG2P/iam/commit/947f58f1b04920854189aa65c8b9c99ff708da39))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented ([`8109437`](https://github.com/OpenG2P/iam/commit/810943725a2040fadbf4c18868471f205daa930c))
- 0.0.0-develop.N versioning implemented. ([`a1579ba`](https://github.com/OpenG2P/iam/commit/a1579ba229373a333ceb75797685e3a086d2b9d8))
- [G2P-5313](https://openg2p.atlassian.net/browse/G2P-5313) Add unit tests for IAM staff portal API components ([`8670822`](https://github.com/OpenG2P/iam/commit/867082285f362b88550be7ba2a265621eb0b8a4d))
- [G2P-5313](https://openg2p.atlassian.net/browse/G2P-5313) Improve unit test coverage for core IAM functionality ([`c762c7b`](https://github.com/OpenG2P/iam/commit/c762c7b741a5c9d19bbd30b6875daacbd5d88717))

# Release candidates

<a id="v-1-4-2-rc-115"></a>

## iam 1.4.2-rc.115 — 2026-09-04

_commit `410978d` · changes since 1.4.2-rc.113_
<!-- build:1.4.2-rc.115 revision:410978d99a81adcc18aa960fe4b92846223c021a ts:1788516183 -->

**Chart:** [openg2p-iam-service 1.4.2-rc.115](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.2-rc.115.tgz)

### Changes

- Bump FASTAPI_COMMON_REF to 1.2.1 and update version numbers to 1.4.2 across multiple files ([`a60d876`](https://github.com/OpenG2P/iam/commit/a60d8761f44e0ffa56011676cecd901a15481250))

<a id="v-1-4-2-rc-113"></a>

## iam 1.4.2-rc.113 — 2026-09-04

_commit `a284b8b` · changes since 0.0.0-develop.98_
<!-- build:1.4.2-rc.113 revision:a284b8ba9d4098bfa469afa3b9e915ef4d0576cf ts:1788507500 -->

**Chart:** [openg2p-iam-service 1.4.2-rc.113](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.2-rc.113.tgz)

### Summary

- **Major:** Refactor database session management to utilize `get_async_session_maker` across services, enhancing session handling.
- Dependency updates: Upgraded `fastapi-commons` to version 1.2.0 and aligned the 1.4 release line with GitHub.
- Session management improvements: Updated Redis token TTLs and cache expiration for better performance.
- Refactorings: Improved `GeoLocationPickerModal` state management and utility function usage; refactored JWT validation to leverage `CryptoFactory`.
- API adjustments: Added registration for MDS, AWE, and partner APIs; removed `include_domains` from request payload in attribute API calls.
- Fixes: Corrected templating for Keycloak base URL in IAM Staff and Agent APIs.

### Changes

- [G2P-5620](https://openg2p.atlassian.net/browse/G2P-5620) Refactor database session management to use get_async_session_maker across services ([`13c0691`](https://github.com/OpenG2P/iam/commit/13c06911830c98ba542d37e9ef52df89cd8dd90d))
- updated fastapi-commons to 1.2.0 ([`ebafe2e`](https://github.com/OpenG2P/iam/commit/ebafe2eaeea1e3d69e1760bf60624f76d5162c2a))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.4 release line with GitHub ([`f8bccfe`](https://github.com/OpenG2P/iam/commit/f8bccfe85f60a9793ff290a785f58e37e0a95927))
- [G2P-5592](https://openg2p.atlassian.net/browse/G2P-5592) Update Redis token TTLs and cache expiration for improved session management ([`1a1ca2b`](https://github.com/OpenG2P/iam/commit/1a1ca2b68810120c30d6f13a2a494b880a2b6dc9))
- [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Refactor GeoLocationPickerModal to use new utility functions for fetching geo levels and improve state management ([`b69ebd6`](https://github.com/OpenG2P/iam/commit/b69ebd628df3aeffa811d8acd0775b73a109adfb))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Update FastAPI common library reference to version 1.2 and add Keycloak initialization configuration ([`bd43783`](https://github.com/OpenG2P/iam/commit/bd43783f8be1d179c58a24aecc47a3a8a2f3babf))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Refactor JWT validation to use CryptoFactory and update tests for component registration ([`9d4d3c1`](https://github.com/OpenG2P/iam/commit/9d4d3c1ce970aca4b51d144ffb9470eb95906a75))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add registration for mds, awe, partner api ([`22af5d6`](https://github.com/OpenG2P/iam/commit/22af5d687c5ff99f03a6adf5ea97e6037b51c04e))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Refactor DataPoliciesTab layout and comment out IconBase64Field in LoginProviderForm ([`6495993`](https://github.com/OpenG2P/iam/commit/649599302609de1af0604741c6fa5a74fe6f8e48))
- Remove include_domains from request payload in attribute API calls ([`dafa801`](https://github.com/OpenG2P/iam/commit/dafa801754b76a0e4591e48da0f47029c4ea4296))
- Fix templating for Keycloak base URL in IAM Staff and Agent APIs ([`ed5741a`](https://github.com/OpenG2P/iam/commit/ed5741a4cac7edafecf79d6f0b132869a605dd18))

<a id="v-1-4-1-rc-111"></a>

## iam 1.4.1-rc.111 — 2026-09-02

_commit `7398f88` · changes since 0.0.0-develop.98_
<!-- build:1.4.1-rc.111 revision:7398f88d3fe3cee5fd26b2bab3b4b54ffa75e560 ts:1788335866 -->

**Chart:** [openg2p-iam-service 1.4.1-rc.111](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.1-rc.111.tgz)

### Summary

- **Major:** Updated FastAPI common library to version 1.2.0, including Keycloak initialization configuration and refactored JWT validation to utilize CryptoFactory.
- Session management enhancements: Updated Redis token TTLs and cache expiration for improved performance.
- Refactoring: GeoLocationPickerModal now uses new utility functions for geo level fetching, and DataPoliciesTab layout has been adjusted.
- API modifications: Removed `include_domains` from request payload in attribute API calls and added registration for mds, awe, and partner API.
- Fixes: Corrected templating for Keycloak base URL in IAM Staff and Agent APIs.

### Changes

- updated fastapi-commons to 1.2.0 ([`ebafe2e`](https://github.com/OpenG2P/iam/commit/ebafe2eaeea1e3d69e1760bf60624f76d5162c2a))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.4 release line with GitHub ([`f8bccfe`](https://github.com/OpenG2P/iam/commit/f8bccfe85f60a9793ff290a785f58e37e0a95927))
- [G2P-5592](https://openg2p.atlassian.net/browse/G2P-5592) Update Redis token TTLs and cache expiration for improved session management ([`1a1ca2b`](https://github.com/OpenG2P/iam/commit/1a1ca2b68810120c30d6f13a2a494b880a2b6dc9))
- [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Refactor GeoLocationPickerModal to use new utility functions for fetching geo levels and improve state management ([`b69ebd6`](https://github.com/OpenG2P/iam/commit/b69ebd628df3aeffa811d8acd0775b73a109adfb))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Update FastAPI common library reference to version 1.2 and add Keycloak initialization configuration ([`bd43783`](https://github.com/OpenG2P/iam/commit/bd43783f8be1d179c58a24aecc47a3a8a2f3babf))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Refactor JWT validation to use CryptoFactory and update tests for component registration ([`9d4d3c1`](https://github.com/OpenG2P/iam/commit/9d4d3c1ce970aca4b51d144ffb9470eb95906a75))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add registration for mds, awe, partner api ([`22af5d6`](https://github.com/OpenG2P/iam/commit/22af5d687c5ff99f03a6adf5ea97e6037b51c04e))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Refactor DataPoliciesTab layout and comment out IconBase64Field in LoginProviderForm ([`6495993`](https://github.com/OpenG2P/iam/commit/649599302609de1af0604741c6fa5a74fe6f8e48))
- Remove include_domains from request payload in attribute API calls ([`dafa801`](https://github.com/OpenG2P/iam/commit/dafa801754b76a0e4591e48da0f47029c4ea4296))
- Fix templating for Keycloak base URL in IAM Staff and Agent APIs ([`ed5741a`](https://github.com/OpenG2P/iam/commit/ed5741a4cac7edafecf79d6f0b132869a605dd18))

<a id="v-1-4-0-rc-101"></a>

## iam 1.4.0-rc.101 — 2026-09-01

_commit `ebafe2e` · changes since 1.4.0-rc.100_
<!-- build:1.4.0-rc.101 revision:ebafe2eaeea1e3d69e1760bf60624f76d5162c2a ts:1788258730 -->

**Chart:** [openg2p-iam-service 1.4.0-rc.101](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.0-rc.101.tgz)

### Changes

- updated fastapi-commons to 1.2.0 ([`ebafe2e`](https://github.com/OpenG2P/iam/commit/ebafe2eaeea1e3d69e1760bf60624f76d5162c2a))

<a id="v-1-4-0-rc-100"></a>

## iam 1.4.0-rc.100 — 2026-08-28

_commit `f8bccfe` · changes since v1.3.0_
<!-- build:1.4.0-rc.100 revision:f8bccfe85f60a9793ff290a785f58e37e0a95927 ts:1787897855 -->

**Chart:** [openg2p-iam-service 1.4.0-rc.100](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-1.4.0-rc.100.tgz)

### Summary

- **Major:** CI migration to GitLab, dropping GitHub Actions, and implementing new CI workflows; completed GitLab migration by porting workflows and dropping unused scripts.
- Security enhancements: updated FastAPI library to version 1.2 and added Keycloak initialization configuration; refactored JWT validation using CryptoFactory.
- Session management improvements: updated Redis token TTLs and cache expiration settings for better session handling.
- Feature additions: implemented data policy management and middleware, added policy filter preview and view data policy modal components, and enhanced application management with Keycloak integration.
- UI/UX refinements: refactored application and login provider components for consistency, improved accessibility, and introduced reusable UI components; enhanced modal styling and user experience across various components.
- API updates: enabled agent portal API by default, wired iam-agent-portal-api into the IAM chart, and removed include_domains from attribute API calls.
- Testing improvements: updated data policy middleware tests for accuracy and coverage, added unit tests for IAM staff portal API components, and improved overall unit test coverage for core IAM functionality.
- Versioning and dependency updates: bumped version to 1.4.0, aligned release line with GitHub, and updated image tags in values.yaml.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.4 release line with GitHub ([`f8bccfe`](https://github.com/OpenG2P/iam/commit/f8bccfe85f60a9793ff290a785f58e37e0a95927))
- [G2P-5592](https://openg2p.atlassian.net/browse/G2P-5592) Update Redis token TTLs and cache expiration for improved session management ([`1a1ca2b`](https://github.com/OpenG2P/iam/commit/1a1ca2b68810120c30d6f13a2a494b880a2b6dc9))
- [G2P-5587](https://openg2p.atlassian.net/browse/G2P-5587) Refactor GeoLocationPickerModal to use new utility functions for fetching geo levels and improve state management ([`b69ebd6`](https://github.com/OpenG2P/iam/commit/b69ebd628df3aeffa811d8acd0775b73a109adfb))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Update FastAPI common library reference to version 1.2 and add Keycloak initialization configuration ([`bd43783`](https://github.com/OpenG2P/iam/commit/bd43783f8be1d179c58a24aecc47a3a8a2f3babf))
- [G2P-5581](https://openg2p.atlassian.net/browse/G2P-5581) Refactor JWT validation to use CryptoFactory and update tests for component registration ([`9d4d3c1`](https://github.com/OpenG2P/iam/commit/9d4d3c1ce970aca4b51d144ffb9470eb95906a75))
- [G2P-5578](https://openg2p.atlassian.net/browse/G2P-5578) Add registration for mds, awe, partner api ([`22af5d6`](https://github.com/OpenG2P/iam/commit/22af5d687c5ff99f03a6adf5ea97e6037b51c04e))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Refactor DataPoliciesTab layout and comment out IconBase64Field in LoginProviderForm ([`6495993`](https://github.com/OpenG2P/iam/commit/649599302609de1af0604741c6fa5a74fe6f8e48))
- Remove include_domains from request payload in attribute API calls ([`dafa801`](https://github.com/OpenG2P/iam/commit/dafa801754b76a0e4591e48da0f47029c4ea4296))
- Fix templating for Keycloak base URL in IAM Staff and Agent APIs ([`ed5741a`](https://github.com/OpenG2P/iam/commit/ed5741a4cac7edafecf79d6f0b132869a605dd18))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Bump version to 1.4.0 and update image tags in values.yaml ([`1eb3a25`](https://github.com/OpenG2P/iam/commit/1eb3a250b00aefbec03aaadf96e2516f4bc07756))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Add iam-staff-ui to the build/publish pipeline and pin its chart image tag ([`d7fdd9c`](https://github.com/OpenG2P/iam/commit/d7fdd9c233643770a9f132d96649ec0ee76f5248))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Fix pre-commit ([`a2157ea`](https://github.com/OpenG2P/iam/commit/a2157eaed5056c130daac1cf760b0e63a8af78fe))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Remove registry API URL from env and add API URL to staff portal application ([`69495bf`](https://github.com/OpenG2P/iam/commit/69495bf53b3fb5b2ef72d4ecf3772017c6d8d3d2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal API by default and fix show_if conditions ([`da9db90`](https://github.com/OpenG2P/iam/commit/da9db90f1c0dd7702b650d205c8535b819a4d6a8))
- [G2P-5537](https://openg2p.atlassian.net/browse/G2P-5537) Port attribute-management API routes and hooks from upstream develop; drop wrongly-ported role-permission caching ([`74c5879`](https://github.com/OpenG2P/iam/commit/74c587992636e1c4fa913457035817272c3e573e))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Complete GitLab migration: port GitHub workflows to CI guards, drop .github, and port pending upstream commits ([`e04966e`](https://github.com/OpenG2P/iam/commit/e04966ec74808402fc600f9f1e936a5c8351595f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`3ed9ea0`](https://github.com/OpenG2P/iam/commit/3ed9ea066ce582c301e59ef4fc01d4b083b42fe2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Wire iam-agent-portal-api into the IAM chart behind a disabled-by-default switch ([`9de210b`](https://github.com/OpenG2P/iam/commit/9de210b49892450a651173bdd85538db21e692b9))
- Remove unused SQL seed script and login providers JSON; update IAM_STAFF_UI_PERMISSIONS to include delete permissions ([`1c5a6a6`](https://github.com/OpenG2P/iam/commit/1c5a6a633a477e72d5d16ff6e67fd97fc0fd39eb))
- Enhance values.yaml: Add backend API URLs for iam-staff-ui and update login provider ID ([`6d1d4f9`](https://github.com/OpenG2P/iam/commit/6d1d4f9d7708a7484dbff19db6fc89ab2cbfac34))
- Refactor: Remove unused use client directives and implement ApplicationsPageClient component ([`a694c5d`](https://github.com/OpenG2P/iam/commit/a694c5d11faf44ea65ea3197bc173ec56486d6f4))
- [G2P-5485](https://openg2p.atlassian.net/browse/G2P-5485) Enhance IconBase64Field with MIME type detection ([`2556ffa`](https://github.com/OpenG2P/iam/commit/2556ffa32f5137038cffca59e9e5deb91e5a82af))
- [G2P-5479](https://openg2p.atlassian.net/browse/G2P-5479) Add policy filter preview and view data policy modal components ([`5234a36`](https://github.com/OpenG2P/iam/commit/5234a3655cc2f27e4bb0471743df402ff66df143))
- Test: Update data policy middleware tests for accuracy and coverage ([`35f3bd9`](https://github.com/OpenG2P/iam/commit/35f3bd9004798e51b97bcdec69528df7cd9e9476))
- Feat: Implement data policy management and middleware ([`8a1c8cd`](https://github.com/OpenG2P/iam/commit/8a1c8cdca49d67828304428cd64f38da89570977))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Enhance application management with Keycloak integration ([`d7b1c7f`](https://github.com/OpenG2P/iam/commit/d7b1c7f348009636a95db8db1d0fd2c060250b12))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor UI components for consistency: update styles, improve accessibility, and enhance user experience across error, button, input, and modal components ([`0c1d936`](https://github.com/OpenG2P/iam/commit/0c1d93694207a526adc4162de79743275c451bde))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Add reusable UI components, improve modal styling, and refactor application and login provider pages ([`12956d8`](https://github.com/OpenG2P/iam/commit/12956d893015c299b7f4057572f7bd9b6f33c6f0))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor application and login provider components ([`b582d6f`](https://github.com/OpenG2P/iam/commit/b582d6fcd7a74a1202f7a642e1fa410c093301ed))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Add Roles, Permissions, and Role-Permissions management tabs with reusable modals, enhanced tables, login provider improvements, and loading skeletons ([`e70231c`](https://github.com/OpenG2P/iam/commit/e70231c8b56f1b0c908f5075025dbc038dc69abf))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor authentication and RBAC contexts, introduce reusable hooks/components, and add typed application and login provider data management ([`7ff270c`](https://github.com/OpenG2P/iam/commit/7ff270cb101d0861b808be879b220880a3c8e5c9))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor ApplicationAccess, Applications, and LoginProviders controllers to use strongly typed response models ([`ab5686d`](https://github.com/OpenG2P/iam/commit/ab5686dd272343ca932825f65a8acbc83da3cbfe))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Implement Application Management module in IAM Staff UI ([`235f138`](https://github.com/OpenG2P/iam/commit/235f138d8a691ee6efb123d4791238748ec74a8e))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix chart-image-paths to .iamStaffPortalApi.image.tag (chart shipped unpinned) ([`947f58f`](https://github.com/OpenG2P/iam/commit/947f58f1b04920854189aa65c8b9c99ff708da39))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented ([`8109437`](https://github.com/OpenG2P/iam/commit/810943725a2040fadbf4c18868471f205daa930c))
- 0.0.0-develop.N versioning implemented. ([`a1579ba`](https://github.com/OpenG2P/iam/commit/a1579ba229373a333ceb75797685e3a086d2b9d8))
- [G2P-5313](https://openg2p.atlassian.net/browse/G2P-5313) Add unit tests for IAM staff portal API components ([`8670822`](https://github.com/OpenG2P/iam/commit/867082285f362b88550be7ba2a265621eb0b8a4d))
- [G2P-5313](https://openg2p.atlassian.net/browse/G2P-5313) Improve unit test coverage for core IAM functionality ([`c762c7b`](https://github.com/OpenG2P/iam/commit/c762c7b741a5c9d19bbd30b6875daacbd5d88717))

# Develop builds

<a id="v-0-0-0-develop-98"></a>

## iam — develop 0.0.0-develop.98 (2026-09-02)

_commit `6ebcbf3` · changes since 0.0.0-develop.97_
<!-- build:0.0.0-develop.98 revision:6ebcbf3b1b7d03dfa21016e8a47eb611c751ac40 ts:1788254954 -->

**Chart:** [openg2p-iam-service 0.0.0-develop.98](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-0.0.0-develop.98.tgz)

### Changes

- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Render the Keycloak base URL and point the agent app at the agent portal ([`6ebcbf3`](https://github.com/OpenG2P/iam/commit/6ebcbf3b1b7d03dfa21016e8a47eb611c751ac40))

<a id="v-0-0-0-develop-97"></a>

## iam — develop 0.0.0-develop.97 (2026-08-28)

_commit `8682df5` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.97 revision:8682df599b0dc919606c8e9f77387d09d0479829 ts:1787883007 -->

**Chart:** [openg2p-iam-service 0.0.0-develop.97](https://openg2p.github.io/openg2p-helm/openg2p-iam-service-0.0.0-develop.97.tgz)

### Summary

- **Major:** CI transition: switched from GitHub Actions to GitLab CI, completing migration by porting workflows and dropping unused scripts.
- Security enhancements: separated agent and staff auth cookies, enforced 401 responses on unverifiable tokens, and seeded the agent realm's login provider for token validation.
- API updates: matched the staff portal's auth surface in the agent portal API and enabled the agent portal API by default with fixed conditions.
- Build improvements: added iam-staff-ui to the build pipeline, updated image tags, and applied black formatting across the repository.
- Dependency management: bumped version to 1.4.0 and enhanced values.yaml with backend API URLs and updated login provider IDs.
- Code cleanup: removed unused SQL seed scripts and login providers JSON, and refactored components to eliminate unused directives.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub ([`8682df5`](https://github.com/OpenG2P/iam/commit/8682df599b0dc919606c8e9f77387d09d0479829))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) applied the platform-service group change on iam service ([`0d0ba76`](https://github.com/OpenG2P/iam/commit/0d0ba7675231135ba843f99eaa598bab9dfdf60a))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Run pre-commit as a single looping job without a runner-local cache ([`4c9d599`](https://github.com/OpenG2P/iam/commit/4c9d599acd40e81a8620243632ea80a86a3b0bd4))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Match the staff portal's auth surface in the agent portal API ([`31250d7`](https://github.com/OpenG2P/iam/commit/31250d7f4207e9d946c1986fa0ea3311d8dbfcce))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Keep agent and staff auth cookies apart and 401 on unverifiable tokens ([`2c74a91`](https://github.com/OpenG2P/iam/commit/2c74a91033590b4355e9d0ce1898adbe900edd14))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Apply black formatting at the repo's 110-column line length ([`29983b7`](https://github.com/OpenG2P/iam/commit/29983b7ccd0e6a9d4ab68ca61e642e13efc129ad))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Seed the agent realm's login provider so agent tokens validate ([`d6ecd80`](https://github.com/OpenG2P/iam/commit/d6ecd80f634a0306d02458a9474144abc24b324f))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Bump version to 1.4.0 and update image tags in values.yaml ([`1eb3a25`](https://github.com/OpenG2P/iam/commit/1eb3a250b00aefbec03aaadf96e2516f4bc07756))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Add iam-staff-ui to the build/publish pipeline and pin its chart image tag ([`d7fdd9c`](https://github.com/OpenG2P/iam/commit/d7fdd9c233643770a9f132d96649ec0ee76f5248))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Fix pre-commit ([`a2157ea`](https://github.com/OpenG2P/iam/commit/a2157eaed5056c130daac1cf760b0e63a8af78fe))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Remove registry API URL from env and add API URL to staff portal application ([`69495bf`](https://github.com/OpenG2P/iam/commit/69495bf53b3fb5b2ef72d4ecf3772017c6d8d3d2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal API by default and fix show_if conditions ([`da9db90`](https://github.com/OpenG2P/iam/commit/da9db90f1c0dd7702b650d205c8535b819a4d6a8))
- [G2P-5537](https://openg2p.atlassian.net/browse/G2P-5537) Port attribute-management API routes and hooks from upstream develop; drop wrongly-ported role-permission caching ([`74c5879`](https://github.com/OpenG2P/iam/commit/74c587992636e1c4fa913457035817272c3e573e))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Complete GitLab migration: port GitHub workflows to CI guards, drop .github, and port pending upstream commits ([`e04966e`](https://github.com/OpenG2P/iam/commit/e04966ec74808402fc600f9f1e936a5c8351595f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`3ed9ea0`](https://github.com/OpenG2P/iam/commit/3ed9ea066ce582c301e59ef4fc01d4b083b42fe2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Wire iam-agent-portal-api into the IAM chart behind a disabled-by-default switch ([`9de210b`](https://github.com/OpenG2P/iam/commit/9de210b49892450a651173bdd85538db21e692b9))
- Remove unused SQL seed script and login providers JSON; update IAM_STAFF_UI_PERMISSIONS to include delete permissions ([`1c5a6a6`](https://github.com/OpenG2P/iam/commit/1c5a6a633a477e72d5d16ff6e67fd97fc0fd39eb))
- Enhance values.yaml: Add backend API URLs for iam-staff-ui and update login provider ID ([`6d1d4f9`](https://github.com/OpenG2P/iam/commit/6d1d4f9d7708a7484dbff19db6fc89ab2cbfac34))
- Refactor: Remove unused use client directives and implement ApplicationsPageClient component ([`a694c5d`](https://github.com/OpenG2P/iam/commit/a694c5d11faf44ea65ea3197bc173ec56486d6f4))
- [G2P-5485](https://openg2p.atlassian.net/browse/G2P-5485) Enhance IconBase64Field with MIME type detection ([`2556ffa`](https://github.com/OpenG2P/iam/commit/2556ffa32f5137038cffca59e9e5deb91e5a82af))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
