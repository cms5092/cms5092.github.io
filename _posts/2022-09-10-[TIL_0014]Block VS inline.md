
2022.09.10.토 // [Start-kit] 14. [CSS] block vs inline
========

## 부트캠프 사전 스터디 기본 교육자료 HTML/CSS 정리   


```js
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>repl.it</title>
    <style>
      .inlineP {
        display: inline-block;
      }
      p {
        background-color: yellow;
      }  
      span {
        background-color: blue;
        color: white;
      }
      .floatLeft {
        float: left;
      }
      .floatRight {
        float: right;
      }
      .blockSpan {
        display: block;
      }

    </style>
</head>
<body>
  none태그
  <p class="inlineP">p태그+class="inlineP"</p>
  <p>p태그만 사용(배경 노랑)</p>
  <p class="floatLeft">p태그+class="floatLeft" 좌측정렬</p>
  <p class="floatRight">p태그+class="floatRight" 우측정렬</p><br/><br/>

  <span>span태그(즉 inline요소)</span>
  <span class="blockSpan">span태그+class="blockSpan"</span>

</body>
</html>

```

### ◆Block   
* **정의: 옆(좌우측)에 다른 요소를 붙일 수 없음**   
예: `<header>`, `<footer>`, `<p>`, `<li>`, `<table>`, `<div>`, `<h1>` 등

**특징** 태그를 끊고 새로 시작할 때마다 *새롭게 한 줄씩 형성*되고 가로길이는 최대가 됨   


#
### ◆inline
* **정의: 옆(좌우측)에 다른 요소를 붙일 수 있음**   
예: `<span>`, `<a>`, `<img>` 등   

**특징** 태그를 끊고 새로 시작해도 이전 *태그 내용 옆에 형성*되고 가로길이는 내용만큼 형성 됨   

#
### ◆추가 알 것   
*block든 inline이든 css로 스타일을 바꿀 수 있음*   
* **To inline 예시**   
`.ToInlien1{display: inline-block;}` 그냥 붙여쓰기   
`.ToInline2{float: left;}` 좌로 정렬   
`.ToInline3{float: right;}` 우로 정렬   

* **To block 예시**     
`.ToBlock{display: blocd;}` p태그처럼 한 줄 씩 작성욈    

* **내용 숨기기**   
`.hide{display: none;}` 내용만 화면에서 보이지 않게 됨      
검색엔진의 연관검색어 자동출력과 같은 기능에 사용

