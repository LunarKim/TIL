width = 20

height = 5 * 9

width * height

마지막에 인쇄된 표현식은 변수 `_` 에 대입됩니다.  

이 변수는 사용자로서는 읽기만 가능한 것처럼 취급되어야 합니다. 값을 직접 대입하지 마세요 --- 만약 그렇게 한다면 같은 이름의 지역 변수를 새로 만드는 것이 되는데, 내장 변수의 마술 같은 동작을 차단하는 결과를 낳습니다. 

이미 내장되어있는 멋진 변수를 망가트리지 마세요~

\n produces a new line

\이 특수문자(기능)로 취급되게 하고 싶지않다면, 첫 따옴표 앞에 ```r```을 붙여서 날 문자열을 만들 수 있다. 

문자열 리터럴은 여러 줄로 확장될 수 있습니다. 한 가지 방법은 삼중 따옴표를 사용하는 것입니다. """...""" 또는 '''....''' 줄 넘김 문자는 자동으로 문자열에 포함됩니다. 하지만 줄 끝에 \를 붙여 이를 방지할 수도 있습니다. 

불변인 문자열과는 달리 리스트는 가변입니다. 즉 내용을 변경할 수 있습니다. 

append() __method__를 사용하면 리스트의 끝에 새 항목을 추가할 수 있습니다. 

> cubes. append 
>
> len() 이 왜 적	ㅇ

02 - 6 집합 자료형의 특징 

집합 자료형은 중복을 허용하지않음, 순서가 없음. 

튜플의 요소를 리스트처럼 del 함수로 지우려고 한 예이다. 



인덱싱  t1[0] 







딕셔너리는 리스트나 튜플처럼 순차적으로  해당 요소값을 구하지 않고 key를 통해 value를 얻는다. 이것이 바로 딕셔너리의 가장 큰 특징이다. baseball 이라는 단어를 찾기 위해 baseball만 들여다보는 것과 같은 맥락. 

- 딕셔너리는 어떻게 만들까?

  {Key1 : Value1, Key2  : Value2 }

  key 에는 변하지 않는 값을 사용하고, Value에는 변하는 값과 변하지 않는 값 모두를 사용할 수 있다. ex) key값에는 리스트(가변) 는 사용할 수 없으나 튜플(불변)은 사용할 수 있따. 

  - 딕셔너리 요소 삭제하기

    ```>>> del a[1]```

    ```>>> a ```

  - 딕셔너리는 인덱싱이나 슬라이싱 기법이 먹히지 않는다. 

    : 방법은 ```dic[key]```

    - 딕셔너리에서 중복되는 key값을 사용할 경우 랜덤으로 무엇인가가 무시될 수 있다. 

      

- 딕셔너리 관련 함수들 

  - key list만들기 

  ```>>> a.keys()```

  ````dict_keys(['name', 'phone','birth')```

  a. keys()는 딕셔너리 a의 key만을 모아서 dict_keys라는 객체를 리턴한다. 



이런 객체를 *이터러블* 이라고 부릅니다. 공급이 소진될 때까지 일련의 항목들을 얻을 수 있는 무엇인가를 기대하는 함수와 구조물들의 타깃으로 적합합니다. 

파이썬 프로그램안에서 파이썬 프로그램을 또 실행하는 것. 함수 안에 함수로 들어가는 것. 마지막에서 return되면 꿈에서 깨는 것이다. 마지막 함수가 가장 깊숙한 꿈. 토템을 쥐고 들어가면 꿈에서 잘 깰 수 있는데, 파이썬에서는 인자라고 할 수 있다. score를 들고 꿈에 빠져드는 것. score는 꿈에서 다시 data가 됨. 함수가 너무 많으면 stack over flow가 생긴다. 

꿈에 가지고 갈 수 있는 것을 parameter라고 한다. 

rambda?

sorted함수에 key를 추가로 넘겨주면서 뭘 기준으로 정렬할지를 넘겨준다. 

def by_names(student):

​    return student[0]

sorted(students, key=by_name)

def by_age(student) :

함수의 이름을 어떻게 짓느냐에 따라 메타포가 되어 프로그램 방향에 영향을 주기도 한다.

그래서 이름짓는것이 중요하다. 

함수를 이름짓지않고 순식간에 쓰고 버리는 것을 람다라고한다.

sorted(students, key = lambda, student: student[0])

by_name = lambda s: s[0]

sorted(students, key = by_name)

프로그램이 짧으면 짧을수록 대충써도 헛갈릴일이 없다. 코드가 간단해짐.  

프로그램이 길면 변수이름을 길게 지어야한다. 

but 여러번 쓸 경우에는 이름을 짓는게 좋음. 

나이순으로 정렬됨.

sorted는 return하거나 print하지는 않는다. 정렬만 할 뿐. 

기존에 탑재되어있지 않은데, 내가 쓰고 버리고 싶을 때 쓰면된다. 간단한 기능. 

lambda는 그냥 키워드다. 

def blah(어쩌고, 저쩌고) :

​    return 어쩌고 + 저쩌고

blah = lambda 어쩌고, 저쩌고 : 1

(결과값을 지정했다는 뜻)

lambda 어쩌고 : 아무 표현식

이거 전체를 표현한 결과 lambda가 만들어지고 인자가 하나임. 

blah를 적용하고 호출 하는 것. application 와 abstraction 

함수의 인자로는 명사형이 들어감. 함수이름은 동사가 들어감. 

몇몇 함수들은 함수의 인자로 함수를 받는다. sort함수가 대표적이 예인데, 함수의 인자로 함수를 받음. 

second order function이라고 함.(함수를 계속 포갬 우리가 배운 이차함수와는 관련없다.) 얘를 인자로 order를 받으면 third 

higher order function : sort 이차함수, 고차함수 라고 부른다. 



- 