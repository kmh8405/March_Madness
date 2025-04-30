# 🏀 Project 5 - March Madness (PYTHON)

## 🧭 프로젝트 소개

NCAA(National Collegiate Athletic Association) 라는 **전미 대학 체육 협회**의 여러 스포츠 중, 농구에 대한 데이터 조사입니다.

“농구”하면 대표적으로 떠오르는 것은 **NBA**로, 한국에서도 많은 사람들에게 익숙하고 즐겨보는 사람들이 많지만, 미국 내에서는 NCAA농구가 NBA만큼 인기가 높으며, 특히 3월에 진행되는 **March Madness**는 미국에서 큰 관심을 갖습니다.

이러한 이유로 과연 미국 내에서의 NCAA 농구의 인기는 어느정도인지 확인해보고자 진행하게 된 프로젝트 입니다. 

이 프로젝트는 **NCAA 농구(March Madness)** 의 인기를 두 가지 방식으로 분석했습니다: 

1. **연도별 베팅 금액 변화** 분석
2. **NBA 결승과 NCAA 결승 시청률 비교** 분석

---

## 💡 제작 동기

R과 Python은 데이터 분석에 많이 사용되는 언어입니다. 대학에서 R (R-Studio)을 배웠고 Python은 이번에 처음 배워보게 되어, R을 사용하여 제작했던 프로젝트와 동일한 주제로 Python을 활용하여 프로젝트를 진행했습니다.

---

## 🔗 관련 링크

- 🔗 Colab:  [Colab](https://colab.research.google.com/drive/15gGNITW41iiDl9lQNqf0kp4BGJp_Qdmx?usp=sharing)
- 🔗 R-project: [R-project](https://aerial-scarer-980.notion.site/R-Project-1e44ffa3e1d78001863fdf8444689153?pvs=4)

---

## 📦 프로젝트 구조
```
PYTHON PROJECT/
├── screenshots/                     # README 용 스크린샷 모음
│   ├── bet.png
│   ├── nba_vs_ncaa.png
│   ├── nba.png
│   └── ncaa.png
├── march_madness_wagers.csv         # 연도별 베팅 금액 데이터
├── nba_finals_viewership.csv        # NBA 결승 시청률 데이터
├── ncaa_final_viewership.csv        # NCAA 결승 시청률 데이터
├── ncaa.ipynb                       # Jupyter Notebook (markdown + python)
├── README.md                        # README
├── requirements.txt                 # pip로 설치한, 이 프로젝트에서 사용한 외부 라이브러리 목록
```
---

## 🗓️ 제작 기간

- **2025.04.24 ~ 2025.04.27 (총 4일)**

---

## 🧑 제작 인원

- 개인 프로젝트 (1인 개발)

---

## 💻 사용 기술 스택

- **Python** (웹 크롤링 및 데이터 분석)
    - **Requests** (웹 페이지 요청 및 데이터 수집)
    - **BeautifulSoup** (HTML 파싱 및 데이터 추출)
    - **Pandas** (데이터 처리 및 분석)
    - **Matplotlib** (데이터 시각화)
    - **Seaborn** (통계적 데이터 시각화)
    - **Plotly** (인터랙티브 데이터 시각화)
    - **Numpy** (수치 계산 및 배열 처리)

---

## 🕹️ 웹크롤링 페이지

- NCAA 베팅 금액 관련 :
    - https://www.boydsbets.com/much-bet-march-madness/ 에서 제공하는 베팅 금액의 변화를 확인했습니다.
- NCAA Championship Final Viewership :
    - https://www.sportsmediawatch.com/ncaa-final-four-ratings-history-most-watched-games-cbs-tbs-nbc/ 에서 NCAA 결승의 시청률 데이터를 크롤링했습니다.
- NBA Finals Viewership :
    - https://www.sportsmediawatch.com/nba-finals-ratings-viewership-history/ 에서 NBA 결승의 시청률 데이터를 크롤링했습니다.

---

## 📊 분석 결과

1. **연도별 베팅 금액 변화**: 시간이 지날수록 NCAA 농구에 대한 베팅 금액이 꾸준히 증가하는 경향을 보였습니다. → 인기가 꾸준히 상승하는 것으로 보여집니다.
2. **NBA 결승과 NCAA 결승 시청률 비교**: 분석 결과, NCAA (March Madness) 결승의 시청률이 NBA 결승보다 대체로 더 높았습니다. → NBA보다 NCAA의 주목도가 더 높은 것으로 보여집니다.

결론 : 미국 내에서 NCAA의 인기는 점점 증가하는 추세이며, 시청률로만 본다면 March Madness는 NBA보다도 더 인기가 많은 농구 경기입니다.

---

## 🔮 향후 추가 가능 데이터

- **다른 스포츠 종목과의 비교**: NBA 외에도 NFL이나 MLB 등 다른 스포츠와 NCAA 농구의 시청률 및 베팅 금액 변화를 비교하는 작업을 추가할 수 있습니다.
- **기타 변수 분석**: 경기 승패나 유명 선수들(떠오르는 신예 스타 선수들)의 출전 여부 등을 포함하여 좀 더 세밀한 분석을 할 수 있습니다.

---

## 🛠️ 기술적 문제 해결 및 구현 전략

- 웹크롤링 시 `requests` 모듈로 접속할 때 **"봇(Bot)"** 으로 인식해서 차단되는 문제를 해결하기 위해 `User-Agent`가 포함된 `headers`를 설정해 사람처럼 보이도록 처리.
- 베팅 금액 데이터를 다루기 위해, 과도한 수치를 백만 단위로 변환하기 위해 `numpy` 활용.
- NBA 결승은 최대 7경기로 구성되므로, 단일 경기가 아닌 결승전 전체 평균 시청률을 계산해 저장
- R에서 사용했던 컬러 파레트를 Python의 **matplotlib**로 재현하여 시각화.
- NCAA (March Madness) 연도 추출 시, 코로나19로 인해 경기가 없던 2020년을 제외하기 위해 `re` 모듈로 정규식(2000-2029년)을 활용.
- NCAA (March Madness) 뷰어십 수치 중 괄호 안 스트리밍 수치를 제외한 수치만 추출.
- NCAA결승과 NBA결승 시청률을 연도별로 직접 비교하기 위해 `plotly`로 **인터렉티브 시각화**를 구현.

## 📷 데이터 시각화 캡쳐 화면

![bet.png](/screenshots/bet.png)

![nba.png](/screenshots/nba.png)

![ncaa.png](/screenshots/ncaa.png)

![nba_vs_ncaa.png](/screenshots/nba_vs_ncaa.png)
