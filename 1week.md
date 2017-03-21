# 자바스크립트 프로그래밍 입문
## 1주차

### Variables & DataType

__단어 외우기__

__고유 명사__

Code -> Compile -> Run

Code : 인터프리팅

### Lexical grammar
#### 모든 프로그램 문법정의 전에 기본 문법?
* #### Control Characters 제어문자
* #### White Space 공백
* #### Line Terminators 엔터
* #### Comments 주석
* #### Keywords JS 언어 스펙 내장
* #### Literal 더 이상 나눌 수 없는 값의 표현 ex) 13, "abc"

[Lexical Grammer MDN 링크](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Lexical_grammar)

### Basic grammar
* ### Statements(문)
	#### 컴파일러가 힌트를 받아 처리 후 없어진다. 인터프리터에게 내리는 지시문
	* #### empty statement
		ex) ;;;;;;, i = 0 while(i++<0) ;
	* #### block statement
		단문
		`var i = 10`

		중문
		`{
			var i = 10
		}`

		문 자체는 단일한 하나의 문장입니다. 하지만 중괄호로 묶어 마치 하나의 문처럼 사용할 수 있는데 이를 중문이라고 합니다[1. 한 줄로 된 상대적인 개념은 단문입니다.]

	* ### (flow) control statement
		컴퓨터 FLOW : MEMORY -> ALU -> MEMORY -> ALU 반복
		보통 위에서 아래로 flow
		if() else() true와 false일때 flow가 달라짐

* ### Expressions(식)
	식은 값이다. ex) 1+1, 2 식은 하나의 값(2)으로 귀결
	* #### value expression
		값이 식이다. ex) 4;
	* #### operation expression
		연산자
		연산식의 수용
		연산자 많이 알기!

	* #### call expression
		함수 값 반환, 수렴

		ex) 3 + 1 + a()
* ### Varialbes(변수)
	식별자 : 값을 넣을 수 있다.

### 연산자
#### 이(2)항연산자 : A + B(A 좌항, B 우항)
#### -1 + 1 (-1은 일항) 부호바꿔주는

### assignment
#### 할당 : 변수의 값을 넣는 행위
#### ex) a = 3 ,유일하게 오른쪽에서 왼쪽으로 해석
#### ex) a=b=c=d=e=f=g=5; 5, g=5, f=5 이런식으로 오른쪽부터 해석
#### a += 1; a = a + 1;
