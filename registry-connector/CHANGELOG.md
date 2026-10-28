# registry-connector

_Published automatically._

**Repository:** [github.com/OpenG2P/registry-connector](https://github.com/OpenG2P/registry-connector) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.11`](#v-0-0-0-develop-11) | 2026-10-28 | develop |  |
| [`0.0.0-develop.9`](#v-0-0-0-develop-9) | 2026-10-21 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-11"></a>

## registry-connector — develop 0.0.0-develop.11 (2026-10-28)

_commit `c535ba0` · changes since 0.0.0-develop.9_
<!-- build:0.0.0-develop.11 revision:c535ba0c89c7a53ca4ca618b31c3b863bc92b22a ts:1793185899 -->

**Chart:** [registry-connector 0.0.0-develop.11](https://openg2p.github.io/openg2p-helm/registry-connector-0.0.0-develop.11.tgz)

### Changes

- fix: store last_poll_at as TIMESTAMPTZ ([`42d7c1a`](https://github.com/OpenG2P/registry-connector/commit/42d7c1aa16dac331a22b1b2b1ec59f5998e4fb86))

<a id="v-0-0-0-develop-9"></a>

## registry-connector — develop 0.0.0-develop.9 (2026-10-21)

_commit `57c8e96` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.9 revision:57c8e96e3610ebcee596b07a6f53292e830242ff ts:1792578020 -->

**Chart:** [registry-connector 0.0.0-develop.9](https://openg2p.github.io/openg2p-helm/registry-connector-0.0.0-develop.9.tgz)

### Summary

- **Major:** Introduced a new connector API and admin UI, enhancing functionality and user interaction.
- Packaging updates: renamed components to registry-connector and aligned structure with OpenG2P Gen2 layout.
- Cleanup: removed client-specific environment settings, design documentation, and demo content from the connector PR.
- Dependency management: ceased vendoring the postgres-init helm package, streamlining the project.

### Changes

- fix: repair registry-connector Chart.yaml keywords indent ([`2cf0906`](https://github.com/OpenG2P/registry-connector/commit/2cf090655c7ba49b450aaca2c2fbbbfaf860d016))
- chore: rename packaging parts to registry-connector ([`cc45139`](https://github.com/OpenG2P/registry-connector/commit/cc45139b38c5f72140d22cf82fbd039e30adb3ab))
- chore: align packaging with OpenG2P Gen2 layout ([`663c753`](https://github.com/OpenG2P/registry-connector/commit/663c753f87483e6061f897ae3e0c278568ece88a))
- chore: stop vendoring postgres-init helm package ([`5d07b1e`](https://github.com/OpenG2P/registry-connector/commit/5d07b1ecd808cb840061ea4109e27086c97de884))
- chore: strip client-specific env, design docs, and demos from connector PR ([`905a174`](https://github.com/OpenG2P/registry-connector/commit/905a1747b411cf021062fc5d4ca3641448299cd9))
- feat: add connector API and admin UI ([`458c014`](https://github.com/OpenG2P/registry-connector/commit/458c01481b00efdabad4d357e82e29ce39e1ab30))
- Initial commit ([`1e6c812`](https://github.com/OpenG2P/registry-connector/commit/1e6c8121cf903e065ceeda2923f8927b910a5762))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
