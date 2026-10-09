# agri-stack

_Published automatically._

**Repository:** [github.com/OpenG2P/agri-stack](https://github.com/OpenG2P/agri-stack) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.43`](#v-0-0-0-develop-43) | 2026-10-09 | develop |  |
| [`0.0.0-develop.42`](#v-0-0-0-develop-42) | 2026-10-09 | develop |  |
| [`0.0.0-develop.39`](#v-0-0-0-develop-39) | 2026-10-09 | develop |  |
| [`0.0.0-develop.36`](#v-0-0-0-develop-36) | 2026-10-09 | develop |  |
| [`0.0.0-develop.30`](#v-0-0-0-develop-30) | 2026-10-07 | develop |  |
| [`0.0.0-develop.29`](#v-0-0-0-develop-29) | 2026-10-07 | develop |  |
| [`0.0.0-develop.28`](#v-0-0-0-develop-28) | 2026-10-05 | develop |  |
| [`0.0.0-develop.27`](#v-0-0-0-develop-27) | 2026-10-05 | develop |  |
| [`0.0.0-develop.26`](#v-0-0-0-develop-26) | 2026-10-02 | develop |  |
| [`0.0.0-develop.23`](#v-0-0-0-develop-23) | 2026-10-02 | develop |  |
| [`0.0.0-develop.22`](#v-0-0-0-develop-22) | 2026-10-01 | develop |  |

# Develop builds

<a id="v-0-0-0-develop-43"></a>

## agri-stack — develop 0.0.0-develop.43 (2026-10-09)

_commit `1570399` · changes since 0.0.0-develop.42_
<!-- build:0.0.0-develop.43 revision:1570399f5ed1d5ab0ba627f137e454cce902e33e ts:1791537449 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.43](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.43.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite console: login redirect is an absolute URL on the console's public origin (forwarded host/proto) — a relative "/" sent users to IAM's own host (404) ([`1570399`](https://github.com/OpenG2P/agri-stack/commit/1570399f5ed1d5ab0ba627f137e454cce902e33e))

<a id="v-0-0-0-develop-42"></a>

## agri-stack — develop 0.0.0-develop.42 (2026-10-09)

_commit `09a540f` · changes since 0.0.0-develop.39_
<!-- build:0.0.0-develop.42 revision:09a540f1c9221fe7e8cf8a473bd96c6e0985dc1c ts:1791525195 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.42](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.42.tgz)

### Summary

- **Major:** Backend enhancements for composite review, including signature verification for call logs, batched writer implementation, and improved indexing for use-case names.
- Security improvements: Rejection of untraceable JSONPath at load, and enforcement of full grant for undeclared sources in requested_scopes.
- API stability: Updated iam-core to align with openg2p-fastapi-common, resolving startup crashes related to crypto imports.
- CI/build adjustments: Autoscaling disabled by default for the composite chart, now set to 1 replica, and various audit fixes applied.
- Console updates: Safe login redirect implemented, elimination of login loops, and enhancements to error screens and nullable activity fields.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite review fixes — backend: call log only for signature-verified calls, batched writer, capped counts, indexed use-case name, maintenance loop (advisory-locked create + daily purge, retried), untraceable JSONPath rejected at load, exchange requested_scopes keep the full grant for undeclared sources, subject-less queries not sent, full pages flagged, single-flight catalogue fetch, tests; console: next 16.4.0 + audit fixes, safe login redirect, no login loop, error screens, nullable activity fields, total_capped; chart: service-name helpers, iam-register hook cleanup and keycloakInit gate, postgres-init wait image, no tag defaults in questions; agri-exchange: portal links from baseDomain ([`09a540f`](https://github.com/OpenG2P/agri-stack/commit/09a540f1c9221fe7e8cf8a473bd96c6e0985dc1c))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite API image: iam-core from its develop line (CI-pinned SHA) to match openg2p-fastapi-common develop — iam-core 1.4.x imports openg2p_fastapi_common.crypto, which develop moved to utils.crypto (API crashed at start with the console on) ([`3c3b0d1`](https://github.com/OpenG2P/agri-stack/commit/3c3b0d12cac63e197f50b718b18cb9d2d51a2ed7))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite chart: autoscaling off by default (1 replica) ([`e0092a4`](https://github.com/OpenG2P/agri-stack/commit/e0092a465f6f67a298645868963a327091a0d016))

<a id="v-0-0-0-develop-39"></a>

## agri-stack — develop 0.0.0-develop.39 (2026-10-09)

_commit `2840c08` · changes since 0.0.0-develop.36_
<!-- build:0.0.0-develop.39 revision:2840c08180ea41ae0fae113c23d8c00e3d773ddc ts:1791520418 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.39](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.39.tgz)

### Summary

- Consolidation of scripts: Top-level scripts directory now includes e2e, partner test, partner kit, tests, and composite uninstall scripts, with a root .gitignore for their outputs.
- **Major:** Composite uninstall script enhancements: now includes console coverage, dropping the database and role, deleting IAM application rows while retaining Secrets, and implementing a late-hook sweep and in-progress Helm guard.
- Documentation updates: README now lists key directories (composite/, deploy/, scripts/) and clarifies the project name as "Agri Stack"; chart .helmignore prevents local overrides.yaml from being included in the package.

### Changes

- https://github.com/OpenG2P/agri-stack/actions/runs/37883991411 ([`2840c08`](https://github.com/OpenG2P/agri-stack/commit/2840c08180ea41ae0fae113c23d8c00e3d773ddc))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) scripts consolidated in top-level scripts/ (e2e, partner test, partner kit, tests, composite uninstall); root .gitignore for their outputs; README lists composite/, deploy/, scripts/ and says "Agri Stack"; chart .helmignore keeps the local overrides.yaml out of the package ([`d302be5`](https://github.com/OpenG2P/agri-stack/commit/d302be55c366ae6dc4734a3efe9dab9d685fcc23))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite: uninstall script covers the console — drops its DB and role, deletes its IAM application rows and kept Secrets, late-hook sweep and in-progress Helm guard (as the registry scripts); --keep-db / --keep-iam / --force ([`99bd006`](https://github.com/OpenG2P/agri-stack/commit/99bd006b008b851f65ed00b2d1140d4ed60b070b))

<a id="v-0-0-0-develop-36"></a>

## agri-stack — develop 0.0.0-develop.36 (2026-10-09)

_commit `126cd27` · changes since 0.0.0-develop.30_
<!-- build:0.0.0-develop.36 revision:126cd27a9d0c64cb33fa31a7f3a6400be0bcfbd8 ts:1791510445 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.36](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.36.tgz)

### Summary

- **Major:** Composite chart enhancements: console enabled by default, IAM registration as a Job, and derived hostnames/cookie domains from baseDomain.
- Composite data handling improvements: refined data scopes for use cases, ensuring consent grants required scopes, and registry scope catalogues are now signed.
- UI and API updates: read-only staff console with IAM login, Next.js UI integration, and partner_test.py now limited to public APIs with sample defaults.
- Enhanced error handling: fields from failed sources now return null instead of empty arrays or zeros, clarifying registry responses.
- CI and testing improvements: integration of agri-composite-ui in CI builds, and comprehensive end-to-end tests for registries across namespaces.
- Agri Exchange installation streamlined: helmfile now installs commons and agri-composite with pinned versions, and includes templated overrides for configuration.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite chart: console on by default (values + Rancher form); Agri Exchange bundle runs its IAM registration as a regular Job and derives console/IAM hostnames and cookie domain from baseDomain ([`126cd27`](https://github.com/OpenG2P/agri-stack/commit/126cd27a9d0c64cb33fa31a7f3a6400be0bcfbd8))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite: use cases fix their data scopes (required/optional per source; consent must grant required ones; exchange receipts carry only these); registry scope catalogues (signed); read-only staff console — admin API with IAM login (composite:view), call log in its own DB, Next.js UI on the MDS shell; chart console.enabled (UI, DB init, Keycloak client, IAM registration); CI builds agri-composite-ui; partner_test uses the use case's scopes; tests ([`bc7a2bc`](https://github.com/OpenG2P/agri-stack/commit/bc7a2bc1bacd97f09f238e95ebcca506cee1118d))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite: fields built from a failed source (denied/unavailable/error) are null, not [] / 0 — empty values now mean the registry answered "no record"; tests ([`93d48c7`](https://github.com/OpenG2P/agri-stack/commit/93d48c7ee62a964aed0e024dff64728fe556a5be))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite: partner_test.py — public APIs only; defaults to sample farmer FR-0007 (FAN 946053125409, openg2p-data ETH-IND-0007); PM admin API at pm-staff-portal.&lt;domain&gt;; CM AWE wait only when CM's AWE approval is on ([`c5bc3cf`](https://github.com/OpenG2P/agri-stack/commit/c5bc3cf5e696e2592334846608d1fe6d408d9b75))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite e2e: registries in other namespaces (--fr-namespace/--csr-namespace) — set up each registry's own PM/CM (exchange: composite key + agri-composite binding; passthrough: both keys + partner binding), check receipt trust, read each registry's DB in its namespace ([`272209a`](https://github.com/OpenG2P/agri-stack/commit/272209a211f6067ca6d5a10125aa46408a2cc1e7))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Agri Exchange install bundle (deploy/agri-exchange): helmfile installing commons, commons-services and agri-composite in order into one namespace with pinned chart versions; exchange overrides (Novu/Kafka UI off, slim commons-services with WebSub/AWE off, CM exchange role with the operator's signing key Secret, composite consent mode exchange and registry URLs) templated from a small operator values.yaml; README with helmfile and Rancher steps ([`4950eca`](https://github.com/OpenG2P/agri-stack/commit/4950eca75bd255aac7ab77134f80fb6b51ffb6f9))

<a id="v-0-0-0-develop-30"></a>

## agri-stack — develop 0.0.0-develop.30 (2026-10-07)

_commit `77a4a19` · changes since 0.0.0-develop.29_
<!-- build:0.0.0-develop.30 revision:77a4a19561de07005610ce97381ed3db5f9553ce ts:1791353814 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.30](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.30.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite: consent exchange mode (opt-in, default passthrough) — validate the partner consent at the exchange CM with issue_receipts and send each registry its own receipt; chart consent.mode/exchangeCmUrl with Rancher "Agri Stack exchange" group; tests ([`77a4a19`](https://github.com/OpenG2P/agri-stack/commit/77a4a19561de07005610ce97381ed3db5f9553ce))

<a id="v-0-0-0-develop-29"></a>

## agri-stack — develop 0.0.0-develop.29 (2026-10-07)

_commit `ba31974` · changes since 0.0.0-develop.28_
<!-- build:0.0.0-develop.29 revision:ba319741e9cfbf5d131ab4d25bfed271e730d046 ts:1791336410 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.29](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.29.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite: data scope catalogue is read with the signed POST /partner/data_scopes (comments) ([`ba31974`](https://github.com/OpenG2P/agri-stack/commit/ba319741e9cfbf5d131ab4d25bfed271e730d046))

<a id="v-0-0-0-develop-28"></a>

## agri-stack — develop 0.0.0-develop.28 (2026-10-05)

_commit `5aa87ad` · changes since 0.0.0-develop.27_
<!-- build:0.0.0-develop.28 revision:5aa87ad76c22942468a7761cef0f3be31599bda1 ts:1791172372 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.28](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.28.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) loan-profile: per-source timeout 10 s with no retry (a slow registry search was retried into a timeout), overall 25 s for farmer then crop sources; chart's embedded use case and engine test updated ([`5aa87ad`](https://github.com/OpenG2P/agri-stack/commit/5aa87ad76c22942468a7761cef0f3be31599bda1))

<a id="v-0-0-0-develop-27"></a>

## agri-stack — develop 0.0.0-develop.27 (2026-10-05)

_commit `297d36a` · changes since 0.0.0-develop.26_
<!-- build:0.0.0-develop.27 revision:297d36acec4c292c4424f8a7d91aaa224b74f25e ts:1791164483 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.27](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.27.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Composite: partner kit grants and loan-profile consent notes use registry data scope IDs (farmer-registry.farmer_identifiers carries the farmer ID the crop sources query by); tests ([`297d36a`](https://github.com/OpenG2P/agri-stack/commit/297d36acec4c292c4424f8a7d91aaa224b74f25e))

<a id="v-0-0-0-develop-26"></a>

## agri-stack — develop 0.0.0-develop.26 (2026-10-02)

_commit `3824d2d` · changes since 0.0.0-develop.23_
<!-- build:0.0.0-develop.26 revision:3824d2d245ec41230e11011a8e0f88d0c52e4f38 ts:1790907477 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.26](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.26.tgz)

### Summary

- Documentation overhaul: moved to docs.openg2p.org, removing local docs and READMEs, with chart readme pointing to the new location.
- Testing enhancements: composite end-to-end tests now save full run logs alongside response JSON in git-ignored scripts/out.
- Feature updates: added a TODO for geo dropdowns on registration forms, planning to default sync on and read levels from Master Data at runtime.

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) Docs moved to docs.openg2p.org (Open Agri Stack); remove docs/, READMEs and chart readme point there ([`3824d2d`](https://github.com/OpenG2P/agri-stack/commit/3824d2d245ec41230e11011a8e0f88d0c52e4f38))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) composite e2e: save the full run log next to the response JSON in git-ignored scripts/out/ ([`19e2868`](https://github.com/OpenG2P/agri-stack/commit/19e2868ccf4ffc7ef05f6e9bdce1046cb30d6832))
- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) docs: TODO for geo dropdowns on register forms (default the sync on, later read levels from Master Data at run time) ([`223a3d2`](https://github.com/OpenG2P/agri-stack/commit/223a3d2ebb4ae56c31ceb636a117a5cbd9abb4a2))

<a id="v-0-0-0-develop-23"></a>

## agri-stack — develop 0.0.0-develop.23 (2026-10-02)

_commit `a27df2b` · changes since 0.0.0-develop.22_
<!-- build:0.0.0-develop.23 revision:a27df2ba4a9ae7590fb131a8ef1da233526a5ec2 ts:1790868230 -->

**Chart:** [openg2p-agri-composite 0.0.0-develop.23](https://openg2p.github.io/openg2p-helm/openg2p-agri-composite-0.0.0-develop.23.tgz)

### Changes

- [G2P-5719](https://openg2p.atlassian.net/browse/G2P-5719) CI: build and publish only when composite/ changes, not on docs-only pushes ([`a27df2b`](https://github.com/OpenG2P/agri-stack/commit/a27df2ba4a9ae7590fb131a8ef1da233526a5ec2))

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
