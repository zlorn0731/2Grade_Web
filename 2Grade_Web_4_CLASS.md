# 👨‍💻웹 표준 기술

## HTML5 입력양식 태그와 구조화 태그
- 입력 양식 태그
- HTML5 문서 구조화

### 입력 양식 태그

#### 입력 양식
- 사용자에게 정보를 입력 받는 요소
  - (예) 간단한 회원가입 양식
 
#### 입력 양식 개요
- <form> 태그 : 영역 생성
  - (예) 입력 양식 생성 코드와 실행 결과
  ```
  <body>
    <form>
      <input type="text" name="search">
      <input type="submit">
    </form>
  </body>
  ```
- <form> 태그는 method속성 '방식'으로 action속성 '장소'에 데이터 전달
```
<form action="전송 위치" method="전송 방식">
                  |                   |___________ GET : 주소에 데이터를 직접 입력해 전달
<form/>           |                                POST : 별도의 방법을 사용해 데이터를 해당 주소로 전달
                  |_______________ 데이터를 전달할 목적지
```

#### 데이터 전달 방식
- <form> 태그의 method 속성
  - GET 방식 : 주소에 데이터를 입력해서 전달, 크기가 한정됨
  - POST 방식 : 주소 변경 없이 비밀스럽게 데이터 전달, 용량 제한 없음
```
[예시 : 입력 양식을 사용한 데이터 요청 코드]

<!-- GET 전송 방식-->
<body>
  <form method="get">
    <input type="text" name="search">
    <input type="submit">
  <form/>
</body>

<!-- POST 전송 방식-->
<body>
  <form method="post">
    <input type="text" name="search">
    <input type="submit">
  </form>
</body>
```

#### 데이터 전달 방식
- <form>태그는 method 속성 : GET 방식
  - (1) 입력 양식에 "rint" 값 입력
  - (2) 제출 버튼 클릭
- <form>태그는 method 속성 : POST 방식
  - (1) 입력 양식에 "rint" 값 입력
  - (2) 제출 버튼 클릭

#### 입력 양식 종류
- 입력 양식 태그
- 
| 태그 | 속성 | 모양 | 설명 |
|------|------|-----|-------|
| form |   | 보이지 않음 | 입력 양식의 시작과 끝 표시 |
| input | text | [text    ] | 글자 입력 양식 생성 |
| input | button | [button] | 버튼 생성 |
| input | checkbox | [✔️] | 체크박스 생성 |
| input | file | [파일 선택] | 파일 입력 양식 생성 |
| input | hidden | 보이지 않음 | 해당 내용 표시 안 함 | 
| input | image | [  100 x 100  ] | 이미지 형태 생성 |
| input | password | [.......     ] | 이미지 형태 생성 |
| input | radio | 🔘 | 라디오 버튼 생성 |
| input | reset | [reset] | 초기화 버튼 생성 |
| input | submit | [submit] | 제출 버튼 생성 |

- 입력 양식 태그
- 
| 태그 | 속성 | 모양 | 설명 |
|------|------|-----|-------|
| textarea | clos/rows | [textarea         ] | 여러 행의 글자 입력 양식 생성, cols는 너비를 지정 rows는 높이를 지정 |
| select, optgroup, option |   | [Mulitimedia Tag ✔️] | 선택 양식 생성, 옵션 그룹화, 옵션 생성 |
| fieldset, legend |   | [입력 양식    ] | 입력 양식의 그룹 지정, 입력 양식 그룹의 이름 지정 |

#### 예제 4-1 : 기본 입력 양식 태그
- <input>태그의 type 속성을 이용해 다양한 기본 입력 양식 생성
- (코드 4-1) form_basic.html
```
<body>
  <form>
    <!-- 사용자가 입력하는 입력 양식 -->
    <input type="text" name="text" value="text" /><br />
    <input type="password" name="password" value="password" /><br />
    <intput type="file" name="file" value="file" /><br />
    <input type="radio" name="radio" value="radio" /><br />

    <!-- 보이지 않는 입력 양식 -->
    <input type="hidden" name="hidden" value="hidden" /><br />

    <!-- 버튼 -->
    <input type="button" value="button" /><br />
    <input type="reset" value="reset" /><br />
    <input type="submit" value="submit" /><br />
    <input type="image" src="https://placehold.co/100x100" />
  </form>
</body>
```

#### 참고 : HTNL input value 속성의 3가지 특징
- 미리보기, 버튼이름, 데이터 제출 기능
  - text, password 속성에서 초기 미리보기 글자를 설정
  ```
  <input type="text" value="아이디를 입력하세요.">
  <input type="password" value="비밀번호를 입력하세요.">
  ```
  - button, submit 속성의 버튼 이름을 지정
  ```
  <input type="submit" value="하하">
  <input type="button" value="하하">
  <input type="reset" value="ㅋㅋ">
  ```
  - checkbox, radio 속성에서 서버에 텍스트를 전달할 때 사용
  ```
  <label><input type="radio" value="red">apple</label>
  <br>
  <label><input type="checkbox" value="green">melon</label>
  ```

#### 참고 : label 태그
- label 태그의 for 속성에 input 태그의 id 속성을 입력해 input 태그 설명
- for 속성을 연결하면, label 태그를 클릭했을 때 input 태그에 포커스가 감
```
<form>
  <label for="name">이름</label>
  <input id="name" type="text">
  ...(생략)...
</form
```

#### 예제 4-2 : 간단한 입력 양식 생성
- 라디오 버튼의 name 속성을 이용해 여러 대상 중 하나만 선택하는 형태
- (코드 4-2) form_radio.html
```
<body>
  <form>
    <table>
      <tr>
        <td><label for="username">이름</label></td>
        <td><input id="username" type="text" name="username" /></td>
      </tr>
      <tr>
        <td>성별</td>
        <td>
          <input id="nam" type="radio" name="gender" value="m" />________| Input 태그와 label태그
          <label for="man">남자</label>___________________________________|
          <input id="woman" type="radio" name="gender" value="m" />
          <label for="woman">여자</label>
        </td>
      </tr>
    </table>
    <input type="submit" value="가입" />
  </form>
</body>
```

#### 예제 4-3 : 선택 가능한 입력 양식
- 1. 한 항목만 선택하기 : <select> 태그 이용
     - 목록으로 보여 주는 항목 중 하나 또는 여러 개를 선택할 때 사용
     - 기본적으로 하나만 선택가능
     - <optgroup>, <option> 태그와 함께 사용하면 선택요소 생성
- (코드 4-4) form_selectBasic.html
```
<body>
  <select>
    <option>김밥</option>
    <option>떡볶이</option>
    <option>순대</option>
    <option>어묵</option>
  </select>
</body>
```
- 2. 여러 항목 선택하기 : <select> 태그의 multiple 속성 사용
- (코드 4-5) form_selectMulti.html
```
<body>
  <select multiple="multiple">
    <option>김밥</option>
    <option>떡볶이</option>
    <option>순대</option>
    <option>어묵</option>
  </select>
</body>
```
- 3. 선택 옵션 묶기 : <optgroup> 태그 사용
- (코드 4-6) form_selectGroup.html
```
<body>
  <select>
      <optgroup label="HTML5">
        <option>Multimedia Tag</option>
        <option>Connectivity</option>
        <option>Device Access</option>
      </optgroup>
      <optgroup label="CSS3">
        <option>Animation</option>
        <option>3D Transform</option>
      </optgroup>
  </select>
</body>
```

#### 예제 4-4 : 연관 있는 입력 양식 그룹으로 묶기
- <fieldset> 태그, <legend> 태그
- (코드 4-4) form_group.html
```
<body>
  <form>
    <fieldset>
      <legend>입력 양식</legend>
      <table>
        <tr>
          <td><label for="name">이름</label></td>
          <td><input id="name" type="text" /></td>
        </tr>
        <tr>
          <td><label for="mail">이메일</label></td>
          <td><input id="mail" typ="email" /></td>
        </tr>
      </table>
      <input type="submit" />
    </fieldset>
  </form>
</body>
```

#### 참고 : textarea 태그 주의 사항
- textarea 태그 내 들여쓰기가 입력 양식 내부에 출력되므로 주의
```
<body>
  <textarea>
    Textarea 태그
    Textarea 태그
  </textarea>
</body>

잘못된 형태

[    Textarea 태그    ]
[    Textarea 태그    ]
```
```
<body>
  <textarea>Textarea 태그
  Textarea 태그</textarea>
</body>

올바른 형태

[Textarea 태그        ]
[Textarea 태그        ]
```

### HTML5 문서 구조화

#### 공간 분할 태그
- CSS로 원하는 레이아웃을 구성하기 위해 공간 분할
  - (예) 쿠팡 메인 페이지의 div 태그 (http://www.coupang.com)
 
#### HTML5의 대표적인 공간 분할 태그
- 기본 공간 분할 태그
  - <div> 태그
    - 블록(block) 형식, 각 태그가 한 행을 전체를 차지함
  - <span> 태그
    - 인라인(inline) 형식, 각 태그가 자신의 글자 크기만큼 영역을 차지(왼쪽에서 오른쪽으로 쌓임)
- 
| 태그 | 설명 |
|------|------|
| div | 블록 형식으로 공간 분할 |
| span | 인라인 형식으로 공간 분할 |

#### 예제 4-5 : 공간 분할 방법
- 1. 공간을 블록 형식으로 분할하기
- (코드 4-9) space_block.html
```
<body>
  <div>div 태그 - block 형식</div>
  <div>div 태그 - block 형식</div>
  <div>div 태그 - block 형식</div>
  <div>div 태그 - block 형식</div>  
  <div>div 태그 - block 형식</div>
</body>
```
- 2. 공간을 인라인 형식으로 분할하기
  - 자신의 글자 크기만큼 영역 차지
  - 왼쪽에서 오른쪽으로 쌓임
- (코드 4-10) space_inline.html
```
<body>
  <span>span 태그 - inline 형식</span>
  <span>span 태그 - inline 형식</span>
  <span>span 태그 - inline 형식</span>
  <span>span 태그 - inline 형식</span>
  <span>span 태그 - inline 형식</span>
</body>
```

#### 참고 : 블록 형식 태그와 인라인 형식 태그
- 블록 형식과 인라인 형식이 적용된 일반 태그
  - h1태그, p태그는 블록 형식으로 출력
  - a태그와 i태그는 인라인 형식으로 출력
- (예시) reference_otherDisplayTag.html
```
<!DOCTYPE html>
<head>
  <title>HTML Space Basic Page</title>
</head>
<body>
  <h1>h1 태그</h1>
  <p>p 태그</p>
  <hr>
  <a href="#">a 태그</a>
  <i>i 태그</i>
</body>
</html>
```

#### 시맨틱 태그
- 시맨틱(semantic) 웹
  - 컴퓨터 프로그램이 코드를 읽고 의미를 인식할 수 있는 지능형 웹
    - semantic : '의미론적인'의 의미
    - 시맨틱 태그 : 웹 페이지의 태그에 의미를 부여하는 태그
- 시맨틱 태그를 사용한 시맨틱 웹 구현
  - HTML5의 시맨틱 태그
- 
| 태그 | 설명 |
|------|------|
| (1)header | 머리말(페이지 제목, 페이지 소개) |
| (2) nav | 하이퍼링크들을 모아 둔 내비게이션 |
| (3) aside | 본문 흐름에 벗아나는 노트나 팁 |
| (4) section | 문서의 장이나 절에 해당하는 내용 |
| (5) article | 본문과 독립적인 콘텐츠 영역 |
| (6) footer | 꼬리말(저자나 저작권 정보) |
```
______________________________________________
|                   (1)<header>              |
|____________________________________________|
|                   (2)<nav                  |
|____________________________________________|
|         |      (4)<section>      |         |
|         |   ____[<article>]____  |         | 
| <aside> |   |   [<article>]   |  | <aside> |
|         |(5)|   [<article>]   |  |         |
|         |   |_________________|  |         |
|____________________________________________|
|                   (6)<footer>              |
|____________________________________________|
```

#### 예제 4-6 : 시맨틱 태그를 이용해 레이아웃 구성
- (코드 4-12) space_semanticLess.html
```
<body>
  <div>
    <h1>HTML5 기본</h1>
  </div>
  <div>
    <ul>
      <li><a href="#">메뉴 - 1</a></li>
      <li><a href="#">메뉴 - 2</a></li>
      <li><a href="#">메뉴 - 3</a></li>
    </ul>
  </div>
    <div>
      <h1>Lorem ipsum dolor sit amet</h1>
      <p>Lorem ipsum dolor sit amet...</p>
    </div>
    <div>
      <h1>Lorem ipsum dolor sit amet</h1>
      <p>Lorem ipsum dolor sit amet...</p>
    </div>
  </div>
  <div>
      <span>서울특별시 강서구 내발산동</span>
  </div>
</body>

div 태그를 사용한 웹 페이지의 레이아웃 구성
```
- (코드 4-13) space_semantic.html
```
<body>
  <header>
    <h1>HTML5 기본</h1>
  </header>
  <nav>
    <ul>
      <li><a href="#">메뉴 - 1</a></li>
      <li><a href="#">메뉴 - 2</a></li>
      <li><a href="#">메뉴 - 3</a></li>
    </ul>
  </nav>
  <section>
    <article>
      <h1>Lorem ipsum dolor sit amet</h1>
      <p>Lorem ipsum dolor sit amet...</p>
    </article>
    <article>
      <h1>Lorem ipsum dolor sit amet</h1>
      <p>Lorem ipsum dolor sit amet...</p>
    </article>
  </section>
  <footer>
    <address>서울특별시 강서구 내발산동</address>
  </footer>
</body>

시맨틱 태그를 사용한 웹 페이지의 레이아웃 구성
```

##### ✍️작성자: 박지안
##### 🗓️ 작업일: 2026-10-17
