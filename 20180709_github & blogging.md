# 20180709_github & blogging

jekyll을 이용해서 정적 블로깅. 



- 복습

```clone clone``` 을 해오면 아무것도 아닌 폴더를 ```git init```할 필요가 없다. 

내 깃헙은 : origin 

daitgirls :  upstream.

remote를 local에 등록을 해주는데 원래것은 upstream이라고 한다. 

twl을 하나 정의했다. ex)typora로 md를 정리해서 20180705_statistics. 로 정리했다. 얘를 나의 깃헙에 올리려면 ```git add``` -> stage상태로 만들어야한다. 이 변경사항을 ```git commit``` 

 ```git push```

```git push -u origin master. ```

2018 할때 처음에는 master브랜치로 push하고 나중에는 2018branch로 push했다. 

다른 사람들이 한 것을 가져오려면 git pull을 해야한다. 

```git pull ``` (fetch & merge) 다음에 목적어를 무엇을 써주느냐에 따라서 달라진다.

rebase는  fetch, merge까지 다 되는 것이다. commit 메세지가 남지않는다. git 이력이 깔끔해진다. remote와 통신할 때는 pull과 push를 쓴다. 이 뒤가 origin인지 master인지 어떤 브랜치에서 가져오고 보낼것인지가 뒤에 가 목적지를 쓰고 가운데 옵션을 적는다. 

__ex__ : 

```pull -옵션 f 목적지```

특정파일을 추가하고 원격으로 관리하려면 add, push하는데, 전체를 git으로 관리하겠다는 것이다. 

git ignore, git quore compile된 파일은 작업하지 말라는 것이다. local에서 관리하면 파일참, 이라던지 에디터를 쓰면 에디터에서 자동으로 생성하는 관리파일, 설정파일이 생긴다. 이런파일까지 커밋할필요가없어서 git ignore에 이런 파일을 써주면 무시하고 commit된다. 

크롤링을 할 때 key값을넣는데, 이런것도 공개되면 곤란해서 별도로 ignore에 저장한다. 

깃헙상에서는 daitgirls에서 내걸로 바로 반영할 수 없다. 따라서 local로 받아와서 내걸로 git push할 수 있다. 여전히 내것만 잇어서 git pull로 데잇걸즈 것을 받아올 수 있다. 내가 변경된 것에 대해서 반영할 때는 또 풀리퀘를 보낸다. 

최신으로 동기화하는게 이런 과정이다. 

git pull / push를 가장많이 쓰는데 , 

git push 하고 -h를 하면 도움말을 볼 수 있다. 각각의 옵션명령어의 설명을 볼 수 있다. --up amend 를 하면 커밋메세지를 수정할 수 있다. 

:q 하면 닫는것. 

:w q하면 쓰고 끈다는 것. push 했는데 push가 안된 것 같고 local에 남아 있는 것 같다고 하면 git status를 해보면 어떤 파일이 stage에 있고 head에 있는지 볼 수 있다. 

## 정적 블로깅 만들기

깃헙으로 블로그 만들기. 저장소를 만들고 거기서 pages로 만든다. 

master branch로 테마를 만들었다. custom domain도 설정할 수 있다. 

jekyll 

local에서 

로컬에서 확인해보고 서버를 뛰어보고 싶을 떄 로컬에 루비가 있으면 로컬에서 확인해보고 푸시ㅎ를 하면됨.  gh pages라는 것을 만들어야한다. 

gh pages branch 이걸 만든다. 그러면 정적 블로그처럼 사용할 수 있따. master branch로 쓰는 법과 gh pasges로 쓰는 두가지 방법이 있다. 

first. md 만들고 난 뒤 index.md에 가서 ```#[first post](first.md) commit change```라고 만들면 first post가 생긴다. 

다 지우고 link를 걸면 블로그처럼 쓸 수 있는 것이다. 

jekyll 과 루비. 루비 안되면 config만 수정해서 쓸 수 있다. 서버가 돌아가는걸 보려면 루비를 깔아서 해야한다. 

###### 루비와 파이썬

루비는 프로그래밍 언어이다. 루비는 루비를 많이 쓰게 된 계기는 ruby on rails라는 웹프레임웤때문이었다. 파이썬은 커뮤니티가 활성화되어있어 궁금한 것을 물어볼 곳이 있다. 그래서 더 많이 쓰는 편이다. 

gem은 명령을 좀 더 쉽게 할 수 있는 것이다. window에서 지킬 설치하는 것이 



```bundle exec ```를 붙여야함. 

```jekyll install ```



지킬 테마 - 3- sleek



아담블로그 테마를 포크해옴. 

포크해온 애의 gh -pages라는 b를 만들면, 이를 프로젝트 페이지로 쓸 수 있다. 

1. adam blog fork. 
2. gh - pages라는 branch생성. (깃헙상에서 gh - pages)라는 것을 생성. 내꺼에서 블로그를 볼 수 있다. 
3. settings gh pages branch.  - 이 페이지를 선택하면 정적블로그로 보여진다.
                                                  - blog rename도 가능하다. 
4. 잘 안되면 그냥 마크다운 페이지에서 해도된다. 깃헙에서 제공하는 블로그를 사용해도된다. 
5. rename이후에는 config . yml파일을 열어서 l8의 baseurl을 바꾼다.  yml파일에 adam blog를 blog로 다 바꿔야된다.

yml에서 google analytics만 수정하면 GA에서 바로 TRACKING이 된다. 

소스트리를 이용해서 add. 해보자

포크해온 것을 클론하고 이걸 로컬에서 수정하고 커밋할 것이다. 

루비에서는 yml을 설정파일로 관리한다. json form을 곧 배울 텐데, jekyll에서는 yml을 설정파일로 쓰고 있고, 이를 수정하면 반영이 된다. 

```permalink``` general을 무엇으로 보여줄것인지. markdown : kramdown. 마크다운에도 다른 형식이 있다. 

```plugins``` : gem으로 설치해주는 것이다. 번들러로 의존성이 ㅆ는 gem을 설치해서 페이지를 보여준다던지 sitemap을 보여주는 역할을 한다. google colab에서도 pip로 뭔가를 불러왓을 텐데, 이게 파이썬에서도 package manager이다. 



- 캐글. 레이블이 있느냐 없느냐에 따라 다르다. 
- 이 데이터에 따라 이 사람이 살았는지에 따라서 살아있는가를 나타냄. 
- 비지도학습은 클러스터링을 한다던지 차원축소를 하는 등. 군집화해서 비지도 학습을 하는 것. 경진대회는 특정대회에서 많이 올린다.특정 부동산회사에서 
- 데이터를 주고 정답을 맞추게 하는 것, 악성댓글인지 아닌지를 알려주는 경진대회 등이 있다. 
- 튜토리얼이 있는 경진대회는 몇개가 없는데, 타이타닉이나 백오브 ..? 어쩌구 자연어처리 경진대회가 있다. 
- 커널어워드라는 것도 있다. 커널들을 따라해보는 것도 좋다. 
- 이것을 일일커밋으로 많이 올린다. daily commit해보면 일일 커밋할게 많다. pandas나 numpy에 익숙해질 수 있다. 
- user rankings도 있다. 사람들 계정을 보고 소스를 보고 공부를 해볼 수 있다. 
- kaggle ml & 어쩌구를 분석할 것이다. 
- 아나콘다를 이용하면 데이터셋을 다운받아서 시행해볼 수 있다. 
- 10minute to pandas에 보면 설명이 나와있다. 
- 최성준 edwith  패캠강의들을 수 있음. 



데이터를 다운받은 곳에서 git bash로 터미널을 열 수 있다. 



data를 아나콘다에서 열기. 

지연쌤이 내준 폴더에 예시 notebook을 올려주실 것이다. 