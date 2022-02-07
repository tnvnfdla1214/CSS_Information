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

### 상태 선택자

이 차트는 타입이 아닌 상태에 따라서 CSS 속성의 변화를 줄 수 있습니다.

예를 들어 input:focus, enable, disable 로 나눌 수 있습니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152777683-80ef221f-0454-461b-b0da-08b6f68920d8.png">
</div>

### 구조 선택자
구조에 따라서 CSS 속성이 변화는 설정을 할 수 있습니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152778390-15927fc0-ac1f-417d-ae39-dd4b764eca94.png">
</div>

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
    <style>
        ul li {
            list-style:none;/*앞 에 . 없애기*/
            border:1px solid #cccccc;
            padding:10px;
            background-color:#efefef;
            font-weight:bold;
            font-size:20px;
        }

            ul li a {
                color:#000000;
            }
            ul li:nth-last-child(2n+1) {/*구조중 홀수인것 선택*/
                background-color:#de9393;
            }
            ul li:first-child, ul li:last-child {/*첫번쨰와 마지막것을 선택*/
                background-color:yellow;
            }
            ul li first-child { /*첫번쨰의 라운드를 깎는다*/
                border-radius:10px 10px 0 0;
            }
            ul li last-child {/*마지막의 라운드를 깎는다*/
                border-radius:0 0 0 10px;
            }
    </style>
</head>
<body>
    <div id="ccontent">
        <ul>
            <li><a href="#">memu1</a></li>
            <li><a href="#">memu2</a></li>
            <li><a href="#">memu3</a></li>
            <li><a href="#">memu4</a></li>
            <li><a href="#">memu5</a></li>
            <li><a href="#">memu6</a></li>
            <li><a href="#">memu7</a></li>
            <li><a href="#">memu8</a></li>
        </ul>
    </div>
 
</body>
</html>
```
## 전체적인 레이아웃 설정 예시

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152785697-ca28a39f-c761-4f76-8549-ab56b2bfbfba.png">
</div>

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>

        #header, #content, #footer {
            width:1000px;
            margin : 0 auto;
            overflow:hidden;
        }

        #header .left_space, #content .left_space, #footer .left_space { 
            width:150px; height:150px;
            float:left;
            background-color:#f3f3f3;
            border:1px solid #cccccc;
        }

        #header .center_space, #content .center_space, #footer .center_space { 
            width:694px; height:150px;
            float:left;
            background-color:#f3f3f3;
            border:1px solid #cccccc;
        }

        #header .right_space, #content .right_space, #footer .right_space { 
            width:150px; height:150px;
            float:right;
            background-color:#f3f3f3;
            border:1px solid #cccccc;
        }

        #header .left_space, #footer .right_space {
            border-radius:30px 0;
        }

        #header .right_space, #footer .left_space  {
            border-radius:0 30px;
        }

        #content .left_space  {
            border-radius:0 30px 30px 0;
            height:300px;
        }

        #content .right_space  {
            border-radius:30px 0 0 30px;
            height:300px;
        }

        #header .center_space  {
            border-radius:0 0 30px 30px;
        }

        #content .center_space  {
            border-radius:30px;
            height:300px;
        }

        #footer .center_space  {
            border-radius:30px 30px 0 0;
        }

        #content .center_space ul li {
            list-style:none;
            float:left;
            padding:0 40px;
            font-weight:bold;
            font-size:20px;
        }

        #content .hiseoul {
            clear:both;
            padding:10px;
        }

    </style>
</head>
<body>
    <div id="header">
        <div class="left_space"></div>
        <div class="center_space"></div>
        <div class="right_space"></div>
    </div>

    <div id="content">
        <div class="left_space"></div>
        <div class="center_space">
            <div>
                <ul>
                    <li>menu1</li>
                    <li>menu2</li>
                    <li>menu3</li>
                    <li>menu4</li>
                </ul>
            </div>
            <div class="hiseoul">
                <h1>하이서울브랜드</h1>
                <p>서울시와 서울산업진흥원(SBA)이 공동으로 지원하는 하이
서울브랜드 사업은 우수한 기술력과 상품력을 보유하고 있으나
 고유브랜드 육성에 어려움을 겪고 있는 우수기업들이 서울시가 인정한 중소기업 공동브랜드인 하이서울브랜드를 활용하여 제품 경쟁력을 강화할 수 있도록 각종 홍보 마케팅을 지원하는 사업입니다. </p>
            </div>
        </div>
        
        <div class="right_space"></div>
    </div>

    <div id="footer">
        <div class="left_space"></div>
        <div class="center_space"></div>
        <div class="right_space"></div>
    </div>
</body>
</html>
```
## 4강
### 문자 선택자

특정 문자 또는 문자열을 선택하여 CSS 속성을 설정할 수 있습니다.

아래 예시는 history1과 history2의 첫번째 문자를 선택하여 크기를 키워 주었고 history2와 history1의 첫번쨰 라인을 선택하여 폰트와 칼라를 바꿔줬습니다. 

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152798660-0865ac15-b9ec-475d-915b-c7826a30b1fc.png">
</div>


```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
    <style>

        #wrap {
            width:800px;
            margin:0 auto;
        }

        #header {
            border-bottom:1px solid #cccccc;
        }

        #content a {
            text-decoration:none;
        }

        #content a::after {
            content: ' - ' attr(href);
        }

        #content li:not(.fa) {
            background-color:#ffd800;
        }

        #footer ul {
            overflow:hidden;
            border:2px solid #cccccc;
        }

        #footer ul li {
            list-style:none;
            float:left; padding:20px;
        }

    </style>
</head>
<body>
    <div id="wrap">

        <div id="header">
            <h1>weekly connect website</h1>
        </div>

        <div id="content">
            <ul>
                <li><a href="http://www.sba.seoul.kr" target="_blank">서울산업진흥원</a></li>
                <li class="fa"><a href="http://wiz.center" target="_blank">위즈센터</a></li>
                <li><a href="http://www.yahoo.com" target="_blank">야후</a></li>
                <li class="fa"><a href="http://www.google.com" target="_blank">구글</a></li>
            </ul>
        </div>

        <div id="footer">
            <ul>
                <li><img src="http://www.sba.seoul.kr/kr/images/footer/f_logo.png"></li>
                <li><img src="http://www.sba.seoul.kr/kr/images/footer/copyright.png"></li>
            </ul>
        </div>

    </div>

</body>
</html>
```

### 링크 선택자
문서에서 링크되어 있는 문자를 선택하여, CSS 속성을 설정할 수 있습니다.

아래 예시에서는 a 태그 뒤에 '-'를 붙여줍니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152799974-3c93ac33-f7a1-45d8-97d4-fc2f553c1c1d.png">
</div>

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
    <style>

        #wrap {
            width:800px;
            margin:0 auto;
        }

        #header {
            border-bottom:1px solid #cccccc;
        }

        #content a {
            text-decoration:none;
        }

        #content a::after {
            content: ' - ' attr(href);
        }

        #footer ul {
            overflow:hidden;
            border:2px solid #cccccc;
        }

        #footer ul li {
            list-style:none;
            float:left; padding:20px;
        }

    </style>
</head>
<body>
    <div id="wrap">

        <div id="header">
            <h1>weekly connect website</h1>
        </div>

        <div id="content">
            <ul>
                <li><a href="http://www.sba.seoul.kr" target="_blank">서울산업진흥원</a></li>
                <li><a href="http://wiz.center" target="_blank">위즈센터</a></li>
                <li><a href="http://www.yahoo.com" target="_blank">야후</a></li>
                <li><a href="http://www.google.com" target="_blank">구글</a></li>
            </ul>
        </div>

        <div id="footer">
            <ul>
                <li><img src="http://www.sba.seoul.kr/kr/images/footer/f_logo.png"></li>
                <li><img src="http://www.sba.seoul.kr/kr/images/footer/copyright.png"></li>
            </ul>
        </div>

    </div>

</body>
</html>
```

## 5강
### CSS 단위

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152801990-399881b3-4756-42e3-bac1-c51e126803d7.png">
</div>

p태그의 단위
- px (실제 단위 기본은 16px)
- % (100%가 기본 사이즈로 크기를 키우고 줄입니다.)
- em (1.0em 이 기본 단위로서 16px == 1.0em 입니다.)

### url()

Backgraount-img 속성의 속성값으로 많이 사용됩니다. 이 경우 배경 이미지의 경로를 나타냅니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152802674-cbe31e36-ffd4-4c7a-a2a8-752a7aa5c580.png">
</div>

### display 속성
화면에 어떻게 보이는지를 설정하는 속성입니다. 다양한 속성값이 있지만, 주로 몇 가지만 많이 사용됩니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152803158-46c5fd32-9137-4188-9c23-5954c7ffcfb1.png">
</div>

display 태그는 크게 2가지로 나누어 집니다.
1. block 태그 (블록처럼 아래로 쌓아내려갑니다.)
    - div
    - p
    - li
2. inline 태그 (왼쪽으로 쌓입니다.)
    - span

이 둘은 차이점이 있습니다. block은 높이가 있습니다. 하지만 line은 높이의 최소값을 사용합니다. 그래서 Inline-block 태그는 옆으로 쌓이지만 높이를 가지고 있습니다.

아래와 같이 content5,content6,content7,content8 은 높이 속성을 추가했음에도 적용되지 않았습니다.

또한 content7에는 none 추가 하여 없앴습니다.

다만 content5에서의 마진을 보면 상하에는 마진이 들어가 있지 않지만 죄우에는 들어갑니다.

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>

        body div:nth-child(1) {
            width:100px;
            height:100px;
            background-color:#ff0000;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

        body div:nth-child(2) {
            width:100px;
            height:100px;
            background-color:#00ff00;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

        body div:nth-child(3) {
            width:100px;
            height:100px;
            background-color:#0000ff;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

        body div:nth-child(4) {
            width:100px;
            height:100px;
            background-color:#ff0000;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

        body div:nth-child(5) {
            width:100px;
            height:100px;
            background-color:#00ff00;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            display:inline; /*inline으로 바꿈*/
            margin:10px 10px 10px 10px; /*마진 추가*/
        }

        body div:nth-child(6) {
            width:100px;
            height:100px;
            background-color:#0000ff;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            display:inline;
        }
        body div:nth-child(7) {
            width:100px;
            height:100px;
            background-color:#ff0000;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            display:none; /*none 추가*/
        }
        body div:nth-child(8) {
            width:100px;
            height:100px;
            background-color:#00ff00;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            display:inline;
        }
        body div:nth-child(9) {
            width:100px;
            height:100px;
            background-color:#0000ff;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            display:inline-block; /*inline-block 적용*/
        }

    </style>

</head>
<body>

    <div>
        content1
    </div>
    <div>
        content2
    </div>
    <div>
        content3
    </div>

    <div>
        content4
    </div>
    <div>
        content5
    </div>
    <div>
        content6
    </div>
    <div>
        content7
    </div>
    <div>
        content8
    </div>
    <div>
        content9
    </div>

</body>
</html>
```

### Visible 속성
display속성의 none 속성값과 비교하여 이해합니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152805166-f1c3b2a5-da57-4ae9-9e0b-e675188a0c0f.png">
</div>

display는 none을 추가 하여 없앴지만 Visiblity의 hidden은 없애지 않고 칸을 차지합니다.

```HTML
<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>

    <style>

        #display_none div:nth-child(1) {
            width:100px;
            height:100px;
            background-color:#ff0000;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

        #display_none div:nth-child(2) {
            width:100px;
            height:100px;
            background-color:#00ff00;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            display:none; /*none 추가*/
        }

        #display_none div:nth-child(3) {
            width:100px;
            height:100px;
            background-color:#0000ff;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }


        #visibility_hidden div:nth-child(1) {
            width:100px;
            height:100px;
            background-color:#ff0000;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

        #visibility_hidden div:nth-child(2) {
            width:100px;
            height:100px;
            background-color:#00ff00;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
            visibility:hidden; /*hidden 추가*/
        }

        #visibility_hidden div:nth-child(3) {
            width:100px;
            height:100px;
            background-color:#0000ff;
            color:#ffffff;
            font-weight:bold;
            text-align:center;
        }

    </style>

</head>
<body> 
    <div id="display_none">
        <div>
            content1
        </div>
        <div>
            content2
        </div>
        <div>
            content3
        </div>
    </div>

    <div id="visibility_hidden">
        <div>
            content1
        </div>
        <div>
            content2
        </div>
        <div>
            content3
        </div>
    </div>

</body>
</html>
```

### opacity 속성
투명도를 조절하는 속성입니다. 여러 곳에 유용하게 사용 됩니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152806251-56545cbd-a8ae-4e44-80e4-cf664a8a76fa.png">
</div>

## 6강
### margin 및 padding 속성

margin 과 padding의 차이는 마진만 넣을경우 원래의 형태에서 주변에 투명하게 거리가 늘어납니다. 반대로 padding은 원래의 형태에서 늘어나게 됩니다. 만약 백그라운드에 색을 넣을경우 패딩은 늘어난 영역마저 색이 변하게 되고 반대로 마진은 색이 생기지 않습니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152810266-fa53c3c3-7fd0-47b2-9565-12ea571e71db.png">
</div>

### box-sizing 속성

border는 영역에 태두리를 만들어집니다. 이말은 즉슨 바깥으로 태두리가 생겨서 원래의 영역은 변화가 없습니다. 그런데 box-size를 줄시 바깥쪽이 아닌 안쪽으로 형성됩니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152810751-a28e6859-7372-4f3a-b5e5-babbfca705bb.png">
</div>


### border 속성

border 속성에는 대표적으로 아래와 같습니다.
+ width : 두꼐
+ style : 스타일 (solid, dashed)
+ color : 색

여기서 위의 속성을 한번에 정의하는것이 지금까지 했던 방법(3번쨰꺼)입니다.

<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152810878-57fcf69c-8097-4e47-9788-b6dcc85d45da.png">
</div>


### background-image 속성

background-image 속성으로는

+ background-size : 크기 (기본은 100%)
+ background-repeate : 반복을 하지 않습니다.
+ background-attachment : 이미지가 화면 제일 끝에 붙습니다.
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152811001-a175890b-e482-4f0a-9a36-ed7f1bf9738a.png">
</div>
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152811041-0e53865b-bd94-499f-8f7e-093ff0ba0349.png">
</div>
<div align="center">
<img src = "https://user-images.githubusercontent.com/48902047/152811090-e90bead7-87a1-4ad6-adae-139434ccc546.png">
</div>






