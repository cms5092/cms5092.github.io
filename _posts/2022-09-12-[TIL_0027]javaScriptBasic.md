
2022.09.12.월 // [javascript] 
========

## 부트캠프 사전 스터디 기본 교육자료 javascript 정리   


```js

```

### ◆ JS 주석
* // 주석 한 줄입력     
* / 주석 여러 줄 입력 / 

### ◆ 명령어
* `consile.log(내용)` 괄호 안의 메세지를 '콘솔창'에 출력    
*단 문자는 ""사이에 입력_숫자는 바로 입력*      

### ◆ 변수 선언 
[변수개념참고(고급)](https://gist.github.com/LeoHeo/7c2a2a6dbcf80becaaa1e61e90091e5d)
* `const` constant의 준말_상수_값이 변할 수 없음 (변수 재선언, 재할당 불가)   
* `let` 변수 재선언, 재할당 가능
* `var` 단순 변수 선언_어떤 규칙도 없어 위 두개보다 안좋다는 평 
* `아무변수선언문 a` 변수선언 후 아무것도 대입하지 않으면 'undefined', 즉 정의되지 않음 상태    
* 정의하지 않은 상태에서 출력하면 'undefined' 또는 'NaN'출력됨(NaN: Not A Number)   

### ◆ 대입연산자    
* 오른쪽 항에 있는 **값**을 왼쪽 **변수**에 대입
* `let myVar =5;` 값'5'를 'myVar'이라는 변수에 대입     
* `let a = "hello "; let b = "world"; console.log(a+b);`의 출력값은 hello world다   
* `let b = "world"; console.log("hello "+b)`의 출력값도 hello world다   

### ◆ null & undefined      
* `undefined` 선언은 됐지만 value가 없음    
* `unll` 빈 값(blank)자체가 value   


### ◆ 같이 나온 연산자
* `==` 데이터의 모양새만 같으면 **참**
* `===` 데이터의 타입까지 같아야 **참**
```js
a = 1; A = "1";
b = 2;
console.log (a == b) // false
console.log (a == A) // true
console.log (a === A) // false
```


### ◆ 같이나온개념  
* `typeof` 변수, 객체, 함수, 표현식의 **데이터타입**을 반환해줌     
```js
let a = "아니"; // string
let b = 1; // number
let c = true; // boolean

console.log(typeof 데이터)
```