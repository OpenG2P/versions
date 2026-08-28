# id-generator

_Published automatically._

**Repository:** [github.com/OpenG2P/id-generator](https://github.com/OpenG2P/id-generator) · **Container images:** [Container Registry](https://hub.docker.com/r/openg2p/openg2p-id-generator)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.47`](#v-0-0-0-develop-47) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-47"></a>

## id-generator — develop 0.0.0-develop.47 (2026-08-28)

_commit `6afff1c` · changes since 1.1.0_
<!-- build:0.0.0-develop.47 revision:6afff1cbaabc679c371cd66b3ebd7f3211a0bd3e ts:1787883057 -->

**Chart:** [openg2p-id-generator 0.0.0-develop.47](https://openg2p.github.io/openg2p-helm/openg2p-id-generator-0.0.0-develop.47.tgz)

### Summary

- **Major:** Migration to GitLab for CI/CD, including the switch from GitHub Actions to GitLab CI with the new `.gitlab-ci.yml` configuration and disabling GitHub build/publish.
- Repository restructuring: applied platform-service group changes to the id-generator project.
- GitHub Actions integration: added caller functionality and restored build/publish capabilities for GitHub.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Add the GitHub Actions caller ([`6afff1c`](https://github.com/OpenG2P/id-generator/commit/6afff1cbaabc679c371cd66b3ebd7f3211a0bd3e))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`eb2f9f2`](https://github.com/OpenG2P/id-generator/commit/eb2f9f2adb91afaec00dab9f8f5c364ab7e7a98d))
- [G2P-5575](https://openg2p.atlassian.net/browse/G2P-5575) Changes applied the platform-service group change on id-generator ([`1b69ab5`](https://github.com/OpenG2P/id-generator/commit/1b69ab5bc3a65e9dc883256c8dd0962436081a59))
- Moved to GitLab: openg2p/id-generator (read-only; build/publish disabled) ([`baa00de`](https://github.com/OpenG2P/id-generator/commit/baa00de73819bd5ed80d9867c65371f9ebd3e1c6))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`da86c41`](https://github.com/OpenG2P/id-generator/commit/da86c41d00c48db6030005548ef6c1d31d4b6e48))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
