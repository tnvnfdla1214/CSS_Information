# CSS_Information
## 1강
### 선택자란
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152728581-40657b26-4b4e-4ecc-95c5-c7784ac0369a.png">
</div>

특정 태그를 선택하여, 해당 태그의 속성을 변경하는 목적으로 사용합니다.

위의 예시를 보면 head안에서 div태그를 찾아 배경색을 바꾸어 줍니다. 또 다른 div태그가 있어도 전부 찾아 바꿔줍니다.

### tag 선택자
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152728963-415ab784-b6e6-470a-a22d-ebb6b30be0ba.png">
</div>

특정태그를 선택하여 CSS 속성을 적용할 수 있습니다.

위의 예시는 아래와 같습니다. 아래 코드에서 볼 곳은 처음 h1의 색을 바꾸어도 아래에서 재정의를 하였다면 다시 변경됩니다.

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>
        li, ul, h1 {
            color : #ff006e;
        }
        h1 {
            color : #ffd800;
        }
        p {
            background-color: #00ff21;
            font-weight: bold
        }
    </style>

</head>
<body>
    <header>
        <h1> OO 주식회사</h1>
    </header>
    <nav>
        <ul>
            <li> 회사소개 </li>
            <li> 제품소개 </li>
            <li> 고객센터 </li>
            <li> 공지사항 </li>
        </ul>
    </nav>

    <section>
        <p>
            우리 회사는 50년 전통의 역사와 뛰어난 기술을 바탕으로 좋은 회사 입니다.
        </p>
    </section>

    <footer>
        <p>
            서울시 oo구 oo동 oo빌딩
        </p>
    </footer>
</body>
</html>
```
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152730703-c7d1389c-c7e0-46df-9892-e290364b3674.png">
</div>

### \*선택자

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152731193-b5766d52-fbf3-4b3c-89fa-92dc8c6aac4a.png">
</div>

전체라는 의미의 \*선택자를 사용하면 문서 전체를 선택하는 의미가 있습니다.

### 전체 선택자의 혼합
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152731371-344e43ef-ddbe-428a-af61-42d3a69f06b1.png">
</div>
위의 예시와 같이 처음 전체를 선택하고 그중 원하는 항목을 추가적으로 변경 가능합니다.

## 2강
### id(#) 와 class(.)
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152731836-2b234119-0868-4ace-8a4e-5cacccf0e035.png">
</div>

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>
        #header {
            width: 500px;
            background-color: #ff0000;
            border: 1px solid #b6ff00; <!--태두리 -->
            text-align : center; <!-- align는 가로 정렬 -->
        }
        #wrap {
            width: 500px;
            background-color: #0094ff;
            border: 2px solid #b6ff00;
            text-align: center;
            overflow: hidden;<!--이것이 있으면 float 사용가능 -->
        }
        #content {
            width : 350px;
            border : 1px solid red;
            float : left; <!-- 왼쪽에 붙이기 -->
        }
        #banner {
            border: 1px solid red;
            float: left;
        }

        #footer {
            clear: both; <!-- 위에서 float 가 영향을 줄 수 있으므로 없애주는 역할 -->
            width:500px;
            background-color: #0094ff;
            border: 3px solid #b200ff;
            text-align: center;
        }
        .m1 {
            color:#ffd800;
            font-weight:bold;
        }
        .m1, .m3, .m4 {
            font-size:20px;
        }


    </style>

</head>
<body>
    <div id="header">
        <h1>HEADER</h1>
    </div>

    <div id="wrap">
        <div id="content">
            <h1>CONTENT</h1>
            <ul>
                <li class="m1">메뉴1</li>
                <li class="m2">메뉴2</li>
                <li class="m3">메뉴3</li>
                <li class="m4">메뉴4</li>
            </ul>
        </div>
        <div id="banner">
            <h1>BANNER</h1>
            <img src="#" />
        </div>

    </div>

    <div id="footer">
        <h1>FOOTER</h1>
    </div>
</body>
</html>
```
### 속성 선택자

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152738281-737f6356-2ad9-4228-aa7d-962a81a0f5bf.png">
</div>

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>
        input {
            color:green;
            font-size:30px;
            font-weight:bold;
        }

            input[type = text] {
                color:orange;
                font-size:50px;
                width:200px;
            }
            input[type=tel] {
                border: 5px solid green;
            }
    </style>

</head>
<body>

    <form>
        이름:<input type="text" /><br />
        아이디:<input type="text" /><br />
        비밀번호:<input type="password" /><br />
        전화번호:<input type="tel" /><br />
    </form>

    <img src="#" /><br />

</body>
</html>
```
### 후손 및 자손 선택자

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152739334-b3c7ff98-af90-4d2b-8f51-465ecf0b8980.png">
</div>

1. 후손 선택자 : 한칸 띄어 작성하며 아래 예시와 같이 div 안에 li가 있다면 어디던 다 적용시킵니다.
2. 자손 선택자 : > 표시를 사용하며 아래 예시와 같이 div 바로 아래 h1이 첫번째에 있는 모두를 적용시킵니다. 깊숙히 들어가지 않습니다.

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>
        #header, #wrap, #footer {
            border:1px solid #cccccc;
            width:500px;
        }

        div li { /*후손선택자*/
            background-color:red;
        }

        div p {
            font-size:25px;
        }

        div > h1 { /*자손 선택자*/
            font-weight:bold;
            color:yellow;
        }
    </style>
</head>
<body>
    <div id="header">
        <div class="logo">
            <h1>LOGO</h1>
        </div>
        <div class="copy">
            <h2>global company</h2>
        </div>
    </div>

    <div id="wrap">
        <p>서울시 8대 신성장동력의 하나인 녹색산업을 집중 육성하기 위해 녹색기업에 특화된 지원기관인 녹색산업지원센터는 녹색중소기업의 종합 지원체계를 구축하고 실질적 성과창출을 유도하여 서울형 녹색산업 인프라 조성과 효율적인 지원사업 시행으로 녹색중소기업의 경영내실화 및 산업 저변확대에 기여하는 것이 목적</p>
        <ul>
            <li><p>서울애니메이션센터</p></li>
            <li><h1>서울시녹색산업지원센터</h1></li>
            <li><p>DMC(디지털미디어시티)</p></li>
            <li><h1>서울게임콘텐츠센터</h1></li>
            <li><p>서울시우수사회적기업지원</p></li>
            <li><h1>캐릭터포털사이트</h1></li>
            <li><p>재미로/재미랑</p></li>
        </ul>
    </div>

    <div id="footer">
        <img src="http://www.sba.seoul.kr/kr/images/footer/copyright.png">
    </div>
</body>
</html>
```

### 동위 선택자(~,+)

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152744483-f2ab6381-c7ba-4ad1-989a-ee3b2b487778.png">
</div>

1. ~ 의 경우 동등한 위치에서 아래의 모든 것을 선택해줍니다. 예를 들어 h3~div 경우 h3 아래의 div는 모두 선택하여 적용시켜줍니다.
2. + 의 경우 동등한 위치에서 아래의 첫번째의 것을 선택해 줍니다. 예를 들어 h3+div 경우 h3 아래의 첫번째 div를 선택하여 적용시켜줍니다.

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
    <style>

        h3~div { /*동등한 위치인 것을 다 선택*/
            font-size:10px;
            color:orange
        }

        h3+div { /*동등한 위치인 것중 첫번째를 선택*/
            font-size:20px;
            font-weight:bold;
            color:blue;
        }

        #title ~ div { /*동등한 위치인 것을 다 선택*/
            width: 300px;
            background-color: yellow;
        }

    </style>
</head>
<body>

    <h3 id="title">동위 선택자(+, ~) </h3>
    <div>div_01</div>
    <div>div_02</div>
    <div>div_03</div>
    <div>div_04</div>
    <div>div_05</div>


</body>
</html>
```

## 3강
### 반응 선택자

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152746748-190b8b4c-ac34-4329-bee1-8ca8da1530b2.png">
</div>

마우스의 반응에 따른 속성을 설정할 수 있습니다.

1. : hover : 마우스의 움직에따라 변화 됩니다.

또다른 예시를 보겠습니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152748898-702b2388-489f-4361-aab9-4e151c515d9a.png">
</div>


```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
    <style>
        div {
            width:300px; background-color:red; margin:0 auto;
            /*auto 설정시 좌우를 대칭시켜 브라우져를 늘리거나 줄여도 중앙으로 정렬됩니다. */
        }

        ol li {
            font-size:3em;
            color:#ffffff;
            font-weight:bold;
        }

            ol li:hover {
                color: green; font-size:4em;
            }


    </style>
</head>
<body>

    <div>
        <ol>
            <li>memu1</li>
            <li>memu2</li>
            <li>memu3</li>
            <li>memu4</li>
        </ol>
    </div>

</body>
</html>
```












