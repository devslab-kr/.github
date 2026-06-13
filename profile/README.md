<div align="center">
  <img src="./assets/banner.png" alt="DevsLab — We build your SaaS." />
</div>

<p align="center">
  <a href="https://devslab.kr">🌐 devslab.kr</a> ·
  <a href="mailto:support@devslab.kr?subject=DevsLab%20Project%20Inquiry">📬 support@devslab.kr</a> ·
  <a href="./README.ko.md">🇰🇷 한국어</a>
</p>

---

```bash
$ npx create-saas @devslab/starter
→ Setting up multi-tenant architecture...
→ Configuring auth, billing & permissions...
→ Wiring observability stack...
→ Preparing AI integration layer...
✓ A solid SaaS foundation, ready
```

## `// who we are`

We're a small Korea-based studio that builds SaaS products end-to-end —
**architecture, full-stack & mobile, AI integration** in one team.
No hype-chasing, no resume-driven design. Only what we have shipped to production.

MVP to enterprise, we own every stage all the way to your first users.

## `// what we ship`

| `[01]` | **Scalable Architecture** — Multi-tenant · Auth & Billing · Observability |
|--------|----------------------------------------------------------------------------|
| `[02]` | **Full-Stack Development** — Next.js · Vue · Node · Spring Boot · Cloud Native |
| `[03]` | **AI Integration** — LLM orchestration · RAG pipelines · Agentic workflows |
| `[04]` | **Hybrid + Native Mobile** — Ionic + Vue · Flutter · Jetpack Compose |
| `[05]` | **Open-Source Infra** — Production-proven tools, shared with the community |

## `// stack we trust`

```
frontend  Next.js · React · Vue · HTMX · TypeScript · Tailwind
mobile    Ionic · Flutter · Capacitor · Kotlin · Jetpack Compose
backend   Node.js · Spring Boot · tRPC · Postgres · Redis · Drizzle
cloud     AWS · Vercel · Cloudflare · CloudType · Supabase
devops    Docker · Grafana · Prometheus · Sentry · Firebase
ai        Anthropic · OpenAI · LangChain · pgvector
```

## `// open source`

Battle-tested in our own SaaS first, then shared with the community — Spring Boot libraries on Maven Central (`kr.devslab`), standalone tools as GitHub Releases.

- 🛡️ **[ssrf-guard](https://github.com/devslab-kr/ssrf-guard)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/ssrf-guard)](https://central.sonatype.com/artifact/kr.devslab/ssrf-guard) — SSRF defense for the JVM. Whitelist + IP-bypass hardening (decimal/hex/octal/IPv6 obfuscation) + redirect re-validation across 9 HTTP-client modules (RestClient · RestTemplate · WebClient · Feign · OkHttp · JDK HttpClient · Apache HttpClient 5). Includes **`-springai` and `-langchain4j` for LLM-agent tool URL validation** — the new SSRF surface for `fetch_url`-style tools in Spring AI `ToolCallback` and LangChain4j `ToolExecutor` agents. Plus GraalVM native-image hints and reactor-netty DNS-time guards for WebClient.
- 🪶 **[easy-paging-spring-boot-starter](https://github.com/devslab-kr/easy-paging-spring-boot-starter)** &nbsp;[![Spring Boot 4](https://img.shields.io/maven-central/v/kr.devslab/easy-paging-spring-boot-starter?label=Spring%20Boot%204&versionPrefix=4)](https://central.sonatype.com/artifact/kr.devslab/easy-paging-spring-boot-starter) · [![SB3 maintenance](https://img.shields.io/maven-central/v/kr.devslab/easy-paging-spring-boot-starter?label=SB3%20maintenance&versionPrefix=3)](https://central.sonatype.com/artifact/kr.devslab/easy-paging-spring-boot-starter) — Annotation-driven pagination for Spring Boot + MyBatis. Offset (`@AutoPaginate`) and cursor/keyset (`@KeysetPaginate`) in one starter. Reactive companion artifact (`-reactive`) for WebFlux + R2DBC, identical JSON envelope on the wire. Library major matches Spring Boot major (see [versioning policy](https://github.com/devslab-kr/.github/blob/main/.github/VERSIONING.md)): `4.x` targets **Spring Boot 4 / Spring Framework 7 / Jackson 3**; the `3.x` [maintenance branch](https://github.com/devslab-kr/easy-paging-spring-boot-starter/tree/3.x) keeps SB 3.3–3.5 supported with security patches.
- 📜 **[api-log](https://github.com/devslab-kr/api-log)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/api-log-core)](https://central.sonatype.com/artifact/kr.devslab/api-log-core) — Event-driven API logging for Spring Boot, PostgreSQL JSONB storage. Multi-module: `api-log-core` plus persistence drivers (`-jpa`, `-r2dbc`, `-mybatis`) — all on the same version line. Library major matches the Spring Boot major it targets (see [versioning policy](https://github.com/devslab-kr/.github/blob/main/.github/VERSIONING.md)).
- 🧰 **[devslab-kit](https://github.com/devslab-kr/devslab-kit)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/devslab-kit-spring-boot-starter)](https://central.sonatype.com/artifact/kr.devslab/devslab-kit-spring-boot-starter) — Spring Boot 4 platform starter — authentication, RBAC + groups + ABAC, multi-tenancy, dynamic menus, audit logging, config sync across environments, and an admin REST API, all from auto-configuration. Full docs at [devslab-kit.devslab.kr](https://devslab-kit.devslab.kr).
- 🔌 **[datalinq](https://github.com/devslab-kr/datalinq)** &nbsp;[![Release](https://img.shields.io/github/v/release/devslab-kr/datalinq)](https://github.com/devslab-kr/datalinq/releases/latest) — Convention-driven, cross-vendor JDBC **data-migration TUI** built on [TamboUI](https://github.com/tamboui/tamboui): drop a folder under `sql/`, get a menu. SQL Server / MariaDB-MySQL / PostgreSQL bundled (Oracle / H2 / SQLite one `driver` download away); ETL / SCRIPT / custom HANDLER operations, **dry-run by default**. A standalone CLI tool (not a Maven library) — install with [jbang](https://www.jbang.dev/): `jbang app install datalinq@devslab-kr/datalinq`.
- 🧪 **[devslab-examples](https://github.com/devslab-kr/devslab-examples)** — Runnable Spring Boot demos for every library above (19 demos: 4 easy-paging SB4 + 4 easy-paging SB3 maintenance + 8 ssrf-guard across HTTP clients, LLM frameworks, and GraalVM native-image + 3 api-log persistence backends — JPA / R2DBC / MyBatis; bilingual READMEs). Clone, `./gradlew bootRun`, curl. Smoke tests included.

```
$ ./talk-to-the-maintainers
```

Questions, ideas, sharing your application? Bilingual community in [**devslab-examples Discussions**](https://github.com/devslab-kr/devslab-examples/discussions) — same folks who write the libraries.

## `// partners`

- **[XunyaTech](https://xunya.tech)** — Cybersecurity-first managed IT for growing businesses

## `// say hi`

```bash
$ ./contact --send
```

- 📬 [support@devslab.kr](mailto:support@devslab.kr?subject=DevsLab%20Project%20Inquiry)
- 🌐 [devslab.kr](https://devslab.kr) — available in 14 languages

<sub>© DevsLab · Built in Seoul</sub>
