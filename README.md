# 유수현 | Java 백엔드 개발자

**인증·세션과 데이터 정합성을 다루는 B2B 플랫폼을 개발합니다.**

약 3년의 Java 백엔드 개발 경험을 바탕으로 AlphaKey SSO·Spring Boot 기반 OpenAPI·Dpacto 등 기업용 솔루션의 구축과 고도화에 참여하고 있습니다. 보안관제·QA에서 익힌 로그 분석과 결함 재현 경험을 API 예외 처리와 회귀 검증에 적용합니다.

[프로젝트 상세·월별 구현 이력](https://pond-saturn-4b3.notion.site/3bbc380d44b381e3ab97c52e9167e63e)

## 핵심 성과

- **50여 개 SaaS 연동 로직 구현** — SAML·OIDC의 Metadata·Attribute·Claim 차이를 분석하고 서비스별 호환 처리에 반영했습니다.
- **Java 32개·XML 8개 식별자 참조 전환** — NCP의 USER_ID → USER_NO 변경에서 인증·감지정책·감사 이력의 참조를 정비했습니다.
- **해외 IP 허용 정책을 3개 유형으로 확장** — IP·국가·사용자/그룹별 검증과 기간 관리, 트랜잭션·다건 삭제의 부분 성공 처리를 구현했습니다.

## 주요 프로젝트

### 1. AlphaKey SSO AWS

**2024.04 ~ 현재** · Java 8, Servlet, Tomcat 9, Ant, MyBatis, MariaDB, Redis·Redisson

- 외부 IdP 인증 결과를 기존 사용자·토큰·공유 세션과 연결하는 **SAML SP 브리지**를 개발했습니다.
- SSO 관리자 영역의 **API Token·Route·Rate Limit·사용량 집계·만료 알림**과 Redis를 통한 Gateway 설정 갱신을 구현했습니다.
- **MaxMind GeoIP 전환**과 응답 호환 처리를 구현하고, 위치정보 조회 실패가 전체 로그인 실패로 이어지지 않도록 정책 실행 조건을 분리했습니다.

**2026.12 추가 구현 · 2026.12.09 배포 예정**

- **감지정책의 사용자·조직·SaaS 대상과 IP·기기·도메인 조건 관리**, 정책·할당·감사 이력의 DB 트랜잭션과 로그인·앱 인가 시 판정을 구현했습니다.
- **OIDC 세션의 최대 유지·미사용 만료 및 갱신 시 계정 상태 확인**을 반영하고, 목록 조회·정렬과 Workflow 오류 처리를 보완했습니다.
- **토큰 알림·허용 IP 변경과 이력의 DB 트랜잭션**, 폐기 시 Redis 사용 차단 후 DB 삭제·이력 처리, 알림 선택값 보존과 사용량 차트의 중복 보충 방지를 구현했습니다.
- 우선 대상 API에 **요청 추적 ID·처리 단계·결과를 연결하는 JSON 시스템 로그**와 사용자 식별자 마스킹을 추가했습니다.

[SSO AWS 상세](https://pond-saturn-4b3.notion.site/c7dc380d44b38203a97d81b17c0b747d)

### 2. AlphaKey SSO NCP

**2025.10 ~ 현재** · Java 8, Servlet, MyBatis, MariaDB, Redis, NCP

- **USER_NO 기반 참조 구조**에 맞춰 인증·감지정책·감사로그의 조회 조건과 데이터 타입을 변경했습니다.
- **CSAP 소스 점검**에 대응해 입력 검증·예외·XML·SQL·자원 해제·로그 노출 항목을 보완했습니다.
- 계정 정지·강제 로그아웃으로 **세션이 소멸한 뒤 테넌트 정보를 얻지 못하던 오류**를 수정했습니다.

**2026.10 추가 구현 · 커밋 작성월 기준**

- 감지정책 사용자명·초기화 메일 연동의 복호화, **조치·메일 실패 결과 처리**, 빈 정렬 조건과 위치정보 미사용 환경의 좌표 처리를 보완했습니다.
- SSO 관리자용 API 토큰에 **USER_NO를 연계**하고 Redis 저장 실패에 따른 발급 실패·보상 처리와 삭제 전 검증, 토큰·IP 삭제의 DB 트랜잭션을 구현했습니다.

[SSO NCP 상세](https://pond-saturn-4b3.notion.site/a88c380d44b383e8b0e581193ade8613)

### 3. AlphaKey OpenAPI AWS

**2025.04 ~ 현재** · Java 21, Spring Boot 3.4.3, Gradle 8.13, MyBatis, Redis

- **SSO 관리 REST API**의 앱 연동·이상접속 조치·감지정책을 구현하고 Request DTO·URL·응답·오류코드를 정비했습니다.
- 중복 등록·없는 대상 삭제·빈 검색값·잘못된 타입을 검증하고 **업무 Workflow 연동과 기본 정책 보호**를 구현했습니다.
- **해외 IP 허용 정책**의 국가·기간·네트워크 입력과 사용자·그룹 존재 여부를 검증하고 기존 정책 명칭과의 호환성을 보완했습니다.

**2026.12 추가 구현 · 2026.12.09 배포 예정**

- **감지정책 CRUD·활성화**의 요청 검증과 연관 데이터 트랜잭션을 보완하고, DB 반영 후 Workflow를 전송하도록 연결했습니다.
- **다중 허용 IPv4·사유·전체 허용 조건**과 사용자·앱 할당 검증, 조회·저장 정합성을 반영했습니다.
- **테넌트 헤더·요청자 검증**을 추가하고, 요청자 헤더 누락 시 등록자를 조회하며 등록자·Workflow 관리자가 없는 요청을 거부하도록 처리했습니다.

[OpenAPI AWS 상세](https://pond-saturn-4b3.notion.site/3f8c380d44b3818891c3f361b412159e)

### 4. Dpacto Autodesk SAML 연동

**2025.01 ~ 2025.06** · Java, SAML 2.0, Redis, MariaDB

- Autodesk의 Metadata·Assertion·Attribute 차이를 분석해 호환 처리를 구현하고, 인증 결과를 기존 사용자 조회와 Redis 세션에 연결했습니다.

[Dpacto 상세](https://pond-saturn-4b3.notion.site/f6dc380d44b382a78371016d302e22b9)

## 설계·시험 기록

- **설계:** 인증·세션과 감지정책의 요구사항·데이터·회귀 범위를 분석했습니다. 이후 커밋과 현재 소스에서 확인된 구현은 해당 프로젝트의 추가 구현에 반영하고, 미구현 설계는 성과에 포함하지 않았습니다.
- **시험:** 2026.10.12 Postman CLI 예외시험의 실행 결과를 관리했습니다. **SSO·OpenAPI 합산 204건 중 198건 통과·6건 메시지 불일치**입니다. SSO는 102건 모두 통과했고, OpenAPI는 102건 중 96건 통과·6건 메시지 불일치였으며, 불일치 6건의 HTTP 상태와 업무코드는 기대값과 일치했습니다. 기대·실제 응답과 정리 결과를 증적으로 남겼습니다.

프로젝트의 구현 내용은 본인 커밋과 현재 소스 기준입니다. AWS의 이번 추가 구현은 2026.12.09 배포 예정분이며, NCP는 커밋 작성월로 기록했습니다. 이번 정리는 소스 확인으로 진행했으며, 위 2026.10.12 시험 결과를 신규 구현의 재시험 통과나 배포 완료로 사용하지 않습니다.

## 기술 및 개발 방식

| 영역 | 사용하는 기술·도구 |
|---|---|
| Backend | Java 8·21, Spring Boot, Servlet, REST API, MyBatis, SQL |
| Data·Identity | MariaDB, Redis·Redisson, SAML 2.0, OAuth 2.0, OIDC, JWT |
| Build·Quality | Gradle, Ant, Git, Postman CLI, IntelliJ IDEA |
| 실행 환경·관찰 | AWS·NCP 애플리케이션 개발·연동, Tomcat, EKS·Kubernetes·Docker, Splunk, CloudWatch |

- IAM·MFA·프론트엔드와 API·오류 응답을 조율하고, SAML 연동 기준을 문서화해 사내 개발자 교육을 진행했습니다.
- Claude Code·Codex를 코드 영향도 분석, 구현 대안·예외 흐름·시험 항목 검토에 활용하고 실제 코드와 요청·응답으로 확인합니다.

<details>
<summary>GitHub 활동 · 알고리즘 학습</summary>

[![GitHub stats](https://github-readme-stats-fast.vercel.app/api?username=codefatal)](https://github.com/anuraghazra/github-readme-stats)
[![Solved.ac 프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=codesh000)](https://solved.ac/codesh000)

</details>

*2026.11.05 기준 · 드림시큐리티 ID보안개발팀 선임연구원, 2023.11 ~ 현재*
