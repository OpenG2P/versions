# live-stock-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/live-stock-registry](https://github.com/OpenG2P/live-stock-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.2`](#v-0-0-0-develop-2) | 2026-11-26 | develop |  |

# Develop builds

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
