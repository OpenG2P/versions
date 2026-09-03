# mowsa-nsr

_Published automatically._

**Repository:** [github.com/OpenG2P/mowsa-nsr](https://github.com/OpenG2P/mowsa-nsr) · **Container images:** [Container Registry](https://hub.docker.com/u/openg2p)

| Version | Date | Type | Notes |
| --- | --- | --- | --- |
| [`1.2.0-rc.301`](#v-1-2-0-rc-301) | 2026-09-03 | release candidate |  |
| [`1.2.0-rc.300`](#v-1-2-0-rc-300) | 2026-09-02 | release candidate |  |
| [`1.2.0-rc.299`](#v-1-2-0-rc-299) | 2026-09-02 | release candidate |  |
| [`1.2.0-rc.298`](#v-1-2-0-rc-298) | 2026-09-02 | release candidate |  |
| [`1.2.0-rc.297`](#v-1-2-0-rc-297) | 2026-09-01 | release candidate |  |

# Release candidates

<a id="v-1-2-0-rc-301"></a>

## mowsa-nsr 1.2.0-rc.301 — 2026-09-03

_commit `ce11c7c` · changes since 1.2.0-rc.300_
<!-- build:1.2.0-rc.301 revision:ce11c7c202e5aa1ac6aa2472130bee89c1df9021 ts:1788416986 -->

**Chart:** [mowsa-nsr 1.2.0-rc.301](https://openg2p.github.io/openg2p-helm/mowsa-nsr-1.2.0-rc.301.tgz)

### Changes

- Add image pull secrets for private Docker Hub images in Helm chart values.yaml ([`ce11c7c`](https://github.com/OpenG2P/mowsa-nsr/commit/ce11c7c202e5aa1ac6aa2472130bee89c1df9021))

<a id="v-1-2-0-rc-300"></a>

## mowsa-nsr 1.2.0-rc.300 — 2026-09-02

_commit `5b8dc42` · changes since 1.2.0-rc.299_
<!-- build:1.2.0-rc.300 revision:5b8dc423e305ef6d6510644f970895db791055b2 ts:1788324948 -->

**Chart:** [mowsa-nsr 1.2.0-rc.300](https://openg2p.github.io/openg2p-helm/mowsa-nsr-1.2.0-rc.300.tgz)

### Changes

- Enhance Celery Docker image with NSR-specific run_celery.py and worker patches. The Dockerfile now includes the new script, which implements hot-patching for partner auto-approval in change requests and intake submissions, along with AWE bearer token handling from Keycloak. ([`5b8dc42`](https://github.com/OpenG2P/mowsa-nsr/commit/5b8dc423e305ef6d6510644f970895db791055b2))

<a id="v-1-2-0-rc-299"></a>

## mowsa-nsr 1.2.0-rc.299 — 2026-09-02

_commit `1ab5b1b` · changes since 1.2.0-rc.298_
<!-- build:1.2.0-rc.299 revision:1ab5b1b7a488f2af5d9058ed709a44387c61a26b ts:1788323919 -->

**Chart:** [mowsa-nsr 1.2.0-rc.299](https://openg2p.github.io/openg2p-helm/mowsa-nsr-1.2.0-rc.299.tgz)

### Changes

- Update Helm chart version to 1.2.0 and align dependency version for openg2p-registry ([`1ab5b1b`](https://github.com/OpenG2P/mowsa-nsr/commit/1ab5b1b7a488f2af5d9058ed709a44387c61a26b))

<a id="v-1-2-0-rc-298"></a>

## mowsa-nsr 1.2.0-rc.298 — 2026-09-02

_commit `8b9a1c2` · changes since 1.2.0-rc.297_
<!-- build:1.2.0-rc.298 revision:8b9a1c2e88deef3911081a2dd4b94a21fcab8d52 ts:1788323342 -->

**Chart:** [mowsa-nsr 1.2.0-rc.298](https://openg2p.github.io/openg2p-helm/mowsa-nsr-1.2.0-rc.298.tgz)

### Changes

- [G2P-5630](https://openg2p.atlassian.net/browse/G2P-5630): Rename docker of staff-api to staff-portal-api to align with older images ([`8b9a1c2`](https://github.com/OpenG2P/mowsa-nsr/commit/8b9a1c2e88deef3911081a2dd4b94a21fcab8d52))

<a id="v-1-2-0-rc-297"></a>

## mowsa-nsr 1.2.0-rc.297 — 2026-09-01

_commit `d46c155` · changes since v1.0.0_
<!-- build:1.2.0-rc.297 revision:d46c1553dab3caaea73f7b6f635082808466c7ea ts:1788274661 -->

**Chart:** [mowsa-nsr 1.2.0-rc.297](https://openg2p.github.io/openg2p-helm/mowsa-nsr-1.2.0-rc.297.tgz)

### Summary

_AI summary unavailable — re-run the workflow with `changelog_regenerate=1.2.0-rc.297` to generate it._

### Changes

- Just to trigger a build. No change otherwise ([`c3ebc6e`](https://github.com/OpenG2P/mowsa-nsr/commit/c3ebc6e21744dd173782f7fae76c6432916af886))
- Just to trigger a build. No change otherwise ([`0e21987`](https://github.com/OpenG2P/mowsa-nsr/commit/0e219879c7bbe72915dd7464b338100be5fda711))
- Update version references in CI, Dockerfiles, and Helm charts to 1.1.3, v1.1.7, and v1.3.0 for consistency across the project. ([`ab10486`](https://github.com/OpenG2P/mowsa-nsr/commit/ab10486147a8c289fa3bb1d14525d9103e5aa807))
- Just to trigger a build. No change otherwise ([`c2b8e63`](https://github.com/OpenG2P/mowsa-nsr/commit/c2b8e6338b6105c142f64ae3c7cda7cf48a0087b))
- Revert "Update version references in CI and Dockerfiles to 1.1.3, v1.1.7, and v1.3.0" ([`6c2064c`](https://github.com/OpenG2P/mowsa-nsr/commit/6c2064c9c53ea48d332a22c47b380ac085e9958c))
- Add ALLOW_FORK_PIPELINE variable to CI configuration ([`f909ab6`](https://github.com/OpenG2P/mowsa-nsr/commit/f909ab6e371ab5f5b4843e1fd5033c1bf10c64ae))
- Add PIPELINE_NAMESPACE variable to CI configuration ([`a78f778`](https://github.com/OpenG2P/mowsa-nsr/commit/a78f778395917a764bd4846c20517af8e79b497e))
- Just to trigger a build. No change otherwise ([`053c766`](https://github.com/OpenG2P/mowsa-nsr/commit/053c766070c418a657903db72b41fe1897538353))
- Just to trigger a build. No change otherwise ([`9ef5a7f`](https://github.com/OpenG2P/mowsa-nsr/commit/9ef5a7f345745eff3167b107a4834c8aaa062294))
- Update version references in CI and Dockerfiles to 1.1.3, v1.1.7, and v1.3.0 ([`5b84300`](https://github.com/OpenG2P/mowsa-nsr/commit/5b84300b2f27fc6d53a5cc1788f9ff4c3675e5a7))
- Edit README.md ([`cf03f6a`](https://github.com/OpenG2P/mowsa-nsr/commit/cf03f6af9b18362d99dd0a10ec594aad0a84f28d))
- Update Keycloak configuration in values.yaml and questions.yaml; add admin client realm variable and update README with post-install instructions for MoWSA master-data API. ([`5e91dc1`](https://github.com/OpenG2P/mowsa-nsr/commit/5e91dc1bac9c995d4c8c8fbfa8670ba7bdd16d9d))
- Add MinIO read access keys to global configuration in values.yaml ([`27763b2`](https://github.com/OpenG2P/mowsa-nsr/commit/27763b26967a6a393be80151917edd33ae3dbf0d))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Update values.yaml and templates to properly configure imagePullSecrets for private images, ensuring compatibility with subcharts and enhancing the db-seed job specification. ([`b0beb67`](https://github.com/OpenG2P/mowsa-nsr/commit/b0beb670466e78f1c2c4a965294593797e0263b8))
- Remove deprecated Docker configuration files for celery, partner-api, staff-portal-api, and staff-portal-ui, cleaning up unused versions and streamlining the project structure. ([`5e411f0`](https://github.com/OpenG2P/mowsa-nsr/commit/5e411f01b2301416dcc615bb77f323910d3cef8e))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Add imagePullSecrets configuration in values.yaml for pulling private images from GitLab registry. ([`b03961a`](https://github.com/OpenG2P/mowsa-nsr/commit/b03961a163166d0b8c7b01f9aadc68cda7b01c6f))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Add CHANGELOG_PROJECT variable to .gitlab-ci.yml for version tracking in the national-social-registry project. ([`d6bd49c`](https://github.com/OpenG2P/mowsa-nsr/commit/d6bd49c7d47e5976c94d2d13d746982a79050051))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Update .gitlab-ci.yml and Dockerfile for staff-portal-ui to use Git refs for GIT_BRANCH and improve image fetching process. ([`b854c81`](https://github.com/OpenG2P/mowsa-nsr/commit/b854c814a6cc82b738a0446c42b356ad4e4a1596))
- Update keys in construct_record_name method ([`1f0c1a4`](https://github.com/OpenG2P/mowsa-nsr/commit/1f0c1a4017a0e626aaf7b3ce28b4de9da7afba50))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Enhance .gitlab-ci.yml and values.yaml to include staff-ui service configuration and update image repository structure for national-social-registry. ([`82b9a17`](https://github.com/OpenG2P/mowsa-nsr/commit/82b9a17d804722dd40521cdd36e7cc3a4e54346a))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Update Dockerfiles to use GitLab repository URLs for registry-platform dependencies ([`57e17fb`](https://github.com/OpenG2P/mowsa-nsr/commit/57e17fb019a46f85ed9da2118fc7c66f04b7047b))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Update Dockerfiles and Helm chart to version 1.1, changing image repositories and tags to reflect the new national-social-registry structure. Adjust .gitlab-ci.yml for updated service references. ([`e27586c`](https://github.com/OpenG2P/mowsa-nsr/commit/e27586c067691c66baa8bab79da9fdb8cb17129a))
- Refactor: rename openg2p-registry-nsr-extension to nsr-extension across all files and update documentation accordingly. Introduce new README and LICENSE files for the nsr-extension package, and enhance the build configuration with pyproject.toml. Update Dockerfiles and service files to reflect the new structure. ([`70ce470`](https://github.com/OpenG2P/mowsa-nsr/commit/70ce47006d7c208e1d4545a11b69807517d52b50))
- Just to trigger a build. No change otherwise ([`f467aaf`](https://github.com/OpenG2P/mowsa-nsr/commit/f467aaf05457219a4198ba3e224fd28b448fb55c))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Refactor: Rename mowsa-nsr-extension to nsr-extension and update related Dockerfiles and README. ([`fdc65df`](https://github.com/OpenG2P/mowsa-nsr/commit/fdc65df2af0c5b7ee3a12982159d05bfdf823a60))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): Aligned with newer architecture. ([`039e090`](https://github.com/OpenG2P/mowsa-nsr/commit/039e090c3a5068061b509f8707bcb15ba23f3123))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): fix(ci): update service names and references in .gitlab-ci.yml and Chart.yaml ([`feaabfd`](https://github.com/OpenG2P/mowsa-nsr/commit/feaabfd80586c6d5696694b8346b9afef3bc4ffe))
- Change minioHost to use minio-api ([`737ef40`](https://github.com/OpenG2P/mowsa-nsr/commit/737ef40adde54e1a6b11acc214d0eebf06d0c684))
- Update image repository for staff portal UI ([`43782e4`](https://github.com/OpenG2P/mowsa-nsr/commit/43782e4afd7ff9f7ee2332503d7935fcc5d7647d))
- fix(helm): align staff portal auth Redis and APP_MNEMONIC with IAM ([`7487f6d`](https://github.com/OpenG2P/mowsa-nsr/commit/7487f6d0c83f9c35a6cf45232a087ceb51801070))
- Downgrade keycloak-init version to 1.1.1 ([`bd3322e`](https://github.com/OpenG2P/mowsa-nsr/commit/bd3322e5fd6f49c133ec76a26d3f3586c579d960))
- Create version 1.1.2.txt and update dependencies in Chart.yaml, README.md, and values.yaml ([`d807ea3`](https://github.com/OpenG2P/mowsa-nsr/commit/d807ea3fd0f161e4ea61eeba2e5e56501e4dbde4))
- [G2P-5370](https://openg2p.atlassian.net/browse/G2P-5370) [G2P-5365](https://openg2p.atlassian.net/browse/G2P-5365)  service record name construction for household and individual domains and update SQL insert statements for sections, language and tab_section ([`23fab17`](https://github.com/OpenG2P/mowsa-nsr/commit/23fab17683017e07f46f5bb2c7ed31f95befc930))
- Bump version to 1.1.1 ([`db0767f`](https://github.com/OpenG2P/mowsa-nsr/commit/db0767f81ccddd6c5e89aa0951218cae610be21d))
- fix(nsr): update connectorHostname to use registry-scoped naming ([`0857d47`](https://github.com/OpenG2P/mowsa-nsr/commit/0857d47b9a4f19b2ddd8d31a5a90931cfe0475a1))
- fix(iam): sync role permissions with upstream payload.json ([`09fdd53`](https://github.com/OpenG2P/mowsa-nsr/commit/09fdd5366589f249645c28ab34762b9319d34e0d))
- fix(nsr): map ODK select_multiple assets to uppercase lists ([`939c825`](https://github.com/OpenG2P/mowsa-nsr/commit/939c825c31eb2dcb36722c1cdf9106ea236c3263))
- fix(celery): patch partner auto-approve via on-disk task paths ([`4708c1d`](https://github.com/OpenG2P/mowsa-nsr/commit/4708c1de746af51a255c07112ad3da7b1a62785d))
- feat(helm): opt-in loadGeoData and connector hostname aliases ([`b8f6b9a`](https://github.com/OpenG2P/mowsa-nsr/commit/b8f6b9ab9a9a12b546fa13b33e6e24c082b6c0be))
- chore(scripts): normalize uninstall-registry.sh trailing newline ([`ae57652`](https://github.com/OpenG2P/mowsa-nsr/commit/ae57652106cadda0db246afebda5e705fe4ec7f0))
- chore(i18n): import upstream translation/domain.json ([`7b67faa`](https://github.com/OpenG2P/mowsa-nsr/commit/7b67faa2b08c2767886628a5330e20db0bcb4f4b))
- fix(helm): pass dict context to common.capabilities.hpa.apiVersion ([`2f14a18`](https://github.com/OpenG2P/mowsa-nsr/commit/2f14a18ead9905e9ec11f4b56d909b9775377cf7))
- fix(db-seed): drop psycopg2 pip pin; use alpine apk package ([`2b29265`](https://github.com/OpenG2P/mowsa-nsr/commit/2b2926574c88cdc2435c0b96ae775ba905d1086a))
- feat(db-seed): add opt-in geo loader and dormant seed-data assets ([`25c6288`](https://github.com/OpenG2P/mowsa-nsr/commit/25c6288ba803722361afca3fae6474e12a24d767))
- feat(docker): pin registry-platform core to 1.1.1 on 1.1-develop ([`a51ff1c`](https://github.com/OpenG2P/mowsa-nsr/commit/a51ff1c2007a6d27a327d0da4cad144bf056af69))
- Added 1.1.1 package file ([`4af93bb`](https://github.com/OpenG2P/mowsa-nsr/commit/4af93bb93973800147f753f495f28ca2414dc54e))
- fix(nsr): harden sandbox helm for ODK E2E, IAM logout, and AWE login ([`eed669e`](https://github.com/OpenG2P/mowsa-nsr/commit/eed669e9b7f6e2a115e48f5ffdaa95ef426ab81a))
- fix(nsr): map all ODK v13 select choices to registry enums ([`5a1b540`](https://github.com/OpenG2P/mowsa-nsr/commit/5a1b540a76b626690ea8a6062b312af36616b71b))
- fix(nsr): map ODK geo codes to master-data IDs in Jinja ([`3f12a6f`](https://github.com/OpenG2P/mowsa-nsr/commit/3f12a6f582d309910e4aea8c7d473b1d5bb269e0))
- fix(nsr): normalize ODK prefix casing in Jinja templates ([`ed67b1a`](https://github.com/OpenG2P/mowsa-nsr/commit/ed67b1aab03c92792e66d8229a89d84c3d4a8674))
- feat(helm): add connector stack to mowsa-nsr chart ([`281f1b3`](https://github.com/OpenG2P/mowsa-nsr/commit/281f1b38bd3b2281a8afce75a0d7f9d32f0d2477))
- Update version tags to 1.1.0 ([`a861e0a`](https://github.com/OpenG2P/mowsa-nsr/commit/a861e0aff13f080d4f32b0edacd6f6f3afe70185))
- Add 1.1.0 Docker version files ([`c506820`](https://github.com/OpenG2P/mowsa-nsr/commit/c506820e28943b01cd9071b6aaf6a066af5bc94e))
- [G2P-5366](https://openg2p.atlassian.net/browse/G2P-5366): chore(ci): update Dockerfiles and Helm values for image references according to central build-publish CI. ([`562f2dd`](https://github.com/OpenG2P/mowsa-nsr/commit/562f2dd2ed4b218560b48d1823f8d0d9eb0afc5b))
- Migrate CI to GitLab and point chart images at mowsa1/nsr registry ([`1794fda`](https://github.com/OpenG2P/mowsa-nsr/commit/1794fda597c3b2dcf0bd1c64d06ca632badc383e))
- fix(helm): correct minioHost value in values.yaml ([`37e29c2`](https://github.com/OpenG2P/mowsa-nsr/commit/37e29c276e57a4b6196346fe5879e0eda5090fb6))
- chore(docker): update OPENG2P_DATA_BRANCH in db-seed Dockerfile ([`5d2ebf8`](https://github.com/OpenG2P/mowsa-nsr/commit/5d2ebf8a15b5a69720a4df655fcf5e023548ea87))
- feat(docker): update db-seed image and scripts ([`d69cdbe`](https://github.com/OpenG2P/mowsa-nsr/commit/d69cdbe7d534f7cc5ca9899e6a143fda8898036f))
- chore(sql): update template file references in incoming_templates.sql ([`ec64cf6`](https://github.com/OpenG2P/mowsa-nsr/commit/ec64cf6fa69fdc226ad589e8f1fd2b28ecdec32d))
- Correct dependency URLs in 1.1.txt ([`e905bea`](https://github.com/OpenG2P/mowsa-nsr/commit/e905bea659d265fe32b34d5432af8dbe1358db09))
- Fix dependency URL for fastapi-auth ([`c284d7e`](https://github.com/OpenG2P/mowsa-nsr/commit/c284d7e949cac452465a2652daa9c920e1f68e29))
- Change fastapi-common to develop in 1.1.txt ([`cd06fd5`](https://github.com/OpenG2P/mowsa-nsr/commit/cd06fd53daf252261416086cc151d6af35ae83c3))
- Update version in staff-portal-ui configuration ([`19f0915`](https://github.com/OpenG2P/mowsa-nsr/commit/19f0915c8ed6c51479b89f19cea414c553962c4f))
- Add Dockerfile for staff portal UI version 1.1 ([`477ceb6`](https://github.com/OpenG2P/mowsa-nsr/commit/477ceb6c1644af38be441fa6db465383c082214f))
- Update staff portal UI version to 1.1 ([`c7acfe5`](https://github.com/OpenG2P/mowsa-nsr/commit/c7acfe50e91a5d925cde7da0dba96e4f878c0824))
- Refactor code structure for improved readability and maintainability ([`aab04cf`](https://github.com/OpenG2P/mowsa-nsr/commit/aab04cfb086d4bfeb906205c2f19e336c31783ce))
- Update data seeding for language and configuration ([`27ab0d5`](https://github.com/OpenG2P/mowsa-nsr/commit/27ab0d5df6b710328b06d4935e2034e925b13ad5))
- Implement geo hierarchy handling in household service and utilities ([`0455608`](https://github.com/OpenG2P/mowsa-nsr/commit/0455608a5ced7f584f9457f277edcc3301a28da8))
- Add overcrowding indicator to household roster calculations ([`a225439`](https://github.com/OpenG2P/mowsa-nsr/commit/a2254397b58c86cb22450d99fb9f5017cf6a96f0))
- Add Keycloak configuration to celeryWorker in values.yaml ([`c01420c`](https://github.com/OpenG2P/mowsa-nsr/commit/c01420c219df5071404185dc2431af6a686939b0))
- Remove unused AWE configuration from celeryWorker in values.yaml ([`890d3dc`](https://github.com/OpenG2P/mowsa-nsr/commit/890d3dcc9081ac42874759382c851c85939a8511))
- Bump version to 1.1.0-develop.5 and add PullSecrets for image repositories and correct service port ([`977bd6b`](https://github.com/OpenG2P/mowsa-nsr/commit/977bd6bb6907423a59c152e8c4dde77fa9528592))
- Updated with latest ([`0e029d1`](https://github.com/OpenG2P/mowsa-nsr/commit/0e029d18767b336e48c39136a1ad99aee00166a2))
- Bump version and appVersion to 1.1.0-develop.3 ([`6844f63`](https://github.com/OpenG2P/mowsa-nsr/commit/6844f63676b66bb116b74a384914439dc789752a))
- Add PullSecrets for image repositories ([`68aa1b5`](https://github.com/OpenG2P/mowsa-nsr/commit/68aa1b5f8d3e02cb9f145e327e7c4d6525a556e1))
- Update Chart.yaml ([`109bd24`](https://github.com/OpenG2P/mowsa-nsr/commit/109bd242a48a8be71b74bfbf07cc38df1012d6d0))
- Fix Helm nil pointer: add celeryWorker.serviceAccount defaults and harden templates ([`7f984d2`](https://github.com/OpenG2P/mowsa-nsr/commit/7f984d2a2062b2be1415652b12a7cf1d7c53d614))
- Initial plan ([`c366ad8`](https://github.com/OpenG2P/mowsa-nsr/commit/c366ad84f3a0ef0b1b6c39d6fcf36a34dd58b573))
- Bump version and appVersion to 1.1.0-develop.1 ([`e1121fc`](https://github.com/OpenG2P/mowsa-nsr/commit/e1121fc9775c487e0825764be13035da37a37bb8))
- Update database configuration in values.yaml ([`1f8fd7d`](https://github.com/OpenG2P/mowsa-nsr/commit/1f8fd7d849342c607f7e77e762d7034136c52247))
- fix(helm): use component-scoped service.port in istio virtualservice destinationPort ([`72a55cb`](https://github.com/OpenG2P/mowsa-nsr/commit/72a55cb7a1da008481bf5f10e8e73d0d7d016d34))
- Fix formatting in Dockerfile environment variables ([`776b118`](https://github.com/OpenG2P/mowsa-nsr/commit/776b1180f1c14cfeb2e3417689264c62099b9d98))
- Remove openg2p-data clone from Dockerfile ([`546214a`](https://github.com/OpenG2P/mowsa-nsr/commit/546214af527a2dbf976ab79dc6b3c90e596f021f))
- Update openg2p-awe dependency version to 1.1.0-develop ([`b9cba01`](https://github.com/OpenG2P/mowsa-nsr/commit/b9cba0149546a599b34e22dcc86948ac7c0cdf1a))
- Bump version to 1.1 ([`736c362`](https://github.com/OpenG2P/mowsa-nsr/commit/736c362722e085d49eab8a0dbea279753f19c2e6))
- Corrected version ([`2d70104`](https://github.com/OpenG2P/mowsa-nsr/commit/2d70104dcec94efc7dd43d90548ffa981ca8356c))
- Update record name construction method to use intake record naming ([`57ef1b3`](https://github.com/OpenG2P/mowsa-nsr/commit/57ef1b3230324ea066cc26c9a1873d55978d1f90))
- Refactor household head validation to simplify logic and improve logging ([`15be8f5`](https://github.com/OpenG2P/mowsa-nsr/commit/15be8f53bb757b68ad64e40f7613ff2c5889ca69))
- Fix method name for constructing household intake record name ([`e0fa39f`](https://github.com/OpenG2P/mowsa-nsr/commit/e0fa39f7a2ebaab357e7f188dd5b5a49dc6a2a6c))
- [G2P-5095](https://openg2p.atlassian.net/browse/G2P-5095) [G2P-5203](https://openg2p.atlassian.net/browse/G2P-5203) - Refactor record name construction methods and add household roster utility functions ([`0a8a03c`](https://github.com/OpenG2P/mowsa-nsr/commit/0a8a03c326f1ed4cfcead4fb4fe7194824a8ef43))
- Add staff-portal-ui 1.0 build and pin helm UI image to :1.0. ([`cae0787`](https://github.com/OpenG2P/mowsa-nsr/commit/cae07873ddc5f26758ead2a2a351e10784c2184c))
- Point 1.0 branch CI at docker/*/1.0.txt for registry-platform@1.0. ([`4151dab`](https://github.com/OpenG2P/mowsa-nsr/commit/4151dab77a1fe022a6a2242f86347ea381a55c13))
- Hot-patch partner CR auto-approve in celery run_celery startup. ([`5a9d818`](https://github.com/OpenG2P/mowsa-nsr/commit/5a9d818794d984975c5786aedf181cef044770e3))
- Scope 1.0 branch self-reference to the NSR extension only. ([`22d9fac`](https://github.com/OpenG2P/mowsa-nsr/commit/22d9fac6960f9091d3afb5c86dd1d9990311cc1b))
- Align 1.0 branch CI, Helm, and image tags with the 1.0 release line. ([`d8d29e8`](https://github.com/OpenG2P/mowsa-nsr/commit/d8d29e8813cd82a9d6a616eed194bbcca595c457))
- Add individual household section and tab to metadata; implement validation for single household head ([`83837ef`](https://github.com/OpenG2P/mowsa-nsr/commit/83837ef6b39c0753b573e3f60ba1084086e79e11))
- Enable partner ingest auto-approve via db-seed and celery runtime fixes. ([`b5b9aee`](https://github.com/OpenG2P/mowsa-nsr/commit/b5b9aeefc56c31426039c04be3944c82b6b16f49))
- Fix Istio VirtualService double-slash prefix breaking API routes. ([`0b5a8b2`](https://github.com/OpenG2P/mowsa-nsr/commit/0b5a8b2ec8c48f47c8968d6f09d73b8d1fd04c99))
- Fix Istio VirtualService double-slash prefix breaking API routes. ([`fe50ead`](https://github.com/OpenG2P/mowsa-nsr/commit/fe50ead59767afe249683fb61009563d0315ce0c))
- Remove commons IAM cache overlay; belongs in openg2p-commons-services. ([`7f71cf4`](https://github.com/OpenG2P/mowsa-nsr/commit/7f71cf400a3d5d4b58de6214b17329e614b53b8e))
- Remove commons IAM cache overlay; belongs in openg2p-commons-services. ([`49a9004`](https://github.com/OpenG2P/mowsa-nsr/commit/49a9004b88e26597dab65180e7baa61a76c9101f))
- Cut 1.0.0-develop with Keycloak data policy fix and IAM cache TTL. ([`8d8a32d`](https://github.com/OpenG2P/mowsa-nsr/commit/8d8a32d0fefcdacecd2bf60b43738d3c7d7d9b93))
- Set commons IAM role cache TTL to 10 seconds for NSR deployments. ([`80a2d12`](https://github.com/OpenG2P/mowsa-nsr/commit/80a2d12e57ede631b79b6817b5d5c94e44a02e54))
- Fix data policy Keycloak admin client to use registry-staff-portal. ([`b2e5199`](https://github.com/OpenG2P/mowsa-nsr/commit/b2e519934b3900363db1c449b910fe33416103c0))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
