## GA4 기반 이커머스 사용자 행동 분석

### 1. Overview
#### 🔸프로젝트 소개
이 프로젝트는 Google 애널리틱스 4(GA4)를 통해 수집된 웹사이트 및 앱 사용자 데이터를 활용하여 이커머스 플랫폼에서의 사용자 행동을 분석합니다. 주요 분석 내용은 다음과 같습니다. 

- **탐색적 데이터 분석 (EDA)** : 사용자 활동의 패턴, 트렌드, 분포 조사
- **AARRR 분석** : 각 유입경로별 전환 흐름과 효율성 평가 
- **퍼널 분석 (Funnel Analysis)** : 방문부터 구매 전환까지 사용자 여정 추적
- **이벤트 기반 행동 분석** : GA4 이벤트 데이터를 기반으로 사용자 상호작용 분석
- **페이지 흐름 (pagepath) 분석** : 사용자가 사이트를 이동하는 일반적인 경로와 병목 구간 파악

이를 통해 사용자 경험 개선, 전환율 최적화, 데이터 기반 마케팅 전략 수립에 활용 가능한 인사이트를 제공하고자 합니다. 

#### 🔹프로젝트 목적

| 분석 대상                | 목적                                      | 기대 효과                                 |
| -------------------- | --------------------------------------- | ------------------------------------- |
| **유입경로별 & AARRR 분석** | 사용자가 어떤 경로로 유입되고 성과에 미치는 영향 및 채널별 효율 평가 | 마케팅 자원 효율적 배분, 높은 수익 기여 채널 발굴, ROI 개선 |
| **퍼널 분석**  | 고객 경험을 수치화하고 단계별 이탈 요인 및 병목 구간 파악       | 전환율 개선, 고객 여정 최적화                     |
| **이벤트 행동 분석**        | 사용자 행동 패턴과 주요 액션의 효과 이해                 | UX/서비스 개선, 핵심 전환 행동 강화                |
| **신규 vs 재방문 유저 분석**  | 고객의 실제 흐름을 객관적으로 이해하고 전환 속도 및 활성화 비교    | 맞춤형 전략 수립, 고객 경험 개선                   |
| **날짜별/전체 흐름 지표 분석**  | 시기별 트렌드 및 고객 행동 흐름 파악                   | 시즌/기간별 전략 수립 지원                       |
| **pagePath 분석**      | 세션 단위의 상세 흐름 및 병목 구간 확인                 | 콘텐츠 구성 및 UX 전략 수립 가능                  |



---

### 2. 팀원 소개

| 사진 | 사진 | 사진 | 사진 | 
|------|------|------|------|
| 김혜원 | 변해민 | 양원선 | 전수연 | 

---

### 3. 프로젝트 기간 및 수행 내용

| 기간 | 수행 내용 |
|------|-----------|
| 2025.05.01 ~ 2025.05.18 | - AARRR 분석 |
| 2025.06.05 ~ 2025.06.19 | - AARRR 분석 보완 <br>- A/B test<br>- 퍼널 분석 <br>- pagepath 분석 |
| 2025.06.26 ~ 2025.08.28 | - 보고서 작성 <br>- 코드 정리 <br>- 깃허브 정리 |

### 4. 프로젝트 환경 및 구성 요소
#### Tech stack
##### 사용 프로그램

| 항목 | 내용 |
|------|------|
| Language        | ![Python Badge](https://camo.githubusercontent.com/0d0779a129f1dcf6c31613b701fe0646fd4e4d2ed2a7cbd61b27fd5514baa938/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f707974686f6e2d3336373041303f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d666664643534) |
| Development     | ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=Jupyter&logoColor=white) ![Colab](https://img.shields.io/badge/Colab-F9AB00?style=flat&logo=Google%20Colab&logoColor=white) |
| Collaboration   | ![GitHub](https://img.shields.io/badge/GitHub-100000?logo=github&logoColor=white) ![Discord](https://img.shields.io/badge/Discord-5865F2?logo=discord&logoColor=white) |

##### 사용 라이브러리 

| 항목 | 내용 |
|------|------|
| Python       |![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white) ![matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white) ![seaborn](https://img.shields.io/badge/seaborn-76B7B2?style=flat&logo=seaborn&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white) ![numpy](https://img.shields.io/badge/numpy-013243?style=flat&logo=numpy&logoColor=white)|

#### 데이터 설명 

이 프로젝트에서는 Google BigQuery에서 제공하는 Google Merchandise Store GA 학습용 샘플 데이터를 활용하였습니다. 

- 데이터 출처 : Google BigQuery 공개 데이터셋 (bigquery-public-data.google_analytics_sample)
- 데이터 특징
    - Google Analytics 샘플 스키마 기반, 세션 단위로 유입, 이벤트, 페이지뷰, 거래 로그 포함
    - 데이터 기간 : 2016-08-01 ~ 2017-08-01
- 활용 방법 : BigQuery Python 클라이언트를 통해 데이터 참조
- 데이터 컬럼 참조 : [Google Analytics 샘플 스키마](https://support.google.com/analytics/answer/3437719?hl=ko)



### 5. 프로젝트 내용



### 6. 한 줄 소감 

| 팀원 | 소감 |
|------|------|
| 김혜원 | |
| 변해민 | |
| 양원선 | |
| 전수연 | |