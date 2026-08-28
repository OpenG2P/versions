# iam

_Published automatically._

**Repository:** [github.com/OpenG2P/iam](https://github.com/OpenG2P/iam) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.97`](#v-0-0-0-develop-97) | 2026-08-28 | develop |  |

# Develop builds

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
