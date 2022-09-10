
2022.09.10.토 // [Start-kit] 16. [CSS] 자료구조&알고리즘
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
      .Aa {
        list-style: none;
        border-left: 3px solid black;
        padding: 0 0 0 10px;
      }
      li:nth-child(odd) {
  background: red;
  color: azure;
  }
    </style>
</head>
<body>
    <h3>목록 태그</h3>
<ol>
  <li>List</li>
  <li>Set</li>
  <li>HashMap (Dictionary)</li>
</ol>
<ul>
  <li>Queue</li>
  <li>Stack</li>
  <li>Tree</li>
</ul>
<ul class="Aa">
  <li>Sorting</li>
  <li>Search</li>
</ul>

</body>
</html>
```

### ◆목차 만들기
* `<ol></ol>` ordered list  
안에 `<li>`태그로 작성하면 숫자 목록이 자동 생성됨   

* `<ul></ul>` unordered list    
숫자 없는 목록 자동 생성    

* `list-style: ~;` 을 통해 스타일 설정 가능     
* `border-left:`, `padding:` 을 통한 세로줄 형식 정렬

* 임의의 행 지정법  
`selector:first-child{}` 태그:첫번째 줄 지정{css}   
`selector:last-child{}` 태그:마지막 줄 지정{css}    
`selector:nth-child(odd){}` 홀수 줄 지정    
`selector:nth-child(even){}` 짝수 줄 지정   