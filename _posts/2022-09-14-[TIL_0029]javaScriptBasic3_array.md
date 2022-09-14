
2022.09.14.화 // [javascript] 배열
========

## 부트캠프 사전 스터디 기본 교육자료 HTML/CSS 정리   
#

## **array 기본식**  `요소 = [내용, 내용]`   
  - 하나의 변수 안에 복수의 데이터를 [ , ]를 이용해 배열하듯 입력함 
  - 문자는 "내용"으로 기입
```js
function makeArray(a, b, c, d) {
  let myArray = [a, b, c, d];
  return myArray;
}
console.log (makeArray(1, 100, "Yes!", true))
/ 출력: [1, 100, "Yes!", true]
```   

- **배열 안의 배열**   
  - *multi-dimensional array* 다차원 배열이라 함   
  - 입력 `MDA = [["first", "array"],["second","array"]]`
  - 출력 `[["first", "array"],["second","array"]]`      

- **배열 요소 접근**   
  - index를 통한 배열 내 데이터 접근 가능   
  - 배열 내 특성 요소만 별도로 변경 또한 가능
```js
let array = [1, "two", 3, 4, 5];
array[0]; // mean 1
array[3]; // mean 4
array[1] = 2; // "two" → 2
```
#

## **다차원배열 접근**   
```js   
function accessArray() {
  let myArray = [
    [1,2,3], 
    [4,5,6], 
    [7,8,9], 
    [[10,11,12], 13, 14]
  ];
  let myData = myArray[2][1];
  return myData; // 8
}
console.log (accessArray())
```
- `myArray`는 다차원배열로 [1, 2, 3], [4, 5, 6]...과 같은 배열을 포함한다.   
- `myData`는 접근문으로 [0]은 myArray의 첫번째배열. [1]은 두번째배열을 의미한다.  
- `myData[2][1]`은 myArray의 세번째배열에서 두번째 값을 의미하여 8을 의미한다.   
- `myData[3][0][1]`은 네번째배열 - 첫번째배열 - 두번째 값을 의미해 11을 의미한다.  

## **배열의 추가 제거1 .Slice**
- `slice(left, right)` 배열에서 지정한 만큼 덜어낼 때 사용
  - (1, 5)를 입력하면 둘째부터 여섯째값만 남기고 나머지를 자른다.(or 덜어낸다.)   
  - (-3)을 입력하면 배열 끝에서 세번째값까지만 남기고 자른다.
  - slice로 잘라도 원본 배열은 그대로 남으므로 항상 *새 변수를 만들어야함*  
```js
const Abox = () => {
  let Num = [0, 1, 2, 3, 4, 5, 6]; // 그대로 유지됨
  let Num1 = Num.slice(1,5) // mean [1, 2, 3, 4]
  let Num2 = Num.slice(-3) // mean [4, 5, 6]
}
```
#

## **배열의 추가 제거2 .Splice**
- `splice(a시작, b갯수, c추가1, c추가2)` a에서 b만큼 제거하고 c를 추가함   
*c는 여러번 반복 가능*  
  - `splice`는 slice와 다르게 *원본 변수에 영향을 줌!*
  - 만약 a, b만 넣고 c부터 비우면 "없음값"이 추가됨
  - 사용처) 댓글 제거 기능..버튼에 위치값을 줘서 해당 댓글만 지우게하기(?)  
```js
function array(a, b, c, d) {
  let num = [1,2,3,4,5];
  num.splice(a, b, c, d)
  return num; //
}
console.log (array(1, 3, 3, "호우")) // [1, 3, '호우', 5]
//두번째 값부터 3개 지우고 3과 "호우"를 추가
```  
#

## **배열의 추가 제거3 .Concat**
- `기존배열.concat(추가배열)` 기존배열 뒤에 추가배열을 추가하여 반환함  
  - 새 배열을 만듦. 즉, 기존 배열에 영향 없음  
  - 배열에 배열변수를 인자로 추가하면 다차원배열 추가 가능
  -

```js
function arrConcat () {
 let A = [1, 2, 3]; // A.concat(B) → [1, 2, 3, 4, 5, 6]
 let B = [4, 5, 6]; // B.concat(C) → [4, 5, 6, 7, [8, 9]]
 let C = [7, [8, 9]]; // C.concat([10, [11, 12]]) → [7, [8, 9], 10, [11, 12]]
 let DD = A.concat(A) // [1, 2, 3, 1, 2, 3]
  return base.concat(add)
}
```
#

## **배열의 추가 제거4 .Push**
- `A.push(b)` A배열 우측 끝에 b 추가
 - 기존 배열에 영향줌
```js
function A(a, b) {
  let arr = [1, 2, 3];
  arr.push(a, b)
  return arr
}
console.log (A(1)) // [1, 2, 3, 1, 없음값]
```
#

## **배열의 추가 제거5 .Pop**
- `A.pop()` A배열의 끝 요소 제거(배열도 한번에 제거됨)  
  - ()안에는 뭘 넣어도 의미가 없다. *반복될 때마다 마지막요소제거*
  - *레플릿문제가 아니라면 배열은 배열로 남아야하나 분해된 요소로 반환됨  
    배열변수를 넣어서 강제로 배열로 반환시키는 방법 고려*
```js
function arr() {
  let A = [0, [1, 2], 3];
  let Apop = A.pop();
  return "살아남은"+A+" 뽑혀진"+Apop;
}
console.log (arr()) // 살아남은 0, 1, 2 뽑혀진 3
```
#
## **배열의 추가 제거6 .Shift**
- `A.shift()` A배열의 첫 요소 제거
  - ()안에는 뭘 넣어도 의미가 없다. *반복될 때마다 첫 요소 제거*
```js
function arr() {
  let A = [0, [1, 2], 3];
  let Ashift = A.shift();
  return "살아남은"+A+" 뽑혀진"+Ashift;
}
console.log (arr()) // 살아남은 1, 2, 3 뽑혀진 0
```


#
## **메서드 간단 요약**
1. pop - 마지막 것 뽑기 (뽑은 배열은 사라짐)
2. shift - 처음 것 뽑기 (뽑은 배열은 사라짐)
3. push - 마지막에 추가
4. unshift - 처음에 추가
5. splice(위치, 개수) - 위치로부터 개수만큼 배열에서 뽑음 (뽑은 배열은 사라짐)  

외에도 정렬매서드.sort(), 배열일 때 트루를 반환하는 .isArray() 등 많이 있다.   
[예시링크](https://tutorialpost.apptilus.com/code/posts/js/js-array/)