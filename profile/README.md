<div align="center">
  <img src="https://raw.githubusercontent.com/devslab-kr/.github/main/profile/assets/banner.png" alt="DevsLab — We build your SaaS." />
</div>

<p align="center">
  <a href="https://devslab.kr">🌐 devslab.kr</a> ·
  <a href="https://devslab-kr.github.io/">Products, demos &amp; docs</a> ·
  <a href="mailto:support@devslab.kr?subject=DevsLab%20Project%20Inquiry">📬 support@devslab.kr</a> ·
  <a href="https://github.com/devslab-kr/.github/blob/main/profile/README.ko.md">🇰🇷 한국어</a>
</p>

<!-- publisher:start -->
Published by [데브스랩(DevsLab)](https://devslab.kr/).
<!-- publisher:end -->

---

**Explore DevsLab:** [Company and products](https://devslab.kr/) · [Open source and live demos](https://devslab-kr.github.io/) · [GitLinq for Windows](https://devslab.kr/products/gitlinq/) · [Public repositories](https://github.com/orgs/devslab-kr/repositories?type=public)

## `// who we are`

We're a Korea-based studio building SaaS products, desktop applications, and open-source developer tools —
**architecture, full-stack & mobile, AI integration** in one team.

MVP to enterprise, we own every stage all the way to your first users.

## `// what we ship`

| `[01]` | **Scalable Architecture** — Multi-tenant · Auth & Billing · Observability · AIOps |
|--------|----------------------------------------------------------------------------|
| `[02]` | **Full-Stack Development** — Spring Boot · Spring Cloud · Node · TanStack Start · SolidJS · Next.js · Cloud Native |
| `[03]` | **AI Integration** — LLM orchestration · RAG pipelines · Agentic workflows |
| `[04]` | **Hybrid + Native Mobile** — Ionic + Vue · Flutter · Jetpack Compose |
| `[05]` | **Open-Source Infra** — Production-proven tools, shared with the community |
| `[06]` | **Desktop Applications** — Windows tools for developer and operations workflows |

## `// stack we trust`

```
frontend  TanStack Start · SolidJS · React · Next.js · Vue · HTMX · TypeScript · WASM · Tailwind
mobile    Ionic · Flutter · Capacitor · Kotlin · Jetpack Compose
desktop   Electron · Go · Wails · React
backend   Spring Boot · Spring Cloud · Spring Security · Node.js · tRPC · Postgres · Redis · Drizzle
cloud     AWS · Cloudflare · Vercel · CloudType · Supabase · Firebase
devops    Docker · GitHub Actions · Grafana · Prometheus · Sentry · PostHog
ai        Claude · GPT · Llama · Mistral · Qwen · Gemma · Spring AI · LangChain · pgvector
ai eng    RAG · MCP · Agent Runtime · Evals · Fine-Tuning · LoRA · Distillation
```

## `// products & client work`

Business tools, developer software, and systems we build and operate. The status below follows each product's public introduction.

| Product | What it does | Availability |
| --- | --- | --- |
| **[AskLinq](https://getasklinq.app)** | QR and link-based AI assistance grounded in registered materials, with handoff to a person. | Free beta |
| **[GitLinq](https://devslab.kr/products/gitlinq/)** | Windows Git client for SVN users: author-first logs, selective change cancellation, repository updates, and Git setup. | Preview · [Installer & portable ZIP](https://github.com/devslab-kr/gitlinq-releases/releases/latest) · [Beginner guide (Korean)](https://devslab.kr/products/gitlinq/docs/) |
| **[TraceLinq](https://gettracelinq.app/)** | Local visibility, recovery, and replay for Claude Code and Codex work. | Early access |
| **[BookLinq](https://getbooklinq.app/)** | WhatsApp-centered booking for local businesses, including availability and customer reminders. | Preparing for launch |
| **[VisionLinq](https://getvisionlinq.app/)** | Document AI API that structures images, PDFs, and office documents into text and fields with source references. | Preparing for launch |
| **Chatur-AI** | Voice AI for Indian call centers, developed with an operating partner. | In development |
| **SphereLinq** | A company-wide Agentic OS that connects team and company knowledge and applies shared rules and harnesses across AI agents. | In design |
| **EDS Logistics** | A client system for dental-logistics pickup, dispatch, driver routes, and settlement. | In operation |
| **[EDS Desktop](https://github.com/jlc488/eds-desktop-releases)** | Windows emergency scan console for pickup and delivery operations. | [Installer & portable EXE](https://github.com/jlc488/eds-desktop-releases/releases/latest) |
| **FM Dental Service** | A client system for Busan-area same-day dental-prosthetics pickup and delivery. | In operation |

GitLinq application source is private; [downloads, release notes, and issues](https://github.com/devslab-kr/gitlinq-releases) are public. Daily server commits and direct conflict editing are still in development.

EDS Desktop is distributed through a public release repository while its application source remains private. The installer supports automatic updates; the portable EXE does not.

[More about our products and client work](https://devslab.kr/).

## `// open source`

[Browse live demos and documentation](https://devslab-kr.github.io/) for our libraries and tools.

Battle-tested in our own SaaS first, then shared with the community — Spring Boot libraries on Maven Central (`kr.devslab`), TypeScript packages on npm, standalone tools as GitHub Releases.

- 🛡️ **[ssrf-guard](https://github.com/devslab-kr/ssrf-guard)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/ssrf-guard)](https://central.sonatype.com/artifact/kr.devslab/ssrf-guard) — SSRF defense for the JVM. Whitelist + IP-bypass hardening (decimal/hex/octal/IPv6 obfuscation) + redirect re-validation across 9 HTTP-client modules (RestClient · RestTemplate · WebClient · Feign · OkHttp · JDK HttpClient · Apache HttpClient 5). Includes **`-springai` and `-langchain4j` for LLM-agent tool URL validation** — the new SSRF surface for `fetch_url`-style tools in Spring AI `ToolCallback` and LangChain4j `ToolExecutor` agents. Plus GraalVM native-image hints and reactor-netty DNS-time guards for WebClient.
- 🛡️ **[ssrf-guard-js](https://github.com/devslab-kr/ssrf-guard-js)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fssrf-guard-js)](https://www.npmjs.com/package/@devslab/ssrf-guard-js) — The JS/TS sibling of ssrf-guard, porting the same core security model to Node **and edge runtimes**: URL-time validation (scheme · host allowlist · port · userinfo · IP-literal), private-network IP classification, LLM/tool-call JSON scanning for hidden URLs, and two guarded fetches — `safeFetch` (Node: DNS checks + optional `undici` DNS pinning) and `guardedFetch` (Cloudflare Workers / browsers: redirect revalidation with allowlist-first policies, incl. `sameSitePolicy` for crawl-your-own-site flows). Docs at [devslab-kr.github.io/ssrf-guard-js](https://devslab-kr.github.io/ssrf-guard-js/).
- 🪶 **[easy-paging-spring-boot-starter](https://github.com/devslab-kr/easy-paging-spring-boot-starter)** &nbsp;[![Spring Boot 4](https://img.shields.io/maven-central/v/kr.devslab/easy-paging-spring-boot-starter?label=Spring%20Boot%204&versionPrefix=4)](https://central.sonatype.com/artifact/kr.devslab/easy-paging-spring-boot-starter) · [![SB3 maintenance](https://img.shields.io/maven-central/v/kr.devslab/easy-paging-spring-boot-starter?label=SB3%20maintenance&versionPrefix=3)](https://central.sonatype.com/artifact/kr.devslab/easy-paging-spring-boot-starter) — Annotation-driven pagination for Spring Boot + MyBatis. Offset (`@AutoPaginate`) and cursor/keyset (`@KeysetPaginate`) in one starter. Reactive companion artifact (`-reactive`) for WebFlux + R2DBC, identical JSON envelope on the wire. Library major matches Spring Boot major (see [versioning policy](https://github.com/devslab-kr/.github/blob/main/.github/VERSIONING.md)): `4.x` targets **Spring Boot 4 / Spring Framework 7 / Jackson 3**; the `3.x` [maintenance branch](https://github.com/devslab-kr/easy-paging-spring-boot-starter/tree/3.x) keeps SB 3.3–3.5 supported with security patches.
- 📜 **[api-log](https://github.com/devslab-kr/api-log)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/api-log-core)](https://central.sonatype.com/artifact/kr.devslab/api-log-core) — Event-driven API logging for Spring Boot, PostgreSQL JSONB storage. Multi-module: `api-log-core` plus persistence drivers (`-jpa`, `-r2dbc`, `-mybatis`) — all on the same version line. Library major matches the Spring Boot major it targets (see [versioning policy](https://github.com/devslab-kr/.github/blob/main/.github/VERSIONING.md)).
- 🧰 **[devslab-kit](https://github.com/devslab-kr/devslab-kit)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/devslab-kit-spring-boot-starter)](https://central.sonatype.com/artifact/kr.devslab/devslab-kit-spring-boot-starter) — Spring Boot 4 platform starter — authentication, RBAC + groups + ABAC, multi-tenancy, dynamic menus, audit logging, config sync across environments, and an admin REST API, all from auto-configuration. Full docs at [devslab-kit.devslab.kr](https://devslab-kit.devslab.kr).
- 🔌 **[datalinq](https://github.com/devslab-kr/datalinq)** &nbsp;[![Release](https://img.shields.io/github/v/release/devslab-kr/datalinq)](https://github.com/devslab-kr/datalinq/releases/latest) — Convention-driven, cross-vendor JDBC **data-migration TUI** built on [TamboUI](https://github.com/tamboui/tamboui): drop a folder under `sql/`, get a menu. SQL Server / MariaDB-MySQL / PostgreSQL bundled (Oracle / H2 / SQLite one `driver` download away); ETL / SCRIPT / custom HANDLER operations, **dry-run by default**. A standalone CLI tool (not a Maven library) — install with [jbang](https://www.jbang.dev/): `jbang app install datalinq@devslab-kr/datalinq`.
- ⌨️ **[kokey](https://github.com/devslab-kr/kokey)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fkokey)](https://www.npmjs.com/package/@devslab/kokey) — Wrong-keyboard-layout text restorer. Korean Dubeolsik built in with a full IME automaton (compound vowels/finals, carry-over), plus 7 table-driven layouts — Russian ЙЦУКЕН, Ukrainian, Hebrew, Greek (dead keys), Thai Kedmanee, Arabic (lam-alef), Georgian — with per-script auto-detection (`toEn('안녕 привет')`), a self-healing `data-kokey` DOM layer, adapters for Vue / React / Svelte / Solid (`KokeyInput` components, `use:kokey` action/directive), heuristic paste auto-correction (`fixMistyped`, `data-kokey-paste`), and an in-field suggest button that offers a fix instead of making one (`bindSuggest`, `data-kokey-suggest`) — the same button its browser extension puts on every site. Zero-dependency TypeScript, ESM/CJS dual, localized READMEs in 9 languages. Born from rescuing barcode-scanner input typed while the Korean IME was on.
- 🔢 **[numkey](https://github.com/devslab-kr/numkey)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fnumkey)](https://www.npmjs.com/package/@devslab/numkey) — Numeric input formatting for "it's a string, but it's a number" fields: live thousands grouping with a caret that stays put, one-keystroke deletion across separators, leading-zero cleanup, full-width digit normalization, automatic right-align + `inputmode`, blur-only min/max, and a string-first canonical value model (money-safe — never IEEE 754). **Korean amount UX built in**: live 한글 병기 (`1500000` → "150만"), 만/억 shorthand entry (`3만5천` → 35,000, IME-safe), and a hidden-input canonical sync so classic JSP/PHP form POSTs submit clean numbers. Opt-in locale formatting via `Intl` (separators **and** group sizes — Indian lakh/crore `12,34,56,789` included); one CDN script tag with `data-numkey` auto-init — no build step — plus adapters for Vue 3 / React / Svelte / Solid (`NumkeyInput` components, `use:numkey` action/directive). Accounting negatives (`(1,234)`) paste correctly. kokey's sibling in the "-key" input family. Live demo at [devslab-kr.github.io/numkey](https://devslab-kr.github.io/numkey/).
- 📅 **[vue-date-rail](https://github.com/devslab-kr/vue-date-rail)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fvue-date-rail)](https://www.npmjs.com/package/@devslab/vue-date-rail) — Horizontal **infinite-scroll date rail** (day / month strip) picker for Vue 3 — the calendar-strip pattern delivery, booking, and scheduling apps use instead of a calendar popup. Infinite scroll with scroll-position compensation (no jump when past dates prepend), headless `useDateRail()` core, `Intl`-based i18n (any BCP 47 locale, no locale files), min/max + disabled dates, a marker slot for event dots, desktop wheel/drag scrolling, CSS-variable theming, and Tailwind-ready `unstyled` + `data-*` state attributes. Battle-tested in our dental-logistics mobile app first. Live demo at [devslab-kr.github.io/vue-date-rail](https://devslab-kr.github.io/vue-date-rail/).
- 📏 **[editor-ruler](https://github.com/devslab-kr/editor-ruler)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Feditor-ruler)](https://www.npmjs.com/package/@devslab/editor-ruler) — **Word-like horizontal ruler** for web rich-text editors — the control every general-purpose WYSIWYG (Froala · TinyMCE · CKEditor 5 · Quill) ships without: left/right margin + first-line indent drag handles (hanging indent included), cm/in/px scales switchable at runtime, one undo boundary per gesture, keyboard-accessible ARIA slider handles, CSS-variable theming. **API stable since 1.0.** Guide lines with snapping, a vertical ruler (with a reservable gutter so toggling never reflows the content), and browser-language UI (ko/en) work on every adapter; Word-style whole-table indent and column-width markers come with the direct-DOM adapters. Editor-agnostic zero-dependency core (`@devslab/editor-ruler`) + four per-editor adapters — **`-froala`** and **`-summernote`** (direct-DOM plugins, both with table support), **`-tiptap`** (v2/v3 extension), and **`-ckeditor5`** (model-attribute plugin) — all with one-undo-step drags. CDN script-tag ready (`EditorRuler` global). Live playground at [devslab-kr.github.io/editor-ruler](https://devslab-kr.github.io/editor-ruler/).
- 🌐 **[locale-match](https://github.com/devslab-kr/locale-match)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Flocale-match)](https://www.npmjs.com/package/@devslab/locale-match) — **Locale negotiation that will not hand a Simplified Chinese reader your Traditional text.** A bare `zh` is silent about the one thing that matters, and a mainland browser sends `zh-CN,zh;q=0.9` — so refusing the precise tag hands the match to the vague one right behind it. Both traps are pinned by tests here. **Script guards** classify a tag as supported / unsupported / *unspecified* for one base language, under a two-tier rule: a single declared value (`?lang=`, a cookie) may leave the script unstated; an entry inside a ranked list may not. Chinese is built in and installed automatically from your own `supported` list; any other script-split language (Serbian, Mongolian, Punjabi, Kurdish, Uzbek) is a few lines with `defineScriptGuard`. The matcher also takes the sideways step strict RFC 4647 refuses, so `pt-PT` reaches your `pt-BR` instead of falling to English. Zero dependencies, ESM + CJS + a CDN-ready IIFE build, and bindings for **React** (hydration-safe), **Vue 3**, and **Nuxt** (resolves during SSR, so the page never changes language after it paints). Live playground at [devslab-kr.github.io/locale-match](https://devslab-kr.github.io/locale-match/).
- 🧪 **[devslab-examples](https://github.com/devslab-kr/devslab-examples)** — Runnable Spring Boot demos for easy-paging, ssrf-guard, and api-log (19 demos: 4 easy-paging SB4 + 4 easy-paging SB3 maintenance + 8 ssrf-guard across HTTP clients, LLM frameworks, and GraalVM native-image + 3 api-log persistence backends — JPA / R2DBC / MyBatis; bilingual READMEs). Clone, `./gradlew bootRun`, curl. Smoke tests included.

- 🖥️ **[devslab-kit-admin-ui](https://github.com/devslab-kr/devslab-kit-admin-ui)** — Vue 3 + PrimeVue admin console for devslab-kit, connected to its admin REST API.

Questions, ideas, sharing your application? Bilingual community in [**devslab-examples Discussions**](https://github.com/devslab-kr/devslab-examples/discussions) — same folks who write the libraries.

## `// design system & brand resources`

| Resource | Purpose |
| --- | --- |
| **[DDS](https://github.com/devslab-kr/dds)** | Shared design tokens, CSS, icons, and SolidJS primitives for DevsLab products. Source-available under the [DevsLab Source-Available License](https://github.com/devslab-kr/dds/blob/main/LICENSE). |
| **[@devslab/site-kit](https://github.com/devslab-kr/dds/tree/main/packages/site-kit)** | Product-site infrastructure for localization, SEO metadata, publisher attribution, and shared UI. Part of DDS under the same license. |
| **[linq-brand](https://github.com/devslab-kr/linq-brand)** | Official Linq product registry, brand assets, and usage guidelines. |
| **[oss-brand](https://github.com/devslab-kr/oss-brand)** | Brand assets and guidelines for DevsLab open-source projects. |

## `// partners`

- **[XunyaTech](https://xunya.tech)** — Cybersecurity-first managed IT for growing businesses
- **[EDS Logistics](https://www.eds8282.com)** — Same-day dental prosthetics logistics connecting labs and clinics
- **[FM Dental Service](https://www.fmdental2824.com)** — Busan-area same-day dental prosthetics pickup and delivery

## `// say hi`

- 📬 [support@devslab.kr](mailto:support@devslab.kr?subject=DevsLab%20Project%20Inquiry)
- 🌐 [devslab.kr](https://devslab.kr) — available in 14 languages

<sub>© DevsLab · Built in Seoul</sub>
