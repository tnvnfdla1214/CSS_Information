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
