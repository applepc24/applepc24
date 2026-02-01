<div align="center">

### 👋 안녕하세요, 원준석입니다  
사용자가 좋아하고 자주 찾는 “살아있는 서비스/콘텐츠”를 만드는 걸 좋아하는 주니어 개발자입니다.  
풀스택(Frontend/Backend) + 데이터 파이프라인 + 운영/성능까지 끝까지 책임지는 개발을 지향합니다.

<br/>

<a href="https://github.com/applepc24" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-111111?style=for-the-badge&logo=github&logoColor=white"/>
</a>
<a href="https://applepc24.tistory.com/" target="_blank">
  <img src="https://img.shields.io/badge/Blog-11B48A?style=for-the-badge&logo=tistory&logoColor=white"/>
</a>


<!--
<a href="https://YOUR_PORTFOLIO" target="_blank">
  <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/YOUR_ID" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
-->

</div>

---

## 🚀 Featured Projects

### Mini-CDC — PostgreSQL CDC와 AI 에이전트를 결합한 실시간 데이터 분석 플랫폼
  ![Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mini_cdc)
  [![Demo](https://img.shields.io/badge/Live-Demo-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white)](https://www.stockops.site/dashboard)

   - PostgreSQL(WAL) → Relay → Kafka로 이어지는 CDC 파이프라인으로 데이터 변경사항을 비동기적으로 전파 및 처리
   - CQRS 아키텍처를 적용, PostgreSQL(Write)과 Vector DB(Read) 모델을 분리하여 검색 성능 및 시스템 확장성 확보
   - LLM 기반 AI 에이전트가 재고 데이터를 분석하고, 비즈니스 정책에 따라 능동적으로 보충 제안 및 데이터 변경 실행
   - CDC로 동기화된 Vector DB를 활용하여 텍스트 데이터에 대한 빠르고 정확한 시맨틱 검색 기능 제공

### SnapReport — 1인 창업자 상권·매출 기반 AI 컨설팅 리포트 (FE/BE)
[![Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/reportService)
[![Demo](https://img.shields.io/badge/Live-Demo-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white)](https://www.snapreport.cloud/)
- BullMQ 기반 비동기 작업 설계(POST jobId → GET status/result)로 LLM/RAG 장기 작업을 안정적으로 운영
- tool-calling 기반 Agentic RAG 파이프라인으로 트렌드/임대료 등 근거를 결합해 조언 생성
- PostgreSQL + TypeORM으로 행정동 지표를 병렬 조회하고, 매출 추세 기반 리스크 레벨 정형화
- k6 부하로 작업 큐 enqueue + status 조회 경로 안정성 검증

### SingSongGame — 실시간 6인 노래 맞히기 게임 (FE/BE)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/orgs/DRS-SingSongGame/repositories)
[![DataPipe Repo](https://img.shields.io/badge/DataPipe-Repo-0A66C2?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/SingSongGame-SongData-pipe)
- 실시간 WebSocket/Redis 구조로 채팅/라운드/동기화 처리
- 서버 주도 아키텍처로 TTS 재생 타이밍 오차를 ~1.0s → 0.1s 미만으로 개선
- 외부 API(YouTube/Spotify 등) 기반 데이터 수집 파이프라인 구축

  ### Inventory OOS Analysis — 재고 품절 데이터 기반 운영 이슈 분리 분석 
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/inventory-oos-analysis)
- 6개 매장 × 25개 상품 × 1주일 재고 데이터를 수집·정리해 매장×상품×일 단위 집계 구조 설계
- 평균 품절 비율과 매장 간 편차를 결합한 산점도 분석으로 전체 상품 품절 패턴을 동일 기준에서 비교
- 자주 품절되며 매장 편차가 큰 상품(Q1)과 전 매장 공통 품절 상품(Q4)을 구분해 배분/운영 이슈 vs 구조적 공급 이슈로 해석
- 매장×사이즈 단위 히트맵 분석과 oos_rate = 1 기준의 연속 품절(Persistence) 분석으로 단발성이 아닌 지속적 운영 리스크 상품을 우선 조치 대상으로 도출
- 분석 결과를 산점도·히트맵·Top 문제 상품 차트로 시각화하여 엑셀/PPT 기반 의사결정 자료로 정리

### PintOS — 운영체제 핵심 기능 구현 (C)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/PintOS-VM)
- priority scheduling / donation, syscall, VM(lazy loading, stack growth) 등 커널 핵심 메커니즘 구현
- 동기화/레이스 컨디션 디버깅과 테스트 기반 검증 경험

---

## 🧰 Tech Stack

**Frontend**  
![Next.js](https://img.shields.io/badge/Next.js-111111?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-111111?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-111111?style=for-the-badge&logo=typescript&logoColor=3178C6)

**Backend**  
![Node.js](https://img.shields.io/badge/Node.js-111111?style=for-the-badge&logo=nodedotjs&logoColor=339933)
![NestJS](https://img.shields.io/badge/NestJS-111111?style=for-the-badge&logo=nestjs&logoColor=E0234E)
![Flask](https://img.shields.io/badge/Flask-111111?style=for-the-badge&logo=flask&logoColor=FFFFFF)

**DB / Cache / Queue**  
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-111111?style=for-the-badge&logo=postgresql&logoColor=4169E1)
![MySQL](https://img.shields.io/badge/MySQL-111111?style=for-the-badge&logo=mysql&logoColor=4479A1)
![Redis](https://img.shields.io/badge/Redis-111111?style=for-the-badge&logo=redis&logoColor=DC382D)

**DevOps / Tools**  
![AWS](https://img.shields.io/badge/AWS-111111?style=for-the-badge&logo=amazonaws&logoColor=FF9900)
![Docker](https://img.shields.io/badge/Docker-111111?style=for-the-badge&logo=docker&logoColor=2496ED)
![k6](https://img.shields.io/badge/k6-111111?style=for-the-badge&logo=k6&logoColor=7D64FF)
![Git](https://img.shields.io/badge/Git-111111?style=for-the-badge&logo=git&logoColor=F05032)
