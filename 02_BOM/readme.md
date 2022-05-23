# BOM (Browser Object Model)
웹브라우저의 창이나 프래임을 추상화해서 프로그래밍적으로 제어할 수 있도록 제공하는 수단

BOM은 전역객체인 Window의 프로퍼티(property)와 메소드(method)들을 통해서 제어할 수 있다.
<br><br>

--
## 전역객체 Window
Window 객체는 모든 객체가 소속된 객체이고, 전역객체이면서, 창이나 프레임을 의미한다. 

Window 객체는 식별자 window를 통해서 얻을 수 있다. 또한 생략 가능하다.

객체를 만든다는 것은 결국 window 객체의 프로퍼티를 만드는 것과 같다.

--
## 사용자와 커뮤니케이션 하기
1. alert - 경고창
2. confirm - 확인(true) / 취소(false)
3. prompt - 사용자로부터 입력 받기

--
## Location 객체
문서의 주소와 관련된 객체로 Window 객체의 프로퍼티다.<br>
이 객체를 이용해서 윈도우의 문서 URL을 변경할 수 있고, 문서의 위치와 관련해서 다양한 정보를 얻을 수 있다.

#### 현재 윈도우 URL 알아내기
-> console.log(location.toString(), location.href);

#### URL Parsing
-> console.log(location.protocol, location.host, location.port, location.pathname, location.search, location.hash);

#### URL 변경하기
-> location.href = '변경할 URL'<br>
-> location = '변경할 URL'<br>
리로드 : location.reload() or location.href = location.href

--
## Navigator 객체
브라우저의 정보를 제공하는 객체. 주로 호환성 문제 등을 위해 사용<br>

※ 크로스 브라우징 (cross browsing) - 브라우저마다 다르게 동작하는 문제

#### appName
웹 브라우저의 이름.<br>
IE는 Microsoft Internet Explorer, 파이어폭스, 크롬등은 Nescape로 표시한다.

#### appVersion
브라우저의 버전.

#### userAgent
브라우저가 서버측으로 전송하는 USER-AGENT HTTP 헤더의 내용이다. appVersion과 비슷하다.

#### platform
브라우저가 동작하고 있는 운영체제에 대한 정보.

※ 기능 테스트 - 해당 기능이 브라우저에 있는지 없는지 검사

---
## 창 제어
window.open() : 새 창 생성
- _self : 자기 자신 창
- _blank : 빈 새 창
- 창에 이름을 붙일 수 있다.
