# Kokoa Clone 2021 from Nomadcoder

HTML & CSS are so much fun!


.DS_Store
 - 맥os나 윈도우에서 만든 보이지 않는 임시파일이다.


.gitignore
 - 무시하고 싶은 파일 이름을 기록하는 파일
 - 파일 이름을 쓰면 그 이름의 파일이 commit하는 것을 막아줌
 - 폴더의 경우 /(폴더 이름)


index.html로 파일명을 짖는 이유
 - 대부분의 웹 서버가 default로 index.html을 찾아보도록 설정되어있다.


BEM(Block Element Modifier)
 - 많은 사람들이 적용하는 규칙
 - 좀 더 쉽게 읽히는 css를 가지는 것
 - (block)__(value) / (block)--(modifier) 방식으로 클래스 이름을 지어줌


아이콘을 추가하는 방법
1. 직접 아이콘을 구하는 방법
2. 직접 이미지를 만들고 추출하거나 svg 파일을 이용
    - 픽셀이 없는 이미지 파일형식, 수학으로만 구성된 형식 / 좌표로 되어있어서 원하는만큼 늘릴 수 있다.
3. Heroicons에서 구하기 - 검색 - 클릭 - 붙여넣기
4. FontAwesome (더 좋음!!) 
 - <script src="https://kit.fontawesome.com/6478f529f2.js" crossorigin="anonymous"></script> (무료버젼 kit)
 - script는 항상 마지막에 있어야한다. body 태그를 닫기 직전에

버튼을 추가하는 방법
 1. <input type="submit" />
 2. <button></button>

dafult css를 초기화하는 방법
 - 리셋 css : 대부분의 태그에 margin:0, padding:0. boder:0 등을 가진 css 파일
 - @import "css파일명" 을 통해 추가하여 다른 css로 불러올 수 있다.

:not()
 - css에서 뭔가가 적용되는 걸 원하지 않을 때 사용

cursor:
 - 마우스 포인터 변환을 위해 사용

inherit
 - 부모 tag로부터 상속 받는 것

form에서 아주아주 중요한 2가지 속성(attribute)
 1. action : 어떤 페이지로 data를 보낼건지 지정 가능
 2. method : post와 get 두가지 사용 가능
    ㄴpost : 백엔드 서버에 정보를 전송하는방식
    ㄴget : 보안에 취약하다. URL에 포함되어도 상관없는 정보들을 get방식으로 보내야된다.