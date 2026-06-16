<div align="center">

### 👋 안녕하세요, 원준석입니다
데이터가 수집되고, 정제되고, 품질이 검증되는 전 과정을 직접 만들어왔습니다.

Kafka·Airflow·BigQuery 기반 파이프라인부터 ML 학습 데이터 구축까지, 데이터가 신뢰할 수 있는 형태로 흐르게 만드는 데 집중합니다.

<br/>

<a href="https://github.com/applepc24" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-111111?style=for-the-badge&logo=github&logoColor=white"/>
</a>
<a href="https://applepc24.tistory.com/" target="_blank">
  <img src="https://img.shields.io/badge/Blog-11B48A?style=for-the-badge&logo=tistory&logoColor=white"/>
</a>

</div>

---

## 🚀 Featured Projects

### 항만 CCTV 컨테이너 객체 탐지 · 학습 데이터셋 구축 및 추론 파이프라인
[![Repo](https://img.shields.io/badge/GitHub-데이터구축-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/container-code-labeling)
[![Repo](https://img.shields.io/badge/GitHub-웹서비스-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/labeling_web)

- Label Studio OBB 방식으로 6클래스 수작업 라벨링 1,350장 직접 수행 및 클래스별 품질 기준 수립
- 1차 모델 기반 프리라벨링 9,896장 검수·수정 과정에서 라벨 품질 편차 확인 → 2차 학습 mAP@0.5 0.78→0.52 하락 원인 분석, Confusion Matrix·PR Curve·F1 Curve 비교로 background→container 오탐율 0.24→0.52 증가 특정, 1차 모델 채택 근거 도출
- 수천 장 프레임 수작업 선별 비효율 문제를 OpenCV GUI 기반 인터랙티브 선택기(Y/N/B 키 제어)로 해결
- 영상 업로드 → 프레임 추출 → YOLOv8 OBB 추론 → 결과 정규화·검증 → SQLite 적재의 ingest/inference/transform/load 4단계 추론 파이프라인 직접 설계·구현

**Tech Stack:** YOLOv8 OBB, Label Studio, Python, OpenCV, NumPy, Streamlit, SQLite

---

### Job Postings Data Platform — 채용공고 수집·적재 데이터 플랫폼
[![Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/Lead-insight-platform)

- 채용공고 fetch 실패 시 작업 유실 문제를 DLQ + Replay 시스템으로 해결, failed_stage / error_type / retry_count 기반 격리·추적으로 재처리 가능한 운영 구조 구축
- 동일 공고 중복 적재 문제를 Worker 레벨(job_id 기반) + BigQuery intermediate 레벨(source + original_url 기준 ROW_NUMBER dedup) 다층 구조로 해결
- S3 raw / processed / curated 3레이어 분리로 원본 HTML 보존 및 단계별 재처리 기준점 확보
- Airflow(orchestration) / BigQuery+Grafana(observability) 역할 분리로 실행과 관측을 독립적으로 운영

**Tech Stack:** Python, Kafka, Amazon S3, BigQuery, Airflow, Grafana

---

### SingSongGame — K-POP 하이라이트 데이터셋 구축 파이프라인
[![Repo](https://img.shields.io/badge/GitHub-DataPipe-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/SingSongGame-SongData-pipe)

- songs.txt 입력 기반 멀티소스 수집 파이프라인으로 YouTube·Genius·Spotify·Last.fm 데이터를 자동 수집해 1,100곡 규모 K-POP 하이라이트 데이터셋 구축
- YouTube 다단계 검색(Lv1~Lv3) + 블랙리스트 필터 + 스코어링으로 노이즈 후보 제거, 원본 음원만 선별
- 수작업 시 10곡 기준 30분 이상 소요되던 작업을 자동화 후 5분으로 단축 (6배 향상)
- dataset.csv(title, artist, audio_url, lyrics, tags, hint, answer) 7개 필드 고정 스키마로 팀 공통 데이터셋 완성

**Tech Stack:** Python, yt-dlp, librosa, YouTube API, Genius API, Spotify API, Amazon S3

---

## 🧰 Tech Stack

**Data Engineering**
![Kafka](https://img.shields.io/badge/Kafka-111111?style=for-the-badge&logo=apachekafka&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-111111?style=for-the-badge&logo=apacheairflow&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-111111?style=for-the-badge&logo=googlebigquery&logoColor=4285F4)
![Python](https://img.shields.io/badge/Python-111111?style=for-the-badge&logo=python&logoColor=3776AB)

**ML / Data**
![YOLOv8](https://img.shields.io/badge/YOLOv8_OBB-111111?style=for-the-badge&logo=github&logoColor=white)
![Label Studio](https://img.shields.io/badge/Label_Studio-111111?style=for-the-badge&logo=labelstudio&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-111111?style=for-the-badge&logo=opencv&logoColor=5C3EE8)

**Database**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-111111?style=for-the-badge&logo=postgresql&logoColor=4169E1)
![MySQL](https://img.shields.io/badge/MySQL-111111?style=for-the-badge&logo=mysql&logoColor=4479A1)
![Redis](https://img.shields.io/badge/Redis-111111?style=for-the-badge&logo=redis&logoColor=DC382D)
![SQLite](https://img.shields.io/badge/SQLite-111111?style=for-the-badge&logo=sqlite&logoColor=003B57)

**Cloud / DevOps**
![AWS S3](https://img.shields.io/badge/AWS_S3-111111?style=for-the-badge&logo=amazons3&logoColor=FF9900)
![AWS EC2](https://img.shields.io/badge/AWS_EC2-111111?style=for-the-badge&logo=amazonec2&logoColor=FF9900)
![Docker](https://img.shields.io/badge/Docker-111111?style=for-the-badge&logo=docker&logoColor=2496ED)
![Grafana](https://img.shields.io/badge/Grafana-111111?style=for-the-badge&logo=grafana&logoColor=F46800)

---

## 📚 기본기 (운영체제·네트워크)

### PintOS — 운영체제 핵심 기능 구현
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/PintOS-VM)
- 우선순위 스케줄링 및 Priority Donation 구현을 통해 OS 수준 동시성·락 경합 문제 해결
- 시스템 콜 인터페이스 및 User↔Kernel 모드 전환 흐름 완성, 포인터 검증 기반 커널 방어 로직 구현
- Lazy Loading·Page Fault 처리 포함 가상 메모리 서브시스템 구현 및 동기화 리팩토링
- 50+ 테스트 기반 TDD 방식으로 Race/VM/Process 안정성 검증

### 운영체제 인터뷰 스터디 (OSTEP 기반)
- OSTEP 기반 OS 면접 Q&A 스터디 운영 및 기술 블로그 정리

---

## 🛠 기타 프로젝트 (풀스택)

<details>
<summary>접어두기 (클릭해서 펼치기)</summary>

### stockops — 실시간 재고관리 플랫폼
[![Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/mini_cdc)
[![Demo](https://img.shields.io/badge/Live-Demo-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white)](https://www.stockops.site/dashboard)

- PostgreSQL → Relay → Kafka로 이어지는 CDC 파이프라인으로 데이터 변경사항을 비동기적으로 전파 및 처리
- CQRS 아키텍처를 적용, PostgreSQL(Write)과 Vector DB(Read) 모델을 분리하여 검색 성능 및 시스템 확장성 확보
- LLM 기반 AI 에이전트가 재고 데이터를 분석하고, 비즈니스 정책에 따라 능동적으로 보충 제안
- Slack OAuth 연동으로 워크스페이스/채널에 설치하고, 재고 이벤트·재입고 리포트를 알림으로 전송

### SnapReport — 1인 창업자 상권·매출 기반 AI 컨설팅 리포트
[![Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/reportService)
[![Demo](https://img.shields.io/badge/Live-Demo-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white)](https://www.snapreport.cloud/)

- BullMQ 기반 비동기 작업 설계로 LLM/RAG 장기 작업을 안정적으로 운영
- tool-calling 기반 Agentic RAG 파이프라인으로 트렌드/임대료 등 근거를 결합해 조언 생성
- k6 부하테스트로 작업 큐 enqueue + status 조회 경로 안정성 검증

### Inventory OOS Analysis — 재고 품절 데이터 기반 운영 이슈 분석
[![Repo](https://img.shields.io/badge/GitHub-Repo-111111?style=for-the-badge&logo=github&logoColor=white)](https://github.com/applepc24/inventory-oos-analysis)

- 6개 매장 × 25개 상품 × 1주일 재고 데이터 수집·정리 및 매장×상품×일 단위 집계 구조 설계
- 평균 품절 비율과 매장 간 편차를 결합한 산점도 분석으로 배분/운영 이슈 vs 구조적 공급 이슈 구분

</details>
