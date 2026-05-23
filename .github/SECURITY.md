# Security Policy

**English** · [한국어](#한국어)

DevsLab's open-source libraries (`kr.devslab.*` on Maven Central) take security seriously. Several of them — most notably `ssrf-guard` — *are* security libraries; a vulnerability in them defeats the protection they're meant to provide. This policy applies to every repository under the [devslab-kr](https://github.com/devslab-kr) organization unless an individual repository documents an override.

## Reporting a vulnerability

**Do not report security issues through public GitHub issues, discussions, or pull requests.**

Use one of these private channels:

1. **GitHub Security Advisories (preferred)** — open a draft advisory on the affected repository: `https://github.com/devslab-kr/<repo>/security/advisories/new`. This keeps the report private to the maintainers and the GitHub Security team.
2. **Email** — `support@devslab.kr` with `[SECURITY]` in the subject line. Encrypt with PGP if you prefer; key fingerprint available on request.

Please include:
- Affected library + version (e.g. `kr.devslab:ssrf-guard:3.1.0`)
- Affected module(s) and the API entry point(s) the vulnerability touches
- A minimal reproduction (self-contained snippet or a public repo we can clone)
- Impact assessment (confidentiality / integrity / availability; reachability; who can trigger)
- Suggested mitigation or fix, if you have one

## Response timeline

| Step | Target |
| --- | --- |
| Initial acknowledgement (received, triaging) | within 3 working days |
| Triage decision (confirmed / not-a-vulnerability / need-more-info) | within 7 working days |
| Fix shipped to Maven Central | within 30 days for high/critical severity, best-effort otherwise |
| Public disclosure | coordinated with the reporter; default 90 days after initial report, sooner if fix is already published |

We follow [coordinated vulnerability disclosure](https://www.iso.org/standard/72311.html). If you find a public exploit in the wild before our fix ships, contact us immediately — we'll accelerate the response.

## Supported versions

Each library publishes its own version-support policy in its `CHANGELOG.md` and (where applicable) docs site. Active lines as of this writing:

| Library | Supported lines | Notes |
| --- | --- | --- |
| `ssrf-guard` | `3.x` (active) | Spring Boot 3.x. Security fixes backport to `3.x` until SB4 line ships. |
| `easy-paging-spring-boot-starter` | `3.x` (SB3 active) · `4.x` (SB4 active) | Two parallel lines — see [VERSIONING.md](./VERSIONING.md). |
| `api-log` | `3.x` (active) | Spring Boot 3.x. |

When a library's major version aligns with a Spring Boot major (the [versioning policy](./VERSIONING.md)), security fixes ship to **every line whose Spring Boot major is still receiving upstream support from the Spring team**. We follow Spring's [OSS support timeline](https://spring.io/projects/spring-boot#support).

## Scope

In scope:
- Code in any `kr.devslab/*` Maven Central artifact
- Configuration defaults that produce an insecure setup
- Documentation that recommends insecure patterns

Out of scope:
- Vulnerabilities in third-party dependencies (please report upstream; we will track and bump promptly via Dependabot)
- Vulnerabilities that require the attacker to already have privileged access (e.g. arbitrary classpath modification)
- DoS via maliciously crafted *input policies* (an integrator can already break their own system if they configure `UrlPolicy` to allow everything)

## Hall of fame

Researchers who report valid issues and want public credit are listed in the affected repository's `CHANGELOG.md` next to the fix.

---

# <a id="한국어"></a>한국어

# 보안 정책

DevsLab의 오픈소스 라이브러리 (Maven Central `kr.devslab.*`)는 보안을 진지하게 다룹니다. 일부는 — 특히 `ssrf-guard` — **보안 라이브러리 자체**라서, 거기서의 취약점은 그 라이브러리가 제공해야 할 방어를 무력화합니다. 이 정책은 [devslab-kr](https://github.com/devslab-kr) 조직 산하의 모든 저장소에 적용됩니다. 개별 저장소에서 명시적으로 override한 경우만 예외.

## 취약점 제보

**공개 GitHub 이슈, 디스커션, PR로 보안 이슈를 제보하지 마세요.**

다음 사설 채널 중 하나로:

1. **GitHub Security Advisories (권장)** — 해당 저장소에서 draft advisory 열기: `https://github.com/devslab-kr/<repo>/security/advisories/new`. 메인테이너와 GitHub Security 팀에만 보입니다.
2. **이메일** — `support@devslab.kr`, 제목에 `[SECURITY]` 표기. PGP 암호화 선호 시 키 fingerprint 요청 가능.

제보에 포함해주세요:
- 영향받는 라이브러리 + 버전 (예: `kr.devslab:ssrf-guard:3.1.0`)
- 영향받는 모듈과 API 진입점
- 최소 재현 (자체 완결 스니펫 또는 clone 가능한 공개 repo)
- 영향 평가 (기밀성 / 무결성 / 가용성 / 도달성 / 트리거 가능 주체)
- 가능하다면 완화 방안 또는 수정안

## 응답 타임라인

| 단계 | 목표 |
| --- | --- |
| 최초 수신 확인 (접수, 트리아지 중) | 3 영업일 이내 |
| 트리아지 결정 (취약점 확인 / 아님 / 정보 추가 필요) | 7 영업일 이내 |
| Maven Central에 수정 배포 | high/critical 30일 이내, 그 외 best-effort |
| 공개 공시 | 제보자와 협의 후. 기본 최초 제보로부터 90일, 수정이 먼저 배포되면 더 빨리 |

[조정된 취약점 공시](https://www.iso.org/standard/72311.html) 절차를 따릅니다. 수정 배포 전에 in-the-wild 익스플로잇이 공개되면 즉시 알려주세요 — 응답을 가속합니다.

## 지원 버전

각 라이브러리는 자체 `CHANGELOG.md`와 (해당 시) 도큐 사이트에 버전 지원 정책을 명시합니다. 현시점 active 라인:

| 라이브러리 | 지원 라인 | 비고 |
| --- | --- | --- |
| `ssrf-guard` | `3.x` (active) | Spring Boot 3.x. SB4 라인 출시 전까진 `3.x`에 보안 패치 백포트. |
| `easy-paging-spring-boot-starter` | `3.x` (SB3 active) · `4.x` (SB4 active) | 두 라인 병행 — [VERSIONING.md](./VERSIONING.md) 참고. |
| `api-log` | `3.x` (active) | Spring Boot 3.x. |

라이브러리 메이저 버전이 Spring Boot 메이저와 정렬된 ([버전 정책](./VERSIONING.md)) 라이브러리의 경우, **Spring 팀이 여전히 상위 지원하는 Spring Boot 메이저에 해당하는 모든 라인**에 보안 픽스를 배포합니다. Spring의 [OSS 지원 타임라인](https://spring.io/projects/spring-boot#support)을 따릅니다.

## 범위

In scope:
- `kr.devslab/*` Maven Central 아티팩트의 모든 코드
- 안전하지 않은 셋업을 만드는 기본 설정값
- 안전하지 않은 패턴을 권장하는 문서

Out of scope:
- 서드파티 의존성의 취약점 (해당 프로젝트로 제보하세요. 우리는 Dependabot으로 신속 추적 + bump)
- 공격자가 이미 권한 있는 접근을 가진 상태에서만 가능한 취약점 (예: 임의 classpath 수정)
- 악의적으로 만든 **입력 정책** 자체로 인한 DoS (`UrlPolicy`를 다 허용으로 설정하면 사용자가 자기 시스템을 망가뜨릴 수 있다는 사실은 이미 알려져 있음)

## Hall of fame

유효한 이슈를 제보하고 공개 크레딧을 원하는 연구자는 해당 저장소의 `CHANGELOG.md`의 수정 옆에 명시됩니다.
