4.1 입력 양식 태그
form 태그로 영역 생성 후 내부에 input태그를 넣어 만든다.
form 태그 -> method 속성의 방식 action 속성 장소에서 데이터 전달
GET 방식 -> 주소에 데이터를 입력해 전달 / 데이터 크기 한정
POST 방식 -> 비밀스럽게 데이터 전달 / 데이터 용량 제한 X

(input)
text / 글자 입력 양식
button / 버튼 생성
checkbox / 체크박스 생성
file / 파일 입력 양식 생성
hidden / 해당 내용 표시X
image / 이미지 형태 생성
password / 비밀번호 입력 양식 생성
radio / 라디오 버튼 생성
reset / 초기화 버튼 생성 
submit / 제출 버튼 생성

cols/rows(textarea) / 여러 행의 글자 입력 양식 생성 cols -> 너비 rows -> 높이

(select, optgroup, option) / 선택 양식 생성 / 옵션 그룹화 / 옵션 생성
(fieldset, legend) / 입력 양식의 그룹 지정 / 입력 양식 그룹의 이름 지정

input 태그에 type 속성을 지정해 다양한 종류의 기본 입력 양식을 생성 
select 태그는 목록으로 보여주는 항목 중 하나 또는 여러개를 선택할 때 사용하는 입력 양식 요소
-> otpgroup, option 태그와 함께 사용 / 여러 항목을 선택하려면 select 태그의 multiple 속성을 사용

fieldset 태그와 legend 태그를 사용하면 입력 양식을 그룹으로 묶고 이름을 지정할 수 있음

4.2 HTML5 문서 구조화
HTML5의 대표적인 공간 분할 태그 
-> div(공간을 블록 형식으로 분할) / span(공간을 인라인 형식으로 분할)

시맨틱 웹은 컴퓨터 프로그램이 코드를 읽고 의미를 인식할 수 있는 지능형 웹
시맨틱 태그
header -> 머리말 nav -> 하이퍼링크를 모아 둔 내비게이션 aside -> 본문 흐름에 벗어나는 노트나 팁
section -> 문서의 장이나 절에 해당하는 내용 article -> 본문과 독립적인 콘텐츠 영역 footer -> 꼬리말 

5.1 선태자의 용도와 사용법
html 페이지에 css를 사용해 꾸밀 수 있음
css3에서 특정 html 태그를 선택할 때에는 선택자 사용 
ex) h1 { color:red;} h1 -> 선택자 color -> 스타일 속성 red -> 스타일 값

css3 선택자의 종류
전체 선택자(*), 태그선택자, 아이디 선택자(#아이디), 클래스 선택자(.클래스), 후손 선택자(선택자 선택자)
자손 선택자(선택자> 선택자) 

5.2 기본 선택자
공백으로 구분해 클래스를 여러 개 사용할 수 있음
-> 웹 페이지 내부에서 id 속성은 중복되지 않아야 하지만 class 속성은 중복될 수 있음 class 속성을 서로 다른 태그에 적용할 때는 태그 선택자와 클래스 선택자를 함께 사용해 태그를 더 정확하게 선택 가능

5.3 속성 선택자
선택자[속성] / 특정한 속성이 있는 태그 선택
선택자[속성= 값] /특정한 속성 내부 값이 특정 값과 같은 태그 선택

5.4 후손 선택자와 자손 선택자
ex) div -> 부모 h1, ul -> 자손(후손) li -> 후손

후손 선택자는 특정한 태그의 후손을 선택할 때 사용 
선탁자A 선택자B -> 선택자A의 후손인 선택자B 선택

자손 선택자는 특정한 태그의 자손을 선택할 때 사용
선택자A > 선택자B -> 선택자A의 자손인 선택자B 선택

5.5 반응.상태.구조 선택자
반응 선택자는 사용자 반응으로 생성되는 특정한 상태를 선택
:action -> 사용자가 마우스로 클릭한 태그
:hover -> 사용자가 마우스 커서를 올린 태그

상태 선택자는 입력 양식의 상태를 선택할 때 사용
:checked -> 체크 상태의 input 태그 선택
:focus -> 포커스를 맞춘 input 태그 선택
:enabled -> 사용 가능한 input 태그 선택 
:disabled -> 사용 불가능한 input 태그 선택 

구조 선택자는 특정한 위치에 있는 태그를 선택할 때 사용
:first-child -> 형제 관계에서 첫번째로 등장하는 태그 선택
:last-child -> 형제 관계에서 마지막으로 등장하는 태그 선택
:nth-child -> 형제 관계에서 앞에서 수열 번째로 등장하는 태그 선택
:nth-last-child -> 형제 관계에서 뒤에서 수열 번째로 등장하는 태그 선택

5.6 CSS3단위
스타일 값으로 입력할 수 있는 단위에는 키워드, 크기, 색상, URL이 있음
키워드 / W3C에서 미리 정의한 단어 / 키워드를 스타일 값으로 입력하면 키워드에 해당하는 스타일이 자동 적용

크기 / %(백분율단위), em(배수 단위), cm, mm, inch, px(픽셀 단위) 

색상 / RGB, RGBA(RGB에 알파값을 추가한 형태 / 알파값은 투명도를 나타냄(0.0 = 완전투명, 1.0 = 완전 불투명), HEX코드

URL / 이미지나 글꼴 파일을 불러올 때 사용

6.1 박스 속성
margin 속성 / 테두리와 다른 태그 사이의 테두리 바깥쪽 여백
border 속성 / 테두리
padding 속성 / 테두리와 글자 사이의 테두리 안쪽 여백, 배경색은 padding 영역까지만 적용
width 속성 / 글자 가로
height 속성 / 글자 세로

left, right, top, bottom 사용해서 방향 적용 가능 

테두리 두께 -> border-width 테두리 형태 -> border-style 테두리 색상 -> border-color 
border-radius -> 박스 테두리 둥글게

6.2 가시 속성
가시 속성은 태그가 화면에 보이는 방식을 지정 / 대표적으로 dsplay 속성
none -> 화면에 보이지 않음 / 중간에 있는 div 태그 전체가 화면에서 사라짐
block -> 블록 박스 형식으로 지정 / #box 태그의 display속성을 block 키워드로 바꿈
inline -> 인라인 박스 형식으로 지정 / margin 속성과 padding 속성을 왼쪽과 오른쪽으로만 지정 가능
inline-block -> 블록과 인라인의 중간 형태로 지정
 
6.3 배경 속성
background-image / 배경 이미지 삽입
background-size / 크기 지정
background-repeat / 반복 형태 지정
background-attachment / 부착상태 지정 /fixed 스크롤을 이동해도 배경 이미지가 고정
background-position / 위치 지정
background / 한 번에 모든 배경 속성 입력

6.4 글자 속성
font-size 속성 / 글자 크기를 지정
font-family 속성 / 글꼴 지정 / 여러개 지정 가능 
font-sytle / 글자의 스타일(기울기 등)
font-weight / 글자의 두께 / 400은 일반 글자 두께

text-align / 글자 정렬 지정
line-height / 글자 높이 지정

a 태그에 href속성을 지정하면 글자에 밑줄이 생기며 파란색으로 변경됨
-> a 태그에 적용되는 밑줄을 text-decoration 속성을 사용해 제거 / 밑줄만 제거되며 색상은 color 속성을 사용해 별도로 지정 

6.5 위치 속성
요소 위치를 설정할 때에는 절대 위치 좌표 방법과 상대 위치 좌표 방법을 사용
요소 위치 지정 형식을 설정할 때에는 position 속성 사용
절대 위치 -> absolute(절대 위치 좌표 설정), fixed(화면을 기준으로 절대 위치 좌표 설정)
상대위치 -> static(위쪽에서 아래쪽으로 순서대로 배치) 
-> 2relative 키워드를 적용하면 static 키워드로 초기 위치가 지정된 상태에서 상하좌위 이동 가능

모든 웹 브라우저의 출력 방식을 통일하려면 left속성과 top속성을 적용

z-index / 실행 결과에서 도형 순서를 변경 / 숫자가 클수록 앞에 위치

자손의 position 속성에 absolute 키워드를 적용하려면 부모에 height 속성을 입력
자손의 position 속성에 absolute 키워드를 적용하려면 부모의 positon 속성에 relation 키워드를 적용

overflow 속성은 내용이 요소 크기를 벗어나 모두 보여주기 힘들 때 어떻게 보여 줄지 지정
hidden / 영역을 벗어나는 부분 감춤  scroll / 영역을 벗어나는 부분을 스크롤로 만듦
특정 방향으로만 스크롤을 생성하고 싶을 때 overflow-x 속성과 overflow-y 속성 사용

6.6 유동 속성
float 속성은 레이아웃을 잡을 때 많이 사용 / 그림을 글자 위에 띄울 수 있음
left / 태그를 왼쪽에 붙임 right / 태그를 오른쪽에 붙임

6.7 그림자와 그레이디언트 속성
text-shadow / 글자에 그림자 부여
box-shadow / 박스에 그림자 부여
쉼표를 사용하면 그림자 속성을 여러 개 적용할 수 있음

그레이디언트 속성 / 두 가지 이상의 색상을 혼합하는 채색 기능
