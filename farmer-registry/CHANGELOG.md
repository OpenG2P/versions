# farmer-registry

_Published automatically._

**Repository:** [github.com/OpenG2P/farmer-registry](https://github.com/OpenG2P/farmer-registry) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`0.0.0-develop.198`](#v-0-0-0-develop-198) | 2026-09-01 | develop |  |
| [`1.2.1-rc.159`](#v-1-2-1-rc-159) | 2026-08-28 | release candidate |  |
| [`0.0.0-develop.196`](#v-0-0-0-develop-196) | 2026-08-28 | develop | **Intermediate Stable Version**. Installs fine after moving back to GitHub. Has Verifiable Credentials (Basic) integrated. Compatible with 0.0.0-develop.235 of commons. |

# Release candidates

<a id="v-1-2-1-rc-159"></a>

## farmer-registry 1.2.1-rc.159 — 2026-08-28

_commit `448e66e` · changes since 1.2.0_
<!-- build:1.2.1-rc.159 revision:448e66e023a1dfc38f17486804b8a7fdb711ebd6 ts:1787898576 -->

**Chart:** [openg2p-farmer-registry 1.2.1-rc.159](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-1.2.1-rc.159.tgz)

### Summary

- **Major:** CI transition to GitLab with removal of GitHub Actions for build and publish processes.
- Docker updates: modified Dockerfiles and Chart.yaml to utilize GitLab registry paths and version 1.2.0-rc.419.
- Data model changes: changed land_size field type from string to float, refactored enums, and updated SQL insert statements for crops, livestock, and household sections.
- Record management: reduced record seeding count from 50 to 25 and added seeding functionality for data insertion via intake forms.
- Domain simplification: removed G2PRegisterDomainFactory and related files to streamline the domain registration process.
- Functional enhancements: enabled functional_id generation for farmers and households, and added a script for uploading farmer data and images to MinIO.
- Schema adjustments: updated UI schema and corrected field names in household information sections.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Fix the base images: they come from registry-platform, not this repo ([`448e66e`](https://github.com/OpenG2P/farmer-registry/commit/448e66e023a1dfc38f17486804b8a7fdb711ebd6))
- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Align the 1.2 release line with GitHub ([`b740b81`](https://github.com/OpenG2P/farmer-registry/commit/b740b8138e502451b11bb2b5cd026dbb2dcf74e9))
- [G2P-5576](https://openg2p.atlassian.net/browse/G2P-5576) Refactor enums and update source of income references ([`6dff669`](https://github.com/OpenG2P/farmer-registry/commit/6dff669117c19d9dc6eb84a3b23fd8643fb8c85d))
- [G2P-5574](https://openg2p.atlassian.net/browse/G2P-5574) Reduce record seeding count from 50 to 25 ([`d33c743`](https://github.com/OpenG2P/farmer-registry/commit/d33c743097d2acd59a25f38199e3c3ba7daaf200))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update Dockerfiles and Chart.yaml to use GitLab registry paths ([`212e9e1`](https://github.com/OpenG2P/farmer-registry/commit/212e9e18e588fc59ba7971ab5fbdea4168d21761))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Update Dockerfiles and Chart.yaml to version 1.2.0-rc.419 ([`7db5915`](https://github.com/OpenG2P/farmer-registry/commit/7db5915d453697b102133539c5643b2bbe0303be))
- [G2P-5572](https://openg2p.atlassian.net/browse/G2P-5572) Add seeding to insert data via intake form ([`8dd6d6a`](https://github.com/OpenG2P/farmer-registry/commit/8dd6d6acbcd37be76cd024d1295b2b3f4f09da7c))
- Change in Ui schema and domain translation ([`75f1c68`](https://github.com/OpenG2P/farmer-registry/commit/75f1c685deccc29c8b3d137164ffe35e644c1302))
- [G2P-5543](https://openg2p.atlassian.net/browse/G2P-5543) Add script to upload farmer data and images to MinIO ([`81610dd`](https://github.com/OpenG2P/farmer-registry/commit/81610dd3ffad426f1b9d59a4ee012b8aeffa3ecf))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Enable functional_id generation for farmer and household ([`99cf568`](https://github.com/OpenG2P/farmer-registry/commit/99cf5686d7e32376143ce9b34c9ad1e65ddaf4a5))
- [G2P-5538](https://openg2p.atlassian.net/browse/G2P-5538) Delete attribute sql files ([`ddb078f`](https://github.com/OpenG2P/farmer-registry/commit/ddb078f07fb67d41bf746da66c87857f37f6e614))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): update SQL insert statements for crops, livestocks, and farminputs sections ([`6c6dff7`](https://github.com/OpenG2P/farmer-registry/commit/6c6dff730553ca98dba1aa14482b267540936604))
- [G2P-5480](https://openg2p.atlassian.net/browse/G2P-5480) Change land_size field type from string to float in land model and schema ([`161821a`](https://github.com/OpenG2P/farmer-registry/commit/161821a2b04d18095df90277d5f7404b1994cca0))
- [G2P-5524](https://openg2p.atlassian.net/browse/G2P-5524) refactor: remove G2PRegisterDomainFactory and related files to streamline domain registration process ([`ef21f34`](https://github.com/OpenG2P/farmer-registry/commit/ef21f346f57e7a358f18b5109cc8fcaf1649ebc4))
- [G2P-5519](https://openg2p.atlassian.net/browse/G2P-5519) remove redundant repository entries in values.yaml for openg2p-farmer-registry ([`9d9ba7b`](https://github.com/OpenG2P/farmer-registry/commit/9d9ba7b48356181140821ef3ba9d1ea076ce429e))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): Correct field names in household information section ([`675cf2e`](https://github.com/OpenG2P/farmer-registry/commit/675cf2e87eb1bfc8a057f89d0a73ff821857946f))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`37c1731`](https://github.com/OpenG2P/farmer-registry/commit/37c17318828fbcb4274b33e2eb7b649ee77f5f15))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: enhance SQL insert statements for g2p_register_sections with additional metadata and widget configurations for livestock and household member sections ([`ab6c0db`](https://github.com/OpenG2P/farmer-registry/commit/ab6c0db73d01620066ba6d3c745b219f42cb230b))
- [G2P-5335](https://openg2p.atlassian.net/browse/G2P-5335) Switch CI to GitLab (.gitlab-ci.yml); drop GitHub Actions build/publish ([`1062700`](https://github.com/OpenG2P/farmer-registry/commit/1062700737b8129d66fcc363c7d3809863d0cefb))

# Develop builds

<a id="v-0-0-0-develop-198"></a>

## farmer-registry — develop 0.0.0-develop.198 (2026-09-01)

_commit `a68e552` · changes since 0.0.0-develop.196_
<!-- build:0.0.0-develop.198 revision:a68e552aa9bc35a24975f3d57ba7acf196b23fd5 ts:1788224900 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.198](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.198.tgz)

### Summary

- **Major:** Upgraded RP version to 0.0.0-develop.424, introducing significant changes in the development branch.
- New feature: Added a credential-verification switch to enhance security and control over user authentication processes.

### Changes

- Bumped up RP version to 0.0.0-develop.424 ([`a68e552`](https://github.com/OpenG2P/farmer-registry/commit/a68e552aa9bc35a24975f3d57ba7acf196b23fd5))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add the credential-verification switch ([`1cad544`](https://github.com/OpenG2P/farmer-registry/commit/1cad54408cf651a9d31768e3a1e98a0df2512e59))

<a id="v-0-0-0-develop-196"></a>

## farmer-registry — develop 0.0.0-develop.196 (2026-08-28)

> **Note** — **Intermediate Stable Version**. Installs fine after moving back to GitHub. Has Verifiable Credentials (Basic) integrated. Compatible with 0.0.0-develop.235 of commons.

_commit `07f0237` · changes since 1.3.0_
<!-- build:0.0.0-develop.196 revision:07f02374a8d7d6de89c0261f785a0740c4f16818 ts:1787884394 -->

**Chart:** [openg2p-farmer-registry 0.0.0-develop.196](https://openg2p.github.io/openg2p-helm/openg2p-farmer-registry-0.0.0-develop.196.tgz)

### Summary

- **Major:** Migration to GitLab for the farmer registry repository, with GitHub build/publish disabled.
- Version updates: Incremented RP version multiple times, culminating in 0.0.0-develop.417.
- Feature enhancements: Enabled VC issuance and agent portal by default, added farmer credential issuance behind a disabled switch, and shipped claim-169 QR config requiring registrant authentication.
- Data handling improvements: Normalised foundational ID, fixed full name spacing in VC views, and seeded the pack's real birth date instead of a default.
- Reporting updates: Declared scores against both farmer and household, generated fr_rpt_crop from declarations, and refreshed reporting views on a schedule.
- Configuration adjustments: Created VC card ConfigMap on agent portal deployment and corrected field names in household information.
- Cleanup: Removed obsolete performance templates and dropped duplicated VC questions inherited from the registry subchart.

### Changes

- [G2P-5605](https://openg2p.atlassian.net/browse/G2P-5605) Build and publish on GitHub again ([`07f0237`](https://github.com/OpenG2P/farmer-registry/commit/07f02374a8d7d6de89c0261f785a0740c4f16818))
- Bumped up RP version to 0.0.0-develop.417 ([`777b647`](https://github.com/OpenG2P/farmer-registry/commit/777b647680dcce77e351c4bea6a0eebf88387623))
- Bumped up RP version to 0.0.0-develop.415 ([`2855ab9`](https://github.com/OpenG2P/farmer-registry/commit/2855ab96152250e47cc8554c2496172b2ad8816f))
- Bumped up RP version to 0.0.0-develop.414 ([`9ce672b`](https://github.com/OpenG2P/farmer-registry/commit/9ce672bded8ff68a18e77df2f91c92726e329eeb))
- Bumped up RP version to 0.0.0-develop.411 ([`2b0ed75`](https://github.com/OpenG2P/farmer-registry/commit/2b0ed755c6d3457ca85679cba7fc74196570e857))
- Bumped up RP version to 0.0.0-develop.409 ([`605343d`](https://github.com/OpenG2P/farmer-registry/commit/605343dae8893675263558be8775978424027260))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Build a farmer agent-portal-api image so it maps the farmer register model. Bumped up RP version. ([`e0dae0b`](https://github.com/OpenG2P/farmer-registry/commit/e0dae0bb54567b257263414ea49501c441ab2e4b))
- Bumped up RP version to 0.0.0-develop.408. ([`dd71272`](https://github.com/OpenG2P/farmer-registry/commit/dd7127209ae96e8186d1f83ea05f46903394d5a5))
- Bumped up RP version to 0.0.0-develop.406 ([`8022dfc`](https://github.com/OpenG2P/farmer-registry/commit/8022dfcbcb92bd39b81682a6024997b3274004a1))
- Bumped up RP version to 0.0.0-develop.404 ([`6e3a1f8`](https://github.com/OpenG2P/farmer-registry/commit/6e3a1f8ad8348e6cb082aa15b8b111306ec7ed87))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Point master data DB credentials at the renamed secret ([`ffcc9e7`](https://github.com/OpenG2P/farmer-registry/commit/ffcc9e7f39b441d6e532b2199275427a4ffa1f16))
- Bumped up RP version to 0.0.0-develop.403 ([`9c608d9`](https://github.com/OpenG2P/farmer-registry/commit/9c608d91cdce3713f79c40220fd738c2d3426f60))
- Bumped up RP version to 0.0.0-develop.402 ([`ffb2c75`](https://github.com/OpenG2P/farmer-registry/commit/ffb2c759bf707fd02b6f760f9839eab21e8f653c))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Ship the claim-169 QR config and require registrant authentication ([`acecdce`](https://github.com/OpenG2P/farmer-registry/commit/acecdcedc1261127d012eaca9a5268feaa849e58))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable VC issuance by default ([`7484b69`](https://github.com/OpenG2P/farmer-registry/commit/7484b69721348a1dc415d9a9e1a28b74ee4edd1f))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Normalise foundational ID and fix full name spacing in the VC view ([`f6d4c53`](https://github.com/OpenG2P/farmer-registry/commit/f6d4c53dea0db69353e9493117ec1b431bc32c13))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Fix full name spacing in the farmer VC view ([`fbf66e2`](https://github.com/OpenG2P/farmer-registry/commit/fbf66e28522d5981bf82a0ad99478f7846682f42))
- Bumped up RP version to 0.0.0-develop.392 ([`4196dd6`](https://github.com/OpenG2P/farmer-registry/commit/4196dd6d0c95e79c00e14b5afd04557003f0dcd3))
- Bumped up RP version to 0.0.0-develop.391 ([`1762516`](https://github.com/OpenG2P/farmer-registry/commit/1762516054f3fc491d42cb2e885819f4f99dddf7))
- [G2P-5554](https://openg2p.atlassian.net/browse/G2P-5554) Seed the pack's real birth date instead of inventing 1 January. The pack carried only a year, so every sample farmer in the country shared a birthday; older packs still fall back, since a date column cannot hold a year. ([`a74feca`](https://github.com/OpenG2P/farmer-registry/commit/a74fecacc096f7a06ff97c70dc951e2545ec7540))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Create the VC card ConfigMap whenever the agent portal is deployed ([`94abb14`](https://github.com/OpenG2P/farmer-registry/commit/94abb142887918217bf503ad12eabe3e0555d1d7))
- Bumped up RP version to 0.0.0-develop.389 ([`1b1a77b`](https://github.com/OpenG2P/farmer-registry/commit/1b1a77b3e9612b95e9f5f79247c733b42cd81c61))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Enable the agent portal by default ([`ca4d6ee`](https://github.com/OpenG2P/farmer-registry/commit/ca4d6ee1061b1cc59874c5edf0b33f04b1882c42))
- Bumped up RP version to 0.0.0-develop.388 ([`dfe77b7`](https://github.com/OpenG2P/farmer-registry/commit/dfe77b79d88e9bb50b55ffea5fbb6309316e11f1))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Drop duplicated VC questions inherited from the registry subchart. Bumped up RP version. ([`a29871f`](https://github.com/OpenG2P/farmer-registry/commit/a29871fe6a6052c530afa250176172a7e3ee0955))
- [G2P-4929](https://openg2p.atlassian.net/browse/G2P-4929) Add farmer credential issuance behind a disabled-by-default switch ([`95e4214`](https://github.com/OpenG2P/farmer-registry/commit/95e42143af43a28e72b33f6c4b7855adefd5d415))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402): Correct field names in household information section ([`8599e27`](https://github.com/OpenG2P/farmer-registry/commit/8599e272b4ff53ece192c92f60f6eca9cd4fb16a))
- Bumped up RP version to 0.0.0-develop.384 ([`98180a1`](https://github.com/OpenG2P/farmer-registry/commit/98180a19c65cec2c7bc486a44c9dbc5a2f6d0a97))
- Minor correction in helm comments. ([`835646d`](https://github.com/OpenG2P/farmer-registry/commit/835646d64ea4220110d6b6b6f1171faff3b4c2cb))
- Add seed manifest generation and remove obsolete performance templates ([`bee2c80`](https://github.com/OpenG2P/farmer-registry/commit/bee2c80bda0d7c178d97c2c177c5db7250ea12ab))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) update: modify SQL insert statements for g2p_register_sections and registry_languages ([`b2cda40`](https://github.com/OpenG2P/farmer-registry/commit/b2cda40ae3ff83f6b189a43fd8c160bed6dda398))
- Bumped up RP version to 0.0.0-develop.383 ([`ec8828c`](https://github.com/OpenG2P/farmer-registry/commit/ec8828c439ff33ac65bfb502bdb3bad5358c14d1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare score against both farmer and household. A single install carries both — the bulk generator attaches scores to farmers and the sample loader to households, 5,671 and 6 on a reference install — so naming one parent silently stripped the id and the geography from every row of the other. ([`40556c9`](https://github.com/OpenG2P/farmer-registry/commit/40556c9a6b4ea4f0791f3a2e30a8fbaa428c85ef))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate fr_rpt_crop from declarations instead of hand-written SQL. Verified byte-identical to the previous definition across all seventeen shared columns and 757 rows before the SQL was removed; it keeps its materialization and indexes, and additionally carries the geo pcodes and workflow columns the hand-written version omitted. ([`699b3a2`](https://github.com/OpenG2P/farmer-registry/commit/699b3a283105c25a82b7c87608afb18a1d28a61f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Declare the household member age bands, matching fr_rpt_farmer's edges. The generator derives an age wherever it withholds a birth date, but where the bands fall is policy, and defining them twice with different edges is how two charts come to disagree about how many people are under 25. ([`6daa47a`](https://github.com/OpenG2P/farmer-registry/commit/6daa47af0c0b0abd14b6b4b701db197ac6fd2839))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the mechanical reporting views from the platform generator. reporting.yaml declares the entity tree, names farmer/land/crop as hand-written and marks the cooperative name columns as organisations rather than people; the generated ten add livestock, inputs, membership, scores, households, members, change requests, record history and geo_levels, which used to be derived from registered rows and so was empty on a production install. ([`11e3b8b`](https://github.com/OpenG2P/farmer-registry/commit/11e3b8beb7368af5e1dbf8bb6810c6ef08238a18))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Refresh the reporting views on a schedule, instead of relying on Insights to do it. They are materialized, so they held whatever the install produced and every farmer registered afterwards was invisible with no error anywhere; a CronJob now rebuilds them in dependency order resolved from pg_depend, on analytics.reportingViews.refreshSchedule. ([`8f93c33`](https://github.com/OpenG2P/farmer-registry/commit/8f93c337cbc07bcef9de94f12633572297c92e9f))
- [G2P-5402](https://openg2p.atlassian.net/browse/G2P-5402) fix: correct ui configuration for multiple sections and add dedicated parent lookup sections for crop intake and crop register ([`2f172d4`](https://github.com/OpenG2P/farmer-registry/commit/2f172d4848fecc02c08f9c5a9e83edb76888ba53))
- Moved to GitLab: openg2p/registry/farmer-registry (read-only; build/publish disabled) ([`fab0037`](https://github.com/OpenG2P/farmer-registry/commit/fab003727dda0013ca27f315dd967537756b6171))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
