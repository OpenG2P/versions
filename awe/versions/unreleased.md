## awe — Unreleased (0.0.0-develop.67, 2026-07-17)

_commit `201996b` · baseline: release 1.1.0_
<!-- build:0.0.0-develop.67 revision:201996b6919f3e74def2b6bac25cf5306c5f2e3c -->

### Summary

_All changes since release 1.1.0:_

- Added support for multiple token issuers, allowing tokens minted via the public Keycloak hostname to validate alongside in-cluster tokens, resolving the 'Invalid issuer' error on registry-forwarded user tokens.

### Since last release (1.1.0)

- [G2P-5378](https://openg2p.atlassian.net/browse/G2P-5378) AWE: accept multiple token issuers (issuer + additional_issuers) so tokens minted via the public Keycloak hostname validate alongside in-cluster ones; fixes 'Invalid issuer' on registry-forwarded user tokens ([`201996b`](https://gitlab.com/openg2p/awe/-/commit/201996b6919f3e74def2b6bac25cf5306c5f2e3c))
