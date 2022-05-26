## node

node 객체는 모든 하위 객체들의 뿌리와 같은 역할을 한다

## 관계

> 각각의 노드가 다른 노드와 연결된 정보를 보여주는 API
> Node.childNodes // 하위 노드 탐색 //공백, 줄바꿈 등도 노드에 포함됨
> Node.firstChild // 첫번째 자식 객체를 불러왔을 때 줄바꿈도 포함되기 때문에 #text로 결과가 도출될 수 있음
> Node.lastChild
> Node.nextSibling
> Node.previousSibling
> Node.parentNode
> Node.childNodes // 부모객체가 가진 자식 객체를 모두 담은(text 포힘) 유사배열
> Node.contains()
> Node.hasChildNodes()

## 노드 종류

> node 객체는 모든 구성요소를 대표하는 것이기 때문에 각각의 구성요소가 어떤 카테고리에 속하는 것인지를 알려주는 식별자를 제공한다
> Node.nodeType
> // console.log(name, Node[name]); 으로 노드의 모든 이름과 해당 번호를 가져올 수 있다.
> // nodeType 함수로 해당 객체의 노드 번호를 받아올 수 있다.
> Node.nodeName
> // 태그의 이름 등 조금 더 디테일한 정보를 조회

## 값

> Node 객체의 값을 제공하는 API
> Node.nodeValue
> Node.textContent

## 자식관리

// Node 객체의 자식을 추가하는 방법에 대한 API

> Node.appendChild() //자식으로 추가
> Node.removeChild() //자식 삭제
