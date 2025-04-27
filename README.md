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
- 🔗 R-Project: [R](./BIO_18_Project.html) -> 제작 동기에서 언급한 R을 사용하여 제작했던 팀 프로젝트입니다.

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

## 🧑‍💻 문제 해결 및 도전 과제

- 웹크롤링 중 URL만 포함했을 때, 많은 웹사이트는 `requests` 모듈로 접속할 때 **"봇(Bot)"** 으로 인식해서 차단하지만, 사람처럼 보이게 하기 위해 `headers`에 브라우저 정보(User-Agent)를 넣어 주었습니다.
- 베팅 금액 처리 시, 금액이 너무 큰 관계로 백만 달러 단위로 변환하기 위해 `numpy` 라이브러리를 사용하였습니다.
- NBA 뷰어십 추출 시, NBA는 결승전 경기가 7전 4선승제이므로 한 경기의 시청률을 추출한 것이 아닌, 해당 결승전 경기들의 시청률을 추출한 뒤 평균화한 값으로 저장하였습니다.
- R로 제작했던 프로젝트에서 데이터 시각화를 위해 사용했던 컬러 파레트를 Python에서는 **matplotlib**를 사용하여 재현하였습니다.
- NCAA (March Madness) 연도 추출 시, 코로나19로 인해 경기가 없던 2020년 경기를 제외하기 위해 2000-2024년 데이터 추출을 2000-2029 정규식 사용을 통해 진행하였고, 이 정규식을 사용하기 위해 `re` 모듈을 사용했습니다.
- NCAA (March Madness) 뷰어십 추출 시, 뷰어십이 존재하는 테이블(표) 내부에 분석 기업에서 추적하지 않은 추가 스트리밍 시청이 추가된 값이 괄호 () 안에 추가로 기입되어 있었는데, 괄호 내부의 값은 제외해주었습니다.
- NCAA결승과 NBA결승 시청률을 직접 비교하며 해당 연도에 값을 보여지게 하기 위해 `plotly` 라이브러리를 사용하여 **인터렉티브 시각화**를 구현했습니다.

## 📷 데이터 시각화 캡쳐 화면

![bet.png](/screenshots/bet.png)

![nba.png](/screenshots/nba.png)

![ncaa.png](/screenshots/ncaa.png)

![nba_vs_ncaa.png](/screenshots/nba_vs_ncaa.png)
