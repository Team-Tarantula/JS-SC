## event 등록-inline

태그(input등)의 정해진 속성으로 event handler를 입력
<input type="button" onclick="alert('Hello World');" value="button">

- this
  이벤트가 속한 객체를 의미
  this.value

## 프로퍼티 리스너

js로 객체의 속성을 불러와서 이벤트 핸들러를 지정하는 방식
var t = document.getElementById('target');
t.onclick = function(evnet){ //event:어떤 이벤트인지 ex mouse
alert('Hello world, ' + event.target.value); //event.target: 이벤트가 어디에서 시행되었는지
// ex input
}

## addEventListener()

이벤트를 등록하는 가장 권장되는 방식 //복수의 event handler를 연결할 수 있다
var t = document.getElementById('target');
t.addEventListenser('click', function(event){ //click 이벤트가 발생했을 때 함수 실행
alert('Hello World, ' + event.target.value);
});

===

## 이벤트 전파

- html -> body -> fieldset -> input 순으로 event handling이 발생 : capturing
  //부모에서 자식 방향으로 이벤트 진행 => 매우 드물게 사용됨
- 반대 순서는 bubbling
  => 웹브라우저는 두 기능 모두 지원함
  이벤트가 부모 자식 간에 중첩 설치되어 있는 경우 capturing
- addEventListener('click', handler, false);
  // 세번째 인자가 true면 capturing으로 동작
  // 세번째 인자가 false면 bubbling으로 동작
- event.stopPropagation();
  event 전파를 정지함

## 기본동작의 취소

document.querySelector('a').onclick = function(event){
if(document.getElementById('prevent').checked)
return false;
}

## 폼

사용자가 입력한 정보를 서버로 전달할 때 사용함

- submit
  전송 명령
- value
  사용자가 입력한 정보
- 미입력시 제출 방지
<form id="target" action="result.html">
  <input id="name" type="name">
  <input type="submit">
</form>
<script>
  var t = document.getElementById('target');
  t.addEventListener('submit', function(event){ //validation 함수
    if(document.getElementById('name').value.length === 0){ //입력 값의 길이가 0일때 
      alert('Name field 값이 누락되었습니다');
      event.preventDefault(); //submit을 정지
    }
  })
</script>

- focus
  input 창에 커서가 있는 경우
- blur
  focus가 제거됨

## 문서 로딩

- script 태그를 head에 넣고 싶을 때 : onload
<script>
  window.onload = function(){
    실행하고 싶은 함수
  } //모든 문서를 다 읽고 난 다음 script 읽음 ; 모든 리소스를 다 다운 받고 실행 => 느려질 수도 있음
</script>
- DOMContentLoaded
문서의 DOM이 다 읽어진 후에 실행 => 리소스들은 이후에 다운 받기 때문에 느려지지 않음
라이브러리를 쓰면 알아서 라이브러리가 다 해줌
<script>
  window.addEventListener('DOMContentLoaded', function(){
    실행하고 싶은 함수
  })
</script>

## 마우스
