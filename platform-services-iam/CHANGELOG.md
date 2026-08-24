# platform-services/iam

_Published automatically._

**Repository:** [gitlab.com/openg2p/platform-services/iam](https://gitlab.com/openg2p/platform-services/iam) · **Container images:** [Container Registry](https://gitlab.com/openg2p/platform-services/iam/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.96`](#v-0-0-0-develop-96) | 2026-08-24 | develop |

# Develop builds

<a id="v-0-0-0-develop-96"></a>

## platform-services/iam — develop 0.0.0-develop.96 (2026-08-24)

_commit `0d0ba76` · changes since v1.3.0_
<!-- build:0.0.0-develop.96 revision:0d0ba7675231135ba843f99eaa598bab9dfdf60a ts:1787589624 -->

**Chart:** [openg2p-iam-service 0.0.0-develop.96](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-iam-service-0.0.0-develop.96.tgz)

### Summary

- **Major:** Complete migration to GitLab CI: ported workflows from GitHub, dropped GitHub Actions, and implemented new CI structure.
- Security enhancements: separated agent and staff auth cookies, enforced 401 responses on unverifiable tokens, and seeded agent realm login provider for token validation.
- Feature additions: implemented data policy management and middleware, enhanced application management with Keycloak integration, and added roles and permissions management tabs in the IAM Staff UI.
- UI improvements: refactored components for consistency and accessibility, improved modal styling, and introduced reusable UI components across various pages.
- Testing improvements: updated data policy middleware tests for accuracy and coverage, and added unit tests for IAM staff portal API components.
- Dependency updates: bumped version to 1.4.0, updated image tags in values.yaml, and pinned chart image tags for iam-staff-ui.
- Code quality: applied black formatting at a 110-column line length, removed unused SQL seed scripts, and refactored various components for better maintainability.

### Changes

- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) applied the platform-service group change on iam service ([`0d0ba76`](https://gitlab.com/openg2p/platform-services/iam/-/commit/0d0ba7675231135ba843f99eaa598bab9dfdf60a))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Run pre-commit as a single looping job without a runner-local cache ([`4c9d599`](https://gitlab.com/openg2p/platform-services/iam/-/commit/4c9d599acd40e81a8620243632ea80a86a3b0bd4))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Match the staff portal's auth surface in the agent portal API ([`31250d7`](https://gitlab.com/openg2p/platform-services/iam/-/commit/31250d7f4207e9d946c1986fa0ea3311d8dbfcce))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Keep agent and staff auth cookies apart and 401 on unverifiable tokens ([`2c74a91`](https://gitlab.com/openg2p/platform-services/iam/-/commit/2c74a91033590b4355e9d0ce1898adbe900edd14))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Apply black formatting at the repo's 110-column line length ([`29983b7`](https://gitlab.com/openg2p/platform-services/iam/-/commit/29983b7ccd0e6a9d4ab68ca61e642e13efc129ad))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Seed the agent realm's login provider so agent tokens validate ([`d6ecd80`](https://gitlab.com/openg2p/platform-services/iam/-/commit/d6ecd80f634a0306d02458a9474144abc24b324f))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Bump version to 1.4.0 and update image tags in values.yaml ([`1eb3a25`](https://gitlab.com/openg2p/platform-services/iam/-/commit/1eb3a250b00aefbec03aaadf96e2516f4bc07756))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Add iam-staff-ui to the build/publish pipeline and pin its chart image tag ([`d7fdd9c`](https://gitlab.com/openg2p/platform-services/iam/-/commit/d7fdd9c233643770a9f132d96649ec0ee76f5248))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Fix pre-commit ([`a2157ea`](https://gitlab.com/openg2p/platform-services/iam/-/commit/a2157eaed5056c130daac1cf760b0e63a8af78fe))
- [G2P-5552](https://openg2p.atlassian.net/browse/G2P-5552) Remove registry API URL from env and add API URL to staff portal application ([`69495bf`](https://gitlab.com/openg2p/platform-services/iam/-/commit/69495bf53b3fb5b2ef72d4ecf3772017c6d8d3d2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal API by default and fix show_if conditions ([`da9db90`](https://gitlab.com/openg2p/platform-services/iam/-/commit/da9db90f1c0dd7702b650d205c8535b819a4d6a8))
- [G2P-5537](https://openg2p.atlassian.net/browse/G2P-5537) Port attribute-management API routes and hooks from upstream develop; drop wrongly-ported role-permission caching ([`74c5879`](https://gitlab.com/openg2p/platform-services/iam/-/commit/74c587992636e1c4fa913457035817272c3e573e))
- [G2P-5348](https://openg2p.atlassian.net/browse/G2P-5348) Complete GitLab migration: port GitHub workflows to CI guards, drop .github, and port pending upstream commits ([`e04966e`](https://gitlab.com/openg2p/platform-services/iam/-/commit/e04966ec74808402fc600f9f1e936a5c8351595f))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`3ed9ea0`](https://gitlab.com/openg2p/platform-services/iam/-/commit/3ed9ea066ce582c301e59ef4fc01d4b083b42fe2))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Wire iam-agent-portal-api into the IAM chart behind a disabled-by-default switch ([`9de210b`](https://gitlab.com/openg2p/platform-services/iam/-/commit/9de210b49892450a651173bdd85538db21e692b9))
- Remove unused SQL seed script and login providers JSON; update IAM_STAFF_UI_PERMISSIONS to include delete permissions ([`1c5a6a6`](https://gitlab.com/openg2p/platform-services/iam/-/commit/1c5a6a633a477e72d5d16ff6e67fd97fc0fd39eb))
- Enhance values.yaml: Add backend API URLs for iam-staff-ui and update login provider ID ([`6d1d4f9`](https://gitlab.com/openg2p/platform-services/iam/-/commit/6d1d4f9d7708a7484dbff19db6fc89ab2cbfac34))
- Refactor: Remove unused use client directives and implement ApplicationsPageClient component ([`a694c5d`](https://gitlab.com/openg2p/platform-services/iam/-/commit/a694c5d11faf44ea65ea3197bc173ec56486d6f4))
- [G2P-5485](https://openg2p.atlassian.net/browse/G2P-5485) Enhance IconBase64Field with MIME type detection ([`2556ffa`](https://gitlab.com/openg2p/platform-services/iam/-/commit/2556ffa32f5137038cffca59e9e5deb91e5a82af))
- [G2P-5479](https://openg2p.atlassian.net/browse/G2P-5479) Add policy filter preview and view data policy modal components ([`5234a36`](https://gitlab.com/openg2p/platform-services/iam/-/commit/5234a3655cc2f27e4bb0471743df402ff66df143))
- Test: Update data policy middleware tests for accuracy and coverage ([`35f3bd9`](https://gitlab.com/openg2p/platform-services/iam/-/commit/35f3bd9004798e51b97bcdec69528df7cd9e9476))
- Feat: Implement data policy management and middleware ([`8a1c8cd`](https://gitlab.com/openg2p/platform-services/iam/-/commit/8a1c8cdca49d67828304428cd64f38da89570977))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Enhance application management with Keycloak integration ([`d7b1c7f`](https://gitlab.com/openg2p/platform-services/iam/-/commit/d7b1c7f348009636a95db8db1d0fd2c060250b12))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor UI components for consistency: update styles, improve accessibility, and enhance user experience across error, button, input, and modal components ([`0c1d936`](https://gitlab.com/openg2p/platform-services/iam/-/commit/0c1d93694207a526adc4162de79743275c451bde))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Add reusable UI components, improve modal styling, and refactor application and login provider pages ([`12956d8`](https://gitlab.com/openg2p/platform-services/iam/-/commit/12956d893015c299b7f4057572f7bd9b6f33c6f0))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor application and login provider components ([`b582d6f`](https://gitlab.com/openg2p/platform-services/iam/-/commit/b582d6fcd7a74a1202f7a642e1fa410c093301ed))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Add Roles, Permissions, and Role-Permissions management tabs with reusable modals, enhanced tables, login provider improvements, and loading skeletons ([`e70231c`](https://gitlab.com/openg2p/platform-services/iam/-/commit/e70231c8b56f1b0c908f5075025dbc038dc69abf))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor authentication and RBAC contexts, introduce reusable hooks/components, and add typed application and login provider data management ([`7ff270c`](https://gitlab.com/openg2p/platform-services/iam/-/commit/7ff270cb101d0861b808be879b220880a3c8e5c9))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Refactor ApplicationAccess, Applications, and LoginProviders controllers to use strongly typed response models ([`ab5686d`](https://gitlab.com/openg2p/platform-services/iam/-/commit/ab5686dd272343ca932825f65a8acbc83da3cbfe))
- [G2P-5431](https://openg2p.atlassian.net/browse/G2P-5431) Implement Application Management module in IAM Staff UI ([`235f138`](https://gitlab.com/openg2p/platform-services/iam/-/commit/235f138d8a691ee6efb123d4791238748ec74a8e))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Fix chart-image-paths to .iamStaffPortalApi.image.tag (chart shipped unpinned) ([`947f58f`](https://gitlab.com/openg2p/platform-services/iam/-/commit/947f58f1b04920854189aa65c8b9c99ff708da39))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented ([`8109437`](https://gitlab.com/openg2p/platform-services/iam/-/commit/810943725a2040fadbf4c18868471f205daa930c))
- 0.0.0-develop.N versioning implemented. ([`a1579ba`](https://gitlab.com/openg2p/platform-services/iam/-/commit/a1579ba229373a333ceb75797685e3a086d2b9d8))
- [G2P-5313](https://openg2p.atlassian.net/browse/G2P-5313) Add unit tests for IAM staff portal API components ([`8670822`](https://gitlab.com/openg2p/platform-services/iam/-/commit/867082285f362b88550be7ba2a265621eb0b8a4d))
- [G2P-5313](https://openg2p.atlassian.net/browse/G2P-5313) Improve unit test coverage for core IAM functionality ([`c762c7b`](https://gitlab.com/openg2p/platform-services/iam/-/commit/c762c7b741a5c9d19bbd30b6875daacbd5d88717))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
