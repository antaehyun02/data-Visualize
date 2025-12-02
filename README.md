# data-Visualize
# 🏥 100만 건강검진 데이터 분석 대시보드
### (Analysis of 1 Million Health Checkup Records)

> **"제로(Zero) 음료를 마시는 것보다, 술 한 잔 줄이는 것이 더 중요하지 않을까요?"** > 100만 명의 실제 데이터를 통해 현대인의 생활 습관과 만성 질환의 관계를 시각적으로 증명합니다.

---

## 📖 프로젝트 개요 (Overview)

### 1. 배경 및 목적
최근 '헬시 플레저(Healthy Pleasure)'와 '제로 슈거' 열풍으로 건강 관리에 대한 관심은 높아졌지만, 정작 건강의 기본인 **'금연'과 '절주'**의 중요성은 간과되고 있습니다. 본 프로젝트는 **국민건강보험공단의 100만 건 공공 데이터**를 분석하여, 흡연과 음주가 실제 건강 지표(혈압, 콜레스테롤, 비만 등)에 미치는 영향을 직관적인 **웹 대시보드**로 시각화하는 것을 목표로 합니다.

### 2. 주요 기능
* **방대한 데이터 처리:** 100만 건의 대용량 CSV 데이터를 효율적으로 로드 및 전처리
* **인터랙티브 분석:** 사용자가 직접 변수(X축, Y축)를 선택하여 가설을 검증하는 탐색적 분석 환경 제공
* **스토리텔링 대시보드:** 인구 통계부터 심층 분석까지 논리적 흐름에 따른 페이지 구성

---

## 📊 대시보드 구성 (Features)

이 대시보드는 `Streamlit`을 활용하여 총 4개의 섹션, 12개의 그래프로 구성되어 있습니다.

| 섹션 | 주요 내용 | 시각화 기법 |
| :--- | :--- | :--- |
| **1. 인구 통계** | 연령대별, 성별, 흡연율 분포 확인 | Altair Bar/Pie Chart |
| **2. 생활 습관** | 흡연/음주가 콜레스테롤, 간 수치, 혈압에 미치는 영향 | Box Plot, Violin Plot |
| **3. 당뇨 및 비만** | 연령 증가에 따른 당뇨 발병률 및 복부 비만 추이 | Bar Chart, Line Chart |
| **4. 상세 분석** | 사용자가 선택한 변수 간의 관계 교차 분석 (Interactive) | Heatmap, Interactive Box Plot |

---

## 🛠 사용 기술 (Tech Stack)

* **Language:** Python 3.9+
* **Web Framework:** Streamlit
* **Data Processing:** Pandas (Data Cleaning, Grouping)
* **Visualization:** * **Altair:** Interactive Charts, Tooltips
    * **Seaborn & Matplotlib:** Statistical Plots (Violin, Heatmap)
    * **Koreanize-matplotlib:** 한글 폰트 깨짐 방지

---

## 📂 프로젝트 구조 (File Structure)

```
health_checkup_dashboard/
├── dashboard.py          # 대시보드 메인 소스 코드
├── health_data.csv       # 원본 데이터 (100만 건, 공공데이터포털)
├── requirements.txt      # 필요 라이브러리 목록
└── README.md             # 프로젝트 설명 문서
```

## 설치 및 실행 방법 (Installation)
1. 저장소 클론 및 이동
```
git clone [레포지토리 주소]
cd health_checkup_dashboard
```

2. 가상환경 설정 (권장)
```
python -m venv .venv
# Windows
.\.venv\Scripts\activate
# Mac/Linux
source .venv/bin/activate
```

3. 필수 라이브러리 설치
```
pip install -r requirements.txt
```

4. 대시보드 실행
```
streamlit run dashboard.py
```

실행 후 브라우저에서 http://localhost:8501 접속

---
