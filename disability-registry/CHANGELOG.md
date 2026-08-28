# disability-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/disability-registry](https://github.com/OpenG2P/disability-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.10`](#v-0-0-0-develop-10) | 2026-08-28 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-10"></a>

## disability-registry — develop 0.0.0-develop.10 (2026-08-28)

_commit `ad4bf83` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.10 revision:ad4bf83dd2c8498e01b731123283dce20329c582 ts:1787884394 -->

**Chart:** [openg2p-disability-registry 0.0.0-develop.10](https://openg2p.github.io/openg2p-helm/openg2p-disability-registry-0.0.0-develop.10.tgz)

### Summary

- **Major:** Enabled dashboards and shipped the Superset bundle, ensuring the import job runs correctly with committed reporting views.
- Reporting views job fixed to correctly map entity names and prevent data loss, addressing issues with geography and indexing.
- Cleanup: Removed unused factory classes and related imports from the disability extension to streamline the codebase.
- Build process restored to publish on GitHub, enhancing CI capabilities.
- Version bumped to RP 0.0.0-develop.384, indicating ongoing development progress.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`ad4bf83`](https://github.com/OpenG2P/disability-registry/commit/ad4bf83dd2c8498e01b731123283dce20329c582))
- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Correct the theme comment: the users are government staff, not the people whose records the registry holds. ([`358802c`](https://github.com/OpenG2P/disability-registry/commit/358802c21d5736a6dd1e26b04097775e159676c6))
- [G2P-5524](https://openg2p.atlassian.net/browse/G2P-5524) Remove unused factory classes and related imports from the disability extension ([`4574067`](https://github.com/OpenG2P/disability-registry/commit/45740672d519d167afdac081125b5574913d3973))
- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Enable dashboards and ship the Superset bundle. Reporting views were already on but the bundle was absent, so the import job never ran; CI packages the chart without a database to build one from, so files/dr-dashboards.zip is committed as in FR and NSR. ([`ff74399`](https://github.com/OpenG2P/disability-registry/commit/ff743994f3d382b2248b49a771fed4561673cbff))
- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Fix the reporting views job. The generator derives entity names from table names, and g2p_register_persons_with_disability pluralises the head noun so it never matched the declared tree — every parent link was dropped, costing the children their geography and failing on the geo_1 index. Map it via views:, and stop indexing program_enrolment on program_name, which the pii rules withhold. ([`76890f8`](https://github.com/OpenG2P/disability-registry/commit/76890f82b6daf5aa53aff5e794f156e55d0b98a7))
- Bumped up RP version to 0.0.0-develop.384 ([`975b783`](https://github.com/OpenG2P/disability-registry/commit/975b783a217a6def41a56f8d482eab6788b630ea))
- [G2P-5518](https://openg2p.atlassian.net/browse/G2P-5518) Workflow fix. ([`cd0b5a7`](https://github.com/OpenG2P/disability-registry/commit/cd0b5a7d1cd84f241d4e1175b9b0017fa5005571))
- Initial version. WIP. ([`003c1ea`](https://github.com/OpenG2P/disability-registry/commit/003c1ea8b6c6b1c308b2ab5cb339f12a64fb6c6e))
- Initial commit ([`7e0c0d9`](https://github.com/OpenG2P/disability-registry/commit/7e0c0d97718894e6665695cfbafa05b0b8d18d35))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
