## Ajax

Asynchronous JavaScript and XML
비동기적 통신을 가능하게 함 // 새로고침 없이 데이터 통신을 가능하게 함

### XMLHttpRequest

- time.php : 시간을 출력
<?php
$d1 = new DateTime;
$d1 -> setTimezome(new DateTimezone("asia/seoul"));
echo $d1->format('H:i:s');
?>
