---
title : '02_3.Pandas 데이터프레임 조회 & 집계' 
permalink: /KT_DX/02_3.Pandas데이터프레임조회&집계/
excerpt : "01.데이터 다루기/02_3.Pandas데이터프레임조회&집계"
categories : "KT_AIVLE_SCHOOL"
# tag : #"github.io"
date : '2023-09-12'

toc : True
toc_labels: True
toc_sticky : True
---


## 04.판다스 데이터프레임 조회

특정 열 조회

| 값  | 의미 |
| --- | --- |
| df[’col’] | 열 조회 |
| df.loc[: , ‘col’] | 열 조회 |
| df.loc[: , ‘col’: col3’] | 열 범위 조회 |
| df.loc[ 조건 ] | 단일 조건 조회 (전체 열) |
| df.loc[(조건 1) & (조건 2)] | 여러 조건 조회 (전체 열)
&, | |
| isin() | 하나의 값 or [여러개의 값]  |
| between(a,b) | a부터 b까지의 값  |
| df.loc[조건, [col]] | 조건을 만족하는 행의 일부 열 조회 |
|  |  |

- 열에 대한 조건을 주지만 뽑아내는 결과물은 행
    - 조건을 행에 넣어야



## 05. 데이터프레임 집계

- 연속형 변수 : 합, 평균, 최댓값, 최솟값
- 범주형 변수 : 개수, 최빈값

| 값  | 의미 |
| --- | --- |
| df.groupby(기준열, as_index,)[col].집계함수 | 그룹별 집계 |
| as_index=True | 집계 기준이 되는 열이 인덱스 열이 됨. (False : 인덱스가 012) |
| [col]
[[col]] | 집계하고 싶은 열 : 시리즈 형태
데이터 프레임 형태) |
| 집계함수 | 하고 싶은 집계 방법 |

import matplotlib.pyplot as plt

%config InlineBackend.figure_format='retina'

| 집계 시각화  | 의미 |
| --- | --- |
| plt.figure(figsize=(7,3)) | 그래프 사이즈 지 |
| plt.title(제목
size
pad
fontweight) | 제목 만들기
크기
그래프랑 간격
볼드체 지정 |
| plt.xlabel()
plt.ylabel() | x 라벨
y 라벨 |
| plt.grid() | x,y에 보조선 그리기 |
| plt.legend([],
loc) | 범례 표시
범례 위치 (upper left) |
| plt.axvline() | 버티컬 라인 그리기 |
| plt.axhline() | 수평선 라인 그리기 |
| plt.text(x,y,표시) | 텍스트 표시(x좌표, y좌표, 표시할 것) |
| plt.show() | 그래프 보여주기 |

| 값  | 의미 |  |
| --- | --- | --- |
| plt.bar(x,
height,
color) | 막대 차트 x
y
색 지정 |  |
| plt.bath() | 가로 막대 차 |  |
| plt.plot() | 라인 차트 | 연속형 값의 변화 추이  |
| plt.hist(
bins,
alpha
edgecolor) | 히스토그램 차트
묶음 개수
투명도
테두리 색 | 연속형 값의 분포 확인지 |

집계함수에서 숫자만 집계하기

- mean(numeric_only=True)

