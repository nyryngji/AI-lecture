## 데이터 과학을 위한 파이썬 패키지

> **파이썬 가상환경 만들기**
- **python interpreter** : 현재 설치되어 있는 패키지 확인
<br>

> **numpy**
- **np.random.random** : 0과 1 사이 난수 생성

>
    import numpy as np
    a=np.random.random((2,3))
    print(a)
    -> array([[0.53221954, 0.40125372, 0.86720199],
              [0.66802154, 0.11344105, 0.54052195]])

- **np.zeros**

>
    import numpy as np
    c=np.zeros((2,3))
    print(c)
    -> array([[0., 0., 0.],
              [0., 0., 0.]])

- **.reshape(array 개수,몇 개,행,열)** : 기존 array에서 변환된 것을 반환 

>
    import numpy as np
    a=array([[0.53221954, 0.40125372, 0.86720199],
             [0.66802154, 0.11344105, 0.54052195]])
    b=a.reshape(3,2)
    print(b)
    -> array([[0.53221954, 0.40125372],
              [0.86720199, 0.66802154],
              [0.11344105, 0.54052195]])
    

- **.arange** : list 등을 array로 변환

- **.flatten(), .ravel()** : 1차원으로 변환

- **.T** : 기존에 있던 2차원 행렬의 행과 열을 바꿔서 출력
>
    import numpy as np
    a = [[ 0  1  2  3  4  5]
         [ 6  7  8  9 10 11]]
    b=a.T
    print(b)
    -> array([[ 0,  6],
              [ 1,  7],
              [ 2,  8],
              [ 3,  9],
              [ 4, 10],
              [ 5, 11]])

- **.ndim** : array의 차원이 몇 차원인지 출력

>
    b=np.array([1,2,3])
    print(b.ndim)
    -> 1
<br>

> **pandas**

- Series(데이터, index=첨자, dtype='') : 첨자를 앞에 붙이고 목록 출력 (1차원 배열 형태, 열 데이터를 다룸)
    + index를 지정하지 않으면 첨자가 0부터 시작함

>
    s = pd.Series([1, 3, 5, np.nan, 6, 8])
    print(s)
    -> 0    1.0
       1    3.0
       2    5.0
       3    NaN
       4    6.0
       5    8.0
       dtype: float64

- date_range
- .DataFrame(np.random.randn(행,열), index=행 제목, columns=열 제목) : 엑셀처럼 데이터 출력
- **.head(숫자)** : 행의 개수(숫자)만큼 데이터 출력 (데이터가 많아도 해당 숫자 개수만큼만 출력) 
- .value_counts() : series에 나온 값의 개수를 세서 출력

>
    s = pd.Series(np.random.randint(0,7,size=7))
    s.value_counts()

- .str.lower() : 대문자를 전부 소문자로 변환
- .head(숫자)(<->tail(숫자)) : 데이터 중 앞에서부터 출력
- 
