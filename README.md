# 👨‍💻 Who am I ?

### 🎯 Introduction
**"보안의 시야로 백엔드 아키텍처와 데이터베이스를 설계하는 개발자 유수현입니다."** <br/>

보안관제 및 QA 직무에서 5년 이상 쌓아온 시스템 이해도를 바탕으로, 현재는 엔터프라이즈급 SSO 솔루션의 핵심 백엔드를 주도하고 있습니다.<br/>
기존 구축형(JSP) 레거시 시스템을 프론트엔드와 분리된 REST API 구조로 전면 전환하고, SAML/OIDC 프로토콜 규격을 글로벌 표준으로 개조하여 50여 개의 외부 SaaS 연동과 SP 모드, OpenAPI(JWT) 생태계를 구축했습니다. <br/>
최근에는 공공기관 CSAP 인증 심사에 대응하기 위해, 데이터 정합성과 보안을 모두 충족시키는 대규모 DB 리팩토링(USER_ID → USER_NO)을 완수하며 보안과 성능을 모두 책임지는 IDaaS 분야의 핵심 기술 리더로 성장하고 있습니다.

### 🦸‍♂️ Profile
- **Name** : 유수현 (YooSuHyeon) 
- **Email** : eziofatal@gmail.com 
 <br/>
 
[![Anurag's GitHub stats](https://github-readme-stats-fast.vercel.app/api?username=codefatal)](https://github.com/anuraghazra/github-readme-stats)
[![Solved.ac 프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=codesh000)](https://solved.ac/codesh000)

<br/>

# 💪 Skills
### Backend & DB
![Java](https://img.shields.io/badge/Java-007396.svg?&style=for-the-badge&logo=Java&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F.svg?&style=for-the-badge&logo=Spring&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000.svg?&style=for-the-badge&logo=MyBatis&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=MariaDB&logoColor=white)
![MySQL](https://img.shields.io/badge/Mysql-4479A1?style=for-the-badge&logo=Mysql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000.svg?&style=for-the-badge&logo=Oracle&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438.svg?style=for-the-badge&logo=Redis&logoColor=white)
![Apache Tomcat](https://img.shields.io/badge/apache%20tomcat-%23F8DC75.svg?style=for-the-badge&logo=apache-tomcat&logoColor=black) 

### Identity & Security
![SAML](https://img.shields.io/badge/SAML-000000.svg?style=for-the-badge&logo=SAML&logoColor=white)
![OIDC](https://img.shields.io/badge/OIDC-000000.svg?style=for-the-badge&logo=OIDC&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000.svg?style=for-the-badge&logo=JWT&logoColor=white)

### DevOps & Tools
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=Docker&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)
![IntelliJ](https://img.shields.io/badge/IntelliJ-313131?style=for-the-badge&logo=intellij-idea&logoColor=white)
![Eclipse IDE](https://img.shields.io/badge/Eclipse%20IDE-2C2255.svg?&style=for-the-badge&logo=Eclipse%20IDE&logoColor=white)
![VSCode](https://img.shields.io/badge/VSCode-007ACC.svg?&style=for-the-badge&logo=VSCode&logoColor=white)
 <br/> <br/>

# 🚀 Projects

### LG U+ AlphaKey SSO CSAP 인증 및 보안 고도화
- **기간:** 2026.01 ~ 진행 중
- **기술 스택:** Java, Spring, MariaDB, MyBatis, Redis, Kubernetes, Postman
- **역할:** 백엔드 개발 (CSAP 대규모 리팩토링 및 취약점 조치)
- **주요 성과:**  
  - **[개인정보 파기와 로그 보존 딜레마 해결]** CSAP 심사 기준에 맞춰, DB 기본키를 Auto Increment 기반의 고유 숫자(`USER_NO`)로 전면 교체하는 대규모 리팩토링 주도
  - 수백 개의 쿼리 및 API를 수정하여, 회원 탈퇴 시 이메일(개인정보)은 영구 파기하되 중요 시스템 로그와 데이터 정합성은 안전하게 유지되는 아키텍처 구현
  - 단 1초의 다운타임 없이 무중단 DB 식별자 마이그레이션 완수 및 전체 CSAP 취약점 점검 항목의 약 50% 이상 직접 방어(접근 제어, 이상 접속 탐지)

### LG U+ AlphaKey SSO OpenAPI 및 코어 고도화
- **기간:** 2025.05 ~ 2026.03
- **기술 스택:** Java, Spring, MariaDB, MyBatis, Redis, JWT, Postman
- **역할:** 백엔드 개발 (OpenAPI, JWT, SP 모드 핵심 로직 개발)
- **주요 성과:**  
  - **[인증 생태계 확장]** 외부의 다른 IDP(Identity Provider)를 통해서도 플랫폼에 접속할 수 있도록 SP 모드 핵심 로직을 개발하여 플랫폼 연동성을 양방향으로 확장
  - 최신 인증 트렌드 대응을 위해 Token 기반 로그인(ID Only)을 신규 도입하고, JWT 페이로드 및 발급/검증 로직 직접 설계
  - 레거시 환경 제약(Swagger 도입 불가) 극복을 위해 Postman을 API 명세 도구로 적극 도입, 타사 프론트엔드 팀과의 인터페이스 조율 시간 획기적 단축

### Dpacto 솔루션 고도화
- **기간:** 2025.01 ~ 2025.06
- **기술 스택:** Java, MariaDB, Redis, SAML
- **역할:** SSO 연동 백엔드 개발
- **주요 성과:**  
  - Autodesk 앱 연동 스펙에 맞춘 기존 SAML 인증 로직 전면 리팩토링
  - 백엔드 세션 연계 프로세스 최적화를 통해 인증 시스템의 안정성 확보 및 로그인 실패율 최소화
 
### LG U+ AlphaKey SSO 통합 인증 API 개발
- **기간:** 2024.01 ~ 2025.03
- **기술 스택:** Java, Spring, MariaDB, MyBatis, Redis, SAML, OIDC, Postman
- **역할:** 백엔드 개발 (REST API 아키텍처 전환 및 SaaS 연동)
- **주요 성과:**  
  - **[REST API 및 DB 설계]** 화면(JSP)에 종속된 기존 구축형 시스템을 클라우드에 맞게 프론트엔드와 분리된 REST API 기반으로 전면 개편. 대다수 API의 근간이 되는 DB 테이블 및 MyBatis 쿼리 직접 설계
  - 자사 전용으로 폐쇄적이던 SAML 프로토콜을 국제 표준으로 개조하여, 90여 개의 외부 SaaS 앱 중 **50여 개 앱의 연동 실무 직접 완수**
  - 사내 SAML 연동 교육을 주도해 팀 생산성을 대폭 향상시켰으며, 이상 접속 내역 기록 등 세밀한 로그인 보안 정책 API 100% 전담 구현
