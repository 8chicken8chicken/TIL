# git으로 협업하기
## git hub으로 어떻게 협업하는데?
  1. git hub 로그인
  2. git hub에서 repository(repsoitories)를 생성
  3. git bash를 실행
  4. 내가 원하는 **폴더**에 git init을 입력한다.
    - .git라는 숨김 폴더가 생김
  5. 파일을 생성 및 작업한다.
  6. 저장을 하고 싶을 때는 2가지의 과정을 거친다
      - git add 파일명
      - git commit -m " "
  7. 이제 git repository에서 git url을 복사를 한다.
       - git repository에서 명령어를 참고할 수 있다.  
  8. git remote add oirgin github_url
       - git hub 원격저장소랑 연결하는 과정
       - origin은 먼저 연결할 때 국룰이긴한데 변경가능해
  9. git push와 git pull을 통해 git hub에서 협업과 관리를 한다.
        - git hub origin <branch>
        - git pull origin <branch>
        - 여기서 branch라는 개념은 여러가지 멀티버스에서 다수의 사람들이 안정적으로 개발을 할 수 있게 만들어줘 
        - 처음 설정은 main으로 보통 국룰이야
  10. 그런데 여기서 누군가 내 파일을 가져가는건 오픈소스 세상에서 좋은 영향이 많아 근데 누군가 내 파일을 인위적을 가져간다면 그건 문제이지 않을까?
        - 내 repository로 가서 collaborators에서 나랑 콜라보 하는 친구를 요청을 보내고 그 상대방도 그 요청을 받아야 이제 협업가능이야!!
  11. 여기서 이러한 과정이 전세계사람들과 소통하는데는 불편하겠지? 또 유능한 사람의 코드에는 여러명의 사람들이 commuit하고 싶어할텐데 collaborators를 활용하는 방법말고 code에 대한 제안을 할 수 있는 방법이 있지 않을까?
        - **fork**를 이용해서 주고받을 수 있어!!