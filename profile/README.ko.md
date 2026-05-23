<div align="center">
  <img src="./assets/banner.png" alt="DevsLab — 당신의 SaaS, 우리가 만듭니다." />
</div>

<p align="center">
  <a href="https://devslab.kr">🌐 devslab.kr</a> ·
  <a href="mailto:support@devslab.kr?subject=DevsLab%20프로젝트%20문의">📬 support@devslab.kr</a> ·
  <a href="./README.md">🇺🇸 English</a>
</p>

---

```bash
$ npx create-saas @devslab/starter
→ 멀티테넌트 아키텍처 셋업...
→ 인증·결제·권한 구성...
→ 관측성 스택 연결...
→ AI 통합 레이어 준비...
✓ 견고한 SaaS 기반 완성
```

## `// who we are`

한국 기반의 작은 스튜디오. **아키텍처, 풀스택 · 모바일, AI 통합**을 한 팀에서.
유행 따라 흔들리지 않습니다. 운영 환경에서 증명된 것만 사용합니다.

MVP부터 엔터프라이즈까지, 첫 사용자를 만날 때까지 함께합니다.

## `// what we ship`

| `[01]` | **확장 가능한 설계** — 멀티테넌시 · 인증 · 결제 · 관측성 |
|--------|------------------------------------------------------------|
| `[02]` | **엔드투엔드 개발** — Next.js · Vue · Node · Spring Boot · Cloud Native |
| `[03]` | **AI 통합** — LLM · RAG · 에이전트 워크플로우 |
| `[04]` | **하이브리드 + 네이티브 모바일** — Ionic + Vue · Flutter · Jetpack Compose |
| `[05]` | **오픈소스 인프라** — 우리 SaaS에서 먼저 쓰고 커뮤니티와 공유 |

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

우리 SaaS에서 먼저 검증하고 Maven Central `kr.devslab` 좌표로 공유합니다.

- 🛡️ **[ssrf-guard](https://github.com/devslab-kr/ssrf-guard)** &nbsp;`3.0.1` — JVM용 SSRF 방어. 화이트리스트 + IP 우회 차단 (10진수·16진수·8진수·IPv6 난독화) + 리다이렉트 재검증을 9개 HTTP 클라이언트 모듈 (RestClient · RestTemplate · WebClient · Feign · OkHttp · JDK HttpClient · Apache HttpClient 5)에 동시 적용. **`-springai` 모듈은 LLM 에이전트의 툴 URL 검증** — `ToolCallback` 기반 에이전트의 `fetch_url` 류 새 SSRF 표면 대응.
- 🪶 **[easy-paging-spring-boot-starter](https://github.com/devslab-kr/easy-paging-spring-boot-starter)** &nbsp;`0.4.0` — Spring Boot + MyBatis용 어노테이션 기반 페이지네이션. Offset (`@AutoPaginate`)과 cursor/keyset (`@KeysetPaginate`)을 하나의 스타터로. WebFlux + R2DBC용 자매 아티팩트 (`-reactive`)는 wire에서 동일한 JSON 봉투.
- 📜 **[api-log](https://github.com/devslab-kr/api-log)** &nbsp;`0.6.0` — Spring Boot용 이벤트 드리븐 API 로깅, PostgreSQL JSONB 저장. 멀티모듈 구성: `api-log-core` + 영속성 드라이버 (`-jpa`, `-r2dbc`, `-mybatis`).
- 🧪 **[devslab-examples](https://github.com/devslab-kr/devslab-examples)** — 위 라이브러리 모든 모듈의 실행 가능한 Spring Boot 데모 9개, 이중언어 README. Clone, `./gradlew bootRun`, curl. 스모크 테스트 포함.

```
$ ./talk-to-the-maintainers
```

질문, 아이디어, 사용 사례 공유는 [**devslab-examples Discussions**](https://github.com/devslab-kr/devslab-examples/discussions)에서 — 라이브러리 만든 메인테이너가 직접 답변. 영/한 둘 다 환영.

## `// partners`

- **[XunyaTech](https://xunya.tech)** — 성장하는 기업을 위한 사이버보안 우선 관리형 IT

## `// say hi`

```bash
$ ./contact --send
```

- 📬 [support@devslab.kr](mailto:support@devslab.kr?subject=DevsLab%20프로젝트%20문의)
- 🌐 [devslab.kr](https://devslab.kr) — 14개 언어 지원

<sub>© DevsLab · Built in Seoul</sub>
