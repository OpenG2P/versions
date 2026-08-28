# mock-id-system

_Published automatically._

**Repository:** [github.com/OpenG2P/mock-id-system](https://github.com/OpenG2P/mock-id-system)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.7`](#v-0-0-0-develop-7) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-7"></a>

## mock-id-system — develop 0.0.0-develop.7 (2026-08-28)

_commit `4c1a3c6` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.7 revision:4c1a3c63f5ffe3181351e780d6eaabb88352c396 ts:1787893358 -->

**Chart:** [mock-identity-system 0.0.0-develop.7](https://openg2p.github.io/openg2p-helm/mock-identity-system-0.0.0-develop.7.tgz)

### Summary

- **Major:** Onboarded the mock-identity-system chart to the central pipeline, ensuring streamlined deployment processes.
- Identity management enhancements: fixed identity seeding to validate response bodies and include required photo and biometrics, and seeded mock identities from master data for improved registry authentication.
- Data integrity improvements: stripped whitespace from seeded individual IDs to ensure consistency and reliability.
- Build and deployment updates: implemented GitHub Actions for build and publish processes, enhancing CI/CD workflows.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub ([`4c1a3c6`](https://github.com/OpenG2P/mock-id-system/commit/4c1a3c63f5ffe3181351e780d6eaabb88352c396))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Point the identity seed at the renamed master data secret ([`7420326`](https://github.com/OpenG2P/mock-id-system/commit/7420326d640e73551c9b5e3256f068bab960889b))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Strip whitespace from seeded individual IDs ([`2a23d8f`](https://github.com/OpenG2P/mock-id-system/commit/2a23d8fe6c1e49d5b8e4ef3f0c25f779ed06ee86))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix identity seeding to check response bodies and send required photo and biometrics ([`ca16bdb`](https://github.com/OpenG2P/mock-id-system/commit/ca16bdb8f53e6e07826e76ee87054043271d13ea))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Seed mock identities from master data so registry records can authenticate ([`788bf2b`](https://github.com/OpenG2P/mock-id-system/commit/788bf2bd387f4b8eb10ddc1943ec1c0c9cfad181))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Onboard mock-identity-system chart to the central pipeline (chart-only, upstream images untouched) ([`7a7b3b3`](https://github.com/OpenG2P/mock-id-system/commit/7a7b3b3c66e86f510bd106ee7438821492efcc7a))
- Initial commit ([`f8bb227`](https://github.com/OpenG2P/mock-id-system/commit/f8bb227c1135e5a56922bfa2f33a51c40bfebdf3))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
