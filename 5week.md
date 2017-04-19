# 5주차

## 판단 연산식

삼항연산자 X \
a = 식1 ? 식2 : 식3 \
거짓이 아니라면 식의 결과는 식2
거짓이라면 식의 결과는 식3

a = if(식) 문
else 문

```js
if( a > 3 ) b = 5;
    else b = 7;
```

```js
b = a > 3 ? 5 : 7 ;
```

```js
b = a > 5 ? a > 7 ? 3 : 4 : a < 3 ? 1 : 3 ;
```

```js
b = a > 5 ?
        a > 7 ? 3 : 4
            : a < 3 ? 1 : 3;
```

```js
var a, b;

if ( a > 3 ) func(5);
    else func (7);

func( a > 3 ? 5 : 7 )
```

```js
if( a > 3 ) {
    if(b > 7) func(5,9);
    else func(5,5);
} else {
    if(b > 7) func(7,9);
    else func(7,5);
}


func( a > 3 ? 5 : 7, b > 7 ? 9 : 5 )
```

` 백틱

```js
a = a


test = test || '초기화'

test가 거짓이면 '초기화' 할당
test가 참이면  test 할당

test = test === undefined ? "초기화" : test ;

false : "", 0, false, undefined, NaN
```

## 지연연산자

flow control - statement if, switch \
flow control - operation ? : 판단 연산자 , ||(or), &&(and) \
flow control - function

```js
a  = 3 ;
b = function(k) {
    return k+2;
}
a = a + b(5);

Z 형식이 아닌 위아래 왔다갔다 flow를 따르지 않는다.
```

||(or) : A,B 하나라도 참이면 참
&&(and) : A,B 둘 다 참이면 참

## ||(or)

```js
a || b
좌에서 우로 간다.
1. a부터 식별, 판단
2. ||
3. b 식별, 판단
```

1. a가 거짓이거나 거짓이 아니거나 거짓이아니면 a를 바로 반환 식이 끝남.
1. a가 거짓일 경우 b가 거짓인지 참인지 필요없다 b를 반환
   a를 반환하거나 b를 반환한다. 둘중 하나

```js
a = "" || 3 ;   // 3
a = 3 || false  // 3
a = 5 || 3       // 5
a = 0 || 5       // 5
a = 0 || 'a'    // 'a'
a = true || "a" // true
a = 0 || "" // ""
a = 0 || false // false
```

## &&(and)

```js
a && b
```

a가 거짓일 경우 a만 반환
a가 참일때 b만 반환

***or a가 참이면 a 아니면 b***
***and a가 거짓이면 a 아니면 b***

```js
if(!test) test = "초기화" // 진짜로 바른 구문 거짓일때만 할당
```

if문이 나와야하는 이유는 나와야하니깐 어쩔수 없이
if를 줄인다.

```js
if(a..) {
        if(b..) {
            if(c..) {

            }
        }
    }
```

## conditional statment

메모리(변수)의 conditional(상태)

변수 값

```js
a = 3
a = a + 5
a = a + 7
```

상태 프로그래밍 시점
함수형 프로그래밍

***조건문이 아니고 상태 판단문***

> 커버리지 : 쓸모있게 코드를 썼냐 판단 7/8 1/8이 필요 없다 p.108

```js
var msg = "수강해야 하는 전공 학점: ",
    score;
/*
    switch (level) {
    case 1: msg+="12학점"; break;
    case 2: msg+="18학점"; break;
    case 3: msg+="10학점"; break;
    case 4: msg+="18학점"; break;
}
*/

/*
switch (level) {
    case 1: score="12"; break;
    case 2: score="18"; break;
    case 3: score="10"; break;
    case 4: score="18"; break;
}
*/
switch (level) {
    case 1: score=12; break;
    case 2: score=18; break;
    case 3: score=10; break;
    case 4: score=18; break;
}

/*
switch (level) {
    case 1: score=12; break;
    case 4: case 2: score=18; break;
    case 3: score=10; break;
}
*/
msg += score + "학점";
console.log(msg);
```

## 반복문

* 반복조건 loop condition
* 구간반복
* 반복본체 loop body

### while

```js
    a = 1;
    while(a < 10) {
        console.log(a);
        a=a+1;
    }
    // 1, 2, 3, 4;
```

```js
    a = 1, b = 0
    while(a < 5) {
        b += a;
        a += 1;
    }

    a = 1, b = 1;
    a = 2, b = 3;
    a = 3, b = 6;
    a = 4, b = 10;
    a = 5,
```

a = 밑값
while( a < 최종밗 + 1 )

```js
    min = 4;
    max = 10;
    a = min, sum = 0;
    while ( a <= max ) {
        sum += a;
        a + = 1;
    }
```

> 사람의 두뇌는 상태 추적은 적합하지 않고 상태 변화 추적은 인식이 편하다.