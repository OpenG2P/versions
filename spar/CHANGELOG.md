# spar

_Published automatically._

**Repository:** [github.com/OpenG2P/spar](https://github.com/OpenG2P/spar) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.36`](#v-0-0-0-develop-36) | 2026-08-28 | develop |  |
| [`1.1.0`](#v-1-1-0) | 2026-07-19 | release |  |

# Releases

<a id="v-1-1-0"></a>

## spar 1.1.0 — 2026-07-19

<!-- build:1.1.0 revision:1a7155798e6de6f6abe6bfe109aa5902cc0e660d ts:1784433074 -->

_commit `1a71557` · changes since release v1.0.0_

**Chart:** [openg2p-spar 1.1.0](https://openg2p.github.io/openg2p-helm/openg2p-spar-1.1.0.tgz)

### Release notes

Pegging a stable version; Major structural changes; move to Gitlab

### Summary

- Removed the legacy Keymanager crypto backend from SPAR, including configuration, Keycloak initialization dependency, chart, and uninstall script.
- Signing now uses local key verification instead of Keymanager.
- Switched CI from GitHub Actions to GitLab for build and publish processes.
- Integrated with the partner management service, adjusting names as PM is now installed via commons-services.
- Implemented a new CI configuration and aligned build-publish.yml boilerplate with organizational conventions.
- Fixed a Keycloak error and performed various cleanups.
- Automatic version bumping for the develop branch has been introduced.
- Bumped develop build ordinal past retired run-number versions.

### Changes

- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Remove legacy Keymanager crypto backend from SPAR (config, keycloak-init dep, chart, uninstall script) ([`1a71557`](https://gitlab.com/openg2p/spar/spar/-/commit/1a7155798e6de6f6abe6bfe109aa5902cc0e660d))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`db754ff`](https://gitlab.com/openg2p/spar/spar/-/commit/db754ff2f1e05cc1a77c28a7274dbb890f777dc3))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Bump develop build ordinal past retired run-number versions (3/3). ([`3ec576f`](https://gitlab.com/openg2p/spar/spar/-/commit/3ec576f98cd67ebe7946ae4b21eabe2cfa62e26e))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Bump develop build ordinal past retired run-number versions (2/3). ([`5b0c69a`](https://gitlab.com/openg2p/spar/spar/-/commit/5b0c69a59ce72632f9a0ec079ee3e6dc25e1b85b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Bump develop build ordinal past retired run-number versions (1/3). ([`442eee8`](https://gitlab.com/openg2p/spar/spar/-/commit/442eee8f0c11f82327d2e80ac39499a784df954b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Align build-publish.yml boilerplate with org convention (partner-management/consent-manager). ([`31c1551`](https://gitlab.com/openg2p/spar/spar/-/commit/31c1551ed9c4a67207696e453e2886243deea9e5))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`f833914`](https://gitlab.com/openg2p/spar/spar/-/commit/f8339149ebee8992fe94c252ec872eb9e3ecaa0c))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Keycloak error fix attempt. ([`617df81`](https://gitlab.com/openg2p/spar/spar/-/commit/617df81e8a6f89c51d1657ce80b8de8c93819755))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Adjusting names as PM is now installed via commons-services. ([`7b6317b`](https://gitlab.com/openg2p/spar/spar/-/commit/7b6317b61c215a6a3b07da876560f4de83b5f272))
- [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Cleanups. ([`f240efc`](https://gitlab.com/openg2p/spar/spar/-/commit/f240efc429ad004628fc79c7525a85ab143e433c))
-  [G2P-5261](https://openg2p.atlassian.net/browse/G2P-5261) Integration with partner management service. ([`60468d6`](https://gitlab.com/openg2p/spar/spar/-/commit/60468d63c2d7320ea8839cf733586c7d1a696e2f))
- Removing keymanager. ([`26e1855`](https://gitlab.com/openg2p/spar/spar/-/commit/26e185540960bd41d28fea622661e67826704186))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Automatic bumping up of develop version ([`ac13f5b`](https://gitlab.com/openg2p/spar/spar/-/commit/ac13f5b247ce36fd10a944c1ece92ecefc659360))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Pending changes ([`e6b1285`](https://gitlab.com/openg2p/spar/spar/-/commit/e6b128555d1ca73b1f028d6cf54b3cd3a560d072))
- [G2P-5209](https://openg2p.atlassian.net/browse/G2P-5209) Keymanager not used. Local key verification done. ([`5ffb765`](https://gitlab.com/openg2p/spar/spar/-/commit/5ffb765533ef7bda40aa30304d209cf4a1fb6598))
- Versions updated for develop ([`1993b17`](https://gitlab.com/openg2p/spar/spar/-/commit/1993b175c113ac0032aa7bcb644861ebe0ff4145))

# Develop builds

<a id="v-0-0-0-develop-36"></a>

## spar — develop 0.0.0-develop.36 (2026-08-28)

_commit `d47e6af` · changes since 1.1.0_
<!-- build:0.0.0-develop.36 revision:d47e6af33b6560e5c44d2234ab92192956b75cd3 ts:1787884864 -->

**Chart:** [openg2p-spar 0.0.0-develop.36](https://openg2p.github.io/openg2p-helm/openg2p-spar-0.0.0-develop.36.tgz)

### Summary

- **Major:** Transitioned repository hosting from GitLab to GitHub, re-enabling build and publish functionality.
- Repository access change: GitLab repository is now read-only with build and publish disabled.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`d47e6af`](https://github.com/OpenG2P/spar/commit/d47e6af33b6560e5c44d2234ab92192956b75cd3))
- Moved to GitLab: openg2p/spar/spar (read-only; build/publish disabled) ([`0a8a891`](https://github.com/OpenG2P/spar/commit/0a8a891090d3e84d7a826b5faea4d25cc8f541de))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
