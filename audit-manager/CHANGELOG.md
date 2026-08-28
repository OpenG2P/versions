# audit-manager

_Published automatically._

**Repository:** [github.com/OpenG2P/audit-manager](https://github.com/OpenG2P/audit-manager) · **Container images:** [Container Registry](https://hub.docker.com/r/openg2p/openg2p-audit-manager)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.25`](#v-0-0-0-develop-25) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-25"></a>

## audit-manager — develop 0.0.0-develop.25 (2026-08-28)

_commit `36dbf77` · changes since 1.0.0_
<!-- build:0.0.0-develop.25 revision:36dbf77a0c0ff8afc9a10a1de769b3bdf06d5fd6 ts:1787878791 -->

**Chart:** [openg2p-audit-manager 0.0.0-develop.25](https://openg2p.github.io/openg2p-helm/openg2p-audit-manager-0.0.0-develop.25.tgz)

### Summary

- **Major:** Migration to GitLab for CI/CD, replacing GitHub Actions with a new `.gitlab-ci.yml` configuration and disabling build/publish on GitHub.
- Container registry updated for the audit manager, reflecting changes in deployment strategy.
- GitHub repository remains accessible in a read-only state for reference, but active development has shifted to GitLab.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`36dbf77`](https://github.com/OpenG2P/audit-manager/commit/36dbf77a0c0ff8afc9a10a1de769b3bdf06d5fd6))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) audit manager container regitry changed ([`80dbc1c`](https://github.com/OpenG2P/audit-manager/commit/80dbc1c4d762b12ae19f0ee494d4df041451e831))
- Moved to GitLab: openg2p/audit-manager (read-only; build/publish disabled) ([`42bc760`](https://github.com/OpenG2P/audit-manager/commit/42bc760109bb718406069da8b82efac8fdd63de6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`b63bc77`](https://github.com/OpenG2P/audit-manager/commit/b63bc7753efed44a199939a6033c99539d628295))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
