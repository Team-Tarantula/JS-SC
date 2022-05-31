# Node 객체
DOM에서 시조와 같은 역할

--
## 관계
엘리먼트는 서로 부모, 자식, 혹은 형제자매 관계로 연결되어 있다. 각각의 Node가 다른 Node와 연결된 정보를 보여주는 API를 통해서 문서를 프로그래밍적으로 탐색할 수 있다.

- Node.childNodes
- Node.firstChild
- Node.lastChild
- Node.nextSibling
- Node.previousSibling
- Node.contains()
- Node.hasChildNodes()

--
## 노드의 종류
Node 객체는 모든 구성요소를 대표하는 객체이기 때문에 각각의 구성요소가 어떤 카테고리에 속하는 것인지를 알려주는 식별자를 제공한다.

- Node.nodeType
- Node.nodeName

--
## 값
Node 객체의 값을 제공하는 API

- Node.nodeValue
- Node.textContent

--
## 자식관리
Node 객체의 자식을 추가하는 방법에 대한 API

- Node.appendChild()
- Node.removeChild()
