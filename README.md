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
 1. '<input type="submit" />'
 2. '<button></button>'


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


navigation
 - 보통 ul로 나눠지고 그 안에 많은 li들로 구성됨. 그리고 li는 a(anchor)를 가진다.
 - 구글도 navigation을 찾아서 ul의 li안에 있는 link를 가져오게끔 설정되어 있음


CSS Box Padding의 default 원리
 - CSS에서 200px 크기의 box에 50px의 padding을 원할 경우, 총 크기 200px, (width 150, padding 50 실제 내용 150)의 box를 생각해서 padding : 50px, width : 200px 로 입력한다.
 - 그러나, 이렇게 하면 CSS에서는 padding을 50px 주고, 200px의 box width는 유지하려 하므로, 총 크기 250px (width 200, padding 50 실제 내용 200)의 box를 가지게 된다.
 - box-sizing : border-box 를 입력할 경우, padding을 입력해도 box사이즈를 신경쓰지 않는다는 의미이다. - 중요!!
 - 따라서, 처음에 원했던 50 padding, 150 box 를 가지게 된다.


z-index
 - div가 있는 위치가 맨 뒤(default 값 : 0)에서부터 몇 번째인지를 나타낸다.
 - layer와 같은 것이며, 절대적인 위치(absolute poosition)나 고정된 위치(fixed position)에 대해서 설정 할 수 있다.


100vh : 화면높이의 100%
100vw : 화면 너비의 100%


Splash Screen
 - CSS의 keyframes 애니메이션으로 splash 애니메이션을 줄 수는 있지만, 완벽하게 없어진 상태를 만들 수 없다. 따라서 JavaScript가 필요하다.
 - 애니메이션의 마지막 값을 기억하고 싶다면 forwards라는 단어를 사용 -> 마지막 keyframes를 기억한다.
 - animation-delay로 애니메이션 지연 가능
 - visibility: hidden; -> 마우스에 걸리지 않게 빠져버리게 만드는 것

will-change
 - 애니메이션이 좀 더 부드럽게 동작할 수 있게 만듬 -> 브라우저에게 어떤 것이 변할 건지 예고하는 것
 - 그래픽 카드를 이용해서 애니메이션을 가속화한다.


focus-within : element 내부에 focus 된 element가 있는지 보는 


<GitHub Desktop 이용>
Branches on Git
 - git에서 branch는 코드들의 평행세계
 - 어떤 commit에서든 분화할 수 있음
 - branch끼리 합치는 것 -> merge


Publishing on github Pages
 - 특별한 이름이 붙여진 특별한 branch를 가지고 있으면 Github에서 공짜로 Static 호스팅을 할 수 있도록 해줌
 - 즉, 누구나 웹사이트를 무료로 업로드할 수 있고, Github에서 공짜 URL제공해줌
 - static website : HTML, CSS, JavaScript로만 이루어진 웹사이트. 즉, fornt-end만 가능하고 back-end는 다룰 수 없다.
 - 사용하기 위한 규칙
    1. 'gh-pages' 라는 branch를 생성 (branch이름이 필수적으로 'gh-pages'라고 해야한다.)
    2.  저장소가  Public 상태여야한다.
    3.  자신의 저장소로 이동 후 environments에 github-pages로 이동
    4.  view deplyment 클릭 -> 생성된 URL 로 이동
    5.  URL : (유저명).github.io/(저장소 이름)


Updating Gitjub Pages
 - Github 페이지 업데이트 하기
   1. master branch에서 수정 후 commit  -> push 
   2. gh-pages branch로 이동 -> Branch - Update from master - push
   3. Deployments로 이동 후 새로운 view deplyment 클릭