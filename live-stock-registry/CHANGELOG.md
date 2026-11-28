# live-stock-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/live-stock-registry](https://github.com/OpenG2P/live-stock-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.5`](#v-0-0-0-develop-5) | 2026-11-28 | develop |  |
| [`0.0.0-develop.4`](#v-0-0-0-develop-4) | 2026-11-26 | develop |  |
| [`0.0.0-develop.2`](#v-0-0-0-develop-2) | 2026-11-26 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-5"></a>

## live-stock-registry — develop 0.0.0-develop.5 (2026-11-28)

_commit `77f787a` · changes since 0.0.0-develop.4_
<!-- build:0.0.0-develop.5 revision:77f787a3b26ecfe3ff7e10d3e9498e1c620bfb46 ts:1795831275 -->

**Chart:** [openg2p-livestock-registry 0.0.0-develop.5](https://openg2p.github.io/openg2p-helm/openg2p-livestock-registry-0.0.0-develop.5.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Registry platform develop.858 (DCI search at /dci/registry/sync/search again; consent subject fields per register) ([`77f787a`](https://github.com/OpenG2P/live-stock-registry/commit/77f787a3b26ecfe3ff7e10d3e9498e1c620bfb46))

<a id="v-0-0-0-develop-4"></a>

## live-stock-registry — develop 0.0.0-develop.4 (2026-11-26)

_commit `5747ca8` · changes since 0.0.0-develop.2_
<!-- build:0.0.0-develop.4 revision:5747ca802fd268e231e9e8b4c8f94c01f6e62853 ts:1795692291 -->

**Chart:** [openg2p-livestock-registry 0.0.0-develop.4](https://openg2p.github.io/openg2p-helm/openg2p-livestock-registry-0.0.0-develop.4.tgz)

### Summary

- Data handling enhancement: Sample animals now read directly from `samples/animals.json`, aligning with the Farmer Registry's sample herds, improving consistency in animal code test runs.
- Reporting improvements: Default Superset dashboards for Livestock Overview, Vaccination and Animal Health, and Sales and Deaths are now included, with the bundle managed via `scripts/build_dashboards.py` and deployed as a ConfigMap, enhancing reporting capabilities.
- Cleanup functionality: Uninstalling the application now removes the release's dashboards, ensuring a cleaner environment post-uninstallation.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Sample animals read from the pack's samples/animals.json (shared with the Farmer Registry's sample herds) instead of being derived in the loader; animal codes test runs in checks ([`5747ca8`](https://github.com/OpenG2P/live-stock-registry/commit/5747ca802fd268e231e9e8b4c8f94c01f6e62853))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Sample Superset dashboards, loaded by default: Livestock Overview, Vaccination and Animal Health, Sales and Deaths on the reporting views (bundle built by scripts/build_dashboards.py, shipped as a ConfigMap for the platform's dashboards Job); occurred_month on lsr_rpt_event; uninstall removes the release's dashboards; tests ([`20ef13f`](https://github.com/OpenG2P/live-stock-registry/commit/20ef13f0853c93332c4a26b46616f31633780a92))

<a id="v-0-0-0-develop-2"></a>

## live-stock-registry — develop 0.0.0-develop.2 (2026-11-26)

_commit `e03d487` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.2 revision:e03d4879be37c3b845570a653f7f274dbba38bc4 ts:1795684451 -->

**Chart:** [openg2p-livestock-registry 0.0.0-develop.2](https://openg2p.github.io/openg2p-helm/openg2p-livestock-registry-0.0.0-develop.2.tgz)

### Summary

- **Major:** Introduction of the Livestock Registry feature, including comprehensive animal and veterinarian registers with unique IDs, activity tracking, and consent-based data scopes.
- Enhanced reporting capabilities with new views and visualizations for livestock activities.
- Implementation of a staff-ui wrapper to streamline user interactions within the Livestock Registry.
- Addition of sample data for veterinarians and animals, including images and charts, to facilitate testing and demonstration.
- Comprehensive testing suite established to ensure functionality and reliability of the new features.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Livestock Registry: Animal register (10-digit Animal ID, owner's Farmer ID and national ID, AWE approvals), Veterinarian register (8-digit Vet ID), LivestockEvent activity register (born, vaccinated, treated, sold, died; each animal's current state); data scopes and DCI output with consent; reporting views; Livestock Registry Theme; staff-ui wrapper; sample vets and animals; images, chart, CI; tests ([`e03d487`](https://github.com/OpenG2P/live-stock-registry/commit/e03d4879be37c3b845570a653f7f274dbba38bc4))
- Initial commit ([`39ce403`](https://github.com/OpenG2P/live-stock-registry/commit/39ce4033ebb5e648daee66c67ee1d5df045e877b))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
