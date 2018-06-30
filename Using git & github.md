### 20180628

__lecturer : 배로__

- Why we should use git?  
깃헙상에서는 수정을 할 수 없어서 로컬에서 소스를 가져와서 업데이트를 해야한다. 
  여기부터는 소스트리가 필요하다. 잘못만든 폴더를 수정하고 싶은 사람도 로컬에서 받아서 수정해야한다. 
  로컬에서 작업 -> 깃헙으로 푸시 & 애드 -> 데잇걸즈로 리퀘 -> merge

1. Installing Sourcetree
  소스트리를 이용해서 데잇걸즈 깃헙에 있는 것을 동기화할 수 있다. 
Ssh 키 만들기 : 소스트리를 깐다. 소스트리에서 generate ssh key를 만든다. 깃헙에서 ssh & gpa들어서 new ssh add (맨 위 초록색 키를 누른다. ) 소스트리에서 다운받고 나서 키내용을 복사해서 깃헙에다 붙인다. 
도구 - > 옵션 : 인증 – 호스팅 서비스 깃헙 선택 깃을 쓸 수 있는 호스팅 서비스에는 여러가지가 있는데 깁헙은 아틀란시스에서 만든것이다.
손호 프로토콜은 ssh 선택. 인증은 오오쓰로 한다. 깃헙으로 돌아가서 ssh 등록을 해야한다. New ssh key 로 가서 putty

2. Generate ssh key
:generating a new ssh key and adding it to the ssh agent
clone : 깃헙을 내컴퓨터에 복제해오는 것. 
fork :  github이용하는 것. 기존과 연결된채로 가져오는 것.

3. 한 디렉토리에 아무 파일하나를 만듦. 
remote : 원격저장소
원격저장소에 있는 것을 가져올것이다. 
완벽하지 않은 파일을 완벽하게 수정한 것을 ADD한다.

- 용어정리
  repository는 폴더임. 내 컴퓨터에 폴더를 만든다음 안에 특정한 파일을 넣으면 자동으로 git repository로 저장이됨. 
  Untracked영역임. Tracked영역.
  ADD :  Tracked. U-t에있는 애들중에 t로 옮기는게 애드임. / staged <- unstaged
  Tracked : Divided into two parts. stage/unstaged Stage. 
  STAGE : 영구히 저장된 것이됨. 
  ex) hello에서 hello!는 unstaged인 tracked가 됨. U,t는 무슨짓을 해도 git이랑 상관없음. 
  commit : 영구저장. commit하면 stage내용이 통로 복사되어서 ver.2가 됨. 
  어떤 파일을 수정해서 !로 찍으면 stage되고 커밋하는 순간 v3가 된다. 협업에 도움.
  pull request : 수정할 내용을 반영해달라고 요청하는 것. 
  merge :   master가 검토해보고 마음에 들면 땡겨가는 것이 
  branch : 이력을 관리하기 위해서 가지를 쳐서 일하기 위한 것. 무엇이 바뀌었는지 쉽게 확인할 수 있다.
           특정 branch로 풀리퀘를 보낼 수 있다. 
           게임의 경우 모든 것이 master에 반영되면 안되기 때문에 branch에서 업데이트 작업을 한다.
           그리고 나서 master에 반영을 함. 
           
- github의 용어.
Git을 원격에서 할 수 있는 프로그램. 
우리는 컴에서 작업하는 게 아니라 깃헙에서 작업함. 커밋 : 수정, add(상태를 바꾸는 것), commit 동시. 
협업을 할 때 고치고 싶은 사람이 fork해가고 맘대로 내용을 바꾸고 full reqeust를 보고 reject 할 수 있음.
같은 repository인데 하나를 중앙이라고 치는 것이고 이게 데잇걸즈의 임. 각자 작업한다음에 땡겨가 달라고 얘기하는 것이고 merge를 하는 것임. 

