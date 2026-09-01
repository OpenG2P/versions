# staff-portal

_Published automatically._

**Repository:** [github.com/OpenG2P/staff-portal](https://github.com/OpenG2P/staff-portal) · **Container images:** [Container Registry](https://hub.docker.com/r/openg2p/openg2p-staff-portal-ui)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.64`](#v-0-0-0-develop-64) | 2026-09-01 | develop |  |
| [`1.2.0-rc.63`](#v-1-2-0-rc-63) | 2026-09-01 | release candidate |  |
| [`0.0.0-develop.63`](#v-0-0-0-develop-63) | 2026-08-28 | develop |  |

# Release candidates

<a id="v-1-2-0-rc-63"></a>

## staff-portal 1.2.0-rc.63 — 2026-09-01

_commit `feb830c` · changes since 0.0.0-develop.63_
<!-- build:1.2.0-rc.63 revision:feb830cfb54f5c34d01b7343e88c66a9781d2bbd ts:1787894593 -->

**Chart:** [openg2p-staff-portal-ui 1.2.0-rc.63](https://openg2p.github.io/openg2p-helm/openg2p-staff-portal-ui-1.2.0-rc.63.tgz)

### Changes

_No new commits since 0.0.0-develop.63._

# Develop builds

<a id="v-0-0-0-develop-64"></a>

## staff-portal — develop 0.0.0-develop.64 (2026-09-01)

_commit `80dc9c7` · changes since 0.0.0-develop.63_
<!-- build:0.0.0-develop.64 revision:80dc9c72ece2b00ef01075690b86ca1d451cb840 ts:1788264896 -->

**Chart:** [openg2p-staff-portal-ui 0.0.0-develop.64](https://openg2p.github.io/openg2p-helm/openg2p-staff-portal-ui-0.0.0-develop.64.tgz)

### Changes

- Update image tag to version 1.2.0 ([`80dc9c7`](https://github.com/OpenG2P/staff-portal/commit/80dc9c72ece2b00ef01075690b86ca1d451cb840))

<a id="v-0-0-0-develop-63"></a>

## staff-portal — develop 0.0.0-develop.63 (2026-08-28)

_commit `feb830c` · changes since v1.1.0_
<!-- build:0.0.0-develop.63 revision:feb830cfb54f5c34d01b7343e88c66a9781d2bbd ts:1787894593 -->

**Chart:** [openg2p-staff-portal-ui 0.0.0-develop.63](https://openg2p.github.io/openg2p-helm/openg2p-staff-portal-ui-0.0.0-develop.63.tgz)

### Summary

- **Major:** New CI implementation enhances build processes and integration.
- Security enhancements: added client-side CSRF token handling and updated authentication cookie management with cookieDomain configuration.
- Refactoring efforts: improved icon handling with the new IconDisplay component and utility functions, and streamlined authentication handling in API routes.
- Cleanup and maintenance: removed obsolete tag workflow, eliminated redundant layers from Dockerfile, and updated environment variables and logout handling.
- Documentation update: revised README to reflect migration to GitLab.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Drop the obsolete tag workflow ([`d647281`](https://github.com/OpenG2P/staff-portal/commit/d647281dd61f6deb0096c2247747ce9d02ebd14c))
- Revise README to reflect GitLab migration ([`2e25db7`](https://github.com/OpenG2P/staff-portal/commit/2e25db7c4f818d5216456952ef52692a4b369edf))
- [G2P-5489](https://openg2p.atlassian.net/browse/G2P-5489) Remove redundant sharp install and chown layers from Dockerfile ([`850420b`](https://github.com/OpenG2P/staff-portal/commit/850420b2e78e4abc5fbdb8b6842999efe81b1290))
- [G2P-5484](https://openg2p.atlassian.net/browse/G2P-5484) Refactor icon handling: add IconDisplay component, and utility functions for base64 icons ([`7fb5d39`](https://github.com/OpenG2P/staff-portal/commit/7fb5d390a42f6fd4d93272186d8d00af3e6f6ede))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`beb29e2`](https://github.com/OpenG2P/staff-portal/commit/beb29e20dfe49d9da1642d63f1608f12746412dd))
- [G2P-5232](https://openg2p.atlassian.net/browse/G2P-5232) Add cookieDomain to environment configuration and update auth cookie handling ([`ede5968`](https://github.com/OpenG2P/staff-portal/commit/ede59681012c75d719da766009e6be57ca8595e4))
- [G2P-5183](https://openg2p.atlassian.net/browse/G2P-5183) Add client-side CSRF token handling ([`bd8eba6`](https://github.com/OpenG2P/staff-portal/commit/bd8eba68efd189709e26b6a3bd50d4eec61e3738))
- [G2P-5154](https://openg2p.atlassian.net/browse/G2P-5154) Update environment variables, and refactor logout handling ([`9fcf42d`](https://github.com/OpenG2P/staff-portal/commit/9fcf42d19de685e20b73ab7fa3bc2cee47add333))
- [G2P-5153](https://openg2p.atlassian.net/browse/G2P-5153) Refactor authentication handling and response processing in API routes ([`20bfcd9`](https://github.com/OpenG2P/staff-portal/commit/20bfcd9ce14522008ab55534fcc7e453cd5507bc))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
