<Git 사용법>
=========

### 해당 레파지토리 주소 : https://github.com/nny0ng/SE2

<br>

>## add

add는 해당 파일을 추적(stage)시키는 명령어입니다. 

추적되고 있는 파일만 커밋에 포함됩니다. 

주로 git add . 의 형태로 사용합니다. 

git add . 명령어는 변경이 일어난 모든 파일을 추적하게 합니다.

<br>

>## branch

*branch*는 새로운 브랜치를 만드는 명령어입니다.

git의 브랜치는 놀랍도록 가볍습니다. 

브랜치는 특정 커밋에 대한 참조(reference)에 지나지 않습니다. 

이런 사실 때문에 브랜치는 서둘러서 자주 만들어야 좋습니다.

브랜치를 많이 만들어도 메모리나 디스크 공간에 부담이 되지 않기 때문에, 작업을 커다른 브랜치로 만들기 보다 작은 단위로 잘게 나누는 것이 좋습니다.

단순히 브랜치는 "하나의 커밋과 그 부모 커밋들을 포함하는 작업 내역"이라고 기억하면 됩니다.

<br>

>## checkout

*checkout*은 현재 *이 있는 브랜치에서 다른 새로운 브랜치로 이동할 때 사용하는 명령어입니다.

    git checkout [브랜치명]

<br>

>## clone

*clone*은 로컬에서의 git init에 해당하는 명령어입니다. 

원격에서 저장소를 최초로 가져올 때는 git pull 대신 git clone을 씁니다.

<br>

>## commit

*commit*은 Git 저장소에 디렉토리에 있는 모든 파일에 대한 스냅샷을 기록하는 명령어입니다. 

디렉토리 전체를 복사하여 붙여넣는것과 유사하지만, 훨씬 유용한 방법입니다.

Git은 가능한 한 커밋을 가볍게 유지하고자 하기때문에, 커밋할 때마다 디렉토리 전체를 복사하진 않습니다. 

각 커밋은 저장소의 이전 버전과 다음 버전의 변경내역 ("delta"라고도 함)을 저장합니다. 

그래서 대부분의 커밋이 그 커밋 위의 부모 커밋을 가리킵니다.

<br>

>## config

*config*라는 도구로 설정 내용을 확인하고 변경할 수 있습니다.

 git은 이 설정에 따라 동작하고, 이때 사용하는 설정 파일은 세 가지입니다.

- /etc/gitconfig 파일: 시스템의 모든 사용자와 모든 저장소에 적용되는 설정입니다. git config --system 옵션으로 이 파일을 읽고 쓸 수 있습니다. 

- ~/.gitconfig, ~/.config/git/config 파일: 특정 사용자(즉 현재 사용자)에게만 적용되는 설정입니다. git config --global 옵션으로 이 파일을 읽고 쓸 수 있습니다. 특정 사용자의 모든 저장소 설정에 적용됩니다.

- .git/config : 이 파일은 Git 디렉토리에 있고 특정 저장소(혹은 현재 작업 중인 프로젝트)에만 적용됩니다. --local 옵션을 사용하면 이 파일을 사용하도록 지정할 수 있습니다. 하지만 기본적으로 이 옵션이 적용되어 있습니다. 

<br>

>## init

*init* 명령은 .git 이라는 하위 디렉토리를 만듭니다. 

.git 디렉토리에는 저장소에 필요한 뼈대 파일(Skeleton)이 들어 있습니다. 

이 명령만으로는 아직 프로젝트의 어떤 파일도 관리하지 않습니다.

git이 파일을 관리하게 하려면 add 명령으로 파일을 추가하고 commit 명령으로 커밋해야 합니다.

<br>

>## log

*log*는여태 커밋한 이력을 열람할 수 있도록 하는 명령어입니다.

git log에는 추가적인 옵션을 통해 옵션에 맞는 커밋을 확인할 수도 있습니다.

<br>

>## merge

*merge* 명령은 두 개의 부모(parent)를 가리키는 특별한 커밋을 만들어 냅니다. 

두개의 부모가 있는 커밋이라는 것은 "한 부모의 모든 작업내역과 나머지 부모의 모든 작업, 그리고 그 두 부모의 모든 부모들의 작업내역을 포함한다"라는 의미가 있습니다.

두개의 브랜치를 하나로 합친 후 모든 커밋의 색이 같아지도록 할 수 있습니다. 이는 두 브랜치가 모두 저장소의 모든 작업 내역을 포함하고 있다는 뜻입니다.

<br>

>## pull

*pull* 명령은 대부분 git fetch 명령을 실행하고 나서 자동으로 git merge 명령을 수행하는 것 뿐입니다.

 clone 이나 checkout 명령을 실행하여 추적 브랜치가 설정되면 pull 명령은 서버로부터 데이터를 가져와서 현재 로컬 브랜치와 서버의 추적 브랜치를 Merge 합니다.

    +) fetch 명령은 서버에는 존재하지만 로컬에는 아직 없는 데이터를 받아와서 저장합니다. 이 때 워킹 디렉토리의 파일 내용은 변경되지 않고 그대로 남습니다. 서버로부터 데이터를 가져와서 저장해두고 사용자가 merge 하도록 준비만 해둔다고 말할 수 있습니다.
 
  일반적으로 fetch 와 merge 명령을 명시적으로 사용하는 것이 pull 명령으로 한번에 두 작업을 하는 것보다 낫습니다.

  <br>

>## push

*push* 명령은 쓰기 권한이 있는 리모트 저장소에서 로컬의 브랜치를 서버로 전송하는 역할을 합니다.

로컬 저장소의 브랜치는 자동으로 리모트 저장소로 전송되지 않기에 명시적으로 브랜치를 Push 해야 정보가 전송됩니다. 

따라서 리모트 저장소에 전송하지 않고 로컬 브랜치에만 두는 비공개 브랜치를 만들 수 있습니다. 

또 다른 사람과 협업하기 위해 토픽 브랜치만 전송할 수도 있습니다.

<br>

>## rebase

*rebase* 명령은 브랜치끼리의 작업을 접목하는 두번째 방법입니다. 

리베이스는 기본적으로 커밋들을 모아서 복사한 뒤, 다른 곳에 떨궈 놓는 것입니다.

조금 어렵게 느껴질 수 있지만, 리베이스를 하면 커밋들의 흐름을 보기 좋게 한 줄로 만들 수 있다는 장점이 있습니다. 

즉, 실제로는 두 기능을 따로따로 개발했지만 마치 순서대로 개발한 것처럼 보이게 됩니다.

리베이스를 쓰면 저장소의 커밋 로그와 이력이 한결 깨끗해집니다.

<br>

>## remote

*remote* 명령으로 현재 프로젝트에 등록된 리모트 저장소를 확인할 수 있습니다. 

이 명령은 리모트 저장소의 단축 이름을 보여줍니다. 

저장소를 clone 하면 origin이라는 리모트 저장소가 자동으로 등록되기 때문에 origin이라는 이름을 볼 수 있습니다.

<br>

>## reset

*reset* 명령은 브랜치로 하여금 예전의 커밋을 가리키도록 이동시키는 방식으로 변경 내용을 되돌립니다. 이런 관점에서 "히스토리를 고쳐쓴다"라고 말할 수 있습니다. 

즉, git reset은 마치 애초에 커밋하지 않은 것처럼 예전 커밋으로 브랜치를 옮기는 것입니다.

reset 명령은 정해진 순서대로 세 개의 트리를 덮어써 나가다가 옵션에 따라 지정한 곳에서 멈춥니다.

- 1단계 : HEAD가 가리키는 브랜치를 옮긴다. (--soft 옵션이 붙으면 여기까지)

- 2단계 : Index를 HEAD가 가리키는 상태로 만든다. (--hard 옵션이 붙지 않았으면 여기까지)

- 3단계 : 워킹 디렉토리를 Index의 상태로 만든다.

<br>

>## --hard

위의 reset 명령에서 --hard 옵션을 사용하면 reset 명령은 3단계까지 수행합니다.

<br>

>## status

*status* 명령은 보통 파일의 상태를 확인할 때 사용합니다. 

Staged 상태인지 아닌지, 변경사항이 있는지 없는지 등 파일의 모든 상태를 확인할 수 있습니다.

<br>

>## tag

*tag* 명령으로 이미 만들어진 태그들을 확인할 수 있습니다.

태그는 알파벳 순서대로 보여지며, 검색 패턴을 사용하여 태그를 검색할 수 있습니다. 

Git의 태그는 Lightweight 태그와 Annotated 태그로 두 종류가 있습니다.

    //Lightweight 태그
    git tag 
    => -a, -s, -m 옵션 사용 X

Lightweight 태그는 브랜치와 비슷한데 브랜치처럼 가리키는 지점을 최신 커밋으로 이동시키지 않습니다.

 단순히 특정 커밋에 대한 포인터일 뿐입니다.

    //Annotated 태그
    git tag -a

한편 Annotated 태그는 Git 데이터베이스에 태그를 만든 사람의 이름, 이메일과 태그를 만든 날짜, 그리고 태그 메시지도 저장합니다.

<br>

-----
## 명령어 사용 시나리오 (명령어 사용처)
---
## >> [config](#config)

![image](https://user-images.githubusercontent.com/68502088/116874714-b80ca980-ac54-11eb-8974-acc926a8e241.png)

<br>

## >> [init](#init) / [clone](#clone) / [remote](#remote)

![image](https://user-images.githubusercontent.com/68502088/116874992-27829900-ac55-11eb-803c-cb42fb3f03e1.png)

<br>

## >> [add](#add) / [status](#status) / [commit](#commit)

![image](https://user-images.githubusercontent.com/68502088/116875156-69134400-ac55-11eb-834a-084638772af9.png)

<br>

## >> [branch](#branch) / [checkout](#checkout)

![image](https://user-images.githubusercontent.com/68502088/116876286-31a59700-ac57-11eb-9b6c-1292e9f5b867.png)

<br>

## >> [log](#log)

![image](https://user-images.githubusercontent.com/68502088/116876544-9e209600-ac57-11eb-9fde-9527c6ef128d.png)

<br>

## >> [reset](#reset) / [--hard](#--hard)

![image](https://user-images.githubusercontent.com/68502088/116876714-d9bb6000-ac57-11eb-9fe6-786d13fc0f67.png)

<br>

## >> [tag](#tag)

![image](https://user-images.githubusercontent.com/68502088/116876838-0ff8df80-ac58-11eb-9b04-572574ffa770.png)

<br>

## >> merge 과정 및 [merge](#merge)

![image](https://user-images.githubusercontent.com/68502088/116876934-36b71600-ac58-11eb-92a9-35247ae83e71.png)

![image](https://user-images.githubusercontent.com/68502088/116876972-459dc880-ac58-11eb-948c-3bfec21eb9d5.png)

![image](https://user-images.githubusercontent.com/68502088/116877003-53534e00-ac58-11eb-9369-f532e87987fb.png)

<br>

## >> rebase 과정 및 [rebase](#rebase)

![image](https://user-images.githubusercontent.com/68502088/116877105-74b43a00-ac58-11eb-83ab-c36c4c5d2012.png)

![image](https://user-images.githubusercontent.com/68502088/116877130-7f6ecf00-ac58-11eb-86a7-75fe0e3676c6.png)

![image](https://user-images.githubusercontent.com/68502088/116877170-8d245480-ac58-11eb-9715-183b60bb3421.png)

<br>

## >> [push](#push)

![image](https://user-images.githubusercontent.com/68502088/116877319-c066e380-ac58-11eb-8499-d9ff6ff6278a.png)

<br>

## >> [pull](#pull)

![image](https://user-images.githubusercontent.com/68502088/116877254-a9c08c80-ac58-11eb-9b97-c683c8640d74.png)

<br>

## >> 깃허브 상 커밋 목록

![image](https://user-images.githubusercontent.com/68502088/116878344-2c961700-ac5a-11eb-9e7f-029f112064b4.png)

<br>

>## 명령어 사용여부

| [add](#add) | [branch](#branch) | [checkout](#checkout) | [clone](#clone) | [commit](#commit) | [config](#config) | [init](#init) | [log](#log) | [merge](#merge) | [pull](#pull) | [push](#push) | [rebase](#rebase) | [remote](#remote) | [reset](#reset) | [--hard](#--hard) | [status](#status) | [tag](#tag) |
| --- | ------ | -------- | ----- | ------ | ------ | ---- | --- | ----- | ---- | ---- | ------ | ------ | ----- | ------ | ------ | --- |
| O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O |
