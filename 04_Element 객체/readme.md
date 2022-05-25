# Element 객체
엘리먼트를 추상화한 객체.<br>
Node 객체 > Element 객체 > HTML Element > HTMLHeadElement, HTMLLIElement

--
## 식별자
문서내에서 특정한 엘리먼트를 식별하기 위한 용도로 사용되는 API
- Element.classList
- Element.className
- Element.id
- Element.tagName

--
## 조회
엘리먼트의 하위 엘리먼트를 조회하는 API
- Element.getElementsByClassName
- Element.getElementsByTagName
- Element.querySelector
- Element.querySelectorAll

--
## 속성
엘리먼트의 속성을 알아내고 변경하는 API
- Element.getAttribute(name)
- Element.setAttribute(name, value)
- Element.hasAttribute(name)
- Element.removeAttribute(name)
