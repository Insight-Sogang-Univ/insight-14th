Pandas 사전과제
====

1. 판다스란?
---
* 데이터 분석에 특화된 파이썬 라이브러리.
* 행(Index)과 열(Column)로 이루어진 DataFrame이 기본 틀이다.
* 
```
    import pandas as pd
```
 로 불러온다.
* pd.read.csv('파일경로') 를 통해 데이터를 불러온다.
(html, exel, SQL 등 가능)


---
1. Series
---
* 인덱스와 값으로 이루어진 1차원 자료구조.
* 구성값은 모두 같은 데이터 타입이어야 함
(다른 데이터 타입이 오면 모두 문자열(object)로 처리됨)

```python
    sr = ['a','b','c','d']
    series = pd.series(sr)
```

로 만든다.
* 기본 인덱스는 0부터. 지정해주고 싶으면
```python

    dex=[1,2,3,4]
    series= pd.series(sr,index=dex)

```
하면 된다.

---
3. DataFrame
---
* 2차원 배열 구조 이다. (여러개의 series가 모인다/ 즉 컬럼 단위는 데이터 타입 동일하나 컬럼 간의 데이터 타입은 달라도 무방)
* 딕셔너리를 만들고
```python
    df=pd.DataFrame(dic)
    dex=[1,2,3,4]
    col=['a','b','c','d']
    df=pd.DataFrame(dic, index=dex, columns=col)
```

하면 된다. (인덱스와 컬럼 선택사항임)

---
4. 데이터 추출
---
  + 인덱싱: 단일 항목을 지목한다.
    ```python
    df[1]
    ```
+ 슬라이싱: 범위를 지정해 여러 항목을 추출한다.
   ```python
    df[start:end]
   ```

* 행(열)단위 추출
 ```python
   df.loc[행 이름, (열 이름)]
   df.iloc[행 순서, (열 순서)]
 ```

 * 인덱스 설정: 기존의 열 중 하나를 인덱스로 설정.
  ```python
    df.set_index('열 이름')
  ```

----
5. 데이터 조작
----
* 추가, 삭제, 정렬, 변환, 병합이 가능하다.
----
6. 집계함수
----
* 평균, 표준편차, 합계 등 대푯값을 구할 때 사용하는 함수.