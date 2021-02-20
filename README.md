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