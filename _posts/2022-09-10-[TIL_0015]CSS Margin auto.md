
2022.09.10.토 // [Start-kit] 15. [CSS] Margin 외부공백
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
      div {
        background-color: yellow;
        margin-bottom: 20px;
      }
      .haswidth {
        width: 150px;
      }
      .center {
        margin: 20px auto;
      }

    </style>
</head>
<body>
  <div>그냥div태그 / margin-bottom: 20px;</div>
  <div class="hasWidth">div+가로150px;</div>
  <div class="hasWidth">div+margin All 20px auto;</div>
 
  <p>margin: auto 이건 자동 정렬</p>
  <p>div + margin-bottom 이걸로 행간 조절 가능</p><br>

</body>
</html>

```

### ◆ Margin auto   
* **외부공백 자동정렬 기능**    
`.css{margin: 값 한 개;}` 상하좌우 일괄설정     
`.css{margin: 값A 값B;}` 값A = 상하값 / 값B = 좌우값    
`.css{margin: 값 한 개;}` 상하좌우 일괄설정     

*솔직히 큰 효용은 모르겠는데, 공부하다 보면 알 지 싶다.*