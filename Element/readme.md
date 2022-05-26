## Element 객체

var t = document.getElementById('active');

> t가 나타내는 객체는 HTMLLIElement
> HTMLElement는 style이라는 property를 가짐
> Element는 HTMLElement의 부모객체 => 이 문서 속의 모든 객체의 속성을 정의함
> DOM은 HTML만을 규격화하고 있지 않음 // HTML, XML, SVG, XUL 등 MarkUp 언어들을 정의

### 식별자API

HTML에서는 id와 class
Element.tagName
Element > HTMLElement > HTMLLIElemnt

> Element.tagName => element의 태그 이름을 가져옴 (읽기 전용, ex) li, ul, ...)
> Element.id => element의 id이름을 가져옴 // tag이름.id = '변경할 태그 이름'; => 태그 이름을 변경함
> var active = dociment.getElementById('active');
> console.log(active.id);
> Element.className => element의 class이름을 가져오거나 변경함
> Element.className = 'current readed'; //여러 이름의 class 이름을 넣을 수 있음

> Element.classList
> classList 객체 : DOMTokenList => 한 객체에 존재하는 여러 클래스 이름의 리스트(유사배열)
> class="marked current readed" 일때
> element.classList[1] = "current"
> element.classList.add('important'); // class 이름에 important를 추가
> element.classList.toggle('important'); // 작동할때 마다 껐다 켜졌다하며 class 이름을 추가

### 조회 API

document.getElementsBy\*(''); // 문서 전체에서 어떠한 element를 조회할 때 사용

### 속성 API

attribute : href, value 등의 속성
Element.getAttribute(name)
Element.setAttribute(name, value)
Element.hasAttribute(name);
Element.removeAttribute(name);

### attribute vs property

> attribute 방식
> target.setAttribute('class', 'important');
> => 속성의 이름과 변경사항을 나열
> property 방식
> target.className = 'important;
> => 속성의 이름을 변경하는 '함수'와 변경사항을 정의
