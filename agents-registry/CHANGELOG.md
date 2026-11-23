# agents-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/agents-registry](https://github.com/OpenG2P/agents-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.2`](#v-0-0-0-develop-2) | 2026-11-23 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-2"></a>

## agents-registry — develop 0.0.0-develop.2 (2026-11-23)

_commit `bbcc895` · changes since the start (showing the latest 20 commits)_
<!-- build:0.0.0-develop.2 revision:bbcc895b4a87a5fd73a63a9766c58547b952c697 ts:1795401259 -->

**Chart:** [openg2p-agents-registry 0.0.0-develop.2](https://openg2p.github.io/openg2p-helm/openg2p-agents-registry-0.0.0-develop.2.tgz)

### Summary

- **Major:** Introduction of the Agents Registry feature, including a comprehensive reference for agents serving farmers, with an 8-digit Agent ID, personal details, employment status, and service qualifications.
- Enhanced functionality with an AgentTraining activity register that tracks trainings and certifications, providing a per-agent summary and reporting views.
- Implementation of data integrity measures, including duplicate checks and AWE approvals for agent entries.
- Initial setup includes seed SQL generated from scripts, sample agents, and training data, along with visual reporting elements like charts and images.
- Comprehensive testing framework established to ensure reliability and performance of the new features.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Agents Registry: reference registry of agents who serve farmers — Agent register (8-digit Agent ID, person, national ID, contact, employment, current assignment, service status; specializations and qualifications), AWE approvals, duplicate check; AgentTraining activity register (trainings, certifications, per-agent summary); reporting views; seed SQL generated from scripts/agents_definitions.py; sample agents from the country pack and sample trainings; images, chart, CI; tests ([`bbcc895`](https://github.com/OpenG2P/agents-registry/commit/bbcc895b4a87a5fd73a63a9766c58547b952c697))
- Initial commit ([`7c165be`](https://github.com/OpenG2P/agents-registry/commit/7c165be208f1b271531fb4716a8d3162180fc7f0))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
