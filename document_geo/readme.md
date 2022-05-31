## 문서의 기하학적ㅇ니 특성

clientWidth // 테두리를 제외한 객체의 너비
clientHeight // 테두리를 제외한 객체의 높이
getBoundClientRect() //객체의 위치, 크기 정보
offsetParent //측정의 기준이 되는 객체를 알려줌 ex document 등
//부모 중 CSS position 값이 static인 td, table등인 경우 기준이 됨

======

## viewport

브라우저에서 사용자에게 보여지는 문서의 크기

- pageYOffset
  스크롤을 몇 px만큼 움직였는지 보여줌

- getBoundingClientRect
  viewport 안에서 객체의 위치를 표시함 :: viewport 좌표
  만약 document 좌표를 알고 싶다면 pageYOffset 값과 viewport좌표 top값을 합치면 document 좌표값

## scroll

window.scrollTo(0,1000); //문서의 window를 기준으로 스크롤 y값을 1000px만큼 이동

## 스크린의 크기

window.innerWidth
window.innerHeight
열려있는 window의 크기
screen.width
screen.height
사용자의 화면 크기 // 웹페이지의 폭을 의사 결정할 때 참고함
