공부를 할 때 공식문서를 참고 하는 것을 추천한다. 10minute to pandas를 참고하는 것이 좋다. 

주의할 점은 조선왕은 int인데 집값은 float이다. 포유류에서도 몸무게와 뇌무게도 type이 다르다. 



자료의 요약 시트 불러오기는 colab에서만

pd.read_csv.로 불러올것이다. 

df = pd. 

data frame은 column이 있고 시리즈들을 모여서 보여준 것은 data frame이라고 한다. 데이터를 분석하다보면 벡터와 행렬이라는 게 나온다. 캐글 서베이 조사를 보면 

pd.Da 

google colab에서 인증을 다 받으면 

```get_df``` df로 불러오라. 

```df. iloc[0]`` : 

 ```df.columns = df.iloc[0]``` : 0을 제목으로해라
``` df = df.reindex(df.index.drop(0))``` 0번째를 날려버려라. 

위에 제목으로 가져온 0번애를 해날려버리고 0번째를 제목으로 하겠다. index를 만들어라. 

```df_blood.head()```  상위 5개를 보여줌.  tail로 하면 끝에서부터(3)이렇게 할 수 있음. 

```print(df_blood.shape)``` : 몇개 행이고 칼럼인지. 

```df_blood.info()```  : 요약해서 보여줌. 

```freq``` : 빈도

unique는 안겹치는 거. count는 모든 수 . 

mean 값은 알아서 소수로 바꾼다. 정수도 알아서 소수로 바꿔준다. 



df_king = get_df('조선왕')

# 상위 5개의 데이터를 가져옵니다.
print(df_king.shape)
df_king.tail(3)

df_blood.info()



df 처럼 용어 더 덧붙이면 좋을 것 같다. 

column은 행으로 raw는 열로

note book으로 다 옮기고 난 다음에 맡은 부분을 번역해서 commit add push하면된다. 내용을 다 만들었으면 번역하기 전에 만든내용을 git add를 중간중간 해야한다. index. 

오후 수업 

시나리오 데걸 졸업 -> 데이터분석가 마케팅회사 창업을 하게됨. -> 블로그를 하는데 검증된 과학적 결정에 대한 것을 블로그에 쓴 것. 

모 이통사 사장님이 보고 모셔오게된 것. 

콜센터의 문제.

컨설팅좀 해달라함. 어떻게 하시겠습니까?

비용, 2500정도 

1.  회의 직무분배. 

2.  CS지점에 만들었는데 . -> HR  담당자 개략적인 문제상황파악한다, CS팀별 인터뷰. 

3.  홍보전략을 다시 짠다. CS콜센터 - > 

4. 인터넷 상담게시판 민원분석. -> 부가서비스, 요금제 인터넷으로 바꾸기 힘들다. 

   5. 보이스피싱 관련.

   - 콜센터 만족도가 낮다고 들었다.  HR팀의 팀장. 전국의 5개 센터가 있고 2000명의 직원이 있음.

       

인구통계학적인 정보들, 콜센터 상담센터에 어떤 결과를 가져올까. 질문을 먼저 하지말라고 얘기함. 

전화할때 공식적인 느낌이 안들게하는 게 중요하다. 

<실험적 사고> 교육받는 인원은 100명



보고할 때, 뭔가를 할 건지. 

[Gender, Diversity and Organization, 7.5 ECTS credits](http://lily.oru.se/studieinformation/ects/tillfalle_ects_lista.cgi?amnekod=SOA&kurskod=SO015G&lasar=2018/2019) [Sociology, Globalization Theory, 7.5 ECTS credits](http://lily.oru.se/studieinformation/ects/tillfalle_ects_lista.cgi?amnekod=SOA&kurskod=SO007G&lasar=2018/2019) [Sociology, Sustainability and Organization Theory, 7.5 ECTS credits](http://lily.oru.se/studieinformation/ects/tillfalle_ects_lista.cgi?amnekod=SOA&kurskod=SO008G&lasar=2018/2019) [Sociology, Welfare State and Society, 7.5 ECTS credits](http://lily.oru.se/studieinformation/ects/tillfalle_ects_lista.cgi?amnekod=SOA&kurskod=SO006G&lasar=2018/2019)  