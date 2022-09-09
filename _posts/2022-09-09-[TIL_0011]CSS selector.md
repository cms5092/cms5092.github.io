
2022.09.09.금 // [Start-kit] 11. [CSS] selector 우선순위
========

### 부트캠프 사전 스터디 기본 교육자료 HTML/CSS 정리     

```js
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>repl.it</title>
    <style>
        p{
            font-size: 30px;
        }
        .pTag{
            color:gray;
            font-size: 15px;
        }
        #thirdLine{
            text-decoration: unde rline;
        }
        .pre p{
            background-color: yellow;
            font-size: 15px;
            width: 250px;
            height: 30px;
            border: 3px solid red;
            padding-bottom:30px;
            box-sizing: border-box;
        }
        .container header p.title{
            font-size: 50px;
        }
    </style>

</head>

<body>
  <p>나는 p태그</p>
  <p class="pTag">p태그면서 pTag클래스</p>
  <p class="pTag" id="thirdLine">나는 p태그면서 class도 있고 id도 있다.</p>
  <p class="pTag" id="fourthLine" style="font-size: 50px; 
  color: red; text-decoration: none;">근데 내가 대빵</p><br><br>
  <p>div class="pre"</P>
  <div class="pre">
    <p>pre 클래스 안에 있는 span</p>
  </div>
  <p>div class="none"</P>
  <div class="none">
    <span>main 클래스 안에 있는 span</span><br>
    <sapn>span은 아무 속성값이 없으므로 설정 출력</sapn>
  </div>
</body>

</html>

```
◆출력
추후 입력 예정

◆정리
* 태그 별 css입력을 통해 구분해서 사용 할 수 있음
* 식별자를 태그 내에 입력해 세부적으로 구분 할 수 있음
* 그러나 붉은 글처럼 직접 style을 입력해 덮을 수 있음
* div태그를 이용해 공간을 가르고 공간에 따라 다른 식별자를 정의 할 수 있음