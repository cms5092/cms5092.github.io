
2022.09.11.일 // [Start-kit] 20. [HTML&CSS] 
========

## 부트캠프 사전 스터디 기본 교육자료 HTML/CSS 정리   


```js
<!DOCTYPE html>
<!DOCTYPE html>
<html>

  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <style>
      body {
        background-color:bisque
      }
      .PfixedA {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        height: 48px;
        background-color: rgba(45, 45, 45, 0.95);
      }
      .Pabs {
        position: absolute;
        left: 50%;
        margin-left: -10px;
      }
      .productList {
        width: 100px;
        margin-top: 100px;
      }
      .product:first-child {
        height: 100px;
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <header class="PfixedA">
      <img class="Pabs" src="https://www.apple.com/ac/globalnav/4/en_US/images/globalnav/apple/image_small.svg">
    </header>
    <div class="productList">
      <div class="product">
        상품1
      </div>
    </div>

  </body>
</html>

```

### ◆Position - fixed    

```js
position: fixed;
right: 0;
bottom: 0;
``` 
위치: 고정된    
1행 고정위치: 절대위치와는 다르게 부모위치 없이 눈에 보이는 브라우저 크기만큼 화면 내에서만 움직임    
2행 화면 우측에서 0 위치    
3행 화면 하단에서 0 위치    
