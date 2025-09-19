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

본 프로젝트는 데이터 기반의 체계적인 고객 분석을 통해 이커머스 비즈니스의 전반적인 성과를 개선하고자 한다. 고객이 유입되는 시점부터 최종 구매에 이르는 전 과정을 다각도로 분석함으로써, 각 단계에서 발생하는 **비효율**과 **기회 요소**를 명확히 파악할 수 있다. 이를 마탕으로 마케팅 자원의 효율적 배분, 사용자 경험 최적화, 그리고 신규/재방문별 맞춤 전략을 수립하여 궁극적으로 **매출 증대**와 **고객 만족도 향상**을 동시에 달성하고자 한다. 

---

### 2. 팀원 소개

| ![alt text](image-1.png) | ![alt text](image-3.png) | ![alt text](image-2.png) | ![alt text](image-4.png) | 
|------|------|------|------|
| 김혜원 | 변해민 | 양원선 | 전수연 | 

---

### 3. 프로젝트 기간 및 수행 내용

| 기간 | 수행 내용 |
|------|-----------|
| 2025.05.01 ~ 2025.05.18 | - EDA |
| 2025.06.05 ~ 2025.07.26 | - AARRR 분석 <br>- A/B test<br>- 퍼널 분석 <br>- pagepath 분석 |
| 2025.08.01 ~ 2025.08.28 | - 보고서 작성 <br>- 코드 정리 <br>- 깃허브 정리 |

---

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
| Python       |![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white) ![matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white) ![seaborn](https://img.shields.io/badge/seaborn-76B7B2?style=flat&logo=seaborn&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white) ![numpy](https://img.shields.io/badge/numpy-013243?style=flat&logo=numpy&logoColor=white) ![regex](https://img.shields.io/badge/re-000000?style=flat&logo=regex&logoColor=white) ![collections](https://img.shields.io/badge/collections.Counter-3776AB?style=flat&logo=python&logoColor=white) ![plotly](https://img.shields.io/badge/plotly-3F4F75?style=flat&logo=plotly&logoColor=white) ![networkx](https://img.shields.io/badge/networkx-000000?style=flat&logo=python&logoColor=white) ![hmmlearn](https://img.shields.io/badge/hmmlearn-FF6F00?style=flat&logo=python&logoColor=white) ![LabelEncoder](https://img.shields.io/badge/LabelEncoder-00A98F?style=flat&logo=scikit-learn&logoColor=white)|

#### 데이터 설명 

이 프로젝트에서는 Google BigQuery에서 제공하는 Google Merchandise Store GA 학습용 샘플 데이터를 활용하였습니다. 

- 데이터 출처 : Google BigQuery 공개 데이터셋 (bigquery-public-data.google_analytics_sample)
- 데이터 특징
    - Google Analytics 샘플 스키마 기반, 세션 단위로 유입, 이벤트, 페이지뷰, 거래 로그 포함
    - 데이터 기간 : 2016-08-01 ~ 2017-08-01
- 활용 방법 : BigQuery Python 클라이언트를 통해 데이터 참조
- 데이터 컬럼 참조 : [Google Analytics 샘플 스키마](https://support.google.com/analytics/answer/3437719?hl=ko)

---

### 5. 프로젝트 내용

- 📑 [전체 보고서 (Notion)](https://www.notion.so/273b3e70357580c891dfc87323c20e09) 
- 📊 [A/B test 보고서 (Notion)](https://www.notion.so/A-B-Test-24c95d13920080fbb959c5dc035798f3) 
- 💻 코드
    - [전체 흐름 지표 (colab)](https://colab.research.google.com/drive/1JoRZfBuGixkqC1PJw1y5x9bCIAp2-NyJ)
    - [날짜 및 요일 지표 (colab)](https://colab.research.google.com/drive/1EBY8UBOm26-MkAToXV3EtyQEW9FIa88D)
    - [유입경로별 AARRR (colab)](https://colab.research.google.com/drive/1EnhEJLBnWiBzHtqkc-AYnseuVr66PFOL)
    - [퍼널분석 및 이벤트 행동 분석 (colab)](https://colab.research.google.com/drive/1yeh-CjmYydD-A7G0bsurjRpdO_hMp5Kg)
    - [페이지 흐름 분석1 (colab)](https://colab.research.google.com/drive/1nJ7Xr2dVzaNBtIRGxNYy1981r6z9OQvI)
    - [페이지 흐름 분석2 (colab)](https://colab.research.google.com/drive/1Yuz8QQDo0twzR5zUJyinraOp21ZspXxn)
    - [A/B test (colab)](https://colab.research.google.com/drive/1bjQOVQztZuWdSk9mkEQ1EQdnO0t1pK8A)

#### 🔍 분석 내용 정리

#### 1. 전체 흐름 지표
- 1-1. Acquisition 변수 탐색 및 시각화
- 1-2. ARPU / ARPPU 분석
- 1-3. 고객별 누적 매출 분포 (Pareto)
- 1-4. 브라우저·운영체제·기기별 Top 20 유입군 ARPU/전환율 분석
- 1-5. 기기 유형별 Acquisition 품질 비교 (모바일 vs 데스크탑 vs 태블릿)
- 1-6. 국가별 Revenue Top 10 분석
- 1-7. 제품별 Revenue 비교
    - Repeat Purchase Rate (재구매율)
    - Cart Abandonment Rate (장바구니 이탈률)

---

#### 2. 날짜 흐름 지표
- 2-1. 코호트 분석
- 2-2. visitStartTime 기반 유입 트렌드
- 2-3. DAU / MAU / Stickiness
- 2-4. Classic Retention (N일 후 재방문율)
- 2-5. 요일별 Retention
- 2-6. Long Retention (30~60일 내 재방문)

---

#### 3. 유입경로별 AARRR 분석
- 3-1. Acquisition
    - source별 세션 수와 신규 방문자 수
    - source_medium별 세션 수와 신규 방문자 수
    - channelGrouping별 세션 수와 신규 방문자 수
    - medium의 Non_Paid vs Paid 세션 수 비교
- 3-2. Activation
    - channelGrouping별 체류시간
    - channelGrouping별 이탈률 (bounces 기준)
    - channelGrouping별 이탈률 (eventAction 기준)
- 3-3. Retention
    - channelGrouping별 7일/30일 이내 재방문율
- 3-4. Revenue
    - channelGrouping별 ARPU
    - channelGrouping별 구매 전환율
    - channelGrouping별 첫 방문 이후 평균 구매 소요일 

---

#### 4. 퍼널 분석 및 이벤트 행동 분석
- 4-1. 고객 이탈 발생 단계 분석
    - 퍼널 단계별 세션 수, 전환율, 이탈률
    - 신규 고객과 재방문 고객의 전환율 비교
    - 유입 경로별 퍼널 분석
- 4-2. 퍼널별 체류시간 분석
    - 퍼널 단계별 평균 체류시간
    - 체류시간이 구매 전환에 끼치는 영향 분석
- 4-3. 이벤트 유형별 구매 전환율 차이
- 4-4. 활성화 유저 vs 이탈 유저 행동 비교
- 4-5. 이탈 고객의 재방문 후 전환율
    - 이탈 단계별 전환율
    - 이탈 단계별 평균 전환 소요일 수

---

#### 5. 페이지 흐름 분석 (Page Navigation & Conversion Flow)
- 5-1. 페이지 흐름 분석 결과
    - 유입 페이지 및 초기 행동 흐름 분석
    - 신규 사용자와 재방문 사용자 중심의 랜딩페이지 흐름 분석
- 5-2. 전환 vs 비전환 세션 네비게이션 심층 분석
    - 전환 vs 비전환 세션의 Top 페이지
    - 전환 플로우 정형성 검증 및 basket 중심 접근
- 5-3. 장바구니 중심 트리거 기반 사용자 행동 구조 분석
    - /basket 기준 전환 구조 비교
    - 장바구니 포함 여부 기반 전이·흐름 분석
- 5-4. 모델 기반 전환/이탈 흐름 해석
    - Markov Chain 기반 페이지 기여도 분석
    - HMM 기반 사용자 상태 전환 분석
    - 전환 단계별 HMM 흐름 비교 분석 (전체 / 장바구니 미도달 / 장바구니 도달 / 매출 발생)
    - 매출 전환을 가르는 행동 전이 차이
- 5-5. 이탈률 높은 페이지 분석
    - Top 10 이탈 페이지 시각화
    - 장바구니 도달/구매 여부별 이탈 페이지 비교 분석
    - /googleredesign 내 콘텐츠 수준 분석


---
#### 6. 광고/UX A/B Test 분석

##### 주요 가설
1. 광고 위치(브랜드 영역 vs 하단 추천 영역)에 따른 클릭률 차이
2. 광고 유형(이미지 vs 텍스트)에 따른 구매 전환율 차이
3. 제품 노출 수(12개 이하/이상)에 따른 이탈률 차이

##### 결과 요약
- 광고 위치: 브랜드 영역 클릭률 > 하단 추천 영역 클릭률
- 광고 유형: 전환율 차이 없음(데이터 불균형 이슈)
- 제품 노출 수: 12개 이상 노출 시 이탈률 감소

##### 인사이트
- 광고 위치 최적화로 CTR 향상 가능
- 추가 데이터 확보 후 광고 유형 효과 재검증 필요
- 최소 12개 제품 노출로 이탈률 감소 가능
---
### 6. 한 줄 소감 

| 팀원 | 소감 |
|----------|-------------|
| 김혜원 | 이번 프로젝트를 통해 사용자 행동 데이터를 직접 다루고, BigQuery를 연결해 쿼리를 작성하며 결과를 도출하는 과정을 경험할 수 있었습니다. 단순히 데이터를 불러오는 수준을 넘어 실제로 분석 흐름을 설계하고 시각화까지 이어가면서, 이커머스 데이터 구조와 해석 방식에 대한 이해도를 크게 높일 수 있었습니다. 데이터 분석 전 과정을 직접 수행해 본 값진 경험이었다고 생각합니다. |
| 변해민 | 이커머스 데이터의 전체 구조와 흐름을 이해하고 SQL을 활용하여 실제 분석을 수행하며 데이터 기반 의사결정 과정을 직접 체험하고 실무 감각을 익힐 수 있는 좋은 경험이었습니다. |
| 양원선 | 고객 행동 분석에서 얻은 인사이트를 바탕으로 마케팅 전략을 제시하며, 데이터가 비즈니스의 방향성을 제시하는 중요한 도구임을 실감했습니다. |
| 전수연 | 단순한 지표 해석을 넘어, 사고가 확장되는 과정을 거치며 데이터가 전략적 통찰로 이어지는 즐거움을 경험했습니다. |