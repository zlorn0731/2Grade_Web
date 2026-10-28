# 👨‍💻웹 표준 기술

## CSS3 기초 선택자와 단위
- 선택자의 용도와 사용법
- 기본 선택자
- 속성 선택자
- 후손 선택자와 자손 선택자
- 반응, 상태, 구조 선택자
- CSS3 단위

### 선택자의 용도와 사용법

#### CSS(Cascading Style Sheets) 개요
- 선택자 - CSS3에서 특정 HTML 태그를 선택할 때 사용
  - CSS 블록
```
h1 { color : red; }

h1 : 선택자
color : 스타일 속성
red : 스타일 값
```
- 스타일시트
  - CSS로 작성된 코드
  - <style>..</style>

#### 예제 코드 5-1 : selector_basic.html
```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS3 Selector Basic</title>
  <style>__________________________________________| 스타일시트
    h1 {____________________________| CSS 블록     |
        color: red;                 |              | 
        background-color: orange:   |              |
       }____________________________|              |
  </style>_________________________________________|
</head>
<body>
  <h1>CSS3 선택자 기본</h1>
</body>
</html>
```

#### CSS 선택자 종류
- 
| 종류 | 형태 | 사용 예시 |
|------|------|-----------|
| 전체 선택자 | * | * |
| 태그 선택자 | 태그 | h1 |
| 아이디 선택자 | #아이디 | #id |
| 클래스 선택자 | .클래스 | .header |
| 속성 선택자 | 선택자[속성 = 값] | input[type = text] |
| 속성 선택자 | 선택자[속성 ~= 값] | div[data-role ~= row] |
| 속성 선택자 | 선택자[속성 |= 값] | div[data-role |= row] |
| 속성 선택자 | 선택자[속성 ^= 값] | div[data-role ^= row] |
| 속성 선택자 | 선택자[속성 $= 값] | div[data-role $= 9] |
| 속성 선택자 | 선택자[속성 *= 값] | div[data-role *= row] |
| 후손 선택자 | 선택자 선택자 | header h1 |
| 자손 선택자 | 선택자 > 선택자 | header > h1 |
| 반응 선택자 | 선택자:active | div:active |
| 반응 선택자 | 선택자:hover | div:hover |
| 상태 선택자 | 선택자:checked | input:checked |
| 상태 선택자 | 선택자:focus | input:focus |
| 상태 선택자 | 선택자:enabled | input:enabled |
| 상태 선택자 | 선택자:disabled | input:disabled |
| 구조 선택자 | 선택자:first-child | li:first-child |
| 구조 선택자 | 선택자:last-child | li:last-child |
| 구조 선택자 | 선택자:nth-child(수열) | li:nth-child(2n+1) |
| 구조 선택자 | 선택자:nth-last-child(수열) | li:nth-last-child(2n+1) |
| 구조 선택자 | 선택자:first-of-type | h1:first-of-type |
| 구조 선택자 | 선택자:last-of-type | h1:last-of-type |
| 구조 선택자 | 선택자:nth-of-type(수열) | h1:nth-of-type(2n+1) |
| 구조 선택자 | 선택자:nth-last-of-type(수열) | h1:nth-last-of-type(2n+1) |
| 동위 선택자 | 선택자 + 선택자 | h1 + div |
| 링크 선택자 | 선택자:link | a:link |
| 링크 선택자 | 선택자:visited | a:visited |
| 문자 선택자 | 선택자::first-letter | p::first-letter |
| 문자 선택자 | 선택자::first-line | p::first-line |
| 문자 선택자 | 선택자::after | p::after |
| 문자 선택자 | 선택자::before | p::before |
| 문자 선택자 | 선택자::selection | p::selection |
| 부정 선택자 | 선택자:not(선택자) | li:not(.item) |
```
:: - 가상 요소 선택자(pseudo-element selector)
: - 가상 클래스 선택자(pseudo-class selector)
```

### 기본 선택자

#### 기본 선택자 종류
- 
| 종류 | 형태 | 설명 |
|------|------|------|
| 전체 선택자 | * | HTML 페이지 내부의 태그를 모두 선택 |
| 태그 선택자 | 태그 | HTML 페이지 내부의 특정 태그를 모두 선택 |
| 아이디 선택자 | #아이디 | 특정 id 속성이 있는 태그 선택, 웹 표준에 id 속성은 웹 페이지 내부에서 중복되면 안된다는 규정이 있으므로 아이디 선택지는 특정 태그 하나를 선택할 때 사용 |
| 클래스 선택자 | .클래스 | 특정 클래스가 있는 태그 선택 |

#### 예제 5-1 : 전체 선택자와 태그 선택자
- 1. 전체 선택자 적용하기
- 코드 5-2 selector_wildcard.html
```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS3 Selector Basic Page</title>
  <style>
    * { color: red; }
  </style>
<body>
  <h1>제목 글자 태그</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
  </body>
  </html>
```
- 2. 태그 선택자 적용하기
- 코드 5-3 selector_tag.html
```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS3 Selector Basic Page</title>
  <style>
    h1 { color: red; }
    p  { color: blue; }
  </style>
</head>
<body>
  <h1>제목 글자</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
  <p>Nunc nisl turpis, aliquet et gravida non, facillisis a sem.</p>
</body>
</html>
```
- 선택자 여러 개에 속성 적용하기 : 쉼표(,) 사용
```html
body,p,h1,h2,h3,h4,h5,h6{margin: 0; padding: 0;}
```

#### 예제 5-2 : 아이디 선택자
- 공간분할태그에 아이디 선택자를 사용해 id속성을 적용하고 레이아웃 구성
- 코드 5-4 selector_id.html
```html
<!DOCTYPE html>
<head>
    <title>CSS3 Selector Basic Page</title>
    <style>___________________________________________| 아이디 선택자 사용
        #header {                                     |
            width: 800px; margin: 0 auto;             |
            background: red;                          |
        }                                             | 
        #wrap {                                       | 
            width: 800px; margin: 0 auto;             |
            overflow: hidden;                         |
        }                                             |
        #aside {                                      |  
            width: 200px; float: left;                |
            background: blue;                         |
        }                                             |
        #content {                                    |
            width: 600px; float: left;                |
            background: green;                        |
        }                                             |
    </style>__________________________________________|
    <body>
        <div id="header">_______________________________| 공간분할태그에 적용된 id태그
            <h1>#header 태그</h1>                       |
        </div>                                          |
        <div id="wrap">                                 |
            <h1>#wrap 태그</h1>                         | 
        </div>                                          |
        <div id="aside">                                |
            <h1>#aside 태그</h1>                        |
        </div>                                          |
        <div id="content">                              |
            <h1>#content 태그</h1>                      |
        </div>__________________________________________|
    </body>
</head>
```

#### 예제 5-3 : 클래스 선택자
- 1. 클래스 선택자를 1개 사용하기
- 코드 5-6 selector_class.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic</title>
        <style>_________________________| 클래스 선택자 1개 사용
            .select { color: red; }     |
        </style>________________________|
    </head>
    <body>
        <ul>
            <li class="select">사과</li>_________________ color: red;
            <li>바나나</li>
            <li class="select">오렌지</li>_______________ color: red;
            <li>감</li>
        </ul>
    </body>
</html>
```
- 2. 클래스 선택자를 여러 개 사용하기
- 코드 5-7 selector_multiClass.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic</title>
        <style>_______________________________________| 클래스를 여러 개 사용 
            .item { color: red; }                     | (.item 클래스, .header 클래스)
            .header { background-color: blue; }       |
        </style>______________________________________|
    </head>
    <body>
        <h1 class="item header">동해물과 백두산이</h1>
    </body>              |______________________________두 가지 속성이 모두 적용됨!
</html>                                                 (파란색 배경, 빨간색 글자)
```

### 속성 선택자

#### 속성 선택자 입력 형태
- 
| 형태 | 설명 |
|------|------|
| 선택자[속성] | 특정한 속성이 있는 태그 선택 |
| 선택자[속성=값] | 특정한 속성 내부 값이 특정 값과 같은 태그 선택 |

#### 예제 5-4 : 속성 선택자
- 코드 5-9 attribute_basic.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic Page</title>
        <style>_____________________________________________| 속성 선택자 사용하여 적용할 서로 다른
            input[type="text"] { background: red; }         | input 태그를 선택
            input[type="password"] { background: blue; }    | (text 입력양식은 빨간색, password 입력 양식은 파란색)
        </style>____________________________________________|
    </head>
    <body>
        <form>
            <input type="text">______________| Input 태그는 동일한 이름을 사용하나, 
            <input type="password">__________| type 속성에 따라 형태가 다름
        </form>
    </body>
</html>
```

### 후손 선택자와 자손 선택자

#### 후손과 자손의 개념
- 후손/자손 선택자는 특정 태그의 후손과 자손을 선택할 때 사용
  - 자손 - 특정 태그를 기준으로 바로 한 단계 아래 위치한 태그
  - 후손 - 특정 태그를 기준으로 아래에 위치한 모든 태그
```
       [div] 부모
 __________|___________________________
|   ↓------↓-------↓                   |
|  [h1]   [h2]   [ul] 자손             | 
|                  |                   |
|           ↓------↓-------↓           | 후손
|          [li]   [li]   [li]          |
|______________________________________|
```

#### 예제 5-10 : desc_basic.html
```html
<body>
    <div>
        <h1>CSS3 선택자 기본</h1>
        <h2>기본 선택자</h2>
        <ul>
            <li>전채 선택자</li>
            <li>태그 선택자</li>
            <li>아이디 선택자와 클래스 선택자</li>
        </ul>
    </div>
</body>
```

#### 후손 선택자
- 특정한 태그의 후손을 선택할 때 사용
- 
| 형태 | 설명 |
|-------|-----|
| 선택자A와 선택자B | 선택자A의 후손인 선택자B 선택 |

#### 예제 5-5 : 후손 선택자
- 후손선택자를 사용해 특정 대상의 후손이라는 것을 구별
- 코드 5-11 desc_descendants.html
```html
<!DOCTYPE html>
<head>
    <title>CSS3 Selector Basic</title>
    <style>
        #header h1 { color: red; }________| 후손선택자 지정
        #section h1 { color: orange; }____|
    </style>
</head>
<body>
    <div id="header">
        <h1 class="title">Lorem ipsum</h1>
        <div id="nav">
            <h1>Navigation</h1>
        </div>
    </div>
    <div id="section">
        <h1 class="title">Lorem ipsum</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed</p>
    </div>
</body>
```

#### 후손 선택자 여러 개를 함께 사용할 경우 주의 사항
- (1) <header> 태그의 후손인 <h1> 태그와 일반적인 <h2> 태그 선택
```html
<style>
  #header h1, h2 { color: red; }
</style>
```
- (2) <header> 태그의 후손인 <h1> 태그와 header 태그의 후손인 <h2> 태그 선택
```html
<style>
  #header h1, #header h2 { color: red; }
</style>
```

#### 자손 선택자
- 특정한 태그의 자손을 선택할 때 사용
- 
| 형태 | 설명 |
|------|------|
| 선택자A > 선택자B | 선택자A의 자손인 선택자B 선택 |

#### 예제 5-6 자손 : 선택자
- #nav 태그 아래에 있는 h1태그(후손)는 적용되지 않음
- 코드 5-12 desc_children.html
```html
<!DOCTYPE html>
<head>
    <title>CSS3 Selector Basic</title>
    <style>
        #header > h1 { color: red; }_________| 자손선택자 지정
        #section > h1 { color: orange; }_____|
    </style>
</head>
<body>
    <div id="header">
        <h1 class="title">Lorem ipsum</h1>
        <div id="nav">
            <h1>Navigation</h1>
        </div>
    </div>
    <div id="section">
        <h1 class="title">Lorem ipsum</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </div>
</body>
```

#### 예제 5-6 : <table> 태그 요소 선택할 때 자손 선택자 주의사항
- 코드 5-13 desc_tableWithChildren.html
```html
<!DOCTYPE html>
<head>
    <title>CSS3 Selector Basic</title>
    <style>
        table > tr > th {__________| 예상대로 적용하려면 다음과 같이 수정!
            color: red;            | 선택자 table > tbody > tr > th
        }__________________________|
    </style>
</head>
<body>
    <table border="1">
        <tr>
            <th>이름</th>
            <th>지역</th>
        </tr>
        <tr>
            <td>윤인성</td>
            <td>서울특별시 강서구 내발산동</td>
        </tr>
    </table>
</body>
```

#### 검사를 통한 HTML 페이지의 계층 구조
- 웹 브라우저가 <tbody> 태그를 자동으로 추가하므로 스타일 속성이 적용되지 않음
- table 태그에 스타일을 적용할 때는 자손 선택자를 사용하지 않음

### 반응, 상태, 구조 선택자

#### 반응 선택자
- 사용자 반응으로 생성되는 특정한 상태를 선택
- 
| 형태 | 설명 |
|------|------|
| :active | 사용자가 마우스로 클릭한 태그 선택 |
| :hover | 사용자가 마우스 커서를 올린 태그 선택 |

#### 예제 5-7 : 반응 선택자
- 코드 5-14 etc_action.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic</title>
        <style>
            h1:hover { color: red; }_________ 커서를 올렸을 때 red
            h1:active { color: blue; }_______ 눌렀을 때 blue
        </style>
    </head>
    <body>
        <h1>반응 선택자</h1>
    </body>
</html>
```

#### 상태 선택자
- 입력 양식의 상태를 선택할 때 사용
  - 상태 선택자
  - 상태 선택자의 상태
- 
| 형태 | 설명 |
|------|------|
| :checked | 체크 상태의 input 태그 선택 |
| :focus | 포커스를 맞춘 input 태그 선택 |
| :enabled | 사용 가능한 input 태그 선택 |
| :disabled | 사용 불가능한 input 태그 선택 |

#### 예제 5-8 : 상태 선택자
- 코드 5-15 etc_state.html
```html
<!DOCTYPE html>
<head>
    <title>CSS3 Selector Basic</title>
    <style>
        /* input 태그가 사용 가능할 경우에
            background-color 속성에 white 키워드를 적용합니다. */
        input:enabled { background-color: white; }

        /* input 태그가 사용 불가능할 경우에
            background-color 속성에 gray 키워드를 적용합니다. */
        input:disabled { background-color: gray; }

        /* input 태그에 초점이 맞추어진 경우에
            background-color 속성에 orange 키워드를 적용합니다. */
        input:focus { background-color: orange; }
    </style>
</head>
<body>
    <h2>사용 가능</h2>
    <input>
    <h2>사용 불가능</h2>
    <input disabled="disabled"/>
</body>
```

#### 구조 선택자
- 특정한 위치에 있는 태그를 선택할 때 사용
- 
| 형태 | 설명 |
|------|------|
| :first-child | 형제 관계에서 첫 번째로 등장하는 태그 선택 |
| :last-child | 형제 관계에서 마지막으로 등장하는 태그 선택 |
| :nth-child(수열) | 형제 관계에서 앞에서 수열 번째로 등장하는 태그 선택 |
| :nth-last-child(수열) | 형제 관계에서 뒤에서 수열 번째로 등장하는 태그 선택 |
- nth-child와 nth-last-child 선택자
  - 2n+1 수열에 0부터 숫자를 넣을 경우, "1, 3, 5, 7, 9.....?"
  - 구조 선택자는 수열의 결과 값에 해당하는 위치에 있는 태그에 스타일을 적용

#### 예제 5-9 : 구조 선택자
- 코드 5-16 etc_structure.html
```html
<!DOCTYPE html>
<head>
    <title>CSS3 Selector Basic</title>
    <style>
        ul { overflow: hidden; }
        li {
            list-style: none;
            float: left; padding: 15px;
        }

        li:first-child { border-radius: 10px 0 0 10px; }______________| 처음, 마지막 태그에 둥근 테두리 적용
        li:last-child { border-radius: 0 10px 10px 0; }_______________|

        li:nth-child(2n) { background-color: #FF0003; }_______________| 홀수와 짝수 위치를 판별, 스타일 적용
        li:nth-child(2n+1) { background-color: #800000; }_____________| 홀수와 짝수 번째에 다른 색상 스타일 적용
    </style>
</head>
<body>
    <ul>
        <li>첫 번째</li>
        <li>두 번째</li>
        <li>세 번째</li>
        <li>네 번째</li>
        <li>다섯 번째</li>
        <li>여섯 번째</li>
        <li>일곱 번째</li>
    </ul>
</body>
```
- (주의사항) 코드 5-17 etc_structureFalse.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic Page</title>
        <style>____________________________________| 첫 번째 a 태그에 빨간색을 적용??
            li > a:first-child { color: red; }     |
        </style>___________________________________|
    </head>
    <body>
        <ul>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
        </ul>
    </body>
</html>
```
- 코드 5-18 etc_structureTrue.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic Page</title>
        <style>_____________________________________| 첫 번째 a태그에만 빨간색을 적용!!
            li:first-child > a { color: red; }      |
        </style>____________________________________|
    </head>
    <body>
        <ul>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
            <li><a href="#">주의 사항</a></li>
        </ul>
    </body>
</html>
```

### CSS3 단위

#### 키워드 단위
- 키워드는 W3C에서 미리 정의한 단어
- 키워드를 입력하면 해당하는 스타일이 자동으로 적용

#### 크기 단위
- 크기는 CSS3에서 가장 많이 사용하는 단위
  - %, em, cm, mm, inch, px
- 
| 단위 | 설명 |
|------|------|
| % | 백분율 단위 |
| em | 배수 단위 |
| px | 픽셀 단위 |

#### 예제 5-10 : 다양한 크기의 단위 적용
- 1. HTML 페이지 만들기
- 코드 5-19 CSS3Unit_basic.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Style Property Basic</title>
        <style>____________________________________| 줄마다 한 줄 띄우기
                                                   |
        </style>___________________________________|
    </head>
    <body>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </body>
</html>
```
- 2. % 단위 적용하기
  - % 단위는 기본으로 설정된 크기를 기준으로 상대적인 크기를 지정
  - 초기 설정 크기 : 100%
- 코드 5-20 CSS3Unit_percent.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Style Property Basic</title>
        <style>____________________________________| 
            p:nth-child(1) { }                     | 기본크기, 150%, 200% 크기로 설정
            p:nth-child(2) { font-size: 100%; }    |
            p:nth-child(3) { font-size: 150%; }    |
            p:nth-child(4) { font-size: 200%; }    |
        </style>___________________________________|
    </head>
    <body>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </body>
</html>
```
- 3. em 단위 적용하기
  - 1배 = 1em = 100%, 1.5배 = 1.5em = 150%
  - 초기 설정 크기 : 100%
- 코드 5-21 CSS3Unit_em.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Style Property Basic</title>
        <style>____________________________________| 
            p:nth-child(1) { }                     | 100%, 150%, 200% 대신,
            p:nth-child(2) { font-size: 1.0em; }   | 배수로 1em, 1.5em, 2.0em 사용
            p:nth-child(3) { font-size: 1.5em; }   |
            p:nth-child(4) { font-size: 2.0em; }   |
        </style>___________________________________|
    </head>
    <body>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </body>
</html>
```
- 4. px 단위 적용하기
  - 크기를 절대적으로 지정
- 코드 5-22 CSS3Unit_pixel.html
```
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Style Property Basic</title>
        <style>____________________________________| 
            p:nth-child(1) { }                     | px 단위는 크기를 절대적으로 지정함
            p:nth-child(2) { font-size: 16px; }    |
            p:nth-child(3) { font-size: 24px; }    |
            p:nth-child(4) { font-size: 32px; }    |
        </style>___________________________________|
    </head>
    <body>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </body>
</html>
```

#### 색상 단위
- 색상을 입력
  - 기본 : 영단어 입력
  - 단, 색상이 제한적
```text
[RGB 색상]

형태 : rgb(red, green, blue)
설명 : R(빨간색), G(초록색), B(파란색)를 조합해 색상을 표현하며, 0부터 255 사이의 숫자를 입력합니다.
예시 : <style>
            h1 { background-color: rgb(255, 255, 255); }
       </style>
------------------------------------------------------------------------------------------------
[RGBA 색상]

형태 : rgba(red, green, blue, alpha)
설명 : RGB 색상 단위에 알파 값을 추가한 형태입니다. 알파 값은 투명도를 나타내며,
       0.0부터 1.0사이의 숫자를 입력합니다. 0.0은 완전 투명 상태고 1.0은 완전 불투명 상태입니다.
예시 : <style>
            h1 { background-color: rgba(255, 255, 255, 0.5); }
       </style>
------------------------------------------------------------------------------------------------
[HEX 코드]

형태 : #000000
설명 : RGB 색상 단위를 짧게 입력하는 방법으로 RGB 색상 조합을 #000000같은 16진수로 입력합니다.
예시 : <style>
            h1 { background-color: #0094FF; }
       </style>
```
- 
| 단위 형태 | 설명 |
|-----------|------|
| #000000 | HEX 코드 단위 |
| rgb(red, green, blue) | RGB 색상 단위 |
| rgba(red, green, blue, alpha) | RGBA 색상 단위 |
| hsl(hue, saturation, lightness) | HSL 색상 단위 |
| hsla(hue, saturation, lightness, alpha) | HSLA 색상 단위 |
- 색상 선택 도구, ColorPicker
  - https://colors-picker.com/
- HSB 색상표
  - 색인 색상, 채도, 명도를 의미
 
#### URL 단위
- 이미지나 글꼴 파일을 불러올 때 URL 단위 사용
- url('경로')

##### ✍️작성자: 박지안
##### 🗓️ 작업일: 2026-10-28
