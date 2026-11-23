# agents-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/agents-registry](https://github.com/OpenG2P/agents-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.5`](#v-0-0-0-develop-5) | 2026-11-23 | develop |  |
| [`0.0.0-develop.4`](#v-0-0-0-develop-4) | 2026-11-23 | develop |  |
| [`0.0.0-develop.2`](#v-0-0-0-develop-2) | 2026-11-23 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-5"></a>

## agents-registry — develop 0.0.0-develop.5 (2026-11-23)

_commit `91023a6` · changes since 0.0.0-develop.4_
<!-- build:0.0.0-develop.5 revision:91023a6ba30f9e41b9b0fb0ee768a6e0386bc51c ts:1795412030 -->

**Chart:** [openg2p-agents-registry 0.0.0-develop.5](https://openg2p.github.io/openg2p-helm/openg2p-agents-registry-0.0.0-develop.5.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Registry platform 0.0.0-develop.845 (fastapi-common JWT classes; Partner API and Consent form groups) ([`91023a6`](https://github.com/OpenG2P/agents-registry/commit/91023a6ba30f9e41b9b0fb0ee768a6e0386bc51c))

<a id="v-0-0-0-develop-4"></a>

## agents-registry — develop 0.0.0-develop.4 (2026-11-23)

_commit `519423f` · changes since 0.0.0-develop.2_
<!-- build:0.0.0-develop.4 revision:519423fa2f60e8f15c2b91aecfc7a3b50121f952 ts:1795404144 -->

**Chart:** [openg2p-agents-registry 0.0.0-develop.4](https://openg2p.github.io/openg2p-helm/openg2p-agents-registry-0.0.0-develop.4.tgz)

### Summary

- New feature implementation: integrated VC issuance with the agent-portal-api image, including agent_vc_view and OpenG2PAgentCredential, alongside updated card design.
- Configuration updates: disabled consent paths and data-scope catalogue for the beneficiary portal, with registry connector defaults adjusted accordingly.
- Documentation enhancement: updated READMEs to link to the official documentation on docs.openg2p.org.
- Testing improvements: added new tests to ensure functionality and reliability of the Agents Registry features.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Agents Registry: consent paths and data-scope catalogue off, beneficiary portal off, registry connector defaults; VC issuance wired (agent-portal-api image, agent_vc_view, OpenG2PAgentCredential, card design; registrant-authentication flag kept across re-seeds); tests ([`519423f`](https://github.com/OpenG2P/agents-registry/commit/519423fa2f60e8f15c2b91aecfc7a3b50121f952))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Agents Registry READMEs point to the documentation on docs.openg2p.org ([`425bfb2`](https://github.com/OpenG2P/agents-registry/commit/425bfb289a24cc061bba87cdf9a7cf0c8b3269a8))

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
