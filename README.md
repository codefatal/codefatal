# 👨‍💻 Who am I?

### 🎯 Introduction
**"보안과 운영의 관점으로 인증·세션·데이터 흐름을 설계하는 Java 백엔드 개발자 유수현입니다."** <br/>

서버 운영, 보안관제, 보안제품 QA 경험을 거쳐 현재는 SSO·IDaaS 분야의 Java 백엔드 개발을 담당하고 있습니다. <br/>
LG U+ AlphaKey SSO에서 구축형 MagicSSO를 AWS 상용 클라우드에 맞는 REST API·분산 세션 구조로 전환하고, SAML·OAuth2/OIDC 기반 SaaS 연동, 접속 보안 정책, OpenAPI Gateway, JWT ID Only 및 SAML SP 기능을 개발했습니다. <br/>
NCP 공공 클라우드 프로젝트에서는 GeoLocation 미지원 기능 분리, CSAP 소스 취약점 조치, `USER_ID → USER_NO` 식별 구조 전환과 개인정보 파기·감사 이력 보존을 위한 백엔드 리팩토링을 수행했습니다.

### 🦸‍♂️ Profile
- **Name** : 유수현 (Yoo Suhyeon)
- **Email** : eziofatal@gmail.com
- **Portfolio** : [Notion Portfolio](https://pond-saturn-4b3.notion.site/f46c380d44b3821d8d21018bcbf0649a)

<br/>

[![GitHub stats](https://github-readme-stats-fast.vercel.app/api?username=codefatal)](https://github.com/anuraghazra/github-readme-stats)
[![Solved.ac 프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=codesh000)](https://solved.ac/codesh000)

<br/>

# 💪 Skills

### Backend & Data
![Java](https://img.shields.io/badge/Java-007396.svg?&style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F.svg?&style=for-the-badge&logo=springboot&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000.svg?&style=for-the-badge)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000.svg?&style=for-the-badge&logo=oracle&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438.svg?style=for-the-badge&logo=redis&logoColor=white)
![Tomcat](https://img.shields.io/badge/Apache_Tomcat-F8DC75.svg?style=for-the-badge&logo=apachetomcat&logoColor=black)

### Identity & Security
![SAML](https://img.shields.io/badge/SAML_2.0-1F2937.svg?style=for-the-badge)
![OAuth2](https://img.shields.io/badge/OAuth2-2F5597.svg?style=for-the-badge)
![OIDC](https://img.shields.io/badge/OIDC-F78C40.svg?style=for-the-badge&logo=openid&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000.svg?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![CSAP](https://img.shields.io/badge/CSAP-0052CC.svg?style=for-the-badge)

### Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-232F3E.svg?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![NCP](https://img.shields.io/badge/NCP-03C75A.svg?style=for-the-badge&logo=naver&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=docker&logoColor=white)

### Tools
![GitHub](https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=github&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37.svg?style=for-the-badge&logo=postman&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000.svg?style=for-the-badge&logo=notion&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellijidea&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC.svg?style=for-the-badge&logo=visualstudiocode&logoColor=white)

<br/>

# 🚀 Projects

### 1. LG U+ AlphaKey SSO - AWS 상용 클라우드 및 OpenAPI 고도화
- **기간:** 2024.04 ~ 현재
- **기술 스택:** Java 8, Servlet, Tomcat 9, Spring Boot, MyBatis, MariaDB, Redis·Redisson, AWS EKS, Kubernetes, Docker, SAML, OAuth2/OIDC, JWT, Splunk, CloudWatch, Kafka, MaxMind GeoIP, Postman
- **역할:** SSO·IDaaS 백엔드 API, 인증·세션, 접속 보안 및 OpenAPI 기능 개발
- **주요 업무 및 결과:**
  - Docker·AWS EKS CI와 CodeQL 기반 배포 구성을 정리하고, Redisson 기반 Tomcat 세션 공유를 적용해 Kubernetes Pod 간 로그인 세션을 유지할 수 있는 기반을 구축했습니다.
  - JSP·레거시 Controller 중심 기능을 Servlet REST API와 Controller·Service·DAO·MyBatis Mapper 구조로 전환하고 테넌트·앱·인증서·Redirect URI·Scope 관리 기능을 재구성했습니다.
  - SAML·OAuth2/OIDC 표준 엔드포인트와 앱별 Metadata·Assertion·Attribute·Claim 검증을 개발하고, 연동 대상 90여 개 중 50여 개 SaaS 연동 로직을 구현했습니다.
  - 사용자·앱 감지정책, 이상접속 이력, 해외 IP 예외, 국가·차단 지역과 비정상 이동 접속 등 GeoIP 기반 로그인 보안 기능을 개발했습니다.
  - OpenAPI Gateway의 Token·Route·Config·Rate Limit·Metric·Redis Reload와 JWT ID Only 로그인을 구현했습니다.
  - 외부 IdP 인증을 AlphaKey 내부 세션으로 연결하는 SAML SP 모드와 Response·Assertion 서명, 재사용 방지 및 OIDC 보안 검증을 고도화했습니다.
  - Naver GeoLocation 종료에 대응해 MaxMind로 전환하고, 외부 API 장애 시 로그인은 유지하면서 위치 기반 정책의 오판을 방지하는 예외 흐름을 구성했습니다.

### 2. LG U+ AlphaKey SSO - NCP 전환 및 CSAP 보안 대응
- **기간:** 2025.10 ~ 2026.05
- **기술 스택:** Java 8, Servlet, Tomcat 9, MyBatis, MariaDB, Redis, NCP, CSAP, SAML, OIDC, Postman
- **역할:** NCP 환경 분기, 데이터 식별 구조 리팩토링 및 CSAP 소스 보안 조치
- **주요 업무 및 결과:**
  - NCP에서 GeoLocation API를 사용할 수 없는 환경 제약을 반영해 해외 접속·차단 지역·비정상 이동 접속 검증이 실행되지 않도록 기능을 비활성화하고 환경별 동작 경로를 분리했습니다.
  - 삭제 대상 데이터를 0으로 5회 덮어쓴 뒤 삭제하는 안전 삭제 처리를 적용했습니다.
  - Null 역참조, 예외 처리, 오류 정보 노출, HTTP 응답 분할, XXE, SQL 삽입, 해시 및 자원 해제 등 CSAP 소스 진단 항목을 Controller·Service·DAO 전반에서 조치했습니다.
  - USER 테이블의 PK와 등록·수정자 등 참조 구조를 이메일 기반 `USER_ID`에서 숫자형 `USER_NO`로 전환하고 Controller·Service·DAO·Mapper·SQL 등 약 100개 파일을 수정했습니다.
  - 회원 탈퇴 시 개인정보를 파기하면서도 업무 데이터와 감사 이력의 참조 관계를 유지할 수 있도록 데이터 구조를 개선했습니다.
  - 미등록·비활성 계정 검증, 이메일 마스킹, 감사로그 대상자, 로그인 잠금과 개인정보·중복 로그 흐름을 안정화했습니다.

### 3. Dpacto 솔루션 고도화 - Autodesk SAML 연동
- **기간:** 2025.01 ~ 2025.06
- **기술 스택:** Java, MariaDB, Redis, SAML
- **역할:** SSO 연동 백엔드 개발
- **주요 업무 및 결과:**
  - Autodesk의 Metadata·Assertion 구조, 필수 Attribute와 인증 흐름을 분석했습니다.
  - 애플리케이션별 SAML 예외 처리와 인증 결과가 Redis 기반 내부 세션으로 연결되는 흐름을 개선했습니다.
  - 로그인 성공·실패·만료·잘못된 Assertion 등 주요 예외 흐름을 재현하고 인증·세션 처리 결과를 검증했습니다.

<br/>

### 🤖 AI-assisted Development
- Claude Code와 Codex를 레거시 코드 영향도 분석, 구현 대안·예외 흐름 검토와 테스트 항목 정리에 활용합니다.
- AI 결과는 실제 코드, 데이터 흐름, 보안 요구사항과 테스트 결과를 기준으로 검증한 뒤 반영합니다.
