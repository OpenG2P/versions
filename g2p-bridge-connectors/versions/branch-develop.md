## g2p-bridge-connectors — `develop` branch (2026-11-20)

_moving branch · latest commit `2ff7e8b` · baseline: 1.2.1_
<!-- build:develop revision:2ff7e8ba2f3d1f7e15ca37c482383ba2e256d64b ts:1795164618 -->

### Summary

_Changes on `develop` since 1.2.1:_

- **Major:** CI/CD overhaul: introduced GitHub Actions with new workflows for build and publish, while removing the legacy GitLab CI configuration.
- Refactoring: unified crypto imports by consolidating the usage of CryptoFactory and CryptoHelper across the codebase.
- Documentation updates: minor improvements to project documentation to reflect recent changes and enhance clarity.

### Recent commits (latest 5)

- [G2P-5956](https://openg2p.atlassian.net/browse/G2P-5956) Refactor crypto imports to unify usage of CryptoFactory and CryptoHelper ([`7b408f9`](https://github.com/OpenG2P/g2p-bridge-connectors/commit/7b408f9432ad838e8452a12a0d637bc230fd084d))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Publish to the catalogue from GitHub ([`ef1b69c`](https://github.com/OpenG2P/g2p-bridge-connectors/commit/ef1b69c7bee98c4c6f4a119130bba59dbbcc918d))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Track version history via packaging pipeline (kind: library) ([`811d31f`](https://github.com/OpenG2P/g2p-bridge-connectors/commit/811d31fd753afb59d7125905aac05e7b8188f3dc))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Fix mapper Initializer order so SPARMapper gets its SPAR client; fail fast if unregistered ([`81a0747`](https://github.com/OpenG2P/g2p-bridge-connectors/commit/81a07477238a1b98a5dfe51f7673461d35061fbf))
- [G2P-5374](https://openg2p.atlassian.net/browse/G2P-5374) Apply black/ruff formatting ([`cc7e0bb`](https://github.com/OpenG2P/g2p-bridge-connectors/commit/cc7e0bbc23f3b354c8956c9143c367b46e3f068f))
