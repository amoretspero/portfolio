# THE portfolio - TL;DR version

## Introduction

- Name: Jiung Hahm
- Email: amoretspero (at) gmail (dot) com
  - Alternative: amoretspero (at) snu (dot) ac (dot) kr
- Github: [https://github.com/amoretspero](https://github.com/amoretspero)

## Education

### University

- 서울대학교 공과대학 컴퓨터공학부 (Undergraduate)
  - Enrollment: Mar. 2013.
  - (Expected) Graduation: Feb. 2022. (Bachelor's)
  - GPA: 3.69/4.3 (as of Aug. 2021.)

## Work Experience

### (주)오너클랜

- 회사 주요 업무: 오픈마켓에서 활동하는 소규모 판매자들을 위한 도매 중개업  

#### Internal / Open API 서비스 및 서버 개발

- Skills
  - Server Runtime: Node.js
  - Programming Language: Typescript
  - API type: GraphQL
  - CI/CD: Gitlab CI/CD
  - Cloud Service Provider: Google Cloud Platform
- GCP Kubernetes Engine를 사용해 프로토타입 개발 및 초기 서비스 운영 후 네트워크 트래픽 등의 문제로 사내 서버로 이전 운영
- 서비스 운영 시 일평균 2M requests, 초당 최대 150-200 requests 처리
  - Single server / PM2 cluster 사용
- Quota 제한을 위해 Redis 기반의 사용량 제한 서비스 구현
- API 서비스 오픈 후 오픈 전 대비 웹사이트의 불필요한 스크랩 트래픽 80% 이상 감소

#### 회사 주요 서비스 리뉴얼 작업 - 백엔드

- Skills
  - Server Runtime: Node.js
  - Programming Language: Typescript
  - API type: GraphQL
  - Database: MySQL
  - CI/CD: Gitlab CI
- 서비스 요구사항 분석 내용에 따른 DB 스키마 재구축
  - TypeORM 패키지를 이용한 스키마 정의
  - 리뉴얼에 필요한 DB migration 코드 작성
- Node.js 및 TypeScript, GraphQL을 기반으로 한 API 서버 구현
  - GraphQL type 정의 및 resolver 구현 등 GraphQL을 기반으로 한 API 서버에서 구현해야 하는 대부분을 담당
  - GraphQL `query`에 대한 TypeScript decorator 기반의 GraphQL query to MySQL query parser 구현
    - GraphQL API 서비스 개발시 data fetch/format 과정의 코드 약 80% 이상 감소

#### 이미지 제공 전용 서버 개발 및 CDN 연동

- Skills
  - Server Runtime: Node.js
  - Cloud Service Provider: Google Cloud Platform
  - CDN Provider: Akamai CDN(main) / GCP CDN(backup)
  - CI/CD: Gitlab CI/CD
  - CDN의 경우 Akamai CDN을 기본으로 하되 Akamai CDN에 대한 failover로 GCS CDN을 사용할 수 있도록 추가 구현
  - GCP의 경우 Storage, Kubernetes Engine 서비스를 주로 사용.
- 웹사이트에서 제공하는 이미지 및 외부에 제공하는 이미지의 트래픽을 줄이기 위해 CDN 연동
- 사용자가 업로드한 원본 이미지 1개로 여러 사이즈의 request에 대응할 수 있도록 URL-based dynamic resizing/rotation 구현
  - CDN caching을 위해 사전 정의된 사이즈 이외의 요청은 거절
- GCP Kubernetes Engine에서 제공하는 Cluster auto-scaling / Container pod auto-scaling 적용

#### 상품 유사도 확인 프로그램 개발

- Skills
  - Server Runtime: Dotnet Core
  - Programming Language: C#
  - Cloud Service Provider: Google Cloud Platform
    - 사내 서버 자원 대용으로 GCP의 Compute Engine만 사용
- 상품 데이터 중 선택된 항목들에 대해 LSH(Locality Sensitive Hashing) algorithm / Min hashing을 적용해 유사도 계산
- Cron 작업으로 일정 주기마다 전체 상품에 대해 계산하도록 구현
- 계산된 유사도를 바탕으로 동일상품으로 의심되는 경우 관리자에게 리포트하여 조치를 취하고, 유사한 상품의 정보는 사용자에게 제공

### (주)스카이시드

- 회사 주요 업무: 웹서비스 개발 및 마케팅 외주 / 학원업

#### 2013.12 - 2016.01

- 마케팅 외주 업무 지원

#### 2016.01 - 2017.08

- 학원 수강생 관리 시스템 제작 (Ruby on Rails)
  - 수강생 및 결제/등록 이력 DB 설계
  - 대량 문자메시지 발송 프로그램 제작 및 OpenAPI 연동
- 자기소개서 작성 지원 웹서비스 개발
  - 사용자의 경우 회원가입 / 자기소개서 작성 및 저장 / 자기소개서 인쇄 기능을,
  - 관리자의 경우 사용자가 동의한 자기소개서 열람 / 회원관리 / 자기소개서 관련 정보 추가 및 편집 기능을 제공.
  - .NET Framework와 C#으로 개발되었으며, 프론트엔드는 Razor 기반으로 간략하게 제작.
- 도서 원고 버전관리 웹서비스 개발
  - 회사에서 제작한 내부용 혹은 외부 출판용 도서 원고의 버전 관리를 지원.
  - 여러 명이 작업할 경우 개인이 작업한 파일을 업로드하면 자동으로 모든 버전이 보관되고 도서 제작 작업 과정에 따른 이력을 쉽게 파악할 수 있도록 제공.
  - .NET Framework와 C#으로 개발.
- 고등학교 수학 기출문제 분류 및 관리 웹서비스
  - 교재 제작과 스타트업에서 운영하는 학원에서 사용하기 위해 수능 및 모의고사 수학 기출문제를 자체적인 기준에 따라 분류하고 결과를 제공하는 웹서비스 제작.
  - 사용자가 최대한 문제 이해와 카테고리 분류에만 집중할 수 있도록 나머지 과정을 최대한 줄여주도록 지원하는 것을 목적으로 함.
  - .NET Framework와 C#으로 개발.
- 고등학생 대상 수학 강의

## Personal / Toy projects

### Periodic Dataloader

- Typescript로 만든, 특정 주기마다 load function을 실행할 수 있는 dataloader.
- GraphQL 방식의 API를 구현할 때 graphqljs에서 제공하는 dataloader에 해당 기능이 없어서 직접 사용하려고 만든 뒤 일반적으로 사용할 수 있도록 약간의 변형을 거쳐서 public package로 배포됨.
- 기존 Dataloader에 없던 기능 중 추가한 2개의 기능
  - Periodic execution of batch load function: Load를 기다리는 key가 있을 경우에, 주어진 시간 간격마다 batch load function을 실행하는 기능.
  - Unique keys only to batch load function: Load를 기다리는 key가 있을 경우에, 모든 key를 batch load function에 넘겨주는 대신 unique key들만 골라서 이들에 대해서만 batch load function을 실행하게 하는 기능.
- [Github Repository](https://github.com/amoretspero/periodic-dataloader)

### FSharp Linear Algebra

- F#을 처음 접한 뒤, 간단한 라이브러리를 구현해보고 싶어 대학교 수업시간에 배운 선형대수의 개념들을 일부나마 직접 구현해 본 라이브러리.
- [Github Repository](https://github.com/amoretspero/FSharp_Linear_Algebra)

### Hml Equation Parser

- 한글 문서에서 수식 부분만 추출해내어 사용할 일이 있어 기존에 다른 곳에서 개발해서 오픈소스로 공개한 repository를 fork해서 기능을 더 보완한 프로그램.
- 기본적으로 한글에서 수식을 입력할 때 사용하는 string을 LaTeX math string으로 변환해주는 기능을 지원.
- [Github Repository](https://github.com/amoretspero/hml-equation-parser)

## Skills

- **굵게 처리된 내용**: 최근 자주 사용해서 익숙한 skill set
- *이탤릭 처리된 내용*: 일에서 자주 사용하지는 않았으나 소규모 프로그램 개발 및 유지가 가능한 skill set
- 그 이외: 주로 대학교 수업 프로젝트 등에 사용했거나, 한 번쯤 다뤄봤던 정도의 skill set

### Programming Languages

- **JavaScript / TypeScript**
- **Python**
- **SQL**(MySQL)
- *C#*
- *F#*
- C/C++
- Java
- PHP

### Frameworks / Databases

- **Node.js**
- **MySQL**
- *Dotnet Framework / Dotnet Core*
- ArangoDB

### Others

- **Google Cloud Platform**
- **Nginx**
- **React**
- Azure

## Interests

- Programming Languages
  - Typescript
  - F#
  - Python
- Frameworks
  - Dotnet Core
  - Node.js
  - Tensorflow
- Others
  - Functional Programming
  - React/Recoil
  - GraphQL
  - Machine Learning
  - Quantum Computing

---

Thank you for reading this portfolio.

You can see the github version at: [Github Link](https://github.com/amoretspero/portfolio/blob/main/tl_dr.md)