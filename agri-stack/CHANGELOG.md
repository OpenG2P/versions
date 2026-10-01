# agri-stack

_Published automatically._

**Repository:** [github.com/OpenG2P/agri-stack](https://github.com/OpenG2P/agri-stack) · **Container images:** [Container Registry](https://hub.docker.com/r/openg2p/openg2p-agri-composite-api)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.22`](#v-0-0-0-develop-22) | 2026-10-01 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-22"></a>

## agri-stack — develop 0.0.0-develop.22 (2026-10-01)

_commit `3b23fae` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.22 revision:3b23faefc8f8c035903880a1f8527190c67e304a ts:1790867701 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.22](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.22.tgz)

### Summary

- **Major:** Composite service implementation with signed partner API, single consent model, and comprehensive documentation on the composite and consent model.
- Documentation enhancements: detailed design reviews, trust verification configurations, and clarifications on participant roles and certificate issuance as verifiable credentials.
- Register model updates: completion of phase 1 with participant and entity definitions, and decisions on trust status vocabulary and temporary ID management.
- New features: activity registers integrated into the staff UI, crop sown registry added, and alignment of Observations with registries for improved data sharing.
- Documentation restructuring: removal of implementation phasing details, retitling to Agri Stack architecture, and improved organization of design documents.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Composite service (use cases as config, signed partner API, single consent, DAG fan-out to FR/CSR, mapping, audit), Helm chart, CI, partner test kit; docs: composite and consent model as built; service-guide notes ([`3b23fae`](https://github.com/OpenG2P/agri-stack/commit/3b23faefc8f8c035903880a1f8527190c67e304a))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: design review — derived values common to both kinds; verification by an activity (site visit as evidence); one form definition for both kinds; participants explained; certificates are VCs (issuance log, Certify credential ID); open item on credentials after a record change ([`8344158`](https://github.com/OpenG2P/agri-stack/commit/83441581f20c85c2ffec0110875f989214fb2163))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: phase 2 trust = verification only (configurable per field, section, record or activity type; one model for both kinds); terms defined (validation, change, correction, void, approval of changes, verification, dispute); programme approval and certificates left to PBMS ([`c84890f`](https://github.com/OpenG2P/agri-stack/commit/c84890f81d092058dcd9c8038511fc8ead78efdc))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: final figures on period lock; aggregate search across subjects (allow-listed partners); open item on PM policy for bulk access ([`b74df56`](https://github.com/OpenG2P/agri-stack/commit/b74df56eecc33cbf0f9b29bc751834dfc7eea6e7))
- Updated ([`ad8bad0`](https://github.com/OpenG2P/agri-stack/commit/ad8bad08d53513a6f3134f07f8d629cae0e81f98))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: register model phase 1 as built (participants, entities first, partner corrections, cluster register, crop-change link, shared sample data); phase 2 scope; temporary IDs withdrawn ([`d37accb`](https://github.com/OpenG2P/agri-stack/commit/d37accbbd6e900a971856df28c533f6147cf5d50))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: register model decisions (trust per section, no plan certificates, typed participants, entities first, trust status vocabulary); temporary IDs open ([`a650dde`](https://github.com/OpenG2P/agri-stack/commit/a650dde998d058358b3d941fa205ed07d59df913))
- Fresh design thoughts ([`5770d19`](https://github.com/OpenG2P/agri-stack/commit/5770d1975975ec50a5616cb8b08fe98e58fd4afb))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: register vs activity register comparison; link from index, activity register and registry model ([`aaf5e96`](https://github.com/OpenG2P/agri-stack/commit/aaf5e96b35d433ada27f31e1a4429ea3ab9ab58a))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: geography and roll-ups, DCI crop-season and aggregate records, season windows, Observations alignment ([`831790d`](https://github.com/OpenG2P/agri-stack/commit/831790d48a0097cdbd1664096d604d85249d7586))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: activity registers listed with the other registers in the staff UI ([`281f676`](https://github.com/OpenG2P/agri-stack/commit/281f676957e206bb0bf354aafa923abb3a91e5b4))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: Observations alignment built; registries share data not code; farmer season summary ([`fa01fba`](https://github.com/OpenG2P/agri-stack/commit/fa01fbae43a9ddff2496c097c5060dbace83c8f5))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: compare with the Observations design; crop sown as its own registry or inside the Farmer Registry; keep "activity" ([`0419f30`](https://github.com/OpenG2P/agri-stack/commit/0419f3044d91f48cc68f7923fd42a0aaf420771d))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: Crop Sown code lists come from Master Data; update open items ([`d9258f5`](https://github.com/OpenG2P/agri-stack/commit/d9258f5ccb5ccc3a6867ff6a3756e796daf22171))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: note extension migration race in open items ([`575a301`](https://github.com/OpenG2P/agri-stack/commit/575a3017d038d25946c8b5d54fd24b2d159abb77))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: activity register as built; add Crop Sown Registry page; update open items ([`c968a77`](https://github.com/OpenG2P/agri-stack/commit/c968a772ea722f9b283bfcdf0552ff8d02b17c51))
- docs: remove implementation phasing and pilot order; keep to architecture and design ([`14b07b4`](https://github.com/OpenG2P/agri-stack/commit/14b07b4b858fe22a78cecdcce2dde517e77db591))
- docs: retitle as Agri Stack architecture; move docs out of data-sharing/ ([`029f6eb`](https://github.com/OpenG2P/agri-stack/commit/029f6eba69d4d071f9476bb078fcacc735efa5e8))
- Updated. ([`45eda2d`](https://github.com/OpenG2P/agri-stack/commit/45eda2dd2eb3deaf813c2df486daaf0e905fee39))
- Updated ([`b0f22cd`](https://github.com/OpenG2P/agri-stack/commit/b0f22cd1f1bc870649defcd683d6409fe5b3f2ed))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
