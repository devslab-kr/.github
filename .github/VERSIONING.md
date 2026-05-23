# Versioning Policy

**English** · [한국어](#한국어)

Applies to every library published under [`kr.devslab`](https://central.sonatype.com/namespace/kr.devslab) on Maven Central.

## The rule

**A library's major version number matches the Spring Boot major it targets.**

| Library major | Spring Boot major | Spring Framework | Notes |
| --- | --- | --- | --- |
| `3.x.y` | Spring Boot 3 | Spring Framework 6 | Java 17+ |
| `4.x.y` | Spring Boot 4 | Spring Framework 7 | Java 21+ (per Spring Boot 4) |
| `5.x.y` | Spring Boot 5 (when it ships) | TBD | TBD |

Minor and patch numbers follow regular [SemVer](https://semver.org) within a major line:

- **Minor** (`x.Y.z`) — new APIs, new features, backwards-compatible behaviour changes.
- **Patch** (`x.y.Z`) — bug fixes, security fixes, internal refactors with no API change.

## Why this rule

Spring Boot's own release cadence is the dominant signal in the JVM ecosystem we ship to. Aligning our majors with theirs has three concrete benefits:

1. **Reader clarity**. "I'm on Spring Boot 3 — which library version do I need?" answers itself: `3.x.y`. No version-matrix lookup, no FAQ entry, no Slack question.
2. **Dependabot correctness**. The standard `update-types: ["version-update:semver-major"]` ignore rule does exactly the right thing — it holds the SB3 demos on `3.x` and lets minor + patch updates flow. Without alignment we have to special-case (`versions: [">= X"]` filters) on every project that consumes us, which we just learned the hard way ([devslab-examples PR #50](https://github.com/devslab-kr/devslab-examples/pull/50)).
3. **Release-line longevity is obvious**. When Spring Boot 3 enters maintenance-only mode, our `3.x` line follows it. The contract reads off the version number.

## What this means in practice

- **Two active lines per library while two Spring Boot lines have upstream support.** Today: `3.x` (SB3) and `4.x` (SB4). When SB3 hits commercial-support-only (per [the official timeline](https://spring.io/projects/spring-boot#support)), we drop `3.x` to security-only maintenance.
- **Security fixes target every supported line.** A `3.x` security fix backports to `3.x`; an issue affecting both lines gets fixes on both. See [SECURITY.md](./SECURITY.md).
- **No 1.0 / 2.0 / 0.x history reuse.** Pre-1.0 versions of libraries that adopted this policy mid-stream (`easy-paging` `0.4.x` / `0.5.x` → `3.x` / `4.x`, `api-log` `0.6.x` → `3.x`) stay on Maven Central as historical artifacts but are deprecated. The renumbering is documented in each library's `CHANGELOG.md`.

## Counter-examples (not what this is)

This policy does **not** mean "version every library at the same number." Libraries on the same Spring Boot line can be at completely different minor / patch numbers:

```
ssrf-guard                              3.1.0
easy-paging-spring-boot-starter         3.0.0  ← same SB major, different lib state
easy-paging-spring-boot-starter         4.0.0  ← SB4 line
api-log                                 3.0.0
```

The only thing the policy fixes is the **major** number's meaning.

## When a library has no Spring Boot dependency

A few sub-modules in our libraries (e.g. `ssrf-guard-core`, `ssrf-guard-httpclient5`, `ssrf-guard-okhttp`, `ssrf-guard-jdkhttp`) have no Spring Boot dependency at all. They version along with their parent library — if `ssrf-guard` is at `3.1.0`, every sub-module is at `3.1.0`, even the Spring-free ones. The major number reflects "what Spring Boot major the project as a whole certifies against."

## Adopting the policy

A library on a pre-1.0 line that's effectively shipping the Spring-major-coupled scheme already (the `0.4.x → 0.5.x` pattern for SB3 → SB4) should re-publish the latest of each line as `<sb-major>.0.0`:

- `easy-paging 0.4.0` → `easy-paging 3.0.0` (same code, same artifact, new coordinates on Maven Central)
- `easy-paging 0.5.0` → `easy-paging 4.0.0`

The renumbering bump:
- Bumps `VERSION` in the repo
- Adds a `[3.0.0]` / `[4.0.0]` CHANGELOG entry documenting the alignment (with a pointer to this document)
- Tags + releases on GitHub (release notes link this document)
- Updates all consumer demos and the docs site

The previous `0.x` artifacts on Maven Central stay published — they don't disappear — but new releases land on the aligned line.

---

# <a id="한국어"></a>한국어

# 버전 정책

Maven Central [`kr.devslab`](https://central.sonatype.com/namespace/kr.devslab) 좌표로 발행되는 모든 라이브러리에 적용.

## 원칙

**라이브러리 메이저 버전은 타겟 Spring Boot 메이저와 일치한다.**

| 라이브러리 메이저 | Spring Boot 메이저 | Spring Framework | 비고 |
| --- | --- | --- | --- |
| `3.x.y` | Spring Boot 3 | Spring Framework 6 | Java 17+ |
| `4.x.y` | Spring Boot 4 | Spring Framework 7 | Java 21+ (Spring Boot 4 기준) |
| `5.x.y` | Spring Boot 5 (출시 시) | TBD | TBD |

마이너와 패치는 메이저 라인 내에서 표준 [SemVer](https://semver.org)를 따릅니다:

- **마이너** (`x.Y.z`) — 새 API, 새 기능, 후방호환 동작 변경
- **패치** (`x.y.Z`) — 버그픽스, 보안픽스, API 변경 없는 내부 리팩토링

## 왜 이 원칙인가

우리가 배포하는 JVM 생태계에서 Spring Boot의 릴리즈 사이클이 지배적 시그널입니다. 우리 메이저를 그 메이저에 정렬하면 구체적 이점 3가지:

1. **독자에게 명확함**. "Spring Boot 3을 쓰는데 어느 라이브러리 버전이 필요하지?" — 답이 자명: `3.x.y`. 버전 매트릭스 조회 불필요, FAQ 항목 불필요, Slack 질문 불필요.
2. **Dependabot 정확성**. 표준 `update-types: ["version-update:semver-major"]` ignore 규칙이 정확히 옳은 일을 함 — SB3 데모를 `3.x`에 잡아두고 minor + patch 업데이트만 통과. 정렬 없으면 우리를 의존하는 모든 프로젝트에서 특수 처리 (`versions: [">= X"]`) 필요. [devslab-examples PR #50](https://github.com/devslab-kr/devslab-examples/pull/50)에서 어렵게 배움.
3. **릴리즈 라인 수명이 명백**. Spring Boot 3이 maintenance-only로 진입하면 우리 `3.x` 라인도 따라감. 계약이 버전 숫자 자체에 박혀있음.

## 실무적 의미

- **두 Spring Boot 라인이 상위 지원받는 동안 라이브러리는 두 라인을 active 유지**. 오늘 기준: `3.x` (SB3), `4.x` (SB4). SB3가 [공식 타임라인](https://spring.io/projects/spring-boot#support)상 상용지원 전용으로 넘어가면 우리 `3.x`도 보안 패치만 유지로 격하.
- **보안 픽스는 지원 라인 전부에 적용**. `3.x` 보안 픽스는 `3.x`에 백포트, 두 라인 모두에 영향가는 이슈는 양쪽 다 픽스. [SECURITY.md](./SECURITY.md) 참고.
- **1.0 / 2.0 / 0.x 히스토리 재사용 없음**. 이 정책을 중간에 도입한 라이브러리의 pre-1.0 버전 (`easy-paging` `0.4.x` / `0.5.x` → `3.x` / `4.x`, `api-log` `0.6.x` → `3.x`)은 Maven Central에 historical artifact로 잔존하나 deprecated. 재번호링은 각 라이브러리의 `CHANGELOG.md`에 문서화.

## 반례 (이 정책이 아닌 것)

이 정책은 "모든 라이브러리를 같은 숫자로"가 **아닙니다**. 같은 Spring Boot 라인에 있어도 라이브러리들의 마이너 / 패치는 완전히 따로 갑니다:

```
ssrf-guard                              3.1.0
easy-paging-spring-boot-starter         3.0.0  ← 같은 SB 메이저, 다른 라이브러리 상태
easy-paging-spring-boot-starter         4.0.0  ← SB4 라인
api-log                                 3.0.0
```

이 정책이 고정하는 건 **메이저** 숫자의 의미뿐.

## 라이브러리가 Spring Boot 의존성이 아예 없을 때

우리 라이브러리의 일부 서브모듈 (예: `ssrf-guard-core`, `ssrf-guard-httpclient5`, `ssrf-guard-okhttp`, `ssrf-guard-jdkhttp`)은 Spring Boot 의존성이 전혀 없습니다. 이들은 부모 라이브러리와 함께 버전이 매겨집니다 — `ssrf-guard`가 `3.1.0`이면 Spring-free 서브모듈도 `3.1.0`. 메이저 숫자는 "프로젝트 전체가 인증하는 Spring Boot 메이저"를 반영.

## 정책 도입 방법

이미 Spring 메이저 결합 스킴을 비공식적으로 쓰던 pre-1.0 라이브러리 (SB3 → SB4를 `0.4.x → 0.5.x`로 표현하던 패턴) 은 각 라인의 최신을 `<sb-major>.0.0`으로 재발행:

- `easy-paging 0.4.0` → `easy-paging 3.0.0` (코드 동일, 아티팩트 동일, Maven Central에 새 좌표)
- `easy-paging 0.5.0` → `easy-paging 4.0.0`

재번호링 bump는:
- repo의 `VERSION` 갱신
- `[3.0.0]` / `[4.0.0]` CHANGELOG 항목 추가, 이 문서로 포인터
- GitHub에 태그 + 릴리즈 (릴리즈 노트가 이 문서를 링크)
- 모든 consumer 데모 + docs 사이트 업데이트

이전 `0.x` 아티팩트는 Maven Central에 그대로 남습니다 — 사라지지 않음 — 신규 릴리즈만 정렬된 라인에 떨어집니다.
