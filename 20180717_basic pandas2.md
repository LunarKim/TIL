20180717

캐글을 할 때 사이트를 먼저 보는 게 좋다. domain지식이 있는 분야에서 주로 일을 하게 된다. 게임회사에서 먼저 커리어를 쌓게 되면 게임에 특화된 domain지식이 생긴다. 

청원 크롤링을 하기전에 사이트를 먼저보고 분석해보는 게 도움이 된다. 최신순으로 볼 수도 있고 분야별로도 볼 수 있다. 국민청원은 정권 바뀌고 부터 생겼다. 

시기별로 핫한 이슈가 있다. 

저작권 정책이 자유롭게 되어있어서 긁어오기 쉽다. 

텍스트 데이터가 많아서 자연어처리를 다뤄볼 수 있을 것이다. 

학습 : 자연어 처리(맞춤법 수정) , 

책추천 : 파이썬 라이브러리를 활용한 데이터 분석. 이 책을 보면 파이썬 튜토리얼 사이트에 가면 보통 이내용이 있다. 10 minute 2 pandas로 가면, 

seaborn, 쓰고싶은 그래프를 눌러서 어떻게 쓰는 건지 예제를 볼 수 있다. 내가 column이나 raw를 바꿔서 적용할 수 있다. 

plotnine을 쓰기도한다. r에 있는 gg plot문법으로 그려져있다. 따라하다보면 어떻게 분석해야할지 감이 온다. 노트북을 하나만들어서 예제를 따라하는 것을 추천한다. 

백터데이터. data range

넘파이에서 내적(행렬의 곱하기연산)을 구할 때 행의 갯수와 백터의 (raw)의 개수가 항상 맞아야한다. df를 부르고 나서는 shape로 찍어본다. 이는 벡터값과 행의 값이 맞아야하기 때문이다. 그래서 합치려면 옵션을 지정해주어야한다. 

data type을 찍어보는 것이 중요하다. describe?를 하면 도움말이 나온다. 

```df2.describe?```: 도움말이 나온다. 

df2.describe() : 데이터의 대략적인 통계값이 나온다. 

```df2.<tap>``` : ta/p을 누르면 df2.모듈에서 쓸 수 있는 함수가 나온다. 

columns를 다 찍어보고 싶을 때가 있다. 그럴때는 column을 지정해주거나 날리거나 한다. 맨 위에 column이 0,1로 들어와서 날려버린 적이 있었다. 

```df. values ```: 행렬로 찍어준다. 

df.sort_index(axis=0,)

axis는 축이라는 뜻이다. = 1 , ascending = False. 

1 = column 0 = row 

```df.sort_values(by='D')```: D에 의해 정렬한다는 뜻임. 

getting 데이터 얻기

df. A와 동일한 Series를 생성하는 단일 열을 선택합니다.

df[['A', 'B']] 이렇게 두번 감싸주면 된다. 

- 국민청원 데이터 분석하기 

  ```import pandas as pd```

  ```inport numpy as np```

  두개를 준비해야한다. 

  (만약에 파이썬 2를 돌리고 싶으면 콜랩에서 runtime을 python2로 바꾼다. )

  

print(pd.__version__) 

pip는 터미널 명령어

pipenv : 특정 가상환경을 만들어서 설치하는 명령어

conda는 아나콘다의 명령어.

pep 8 은 style guide를 정해놓은 규약이고, 아톰에서 이 규약을 지킨다고 하면 알아서 잔소리를 해준다. 

parse date [start, end ] 

df. shape로 하면 몇 행 몇 열인지 알 수 있다. 



# 정규표현식 사용을 위해 import
import re
p = r'.*(돌봄|아이|초등|보육).*'
care = df[df['title'].str.match(p) |
           df['content'].str.match(p, flags=re.MULTILINE)]
care.shape

```match``` :  match되는 것을 알아서 찾아온다. 

결측치 , 전처리 (?)

count 와 unique가 다른 이유는 복붙해서 도배한 것을 알 수 있다.  

pep 8에서는 79character만 허용한다. 해상도가 낮으면 읽기가 힘들기 때문이다.

역슬래쉬 |를 하면 개행을 해도 한줄로 인식한다. 

df iloc [3:5, 0:2]

```df_20 = df.loc[df['votes'] > 200000]```

```df_20.votes.value_counts```: 이렇게 쓰는 것도 가능하다.

```df_20.shape```

```df_20.head(3)```

플롯나인 설치해오기

!pip install plotnine으로 설치하면 됨.

윈도우에서 패키지 없다고 오류가 뜨면 그 패키지 까지 설치해놓으면돼! 

