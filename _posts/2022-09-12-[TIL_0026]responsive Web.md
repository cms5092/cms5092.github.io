
2022.09.12.월 // [Start-kit] 26. media wab_반응형 웹
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
      @media screen and (max-width: 1000px) {
	      body {
		          font-size: 20px;
              background-color: blue;
	            }     
        .aA {
            width: 900px;
            background-color: yellow;
        }
        .bB {
          font-size: 30px;
          background-color: aqua;
        }
      }
      @media screen and (min-width: 600px) {
        .cC {
          background-color: red;
        }
      }

      .def {
        background-color: black;
        color: white;
        width: 600px;
      }
    </style>
  </head>
  <body>
    <p id="window-width"></p>
    
    <script src="index.js"></script>
    <div class="def">기준 600px</div>
    <div class="aA">max-width = 가로1000px이하 .aA</div>
    <div class="bB">max-width = 가로1000px이하 .bB</div>
    <div class="cC">min-width = 가로600px이상 .cC</div>
  </body>
</html>

```

### 미디어웹 사용법
`@media screen and (조건) {내용}`   
* `@media` 미디어 쿼리 시작 선언문  
* `screen` 출력 디바이스 선언문(screen: 모든 스크린, only print: 오직 프린트...)    
* `and (조건)` 조건 선언문(media feature)   
#

#### `acd (max-width)` 최대 가로 1000px을 설정 할 경우
* 조건 외 상황(가로 1000px이상)에서 모든 속성값은 기본값 또는 조건이 없이 선언된 값으로 출력    
* 조건 내 상황(가로 1000px이하)에서 `@media`에 포함된 body, class, id 등 요소에 설정된 값으로 출력      
* 조건 내 상황에서도 특별히 지정된 속성값이 없으면 차상위 선언값이 출력됨   
* `and (조건) and (조건)` 식으로 연달아 조건을 선언할 수 있음   
