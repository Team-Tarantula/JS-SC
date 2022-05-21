## location

http:(protocol)//opentutorials.org(host):80(post)/module/1(pathname)?id=1(search)#hash(hash)

> > console.log(여기에 입력하는 경우 알 수 있는 정보)

console.log(location.href)

> > 'http://~'

location.href = 'http//egoing.net'
location = 'http//egoing.net'

> > 해당하는 위치로 자동으로 이동

location.href = location.href
location.reload

> > 현재 문서의 url을 reload

## Navigator

### cross browsing

개발자 입장에서는 브라우저의 특성에 따라 서로 다른 코딩을 해야하는 경우가 생기는데, 이러한 문제로 인해 생기는 이슈들을 cross browsing issue라고 함

console.dir(navigator);

navigator가 가진 property를 다 보여줌

### appName

Netscape : chrome, opera 등 넷스케이프의 유지를 이은 브라우저들이 이 이름을 가짐

### appVersion

브라우저에 대한 자세한 정보들이 나옴

### userAgent

웹브라우저가 웹서버에 정보를 요청할 때 웹브라우저에 대한 정보도 같이 전달하게 되는데 그 정보가 출력됨

### platform

웹브라우저가 동작하고 있는 운영체제 출력

## 기능테스트

브라우저가 어떠한 기능을 가지고 있는지 여부를 확인
object.keys => 최신자바스크립트 규약이기 때문에 오래된 자바스크립트와 호환되지 않는다
=>
if(!Object.keys) { // Object가 keys를 가지고 있지 않다면 실행한다
Object.keys = (function (){
object.keys가 있는 것처럼 동작할 수 있도록 기능을 추가해주는 함수
})
}

## 창 제어, 창과 창 사이의 커뮤니케이션

window => 브라우저에서 가장 큰 개체

window.open()

## 팝업제어

브라우저에서 사용자의 인터렉션 없이 뜨는 새 창에 대해서 차단하는 기능
=> 보안적인 접근//사용자가 명시적으로 버튼을 클릭하는 것과 같은 행위를 할 때는 팝업차단이 기능하지 않음
