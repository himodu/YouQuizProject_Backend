# YouQuiz_Backend_API_Server
	
## 프로젝트 설명
YouQuiz 프로젝트는 2023년 대구를 빛내는 해커톤 출전을 위해 개발한 서비스이며
대한민국 청소년들의 디지털 문해력 향상을 위한 교육용 웹사이트로써
실제 youtube 영상과 댓글을 보고, 관련된 문제를 풀면서 디지털 문해력을 기르는 서비스이다.

본 레포지토리는 해당 서비스의 동작을 위한 api를 제공하는 backend API 서버로<br/>
서비스 자체 로그인, 회원가입<br/>
학습할 문제의 목록을 확인<br/>
학습할 문제를 확인<br/>
문제를 풀고 정답을 저장<br/>
자신의 정답에 대한 피드백<br/>
등 의 기능을 제공하는 16개의 API를 제공한다.<br/>

### API 명세서 노션페이지
<a href="https://www.notion.so/API-1e699ca81d11435a86296438df798b39?pvs=4"><img src="https://img.shields.io/badge/Notion-FFFFFF?style=for-the-badge&logo=Notion&logoColor=black"></a>

### 사용된 기술
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=for-the-badge&logo=Spring Boot&logoColor=white">  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">  <img src="https://img.shields.io/badge/Naver-03C75A?style=for-the-badge&logo=Naver&logoColor=white"> 

네이버 클라우드 플랫폼 (NCP) 를 사용하였고
본래 도커와 Github action 을 통한 배포를 시도했으나 실패하여<br/>
백엔드서버에는 직접 인스턴스 서버에 java를 설치하였고<br/>
DB서버는 네이버 클라우드에서 제공하는 SaaS를 이용하였다.<br/>
 
### 아키텍쳐 노션페이지
<a href="https://www.notion.so/5d04f492bc3442ff8ddcad1437f7d734?pvs=4"><img src="https://img.shields.io/badge/Notion-FFFFFF?style=for-the-badge&logo=Notion&logoColor=black"></a>


## 프로젝트 설치 및 실행 방법
초반 프로젝트 계획 시, 단일 시스템(클라우드 인스턴스)으로 Docker (Nginx + React + SpringBoot + MySQL) 를 통해 서비스를 구축하려 시도하였다.
그러나, 시스템의 컴퓨팅 파워 한계로 인해 단일 시스템에서 여러 도커 이미지를 구동할 수 없어, 부득이하게 기능별로 시스템을 분리하여 운용하였다.
또한 보안 유지에 있어서 적절한 권한 설정(chown, chmod)은 필수적이나, 상용 서비스 목적으로 작업하는 것이 아니므로, 권한을 비롯한 보안 설정은 고려하지 않았다.

1. FrontEnd - Nginx + React / Port Open 80, 443 (SSL)
- OS: CentOS 7.6
- Nginx: 1.20.1
- NPM: 6.4.18
- NodeJS: 14.21.3
  
2. BackEnd - SpringBoot / Port Open 8080
- OS: 상동
- Java: 17.0.8 (LTS)

3. Database - MySQL / Port Open 3306
- SaaS (Powered by NAVER Cloud Platform)
<br>
