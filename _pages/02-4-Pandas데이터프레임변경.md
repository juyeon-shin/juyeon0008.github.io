---
title : '02_4.Pandas 데이터프레임 변경' 
permalink: /KT_DX/02_4.Pandas데이터프레임변경/
excerpt : "01.데이터 다루기/02_4.Pandas데이터프레임변경"
categories : "KT_AIVLE_SCHOOL"
# tag : #"github.io"
date : '2023-09-12'

toc : True
toc_labels: True
toc_sticky : True
---

## 06. 데이터프레임 변경

- feature engineering 이라고도 함.

| 값  | 의미 |
| --- | --- |
| df.rename(
columns,
inplace) | 열 이름 변경
딕셔너리 형태로 바꿀 내용 입력
원본 대체 유무 |
| df.columns = [] | 열 이름 변경
열을 리스트로 지정함
df 모든 칼럼에 대해 지정해야함 |
| new_col = col1+col2  | 열 추가
등등의 수치 연산으로 파생변수를 생성할 수 있음 |
| tip.insert(위치,
이름 지정,
추가할 것) | 열 추가
원하는 위치에 넣기 |
| df.drop(
삭제할 것
axis,
inplace) | 열 삭제
삭제할 것 (인덱스번호 or 칼럼명)
축 지정 (0:행 삭제, 1:열 삭제)
원본 대체 |
|  |  |

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/39e14227-ace5-4e7b-9e4d-5ef33832c69f/Untitled.png)

- map()
    - 범주형 값을 다른 값으로 쉽게 변경 가능
    - 매핑되지 못한 값들은 결측값이 됨
    - 여러번 돌리면 에러남
    - df[’col’].map({바꿀 것 지정하기})

- replace
    - map과 비슷한 방법으로 사용
    - 매칭되지 않은 값은 원래값으로 넘어옴
    - df[’col’].replace(바꿀 것 지정하기)

범주값 나누기 (이산화)

- 연속된 값을 구간으로 나누어 범주화 시키는 것
- 

| 값  | 의미 |
| --- | --- |
| pd.cut(자를 것
bins
label) | 크기를 가지고 자름
0~50, 51~100
개수가 몇일지는 모름
경계값이 왼쪽에 포함됨 |
| pd.qcut(자를 것
나눌 그룹 개수
labels) | 개수로 나눔
4개씩
크기가 어느정도인지는 모름
같은 값은 한 쪽으로 몰림
 |
|  |  |

## 07. 데이터프레임 변경 (2)

결측치 확인

| 값  | 의미 |
| --- | --- |
| isna()
isnull() | 결측값이 있는 곳은 T, 없는 곳은 F |
| notna()
notnull() | 결측값이 있는 곳은 F, 없는 곳은 T |
|  |  |

결측치 제거

| 값  | 의미 |
| --- | --- |
| df.dropna(
subset,
axis,
inplace) | 결측치가 있는 행,열 제거
열 지정 (열에 있는 결측치만 제거)
0: 행, 1: 열
원본 대체 |

결측치 대체 (채우기)

| 값  | 의미 |
| --- | --- |
| df[’col’].fillna(
채울 값,
method
inplace)

채울 값 or method  | 특정 칼럼에 결측치를 지정해서 채우기
방법 (ffill : 바로 앞 값으로 변경, bfill : 바로 뒤 값으로 변경)
원본 대체 유무 |
| df.[’col’].interpolate(method) | 선형 보간법으로 채우기
방법 (linear : 선형보간법) |
|  |  |

이상치 탐색

- 히스토그램 or 박스플롯으로 가시적인 확인 가능
- IQR보다 큰 값이 존재
    - (IQR3 - IQR1)*1.5 가 일반적임
    - 

가변수 만들기

- 범주형 데이터를 수치형 데이터로 변환
    - 독립된 열로 변환하기에 범주 수 만큼 칼럼이 증가함
    - One-Hot-Encoding
    - fet_dummies()

다중 공선성

- 회귀분석에서 독립변수들 간에 나타나는 강한 상관관계

| 값  | 의미 |
| --- | --- |
| pd.get_dummies(
df,
columns,
drop_first | 가변수화
데이터
가변수화 할 칼럼 (리스트화 해서 일괄처리 가능, 지정 안하면 모든 범주형을 가변수화)
여러 가변수 중 하나 삭제 (다중공선성을 해결하기 위해)
 |

## 08. 데이터프레임 변경 (3)

데이터 합치기

| 값  | 의미 |
| --- | --- |
| pd.concat(
[df1,df2],
axis=1,
join=’outer’) | 데이터 합치기
[] : 합칠 데이터 넣기 (2개 이상 가능)
axis = 1 : 가로로 합치기, 옆으로 붙이기 → 열이 늘어남 : 칼럼이 중복됨
axis = 0 : 세로로 합치기, 아래로 붙이기 → 행이 늘어남 : 인덱스가 중복됨
join = ‘outer’ : 전체 다 붙이기
join = ‘inner’ : 인덱스가 겹치는 것만 붙이기 |
| pd.merge(
df1, df2
axis=1,
on=
how=) | 데이터 합치기
합칠 데이터 넣기 (2개만 가능)
axis = 1 or 0 : 붙일 방향 지정
how =  left, right, outer,inner
비교할  |
|  |  |