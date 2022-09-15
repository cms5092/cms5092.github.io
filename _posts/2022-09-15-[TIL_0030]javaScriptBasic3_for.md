
2022.09.15.수 // [javascript] 반복문
========

## 부트캠프 사전 스터디 기본 교육자료 javascript 정리   
#

## **반복문 for**
- `for(초기화문;조건문;증감식){내용}` /ex/ `for(i=0; i=5; i++){return i}`
  - **초기화문** `let i=0;` index를 의미하는 i를 변수선언자로 많이 선언  
  - **조건문** i의 범위를 설정. 증감식에 따라 i가 변하고 조건이 true일 때 반복  
  - **증감식** `i++`,`i+=1` = i가 참일 때 내용을 반복하고 증감식을 진행   
  - *`i+n;`형태의 증감식 불가!!*  
```js
  for(let i=1; i<10; i++) {
  let gugu = 2*i
  console.log ("2 x "+i+" = "+gugu)
  } // 2 x 1 = 2 ... 2 x 9 = 19 출력
```
**예시2**  
```js
function forA() {
  let myArray = [];
  for (let i=0; i<5; i++){
    myArray.push(i);
  }
  return myArray;
}
console.log (forA()) // [0, 1, 2, 3, 4] 출력
```   
**예시3**   
```js
function getA(str) {
  let strA = [];
  let out = str;
  for (let i=0; i<out.length; i++){
  strA.push(out[i]) 
  }
  return strA;
}
console.log (getA("우효오옷")) // strA = ["우","효","오","옷"]
```    