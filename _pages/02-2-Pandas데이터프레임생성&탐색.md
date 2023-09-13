---
title : '02_2.Pandas 데이터프레임 생성 & 탐색' 
permalink: /KT_DX/02_2.Pandas데이터프레임생성&탐색/
excerpt : "01.데이터 다루기/02_2.Pandas데이터프레임생성&탐색"
categories : "KT_AIVLE_SCHOOL"
# tag : #"github.io"
date : '2023-09-12'

toc : True
toc_labels: True
toc_sticky : True
---


## 02. 판다스 데이터프레임 생성

import pandas as pd

- 일반적인 테이블 형태, 엑셀 형태
- 리스트나 딕셔너리로 저장 불가

| 값  | 의미 |
| --- | --- |
| index | 행 이름 |
| columns | 열 이름 |
| pd.DataFrame(data, index, columns) | 데이터 프레임 생성
딕셔너리, 이중 리스트 → 데이터 프레임으로 생성 가능 |

| csv 다루기 | 의미 |
| --- | --- |
| read_csv(
sep,
header,
index_col,
names,
encoding) | csv 읽기
구분자
칼럼 열
인덱스로 지정할 열
열 이름으로 사용할 문자열 리스트
인코딩 방식 |

| 값  | 의미 |
| --- | --- |
| head() | 앞의 5개 보여줌 |
| tail() | 뒤의 5개 보여줌 |
| set_index(
col,
inplace=False) | 인덱스를 지정한 열로 설정
열 지정
내부 값을 교체해 저장 (True)
 |
| reset_index(
drop=False,
inplace=False) | 인덱스를 초기화
기존 인덱스를 일반 열로 가져옴
내부 값을 교체해 저장 (True) |
| rename(
columns,
inplace=False) | 열 이름 변경
{변경전 : 변경후}
내부 값을 교체해 저장 |

## 03. 판다스 데이터프레임 탐색

| 값  | 의미 |
| --- | --- |
| index | 인덱스 확 |
| columns | 열 이름 확인 |
| values | 값 확인 |
| dtypes | 열 자료형 확인 |
| info() | 열 자료형, 값 개수 확인 |
| describe() | 기술 통계
(데이터 수, 평균, 표준편차, 최소, 4분위수 (1,2(중앙값),3사분위수),최대 |

| 값  | 의미 |
| --- | --- |
| sort_values(
by=[],
ascending=False) | 특정 열 기준으로 정렬
특정 열 지정 (2개 이상은 [] 처리)
내림차순 (2개 이상은 [] 처리) |
| unique() | 고유값 확인 |
| value_counts(
normalize=True) | 열 고유값의 개수 확인
백분율로 바꿈 |

| 값  | 의미 |
| --- | --- |
| sum(
axis=0) | 합계
열을 기준으로 더함 → 한 행이 가지는 요소에 대해 더한다
(axis= 1 : 행을 기준으로 더함 → 한 열이 가지는 요소에 대해 더한다) |
| mean() | 평균 |
| median() | 중앙값 |
| max() | 최대값 |
| min() | 최소값 |
| mode() | 최빈값 확인 |
