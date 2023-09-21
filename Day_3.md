# Web
## 1. HTML
### (1) 구글 검색창에 검색한다는 것은 무슨 의미일까?
  - 검색
    - 서버에 requset하는 과정
    - URL
      - https://www.google.com/
        - - google.com은 domain이라고 부름
      - github를 검색했을 때는 어떤 결과가 나올까?
  
  - 검색 결과를 받음
    - 서버가 response하는 과정
      - https://www.google.com/search?q=github&oq=&aqs=chrome.0.35i39i362l8.3716j0j15&sourceid=chrome&ie=UTF-8
      - search?q=github
        - q = query의 약자 => 물어본다는 뜻(질의어)
      - &aqs=chrome.0.35i39i362l8.3716j0j15
        - 검색 결과를 조정하고 사용자 지정하는데 사용
      - &sourceid=chrome
        - 웹 브라우저나 소프트웨어의 원래 출처
      - &ie=UTF-8
        - 검색 결과의 인코딩 방식
      - 내가 검색한 github가 보이고 그다음 형식은 a=b형식인 것을 확인 가능!!

  - ```client 요청은 URL로 서버의 응답은 문서한장```
    - 요청을 하니까 client이고 응답을 하니까 서버이다

### (2) HTTP는 무슨 뜻일까?
  - **H**yper**T**ext **T**ransfer **P**rotocol
  - (개쩌는 문서) (교환하다) (규약)
    - 개쩌는 문서 -> 인터넷이 없던 시절에는 책을 직접 빌리지 않고 볼 수 있는게 호들갑 떨정도로 놀라운 일이었어 그래서 ```Hyper```가 붙었어
  - 참조를 통해 독자가 한문서에서 다른문서로 즉시 접근할 수 있는 Text야
    - 여기서 참조라는 것이 없다면 어떻게 해야할까?
    - 내가 원하는 단어가 있다면 그 단어를 찾기 위해 내 책을 처음부터 끝까지 scan해야한다는 의미야

### (3) HTML은 뭔데?
  - Hyper Text Markup Language
  - 서버에 있는 정보를 문서한장으로 구현보여주는데 그 문서 한장의 양식이야!!
  - 팀 버너리스

## 2. HTML 문법
### (1) intro
- html은 head, body가 있어
- head에 데이터의 데이터가 들어가
  - UTF-8 -> 현재 많이쓰고 있는 문자열 인코딩이야
  - ko -> korea 한국어라는 뜻이야
- body에 실제 문서에 표시되는 데이터가 들어가
  - \<h1>  \</h1>을 통해서 ```heading 가능```
    - markdown을 먼저 배우긴했는데 markup을 쉽게 만든게 markdown이야
    - 그래서 똑같이 \<h6>  \</h6>까지 가능
    - ```그런데 여기서 중요한건 글자 크기는 CSS의 영역이야 heading은 의미있게 구별하고 싶을 때 넣는 거야 글자 크기 때문에 사용하는게 아니야.``` 
```html
<!DOCTYPE html>
<!-- html입니다 선언 -->
<html>
<!-- Metadata : 데이터의 데이터(문서의 언어, 문서 제목, 문자 인코딩, 문서 설명, 문서 저자 정보) -->
<head>
    <meta charset="UTF-8" lang="ko"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<!-- 실제 문서에 표시되는 데이터 -->
<body>
  <h1>heading1</h1>   
</body>
</html>
```
### (2) paragraph(문단)
- \<p>  \</p>로 표시
- 문단과 문단사이에는 enter가 의미있음 but 문단 안에서는 의미가 없어
- Semantic
  - 강조하고 싶은 내용이 있을 때 쓰는거야!!
  - 어떻게 보이냐는 알빠가아니고 어떤 중요도가 있다면 역할이있다면 표시하는 경우가 있음
  - \<strong>강조1\<strong>
  - \<em>강조2\<em>
- Non Semantic
  - b랑 i가 있음
  - 이 친구들은 굵고 이텔릭은 강조한게 있어 근데 이게 지우라는건지 뭔지 몰라
  - 그니까 의미가 없어 의미를 강조한게 아니라 real로 굵게, 이텔릭으로 바꿨다는 이야기야 그래서 안써
  - 꾸미는건 CSS의 영역이니까!!
- \<pre>  \<pre>
  - enter가 안먹으니까 함수같은거 입력할 때 힘들잖아 그래서 pre tag를 이용해서 그대로 나오게 하는거야
- \<br>로 linebreak가능!! 의미론적으로 글이 이어지지만 가독성때문에 띄어쓰기하는걸 이친구로 써!!

### (3) Hyper Link
- a 태크(anchor)의 약자야 -> inline
- inline
  - \<strong>이 있다면 감싸게 되면 줄이 안 깨짐
  - 근데 \<p>같이 block 특성이 있는 친구들은 줄이 깨짐
- a누르고 tab누르면 나온다!!
- \<a href="https://google.com">
- 새탭에서 열릴 수 있고 현재화면에서 열릴수 있어
  - 새탭 -> \<a href="https://google.com" targe="_black">
  - 현재화면 -> \<a href="https://google.com">
- 목적지를 안절할때는 \<a href="#"> 라고하면 새로고침이 안일어남

### (4) List
  - \<ol>안에 \<li>
  - \<ul>안에 \<li>

### (5) media
- 요새는 image 빼고 iframe 기반으로

```html
<iframe
width="560"
height="315"
src="링크"

frameborder="0">

</iframe>
```