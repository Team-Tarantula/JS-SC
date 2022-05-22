## jQuery

## $('li').css('color','red');

// $('css 선택자') => jQuery 함수
// jQuery 객체 : jQuery에 의해 return된 객체
// .css('') => jQuery 함수의 인자의 성질을 바꿔주는 역할을 수행함
// .css('color','red') => 앞의 인자의 color 속성을 red로 바꿔줌
// var li = $('li') // li = jQuery 객체
// .css('','') //두번째 인자가 있으면 설정, 없으면 해당 인자를 불러옴

---

$('li').css('color','red').css('text-decoration','underline');
//chaining => 두가지 인자를 모두 적용

---

li[0] // 앞서 jQuery로 정의한 객체는 유사 배열이라 이렇게 사용할 수 있다.
li[0].css('','') //이런식의 표현은 DOM 객체이기 때문에 사용 불가능
$(li[0]).css('',''); //이런식으로 사용이 가능하다

### map()

var li = $('li');
li.map(function(index, elem){ //index값 0에서부터 element들에 대해서 모두 function을 호출함
console.log(index, elem);
$(elem).css('color','red')
})

> map은 해당하는 유사 배열의 모든 하위 객체에 function을 적용함

### jQuery API

어떤 메소드를 사용할 수 있는지 사용법이 적힌 리스트
