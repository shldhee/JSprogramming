# 6주차 마지막

## 배열(Array)

3.1 Array (링크드 리스트) length 계산을 자동으로 하는 오브젝트

ES2015에서 생김 ArrayBuffer (배열)

오브젝트
자바스크립트의 object - 고유명사
hashmap - 일반명사

hash : 어떤 문자를 넘기면 숫자로 바꿨다고 보면 된다. "a" -> 0076
hash("ab") = 17
hash("abc") = 18
hash 함수 동일한 문자열을 넘기면 고유한 숫자가 언제나 일정하게 반환됨

map : 어떤 자료를 집어넣을때 key와 value 쌍
"a", "바보"
"b", "천재"
K, V
Key를 알면 Value를 불러온다.

무엇을 자바스크립트의 object

숫자
문자열
불린
null
undefined

Object가 아니면 위에꺼
(function)포함

해시맵
1. 문자열 키에 대응하는 값
2. 자유롭게 추가 삭제 가능

``` js
var a = { };
var b = { "a" : "바보",
          "b" : "천재" };

b["a"] == "바보"; // 추천 언제나 가능
b.a == "바보"; // 예외경우 있음
```

리터럴 값을 표현하는 더 이상 쪼갤수 없는 표현

``` js
var c = { "0" : 3, "1" : 4, "2" : 5 };
c["0"] == 3; // c[0]
c["1"] == 4; // c[1]
```

자바스크립트는 대괄호[] 안에 무조건 문자열로 바꾼다.

해시맵의 키중 숫자처럼 생킨 키중에 가장 큰 값 + 1을 length라고 한다.
c[100] = 7 ;
length는 101

JS의 Array는 타 언어의 Array가 아니다.
타 언어
* 고정메모리 확보
* 공간 한꺼번에 확보
* 위치

JS
* 해시맵
* object

성긴 배열

## while

while(식) 문;
식이 참이면 문이 실행

``` js
var i = 0; // 초기화
var arr = [1, 2, 3, 4];
while( i< arr.length // 판별식) {
    console.log("a");
    i += 1; // 증감식
}
```

초기화
판별식
증감식

## for

for ( 식 ; 식 ; 식) 문;
for ( 초기화식 또는 var 문 ; 판별식 ; 증감식) 문;

``` js
var arr = [1, 2, 3, 4]
for (var i = 0; i < arr.length; i += 1 ) {
    console.log("a");
}
```
