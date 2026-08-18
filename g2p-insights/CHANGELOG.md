# g2p-insights

_Published automatically._

**Repository:** [gitlab.com/openg2p/g2p-insights](https://gitlab.com/openg2p/g2p-insights) · **Container images:** [Container Registry](https://gitlab.com/openg2p/g2p-insights/container_registry)

| Version | Date | Type |
| --- | --- | --- |
| [`0.0.0-develop.72`](#v-0-0-0-develop-72) | 2026-08-18 | develop |
| [`0.0.0-develop.71`](#v-0-0-0-develop-71) | 2026-08-11 | develop |
| [`0.0.0-develop.70`](#v-0-0-0-develop-70) | 2026-08-09 | develop |
| [`0.0.0-develop.69`](#v-0-0-0-develop-69) | 2026-08-08 | develop |
| [`0.0.0-develop.66`](#v-0-0-0-develop-66) | 2026-08-07 | develop |
| [`0.0.0-develop.62`](#v-0-0-0-develop-62) | 2026-08-07 | develop |
| [`0.0.0-develop.61`](#v-0-0-0-develop-61) | 2026-08-07 | develop |
| [`0.0.0-develop.60`](#v-0-0-0-develop-60) | 2026-08-07 | develop |
| [`0.0.0-develop.59`](#v-0-0-0-develop-59) | 2026-08-07 | develop |
| [`0.0.0-develop.56`](#v-0-0-0-develop-56) | 2026-08-07 | develop |
| [`0.0.0-develop.55`](#v-0-0-0-develop-55) | 2026-08-06 | develop |
| [`0.0.0-develop.53`](#v-0-0-0-develop-53) | 2026-08-06 | develop |
| [`0.0.0-develop.50`](#v-0-0-0-develop-50) | 2026-08-03 | develop |
| [`0.0.0-develop.49`](#v-0-0-0-develop-49) | 2026-08-03 | develop |
| [`0.0.0-develop.48`](#v-0-0-0-develop-48) | 2026-08-03 | develop |
| [`0.0.0-develop.46`](#v-0-0-0-develop-46) | 2026-08-03 | develop |

# Develop builds

<a id="v-0-0-0-develop-72"></a>

## g2p-insights — develop 0.0.0-develop.72 (2026-08-18)

_commit `751fc2c` · changes since 0.0.0-develop.71_
<!-- build:0.0.0-develop.72 revision:751fc2c55223b520dee379cf6810d4a8edc43a05 ts:1787020949 -->

**Chart:** [openg2p-insights 0.0.0-develop.72](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.72.tgz)

### Changes since 0.0.0-develop.71

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Run the schema migration after install, not before it. postgres-init renders as an ordinary Job rather than a hook, and Helm completes every pre-install hook before applying ordinary resources — so the migration ran against a database that did not exist yet, and its pg_isready wait passed because that asks whether the server is up without authenticating, turning a missing database into "password authentication failed for user insights_user". ([`751fc2c`](https://gitlab.com/openg2p/g2p-insights/-/commit/751fc2c55223b520dee379cf6810d4a8edc43a05))

<a id="v-0-0-0-develop-71"></a>

## g2p-insights — develop 0.0.0-develop.71 (2026-08-11)

_commit `478c8f3` · changes since 0.0.0-develop.70_
<!-- build:0.0.0-develop.71 revision:478c8f3a8461863add5e50bf75109e63fa01f23c ts:1786448842 -->

**Chart:** [openg2p-insights 0.0.0-develop.71](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.71.tgz)

### Changes since 0.0.0-develop.70

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Point Expert Lab's extractor at the registry database. It used the app's own engine, which holds sessions and the audit log and none of the reporting views, so every function failed with `relation "fr_rpt_farmer" does not exist` while the column picker looked healthy — it reads the catalog, which is a file. Also reports a non-numeric column as a mismatch rather than letting pandas raise "could not convert string to float". ([`478c8f3`](https://gitlab.com/openg2p/g2p-insights/-/commit/478c8f3a8461863add5e50bf75109e63fa01f23c))

<a id="v-0-0-0-develop-70"></a>

## g2p-insights — develop 0.0.0-develop.70 (2026-08-09)

_commit `a454f67` · changes since 0.0.0-develop.69_
<!-- build:0.0.0-develop.70 revision:a454f675a74dbddeb7405bbcdf7e0f11ecf7797e ts:1786255078 -->

**Chart:** [openg2p-insights 0.0.0-develop.70](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.70.tgz)

### Changes since 0.0.0-develop.69

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Make the country pack a free-text field with short form guidance. The two-value enum let an environment pick only ETH or XKM, so a country adding its own pack to openg2p-data could not select it; the Rancher description now says where to find the directory name and the provenance notes move to values.yaml. ([`a454f67`](https://gitlab.com/openg2p/g2p-insights/-/commit/a454f675a74dbddeb7405bbcdf7e0f11ecf7797e))

<a id="v-0-0-0-develop-69"></a>

## g2p-insights — develop 0.0.0-develop.69 (2026-08-08)

_commit `c15f7c7` · changes since 0.0.0-develop.66_
<!-- build:0.0.0-develop.69 revision:c15f7c7196bc3d436ddaa196d0c455c13d4f11af ts:1786203722 -->

**Chart:** [openg2p-insights 0.0.0-develop.69](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.69.tgz)

### Summary

- Build system enhancement: enabled build cache for improved efficiency.
- CSRF token handling: fixed the order of operations in fetching Superset's CSRF token to ensure valid session cookies are used, resolving the "400 The CSRF session token is missing" error across multiple call sites.

### Changes since 0.0.0-develop.66

- Build cache enabled. ([`c15f7c7`](https://gitlab.com/openg2p/g2p-insights/-/commit/c15f7c7196bc3d436ddaa196d0c455c13d4f11af))
- Just to trigger build. No change ([`049fa9b`](https://gitlab.com/openg2p/g2p-insights/-/commit/049fa9b0e92f38108f4ed1d3c37b2bbd9cfa46e0))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fetch Superset's CSRF token before reading the cookies. Keyword arguments evaluate left to right, so cookies=self._ck was read before the inline _csrf() call that obtains the session the token is bound to — every mutating call went out with a valid token and pre-session cookies, and Superset answered "400 The CSRF session token is missing", which describes the token rather than the dropped cookie. Three call sites, including the guest token the Dashboards tab depends on. ([`28d57f4`](https://gitlab.com/openg2p/g2p-insights/-/commit/28d57f44ab631e05040a5e10cd60098fdfd80bd8))

<a id="v-0-0-0-develop-66"></a>

## g2p-insights — develop 0.0.0-develop.66 (2026-08-07)

_commit `03f7864` · changes since 0.0.0-develop.62_
<!-- build:0.0.0-develop.66 revision:03f7864063b09a4fabb009c78a39f9277a9a9f12 ts:1786095275 -->

**Chart:** [openg2p-insights 0.0.0-develop.66](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.66.tgz)

### Summary

- **Major:** Registry enhancements: removed dependency on analytics release for reporting views, allowing charts to manage their own data freshness; introduced a new registry engine for query execution, resolving issues with missing relations and improving query accuracy.
- Cost optimization: adjusted cost gate logic to evaluate query costs relative to the cheapest plan, reducing unnecessary warnings for large datasets and improving performance for COUNT(*) queries.
- AI catalog generation: replaced static catalog shipping with dynamic generation from registry reporting views and Master Data code lists, ensuring accurate and context-specific entity references while enabling per-question token logging for better cost visibility.
- Configuration fixes: corrected COMMON_DB_PASSWORD to prevent broken environment entries and improved the Ask tab's query execution by clarifying geo_2 column meanings.

### Changes since 0.0.0-develop.62

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Stop refreshing the registry's reporting views. That made a registry's own data freshness depend on an analytics release and happen only as a side effect of building maps; the registry charts now own it, and insightMaps.build.refreshViews defaults to empty, kept only for older registry releases with no refresh job. ([`03f7864`](https://gitlab.com/openg2p/g2p-insights/-/commit/03f7864063b09a4fabb009c78a39f9277a9a9f12))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Stop the cost gate charging queries for the size of the register. A fixed planner-cost budget made COUNT(*) on 100k farmers look expensive, so cost is now judged relative to the cheapest plan that could answer, and the "no WHERE" warning fires only on queries returning raw rows. ([`61fbbbe`](https://gitlab.com/openg2p/g2p-insights/-/commit/61fbbbe4f7e795265771d9523b17091a87b443c6))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Point the Ask tab at the registry database, and tell the planner what geo_2 means. The query executor and cost gate ran generated SQL through the app's own engine, which holds sessions and the audit log and none of the reporting views, so EXPLAIN answered 'relation fr_rpt_farmer does not exist' — indistinguishable from a catalog describing tables nobody created; they now use a separate registry engine, configured from global.registryDB*. Column descriptions were carried into ColumnSpec and dropped before the prompt, and the geo_N columns carried none anyway, so 'farmers in each region' grouped by the country column and returned a single row that answered nothing — the generator now names each level from the deployment's own hierarchy. Also corrects COMMON_DB_PASSWORD, whose extra valueFrom level would have rendered a broken env entry on any install that had not been hand-patched.  # Please enter the commit message for your changes. Lines starting ([`cc86093`](https://gitlab.com/openg2p/g2p-insights/-/commit/cc86093efcc828f9f9a6b624eacc441312eae683))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate the AI catalog instead of shipping it. The published default described zero tables, so safe_views — a fail-secure allow-list — matched nothing and the planner refused every question, which reads as the feature being off rather than misconfigured; hand-maintaining it could not work anyway, since the tables differ per registry and the enum values per country. A Job now introspects the registry's *_rpt_* reporting views and Master Data's code lists, picks the entity register structurally by which id the other views reference, and patches the result into the catalog ConfigMap. Adds per-question token logging, since cost here is dominated by the prompt and was previously invisible. ([`0c37acf`](https://gitlab.com/openg2p/g2p-insights/-/commit/0c37acfa6c3bbcf197ddb1c3508d8439ca28eb2f))

<a id="v-0-0-0-develop-62"></a>

## g2p-insights — develop 0.0.0-develop.62 (2026-08-07)

_commit `a2bfd62` · changes since 0.0.0-develop.61_
<!-- build:0.0.0-develop.62 revision:a2bfd6270ef38a974d9bccde4a93d21acbd7331b ts:1786085269 -->

**Chart:** [openg2p-insights 0.0.0-develop.62](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.62.tgz)

### Changes since 0.0.0-develop.61

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Keep the iframe tabs alive, collapse the filter rail, and stop the maps build falling back to reference content. Routing unmounted the Superset and Evidence iframes on every tab switch, so each return re-authenticated, re-rendered and re-downloaded, losing whatever filter or drill-down was set; both now render outside Routes and only toggle visibility. The maps build with no content ConfigMap was building the reference registry's queries against another registry's database — a full, themed site with every panel empty — and now skips with a message naming the setting. ([`a2bfd62`](https://gitlab.com/openg2p/g2p-insights/-/commit/a2bfd6270ef38a974d9bccde4a93d21acbd7331b))

<a id="v-0-0-0-develop-61"></a>

## g2p-insights — develop 0.0.0-develop.61 (2026-08-07)

_commit `15c9585` · changes since 0.0.0-develop.60_
<!-- build:0.0.0-develop.61 revision:15c95852a2b9552bd1ad2764d030d07ad61e1026 ts:1786082221 -->

**Chart:** [openg2p-insights 0.0.0-develop.61](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.61.tgz)

### Changes since 0.0.0-develop.60

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Configure the frontend at runtime, move Evidence off /maps, and drop its branding. VITE_* is substituted at build time, so with no build args the published image fell back to localhost:8088 for Superset and folded the Maps iframe away entirely — neither fixable by deployment; the container now writes /config.js from its environment. Evidence also collided with the shell's own /maps route, so it moves to /evidence, and its header, wordmark and badge are hidden since the page only ever renders inside the Insight shell. ([`15c9585`](https://gitlab.com/openg2p/g2p-insights/-/commit/15c95852a2b9552bd1ad2764d030d07ad61e1026))

<a id="v-0-0-0-develop-60"></a>

## g2p-insights — develop 0.0.0-develop.60 (2026-08-07)

_commit `1f2df62` · changes since 0.0.0-develop.59_
<!-- build:0.0.0-develop.60 revision:1f2df62cc8475085f5e09faee7c6b0d1c871e5ee ts:1786076351 -->

**Chart:** [openg2p-insights 0.0.0-develop.60](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.60.tgz)

### Changes since 0.0.0-develop.59

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Serve the nested maps site correctly, and pick up the build when it lands. `serve -s` rewrites every miss to the root index.html, which no longer exists once the site sits under its basePath, so /maps/ returned a directory listing; the site is prerendered and needs no SPA fallback. The pod also chose its source once at startup, before the post-install hook that produces the build had run, so it served the image's own default-pack copy until restarted — it now serves what is there and swaps when a build publishes, since blocking would deadlock against Helm's own wait. ([`1f2df62`](https://gitlab.com/openg2p/g2p-insights/-/commit/1f2df62cc8475085f5e09faee7c6b0d1c871e5ee))

<a id="v-0-0-0-develop-59"></a>

## g2p-insights — develop 0.0.0-develop.59 (2026-08-07)

_commit `8ea621f` · changes since 0.0.0-develop.56_
<!-- build:0.0.0-develop.59 revision:8ea621f711fd62a144c20b999701ee0f9475bbe0 ts:1786073971 -->

**Chart:** [openg2p-insights 0.0.0-develop.59](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.59.tgz)

### Summary

- **Major:** Build process overhaul: Evidence now builds under its basePath without redirection, resolving issues with ENOENT errors, and outputs to build/maps for proper asset resolution.
- Integration improvements: Maps are now served directly at /maps within the Insight host, eliminating the need for a separate hostname and DNS configuration, while the page theme is centralized and injected at build time.
- API routing fixes: The VirtualService rewrite is now correctly emitted, resolving issues with API calls returning 404 errors due to incorrect forwarding and template rendering for source ports.
- Cleanup enhancements: The build process now clears the /app/build directory before compiling, preventing residual files from previous builds from affecting new deployments.

### Changes since 0.0.0-develop.56

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Nest the built site under its basePath instead of redirecting the build. EVIDENCE_BUILD_DIR sets the SvelteKit adapter's target, resolved relative to .evidence/template/, but the CLI then copies unconditionally to ./build — so an absolute path left the copy step looking for a directory that was never written, and the build died with a bare ENOENT. Evidence now builds as it wants and the result is moved into build/maps afterwards, so /maps/... resolves on disk with no server-side rewriting. ([`8ea621f`](https://gitlab.com/openg2p/g2p-insights/-/commit/8ea621f711fd62a144c20b999701ee0f9475bbe0))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Serve maps at /maps on the Insight host, and move the page theme into the platform. A separate maps-insights hostname meant a second DNS name and certificate and an off-origin iframe for what is a tab inside Insights; Evidence emits absolute asset paths, so this is deployment.basePath plus a matching EVIDENCE_BUILD_DIR, not a gateway rewrite. The theme was a <style> block copied per registry, and the Farmer Registry's copy was missing — its class="split" markup silently rendered stacked — so it now ships with the toolchain and is injected at build time. ([`79a10ed`](https://gitlab.com/openg2p/g2p-insights/-/commit/79a10ed2c0b8161946a9e530929ba0e2e59bd1eb))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Emit the VirtualService rewrite, and tpl the Evidence port. rewriteUri existed in values but the template never read it, so the gateway forwarded /v1/insight/ unchanged to an app that serves at root and every API call 404'd with healthy pods. The maps build had the same class of bug: source.port was not tpl-rendered, so Evidence parsed the literal braces as NaN and refused the connection — after the gate had passed and the boundaries had synced. Also clears /app/build before compiling, so a pack with fewer levels stops publishing the previous pack's deepest geojson. ([`1936160`](https://gitlab.com/openg2p/g2p-insights/-/commit/19361609b2cb02a1cb951b7ef692ee2f2164b696))

<a id="v-0-0-0-develop-56"></a>

## g2p-insights — develop 0.0.0-develop.56 (2026-08-07)

_commit `b22a27e` · changes since 0.0.0-develop.55_
<!-- build:0.0.0-develop.56 revision:b22a27eb241e74a3c9b4cf467ab5b25d25aa5b05 ts:1786066849 -->

**Chart:** [openg2p-insights 0.0.0-develop.56](https://gitlab.com/api/v4/projects/openg2p%2Fcharts/packages/helm/stable/charts/openg2p-insights-0.0.0-develop.56.tgz)

### Changes since 0.0.0-develop.55

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the map boundaries from Master Data at build-job time, not from the image. COUNTRY_PACK is a build arg defaulting to XKM, but the country is chosen at install time in Master Data, so a stock image drew Kamuntu over Ethiopian data — and since the choropleth joins on P-code that renders an EMPTY map with nothing in any log. Master Data already records a boundary URL on every geo row; sync_pack.py --from-master-data now reads it, with the object-store credentials the bucket needs, and falls back to the baked pack if unreachable. ([`b22a27e`](https://gitlab.com/openg2p/g2p-insights/-/commit/b22a27eb241e74a3c9b4cf467ab5b25d25aa5b05))

<a id="v-0-0-0-develop-55"></a>

## g2p-insights — develop 0.0.0-develop.55 (2026-08-06)

_commit `4d2adc6` · changes since 0.0.0-develop.53_
<!-- build:0.0.0-develop.55 revision:4d2adc60ca779b415e3952688e02100befde6a83 ts:1786003211 -->

### Summary

- **Major:** PVC management enhancement: improved deletion process for maps PVC by ensuring all mounts are cleared, including references from Completed or Failed pods, preventing kubectl hangs.
- Registry optimization: switched from using a registry-built image to sourcing map content from a ConfigMap, resolving version pinning issues and improving pipeline reliability.

### Changes since 0.0.0-develop.53

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Clear whatever mounts the maps PVC before deleting it. The pvc-protection finalizer blocks the delete while any pod still references the claim — a Completed or Failed pod counts — and kubectl then hangs with no message saying why. Step 2 only sweeps by label, which misses a maps-build Job re-run by hand, so the step now matches on who mounts the claim and removes the owning Job too. ([`4d2adc6`](https://gitlab.com/openg2p/g2p-insights/-/commit/4d2adc60ca779b415e3952688e02100befde6a83))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Take the registry's map content from a ConfigMap rather than a registry-built image. A registry contributes ~20 KB of queries and a page; requiring it to build that FROM this repo's toolchain made registries pin an Insights version and fail their pipelines on it. insightMaps.build.content.configMap is mounted and overlaid at build time; empty still builds the reference content. ([`28291cf`](https://gitlab.com/openg2p/g2p-insights/-/commit/28291cfb50fb4547965c696328c8c94bf6c05a66))

<a id="v-0-0-0-develop-53"></a>

## g2p-insights — develop 0.0.0-develop.53 (2026-08-06)

_commit `1ec6add` · changes since 0.0.0-develop.50_
<!-- build:0.0.0-develop.53 revision:1ec6addbbc771f2a03c948ee09e99c047cef98f5 ts:1785991995 -->

### Summary

- Backend improvements: Updated the reference maps page to use the `registry` source, resolving issues with the previous `nsr.*` queries; fixed the Dashboards tab to re-authenticate and retry after JWT expiration, correcting false negatives in token probes.
- Deployment configuration: Changed the default backend and frontend replica count to one, disabled autoscaling by default to prevent unintended scaling behavior, and clarified that autoscaling should be enabled only in load-bearing environments.

### Changes since 0.0.0-develop.50

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Point the reference maps page at the `registry` source. It still queried nsr.*, which stopped resolving when the Evidence source was renamed, so the default maps image built nothing for any registry. ([`1ec6add`](https://gitlab.com/openg2p/g2p-insights/-/commit/1ec6addbbc771f2a03c948ee09e99c047cef98f5))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix the Dashboards tab. The backend cached Superset's JWT forever, so the tab worked for minutes after a restart then 401'd permanently; it now re-authenticates and retries. Its /api/v1/me/ token probe was also a false negative, and on the chart side the probes and the gateway rewrite both pointed at a prefix the app does not serve. ([`197c534`](https://gitlab.com/openg2p/g2p-insights/-/commit/197c5349a0b3a432cf91fa66a0756d934b16cf6a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Default backend and frontend to one replica. Two was the default for both, and the backend also shipped autoscaling on with minReplicas 2 — and when autoscaling is on the Deployment omits `replicas` so the HPA owns the count, so lowering replicaCount alone would have changed nothing. Autoscaling is now off by default; turn it on for a load-bearing environment. ([`f4e9e3a`](https://gitlab.com/openg2p/g2p-insights/-/commit/f4e9e3a4b0705d72594b02d9c16177833c9d50a2))

<a id="v-0-0-0-develop-50"></a>

## g2p-insights — develop 0.0.0-develop.50 (2026-08-03)

_commit `82dbb16` · changes since 0.0.0-develop.49_
<!-- build:0.0.0-develop.50 revision:82dbb16f17d3aec3be84aba95d16ff7c22dbea5d ts:1785763445 -->

### Changes since 0.0.0-develop.49

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Refresh the reporting views before extracting the maps. They are materialized and the registry builds them only at install, so every scheduled rebuild re-extracted the same frozen snapshot and published it as current — the maps silently stopped tracking the registry with nothing reporting it. Refreshed CONCURRENTLY so reads are not blocked, and a failure is logged rather than fatal. ([`82dbb16`](https://gitlab.com/openg2p/g2p-insights/-/commit/82dbb16f17d3aec3be84aba95d16ff7c22dbea5d))

<a id="v-0-0-0-develop-49"></a>

## g2p-insights — develop 0.0.0-develop.49 (2026-08-03)

_commit `b141093` · changes since 0.0.0-develop.48_
<!-- build:0.0.0-develop.49 revision:b141093cb6c08c7b40daa763cf6a2965376fc5a3 ts:1785746879 -->

### Changes since 0.0.0-develop.48

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix the maps install and move maps content to the registry. The CronJob got an empty secret name and an unrendered template string: global redeclared registryDBSecret and registryDBUserPasswordKey as empty later in the same map, and the helper tpl'd the ref's name but not its key. The build hook also blocked and failed the release when the registry was unseeded — Helm waits for hooks — so it now skips and leaves it to the schedule. What a map draws is registry-specific, so a registry ships its own maps image built FROM the platform's builder, and the Evidence source is renamed nsr -> registry because it appeared in the env var names. AI defaults to off: enabling it needs an API key that cannot be a form field, so defaulting to on failed a stock install on a credential nobody was told to create. Adds an uninstall script for what helm uninstall leaves — the database, role, maps volume and its Retain PV. ([`b141093`](https://gitlab.com/openg2p/g2p-insights/-/commit/b141093cb6c08c7b40daa763cf6a2965376fc5a3))

<a id="v-0-0-0-develop-48"></a>

## g2p-insights — develop 0.0.0-develop.48 (2026-08-03)

_commit `9695aca` · changes since 0.0.0-develop.46_
<!-- build:0.0.0-develop.48 revision:9695acad1b6e9b3dc0c2804992d0943b09b532bf ts:1785735901 -->

### Summary

- **Major:** Installation process improvements: enforced refusal to install with AI enabled without an OpenRouter key, and resolved conflicts with the Superset Secret to allow multiple chart installations.
- Template handling: standardized install form defaults to match template strings, ensuring consistency in installation behavior across environments.
- Helm chart enhancements: implemented pre-install hooks for key checks and refined rendering logic to prevent issues with existing resources.

### Changes since 0.0.0-develop.46

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Make the install form defaults the same template strings the values carry. They read <namespace>.openg2p.org, which is not a value — an installer accepting the default would have got that literally. Every consumer runs these through tpl, so leaving a field untouched now renders exactly what installing with no overrides does. ([`9695aca`](https://gitlab.com/openg2p/g2p-insights/-/commit/9695acad1b6e9b3dc0c2804992d0943b09b532bf))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Refuse to install with AI enabled and no OpenRouter key, and stop the shared Superset Secret blocking a second chart. The key check is a pre-install hook rather than a template lookup: lookup returns nothing both when a cluster is absent and when the Secret is, so a template check either breaks offline rendering or never fires — a hook only ever runs for real. Separately, both this chart and the registry declared the Superset service-account Secret, and Helm refuses to adopt an object owned by another release, so whichever installed second failed outright; each now renders it only when it does not already exist. ([`58b91d9`](https://gitlab.com/openg2p/g2p-insights/-/commit/58b91d931cda6e34c29113a502122da22c426d8b))

<a id="v-0-0-0-develop-46"></a>

## g2p-insights — develop 0.0.0-develop.46 (2026-08-03)

_commit `a8e9273` · changes since the start_
<!-- build:0.0.0-develop.46 revision:a8e9273ae951c93f4010ec38462c793c433480ab ts:1785718949 -->

### Summary

- **Major:** Split Superset URL for backend REST calls and browser access, transitioning to a single replica on a ReadWriteOnce volume with pod affinity for improved deployment efficiency. 
- Enhanced data handling: Rebuilt maps in-cluster to eliminate image-baked data, implementing a post-install Job and CronJob for live data updates without requiring image rebuilds.
- Security improvements: Generated Superset service-account password matching the registry chart's Secret, ensuring proper authentication and preventing silent failures.
- User interface updates: Applied OpenG2P branding across Maps and Superset, including a new two-column layout and streamlined navigation, enhancing user experience.
- Superset integration: Bundled OpenG2P-branded Superset into the Insights chart, added country-agnostic hierarchical drill-down capabilities, and made Superset opt-in for leaner test stack configurations.
- Bug fixes and enhancements: Resolved various issues in Superset and Maps, including chart interactivity, API authentication, and visual inconsistencies, while enhancing onboarding scripts for better database integration.
- AI/PII pipeline adjustments: Made the AI/PII pipeline an opt-in Docker build and switched LLM integration to OpenRouter-only, improving deployment flexibility and documentation clarity.

### Changes since the start

- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Split the Superset URL: the backend's REST calls go to the in-cluster Service, the browser keeps the public hostname the embed iframe must load from — one value served both, so every service-to-service call left through the ingress and came back. Maps drop to a single replica on a ReadWriteMany volume the build Job and serving pods share. Remove the empty docker/ directory left behind when the Dockerfiles moved into their own contexts. ([`a8e9273`](https://gitlab.com/openg2p/g2p-insights/-/commit/a8e9273ae951c93f4010ec38462c793c433480ab))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Split the Superset URL in two: the backend's REST calls go to the in-cluster Service, the browser keeps the public hostname the embed iframe must load from. One value served both, so every service-to-service call left through the ingress and came back. Drop the maps to a single replica on a ReadWriteOnce volume — RWX does not exist on the local-path provisioner — with pod affinity pinning the build to the serving pod's node, since RWO is node-local and a Job scheduled elsewhere sits Pending on a volume it cannot attach with nothing to say why. Remove the empty docker/ directory left behind when the Dockerfiles moved into their own contexts. ([`892ded3`](https://gitlab.com/openg2p/g2p-insights/-/commit/892ded3fbdc5830ccbd0c1d6b4f012b8aca59729))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Rebuild the maps in-cluster instead of baking data into the image. Evidence runs its SQL at build time and queries the parquet in the browser, so figures only changed when someone rebuilt the image by hand — and a published image must not carry any deployment's registry data. A post-install Job and a twice-daily CronJob now build against the live registry into a shared volume the serving pods read, so a refresh needs neither a restart nor a new image. The build waits on nsr_rpt_household HAVING ROWS rather than on the registry release: the two are separate releases so no hook can order them, seeding happens in hooks afterwards, and gating on the view merely existing would build an empty map that looks correct. Adds a builder image, since the serving image carries no sources or node_modules and cannot rebuild itself. ([`c093100`](https://gitlab.com/openg2p/g2p-insights/-/commit/c0931009c6f57933ff6512dadd69cdd115955520))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Generate the Superset service-account password, matching the registry chart's Secret name and key so either chart can install first. Named superset-svc-account.yaml, not *-secret.yaml: .gitignore excludes that pattern to keep real secrets out of the repo, and it silently swallowed the template — the chart would have installed without it and the Dashboards tab would have failed to authenticate with nothing to explain why. ([`8b3ff01`](https://gitlab.com/openg2p/g2p-insights/-/commit/8b3ff015f7d700bc05141708e7393dc83c69dd7d))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix "All woredasin <zone>" — Svelte trims leading whitespace inside an {#if}, so the space must sit outside it. Same bug in the section heading. Also broadens sync_pack's pattern for that line, which had stopped matching its own generated output and would have skipped it on the next pack switch. ([`b937fd1`](https://gitlab.com/openg2p/g2p-insights/-/commit/b937fd12b038d42b7c0346892d97d66eca956a45))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Restore the Region two-column layout — the barrier scatter had been inserted between its columns — and move that scatter to the static charts at the end. Park the quintile stacked bar behind a TODO (its source query stays). Name the selected zone in the woreda heading and table, since it has scrolled out of view by then. ([`0618254`](https://gitlab.com/openg2p/g2p-insights/-/commit/0618254d716eb840466cc39bdc04c036da73f5f2))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Add a region-level scatter (coverage vs no-ID — the two imply different fixes) and a 100% stacked quintile bar per zone that follows the drill. Scatter sits at region level because at woreda level both counts correlate more with area size (0.67/0.71) than with each other. No pie: Evidence ships none, and stacked bars compare areas rather than one at a time. Shortens the woreda blurb. ([`7975085`](https://gitlab.com/openg2p/g2p-insights/-/commit/7975085bb722798683b6a5e717682a54c0e39bca))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Make the Maps leaf level actionable: expose counts (poorest_not_enrolled, enrolled_hh, no_id_hh) so the table populates instead of blanking under the 30-household suppression, and replace the unlabelled priority scatter with a ranked bar of the enrolment gap. Drop heading numbers; sync_pack anchors on marker comments. Superset header logo becomes the OpenG2P mark. ([`2a2d925`](https://gitlab.com/openg2p/g2p-insights/-/commit/2a2d92561fccbf247995af0c1f0e6c7c47f4a1a2))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix Superset's inert THEME_OVERRIDES (AntD token shape; 4.0.1 wants the legacy colors.primary.base form) and correct two Maps charts — the scatter's size duplicated its x axis, and the bars look clickable but Evidence charts publish no selection. Navbar can't be darkened: its white is grayscale.light5, shared across the whole UI. ([`aa57388`](https://gitlab.com/openg2p/g2p-insights/-/commit/aa57388e9f983a33c0a48820347e73c707dfa3cc))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Black brand bar on the Maps surface, area names in the drill headings, and working woreda interaction. Headings now name the clicked area, guarded on the query row count — the input proxy renders "true" when unset and <Value> renders a "No Records" box, neither usable in a heading. The woreda charts were blank because only 50 of 1,135 areas clear the 30-household suppression bar, so they plot poverty score and household counts instead, with the reason stated on the page. The woreda map had no name= binding, so clicking did nothing; it now drives a Selected area panel. ([`e567437`](https://gitlab.com/openg2p/g2p-insights/-/commit/e567437ca694d2b21120bed60848393d44ea5c72))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Brand the Maps surface and Superset, and give Maps a two-column layout. Adds a G2P Insight / OpenG2P header bar to Evidence and puts each drill level's map beside its numbers instead of stacked full-width, which had one 1400px-wide map per level pushing every figure below the fold. Superset gets APP_ICON and the OpenG2P theme — it had no branding at all; its navbar right side has no config hook, so the OpenG2P mark waits for the Insights shell. Logos are served from the Maps site rather than copied into Superset. ([`7d6c08a`](https://gitlab.com/openg2p/g2p-insights/-/commit/7d6c08a7c2192b4384f7789f92d5612e919f551a))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Package Insights as a standalone openg2p-insights chart with the central GitLab pipeline. Adds the missing backend deployment (its values rendered nothing), drops the bundled Superset and the inert appConfig ConfigMap, and fixes env vars that were silently ignored: the DB settings used the wrong prefix and field names, CONFIG_PATH was read by nothing, and VITE_EVIDENCE_URL was never set so the Maps tab reported no URL. Removes the NL chart-authoring feature, defaults the LLM to Sonnet 4.5, and makes the Maps surface pack-agnostic — it addressed levels as region/zone/woreda and so broke below the first level on the default Kamuntu pack. ([`5ba4f31`](https://gitlab.com/openg2p/g2p-insights/-/commit/5ba4f3161befec5f82ae4857f3966511f365da69))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fix Superset API auth under AUTH_OAUTH: authenticate via /api/v1/security/login with provider=db (POST /login/ is a browser redirect there and 405s), probe /api/v1/me/ to reject a JWT that authenticates but is demoted to anonymous on list endpoints, keep session login as the AUTH_DB fallback, and carry the CSRF session cookie. Login failures now name the cause. ([`37d0c99`](https://gitlab.com/openg2p/g2p-insights/-/commit/37d0c99db7d50a609439565b60c40cf4f8775d63))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Sync the Evidence map assets from a country pack instead of hand-copied GeoJSON (the copies had already drifted and lacked the ring-validity fix). sync_pack.py copies boundaries, clears assets from a deselected pack, and generates the attribution block from manifest.json — COD-AB credited, Kamuntu flagged fictitious. ([`d8dd43f`](https://gitlab.com/openg2p/g2p-insights/-/commit/d8dd43f4a443a04a5ba369b5be430da93f0fb1de))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Point the Evidence Maps surface at live NSR data with click-driven drill-down. ([`ed9740d`](https://gitlab.com/openg2p/g2p-insights/-/commit/ed9740d39881c96c39df43db1289354608ab6010))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Compressed the Dashboards chrome (dropped our duplicate title, page heading and Refresh — Superset supplies all three — and moved "Edit in Superset" into a single slim toolbar), narrowed the left nav to 168px, and retitled the Evidence surface to "Maps". Fixed NL chart authoring producing unrenderable charts on Superset 6.1: map bar/line onto the ECharts viz types (NVD3's dist_bar/line are gone), emit ECharts-shaped form_data (metrics list + x_axis), and send extracted aggregates as adhoc metrics so they resolve instead of 400ing against the dataset's saved-metric list. ([`c8ad053`](https://gitlab.com/openg2p/g2p-insights/-/commit/c8ad0530fb75b175c9b41ad431466cc2c44452d5))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Applied OpenG2P branding to the Maps and Dashboards surfaces: Evidence now hides its own header/wordmark, breadcrumbs and sidebar via frontmatter (full-width, light-pinned) and uses Roboto/Roboto Slab with brand chrome colours; Superset picks up brand tokens through the 6.x THEME_DEFAULT system (yellow primary, blue links, Roboto via fontUrls, single light theme). Chart series and map choropleth palettes deliberately left alone. ([`6129296`](https://gitlab.com/openg2p/g2p-insights/-/commit/612929673372b4f516d8082cbecb401bef518a84))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Made the AI/PII pipeline an opt-in Docker build (INSTALL_AI arg + `make up-ai`) and corrected the misleading spaCy/ANTHROPIC setup docs; the lean image runs drill-down and Ask with graceful fallbacks. ([`ec5f3e3`](https://gitlab.com/openg2p/g2p-insights/-/commit/ec5f3e3b80e95efe51358c6419c7b3e317305cf4))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Switched the LLM integration to OpenRouter-only (removed Anthropic SDK, provider config and key plumbing); made Superset opt-in in the test stack and fixed silently-ignored INSIGHT_ env prefixes in the Helm chart. ([`870a587`](https://gitlab.com/openg2p/g2p-insights/-/commit/870a58729098f945b9f6ed87ea35af9052abddce))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Made Superset opt-in (compose profile) so the test stack runs lean on a laptop, and fixed silently-ignored INSIGHT_ env var prefixes in the Helm chart. ([`b8e6ca3`](https://gitlab.com/openg2p/g2p-insights/-/commit/b8e6ca371451b73a18288613e89bf3277df699d5))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Added a stdlib mock Master Data Service to the test stack so the platform runs fully locally with no external MDS dependency. ([`3e2e2ac`](https://gitlab.com/openg2p/g2p-insights/-/commit/3e2e2ac48a388f13aac7eb0e6cab806b9d70ab80))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Bundled OpenG2P-branded Superset into the Insight chart, added country-agnostic hierarchical drill-down (engine, API and Expert Lab renderer), AI disable switch and master-data change spec. ([`4033a56`](https://gitlab.com/openg2p/g2p-insights/-/commit/4033a565299f0caf4c5886415512d93743db3883))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Bundled OpenG2P-branded Superset into the Insight chart, added country-agnostic hierarchical drill-down engine, AI disable switch and master-data change spec. ([`439d26c`](https://gitlab.com/openg2p/g2p-insights/-/commit/439d26c56fcae57d5c21b79b4e261a7148d0fe8f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Bundled OpenG2P-branded Superset into the Insight chart, added hierarchical drill-down engine, AI disable switch and master-data change list. ([`677c300`](https://gitlab.com/openg2p/g2p-insights/-/commit/677c300160db3bb7651c17da66fa094e4f850086))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Dashboard update. ([`3d6870c`](https://gitlab.com/openg2p/g2p-insights/-/commit/3d6870c14be04c6d4975180247620cf0b6109f1c))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several fixes. ([`dc72aea`](https://gitlab.com/openg2p/g2p-insights/-/commit/dc72aeaca60f25fffbd917e85b2be64852d20c96))
-  [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several improvements to get better SQL resolution by the LLM. ([`f5839f8`](https://gitlab.com/openg2p/g2p-insights/-/commit/f5839f8984563f3a3cb2b52521b64b1e173492e4))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Doc enhanced ([`fbb8c40`](https://gitlab.com/openg2p/g2p-insights/-/commit/fbb8c4020f48dbbb95eda7b595b0e801cca28337))
-  [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Doc enhanced ([`b755a55`](https://gitlab.com/openg2p/g2p-insights/-/commit/b755a55c9509cf58ae5cddf1fd5370e940bd5845))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Onboarding scripts enhanced to look at DB and extensions both. ([`94f26eb`](https://gitlab.com/openg2p/g2p-insights/-/commit/94f26eb4b5700f050fdd1d398807dd4c4cc78ee3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Onboarding scripts enhanced to look at DB and extensions both. ([`ad3a1b7`](https://gitlab.com/openg2p/g2p-insights/-/commit/ad3a1b7e65df02367b19651f841dacbff6182b74))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Onboarding scripts enhanced. ([`89b2448`](https://gitlab.com/openg2p/g2p-insights/-/commit/89b2448228f1bd109c7d2899ba14e92f35a4e557))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several enhancements for superset. ([`9e83b2e`](https://gitlab.com/openg2p/g2p-insights/-/commit/9e83b2e2b005f28505197a8f4c19eed3080ff94f))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several enhancements for superset. ([`5166862`](https://gitlab.com/openg2p/g2p-insights/-/commit/5166862b4c4b1f4aaf803918de0e225481620db1))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Superset integration related changes. ([`d1392d2`](https://gitlab.com/openg2p/g2p-insights/-/commit/d1392d2b16bb43134c28ece39f2cb7d6646ab689))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Decimals reduced. ([`7103bdc`](https://gitlab.com/openg2p/g2p-insights/-/commit/7103bdc7aa8de8c5b28fd85069251304ee9071b3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Script to onboard new database added - to create materialized views. ([`a20216e`](https://gitlab.com/openg2p/g2p-insights/-/commit/a20216e8a37489dd64b3502e16c9e5a62ad3dfb7))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) More context sent to LLM under Ask. Few fixes. ([`73bbb1b`](https://gitlab.com/openg2p/g2p-insights/-/commit/73bbb1bb9d806932fcb310efc96d96076db06c9e))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Expert Lab enhanced by adding pre-built common statistical functions. ([`c7e462d`](https://gitlab.com/openg2p/g2p-insights/-/commit/c7e462df2234afd91c7ac7e61e6a9cb9ab17a7d8))
-  [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fixes, enhancements. ([`8e3a355`](https://gitlab.com/openg2p/g2p-insights/-/commit/8e3a35584f4ec15cecef46d0b265419420285c85))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Several additions. ([`838f445`](https://gitlab.com/openg2p/g2p-insights/-/commit/838f445b9f151d2797833bd76b47ac2fd4247d95))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Integration with local superset. ([`13a3365`](https://gitlab.com/openg2p/g2p-insights/-/commit/13a33656d15364598b1c2f2cd3198216f237e6d3))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Fixed few issues. ([`c904390`](https://gitlab.com/openg2p/g2p-insights/-/commit/c904390eb078edb94672806332f919fc3ed3a8cf))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Base coded added. WIP. ([`4da595d`](https://gitlab.com/openg2p/g2p-insights/-/commit/4da595d16a371e506c2e35573a6ec2cd8b444687))
- [G2P-4804](https://openg2p.atlassian.net/browse/G2P-4804) Concept note. ([`ae53616`](https://gitlab.com/openg2p/g2p-insights/-/commit/ae53616693b1200e4c822d78e20662b732770c2c))
- Initial commit ([`8d20683`](https://gitlab.com/openg2p/g2p-insights/-/commit/8d206833d025c30b4c7d540ee66909edc9881abb))

---

> **What's shown here.** This catalogue lists **every stable release**, plus
> the **latest 20 develop builds** and the **latest 10 release
> candidates** per release line -- candidates are KEPT after their release
> ships, as the audit trail of the release run. Older develop builds and
> release candidates are pruned as they are superseded. Those versions
> still exist in the container and Helm
> registries — they are simply not listed here. This page is generated
> automatically from commit history; do not edit it by hand.
