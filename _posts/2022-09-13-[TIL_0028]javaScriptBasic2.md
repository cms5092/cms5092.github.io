
2022.09.13.화 // [javascript] basic2
========

## 부트캠프 사전 스터디 기본 교육자료 HTML/CSS 정리   
#

## ◆ 변수&메서드 선언 기본 정리    
* `console.log (functionA.length)`  메서드와 변수를 연계 할 수 있음     
*콘솔에 출력하라(펑션A의 길이)*     
#

* 복합적으로 변수와 메서드를 활용   
```js
let A = 'abc';
let B = 'defg';
let L1 = A.length;
let L2 = B.length;
console.log (L1+L2 / 2) // console: 3.5
```     
    * 변수 안에 다른 변수와 메서드를 넣을 수 있음   
    * 그 메서드를 다른 메서드에서 간단한 기호를 활용한 수식으로 계산 할 수 있음     
#

## ◆ 함수 선언 기본 정리     
* `function(매개 변수) 함수명 {메서드, 변수...}`    
  * 매개 변수에 대한 설명은 나중에.     
  * 함수명 뒤 {}에 변수나 메서드를 함수라고 하는 *큰 상자에 넣는 개념*      
```js
let A = 8;
let B = 2;
let C = 'i love wecode' // 13

function ex () {
  console.log(A+B+C.length)
}
ex() // 8+2+13 = 23 콘솔 출력
```     
#

## ◆ return 메서드와 함수 선언 기본 활용
  - `return`은 오직 '반환'기능만 함(출력 기능 없음)     
  - 함수 안에 복수의 변수선언, 메서드 입력, 변수 조합 등 복합적 활용 가능   
```js
function Seven() {
  let seven = '안녕히 계세요'  // 변수 '생성'
  let conso = "콘솔"  
  return conso+seven.length // 변수+변수.메서드 '반환'
}
Seven() // ←얘는 있으나 없으나 아래 메서드들은 작동함 and 반환과 화면 출력은 다름
console.log (Seven())
```     
#

## ◆ 함수의 매개변수(parameter) & 인자(argument)
  - 함수 선언할 때 매개변수(parameter)를 함께 선언해 앞으로 해당 함수인자(argument)를 입력하면 매개변수에 대입돼 실행됨     
```js
  function A(left, right) {
  console.log (left) // 인자 'left'출력
  console.log (right+left) // 인자 'right'+'left'출력
  return left.length // 인자 'a'의 길이 !반환!
}
A ('코드','김')

function B(c, d) {
  let sunn = c + d; // 인자 c, d를 합쳐 변수선언
  console.log (sunn); // 변수 출력
  return sunn; // 변수 !반환!
}
B(10, 5)
```     

## ◆ 조건문(if, else, else if) 
  - `if(조건){참의 경우}` 조건문을 실행하고 불린 값으로 변환!   
  - `if(조건){참의경우}else if(조건){다른경우}`
  - `if(조건){참의경우}else{거짓인 경우}`   
```js
function Qq (a) {
  let awe = a;
  if (awe > 2022) {
    return "down"
  } else if(awe < 2022) {
    return "up"
  } else {
    return "정답!"+awe
  }
}
console.log (Qq(20220))
```
  - **해석**
    - 2022sms 인자(argument)로 Qq의 매개변수(parameter)에 대입된다. awe = 20220  
    - if문의 조건인 `(awe > 2022)`에 따라 awe(20220)은 참이 아니므로 다음 조건인 `else if`로 넘어간다.  
    *만약 뒤에 else if 나 else의 경우가 없으면 그냥 거짓만 출력*    
    - `else if(){}`의 `(awe > 2022)`에서 20220은 **참**이므로 조건문 뒤에 붙는 중괄호 {}에 따라 출력된다.
#

## ◆ 참고할만한 연산자
- **나머지 연산자 %**
  - `a%b` 나머지를 구하는 연산자. a를 b로 나누고 남은 값 출력
  - `console.log(3 % 5, 4 % 2)` → 3 0 출력   
  - *짝수를 구할 떄 (n&2) 등 응용하여 사용 가능   

- **and && 와 or ||**
  - and 기본 예시 `if(조건A && 조건B){실행}` 동시 만족 필요   
  - or 기본 예시 `if(조건A || 조건B){실행}` 선택 만족 필요    

- **상위개념**
```js
function A (a) {
 let score = a;
  if (a > 100 || a < 0) {return "error";} 
  else if(a >= 90){return "tear A";} 
  else if(a >= 80){return "tear B";}
}
console.log (A(90)) // tear A 출력
```
  - 위 코드는 90점 이상일 때 tear A와 B동시에 만족하지만 **A가 상위 단**에 있어 **tear A**가 출력된다.    
  - 만약 반대로 **tear B**가 상위 단에 있다면, 90점 이상 또한 tear B가 출력된다.    