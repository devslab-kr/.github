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

우리 SaaS에서 먼저 검증하고 커뮤니티와 공유합니다 — Spring Boot 라이브러리는 Maven Central(`kr.devslab`), TypeScript 패키지는 npm, 독립 실행 도구는 GitHub Releases로.

- 🛡️ **[ssrf-guard](https://github.com/devslab-kr/ssrf-guard)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/ssrf-guard)](https://central.sonatype.com/artifact/kr.devslab/ssrf-guard) — JVM용 SSRF 방어. 화이트리스트 + IP 우회 차단 (10진수·16진수·8진수·IPv6 난독화) + 리다이렉트 재검증을 9개 HTTP 클라이언트 모듈 (RestClient · RestTemplate · WebClient · Feign · OkHttp · JDK HttpClient · Apache HttpClient 5)에 동시 적용. **`-springai` / `-langchain4j` 모듈은 LLM 에이전트의 툴 URL 검증** — Spring AI `ToolCallback`, LangChain4j `ToolExecutor` 기반 에이전트의 `fetch_url` 류 새 SSRF 표면 대응. GraalVM native-image 힌트와 WebClient용 reactor-netty DNS-time 가드도 포함.
- 🛡️ **[ssrf-guard-js](https://github.com/devslab-kr/ssrf-guard-js)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fssrf-guard-js)](https://www.npmjs.com/package/@devslab/ssrf-guard-js) — ssrf-guard의 JS/TS 자매 라이브러리, 같은 핵심 보안 모델을 Node**와 edge 런타임**으로 이식: URL 시점 검증 (스킴 · 호스트 허용목록 · 포트 · userinfo · IP 리터럴), 사설망 IP 분류, LLM/툴콜 JSON 내 숨은 URL 스캔, 그리고 두 가지 guarded fetch — `safeFetch` (Node: DNS 검사 + optional `undici` DNS pinning), `guardedFetch` (Cloudflare Workers/브라우저: allowlist 우선 정책의 리다이렉트 재검증, 자기 사이트 크롤링용 `sameSitePolicy` 포함). 문서: [devslab-kr.github.io/ssrf-guard-js](https://devslab-kr.github.io/ssrf-guard-js/).
- 🪶 **[easy-paging-spring-boot-starter](https://github.com/devslab-kr/easy-paging-spring-boot-starter)** &nbsp;[![Spring Boot 4](https://img.shields.io/maven-central/v/kr.devslab/easy-paging-spring-boot-starter?label=Spring%20Boot%204&versionPrefix=4)](https://central.sonatype.com/artifact/kr.devslab/easy-paging-spring-boot-starter) · [![SB3 maintenance](https://img.shields.io/maven-central/v/kr.devslab/easy-paging-spring-boot-starter?label=SB3%20maintenance&versionPrefix=3)](https://central.sonatype.com/artifact/kr.devslab/easy-paging-spring-boot-starter) — Spring Boot + MyBatis용 어노테이션 기반 페이지네이션. Offset (`@AutoPaginate`)과 cursor/keyset (`@KeysetPaginate`)을 하나의 스타터로. WebFlux + R2DBC용 자매 아티팩트 (`-reactive`)는 wire에서 동일한 JSON 봉투. 라이브러리 메이저가 Spring Boot 메이저와 일치 ([버전 정책](https://github.com/devslab-kr/.github/blob/main/.github/VERSIONING.md#한국어) 참조): `4.x` 라인은 **Spring Boot 4 / Spring Framework 7 / Jackson 3** 대상이며, `3.x` [maintenance 브랜치](https://github.com/devslab-kr/easy-paging-spring-boot-starter/tree/3.x)가 SB 3.3–3.5에 대한 보안 패치를 계속 제공합니다.
- 📜 **[api-log](https://github.com/devslab-kr/api-log)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/api-log-core)](https://central.sonatype.com/artifact/kr.devslab/api-log-core) — Spring Boot용 이벤트 드리븐 API 로깅, PostgreSQL JSONB 저장. 멀티모듈 구성: `api-log-core` + 영속성 드라이버 (`-jpa`, `-r2dbc`, `-mybatis`) — 모두 같은 버전 라인. 라이브러리 메이저가 타겟 Spring Boot 메이저와 일치 ([버전 정책](https://github.com/devslab-kr/.github/blob/main/.github/VERSIONING.md#한국어) 참조).
- 🧰 **[devslab-kit](https://github.com/devslab-kr/devslab-kit)** &nbsp;[![Maven Central](https://img.shields.io/maven-central/v/kr.devslab/devslab-kit-spring-boot-starter)](https://central.sonatype.com/artifact/kr.devslab/devslab-kit-spring-boot-starter) — 인증, RBAC+그룹+ABAC, 멀티테넌시, 동적 메뉴, 감사 로깅, 환경 간 설정 동기화, 관리자 REST API를 자동 구성으로 제공하는 Spring Boot 4 플랫폼 스타터. 전체 문서는 [devslab-kit.devslab.kr](https://devslab-kit.devslab.kr).
- 🔌 **[datalinq](https://github.com/devslab-kr/datalinq)** &nbsp;[![Release](https://img.shields.io/github/v/release/devslab-kr/datalinq)](https://github.com/devslab-kr/datalinq/releases/latest) — [TamboUI](https://github.com/tamboui/tamboui) 기반의 관례 주도 크로스벤더 JDBC **데이터 마이그레이션 TUI**: `sql/` 에 폴더만 떨구면 메뉴가 됩니다. SQL Server / MariaDB-MySQL / PostgreSQL 번들(Oracle / H2 / SQLite 는 `driver` 한 줄 다운로드), ETL / SCRIPT / 커스텀 HANDLER 작업, **기본 dry-run**. 라이브러리가 아닌 독립 실행 CLI 도구 — [jbang](https://www.jbang.dev/) 으로 설치: `jbang app install datalinq@devslab-kr/datalinq`.
- ⌨️ **[kokey](https://github.com/devslab-kr/kokey)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fkokey)](https://www.npmjs.com/package/@devslab/kokey) — 자판 오입력 복원 라이브러리. 한국어 두벌식은 완전한 IME 오토마타(겹모음/겹받침, 받침 넘김)로 기본 내장, 여기에 러시아어 ЙЦУКЕН·우크라이나어·히브리어·그리스어(dead key)·태국어 Kedmanee·아랍어·조지아어 7종 지원. 스크립트 자동 감지(`toEn('안녕 привет')`), 스스로 복원되는 `data-kokey` DOM 레이어, React/Vue controlled 인풋용 `KokeyInput` 컴포넌트까지. Zero-dependency TypeScript, ESM/CJS 듀얼, 9개 언어 README. 한글 IME가 켜진 채 들어온 바코드 스캐너 입력을 복원하다 태어난 라이브러리.
- 🔢 **[numkey](https://github.com/devslab-kr/numkey)** &nbsp;[![npm](https://img.shields.io/npm/v/%40devslab%2Fnumkey)](https://www.npmjs.com/package/@devslab/numkey) — "문자열인데 숫자"인 필드를 위한 숫자 인풋 포맷팅: 커서가 튀지 않는 실시간 천 단위 콤마, 구분자 건너뛰는 원터치 삭제, 앞자리 0 정리, 전각 숫자 정규화, 오른쪽 정렬 + `inputmode` 자동 설정, blur 시에만 적용되는 min/max, 문자열 우선 정식 값 모델(금액 안전 — IEEE 754를 거치지 않음). **한국형 금액 UX 내장**: 실시간 한글 병기(`1500000` → "150만"), 만/억 축약 입력(`3만5천` → 35,000, IME 안전), 그리고 클래식 JSP/PHP 폼 POST가 깨끗한 숫자를 전송하게 하는 hidden 정식 값 동기화. `Intl` 로케일 구분자는 옵트인, CDN 스크립트 태그 한 줄 + `data-numkey` 자동 초기화로 빌드 도구 없이 동작, Vue 3 / React용 `NumkeyInput` 컴포넌트 포함. kokey의 형제 — "-key" 인풋 패밀리. 라이브 데모: [devslab-kr.github.io/numkey](https://devslab-kr.github.io/numkey/).
- 🧪 **[devslab-examples](https://github.com/devslab-kr/devslab-examples)** — 위 라이브러리 모든 모듈의 실행 가능한 Spring Boot 데모 19개 (easy-paging SB4 4개 + easy-paging SB3 maintenance 4개 + ssrf-guard 8개 — HTTP 클라이언트, LLM 프레임워크, GraalVM 네이티브 이미지 전반 + api-log 영속 백엔드 3개 — JPA / R2DBC / MyBatis), 이중언어 README. Clone, `./gradlew bootRun`, curl. 스모크 테스트 포함.

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
