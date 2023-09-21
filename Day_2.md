# git으로 협업하기
## git hub
- 어떻게 협업하는데?
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