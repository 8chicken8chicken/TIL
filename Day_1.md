# git
- git을 왜배워?
  - 버전관리를 위해서 배워
    - 코드 변경내용을 추적 가능하고 이전버전으로 돌아갈수 있어
  - 협업을 위해서 배워
    - 공유가 쉽고 가벼워
    - 동시에 다수의 사용자가 사용 가능해


- git이 뭐야?
  - 협업을 위한 코드 관리 도구야
    1. 코드 관리도구
    2. 코드 협업도구
    3. 코드 배포도구


- git을 이해하는데 주의사항이 있어?
  - git은 폴더 안에 .git 폴더가 생기는거야
  
- 어떤 과정으로 이루어져?? 
  - 현재 폴더(working diretory/tree), 스테이지(stage), 버전/커밋 히스토리(commit log)으로 구성돼
![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*diRLm1S5hkVoh5qeArND0Q.png)
    - working diretory에서 스테이지로 가는 과정이 **Git add**
      - git add a.txt
    - stage에서 commit log로 가는 과정이 **git commit**
      - git commit -m "add a.txt"  
    - stage에 사진기가 있다고 가정하는게 편해 현재 파일에서 내가 원하는 파일을 선택하고 그 상태를 사진에 찍어서 commit history에 올리는 개념이야 만약 내가 추가 행동을 할때마다 이 작업을 한다면 내가 원하던 시간으로 시간여행이 가능해 그리고 그게 나뿐만이 아니고 전세계에 있는 사람이 가능해
    - working directory를 엄밀히 따지자면 2가지야 tracked가 있고 untracked가 있어 그리고 tracked에서도 modify하고 unmodify가 있어
      - tracked : .git에 commit된적이 있던 친구들
      - untraked : .git에 commit된적이 거나(새로 만든 파일이거나) .git의 정보를 모두 삭제한 상태
      - modify : stage에 git add를 했어 근데 파일을 수정 할 수도 있잖아 그러면 status를 해보면 modify 중이라고 뜸
      - unmodify : commit된 친구들 중에서 modify(수정하다)가 안된 친구들!!

## git 명령어

### (1) git init

- (master) : 현재 branch 명
- .git 폴더 생성
  - git bash에서 git init을 입력하게 되면 그 디렉토리 안에 .git라는 숨김파일이 생성돼
  - 그 폴더에는 프로젝트의 모든정보가 저장되고 폴더가 없으면 git은 현재 디렉토리를 git 저장소로 인식하지 않아

### (2) git status
- 현재의 상태를 출력
### (3) git add
- stage로 올려
### (4) git commit -m "커밋 메시지"
- 사진기로 찍고 저장
### (5) git config
- git config --global user.email "이메일" : global(전역으로) user의 email을 설정
- git config --global user.email : 설정값 확인
### (6) git log 
- commut을 출력
- git log --oneline 을 하게된다면 한줄로나옴



