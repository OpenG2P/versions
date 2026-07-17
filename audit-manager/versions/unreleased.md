## audit-manager — Unreleased (0.0.0-develop.20, 2026-07-17)

_commit `b63bc77` · baseline: release the start_
<!-- build:0.0.0-develop.20 revision:b63bc7753efed44a199939a6033c99539d628295 -->

### Summary

_All changes since release the start:_

- Breaking Change: CI has been switched from GitHub Actions to GitLab CI, with a new configuration implemented in `.gitlab-ci.yml`.
- New Feature: A test script to call the partner API has been added.
- New Feature: An uninstall script has been introduced to facilitate easier removal of the application.
- Enhancement: OpenAPI documentation has been enriched and the OpenAPI JSON specification has been generated.
- Bug Fix: Several bugs have been fixed, including issues with Kafka initialization and Helm publishing.
- Improvement: The column structure in the database has been simplified for better clarity and usability.
- Documentation: Project documentation has been migrated to Gitbook for improved accessibility.
- Maintenance: URLs have been updated throughout the application to ensure accuracy.
- Maintenance: A `.gitignore` file has been added to streamline version control.
- Maintenance: Fix attempts have been made for Docker build failures and other minor issues.

### Since last release (the start)

- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`b63bc77`](https://gitlab.com/openg2p/audit-manager/-/commit/b63bc7753efed44a199939a6033c99539d628295))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) New CI implemented. ([`2c920b4`](https://gitlab.com/openg2p/audit-manager/-/commit/2c920b4db9827ae216e3d712f657a0f2bc0492e5))
- [G2P-4818](https://openg2p.atlassian.net/browse/G2P-4818) Test script to call partner api added. ([`01daf0c`](https://gitlab.com/openg2p/audit-manager/-/commit/01daf0c352b8572ef57144299d89fde03656b037))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) tpl applied to variables. ([`7b97069`](https://gitlab.com/openg2p/audit-manager/-/commit/7b970697881f76777fd7612dc195a54c3a02b129))
- chore: auto-generate OpenAPI spec [skip ci] ([`b355590`](https://gitlab.com/openg2p/audit-manager/-/commit/b35559029ab3aaf53d0b193858d25824a61f412c))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Uninstall script added. ([`bc5d101`](https://gitlab.com/openg2p/audit-manager/-/commit/bc5d1018dbea50dabe6e3142034c556c1ada838f))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Few bugs fixed ([`0ba7140`](https://gitlab.com/openg2p/audit-manager/-/commit/0ba71400946df72f30bbc8b2b1de51b4f886a299))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Fixes in schema for actor fields. ([`c9d554b`](https://gitlab.com/openg2p/audit-manager/-/commit/c9d554baff6b5b5273cf80f3cb454852f8110463))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) OpenAPI docs enriched. ([`3450fe8`](https://gitlab.com/openg2p/audit-manager/-/commit/3450fe8dd72171245ccd3f900e878186821bea46))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) OpenAPI json written. ([`56aac35`](https://gitlab.com/openg2p/audit-manager/-/commit/56aac35a1d09e1e2876f46a3b0b8d9c0efc2c0a7))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) URLs updated. ([`4377bc5`](https://gitlab.com/openg2p/audit-manager/-/commit/4377bc5fb8fe6661eef6d3fc9b6bad1cd0128f8e))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Helm publish issue fix attempt. ([`4ee51a3`](https://gitlab.com/openg2p/audit-manager/-/commit/4ee51a3ad841a55aa7e23ebbfc14b3ed0fa822fa))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Kafka init bugs fixed. Added gitignore. ([`86dcd2a`](https://gitlab.com/openg2p/audit-manager/-/commit/86dcd2aa5065306ea08f0d4b43834369351de78c))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Documentation moved to Gitbook ([`20545ea`](https://gitlab.com/openg2p/audit-manager/-/commit/20545ea9aa351d26c115486c78159e9b2f861579))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Column structure simplified. ([`5a224f3`](https://gitlab.com/openg2p/audit-manager/-/commit/5a224f36179af85c3f0d78cb08001489ab0963b1))
-  [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Fixes. ([`4e75b8d`](https://gitlab.com/openg2p/audit-manager/-/commit/4e75b8d7c0244c970beb3d852c8c334edf0723ca))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Fix attempt for docker build failure. Renaming. ([`476718d`](https://gitlab.com/openg2p/audit-manager/-/commit/476718d698b2dd8a9f5adfa633250de67f3dc986))
- [G2P-4644](https://openg2p.atlassian.net/browse/G2P-4644) Initial version. WIP. ([`8b174a7`](https://gitlab.com/openg2p/audit-manager/-/commit/8b174a70aeab0b676babc3ac72af075ddf8b7426))
- Initial commit ([`06d5c61`](https://gitlab.com/openg2p/audit-manager/-/commit/06d5c61632c103036c0eacac375b080c1d6fe341))
