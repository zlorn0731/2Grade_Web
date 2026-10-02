# 👨‍💻웹 표준 기술

## 3장 웹 페이지 기본구조와 작성방법
- HTML5 기본 용어
- HTML5 페이지 구조와 작성법
- 오류와 검증

### HTML5 기본 용어

####  태그와 요소
- 요소(element)
  - HTML페이지를 구성하는 각 부품(제목, 본문, 이미지, 등)
- 태그(tag)
  - 요소를 만들 때 사용하는 작성 방법이며, 요소 생성과 태그 생성은 같은 의미
- 생성 방법에 따른 요소 구분
- 
| 요소 구분 | 형태 | 예시 |
|----------|-------|------|
| 내용을 가질 수 있는 요소 | <요소 이름>내용</요소 이름> | <hl>Hello HTML5</hl>, <p>즐거운 웹 프로그래밍 입문</p> |
| 내용을 가질 수 없는 요소 | <요소 이름> | <img>, <br>, <hr> |
- 내용을 가질 수 있는 요소 생성
```
<hl>Hello HTML5</hl>
  ↑시작 태그      ↑끝 태그
```
- 
| 내용 구분 | 예시 |
|-----------|------|
| 텍스트인 경우 | <h1>Hello HTML5</hl>, <p>즐거운 웹 프로그래밍 입문</p> |
| 다른 태그인 경우 | <div>  <hl>Hello HTML5</hl> <p>즐거운 웹 프로그래밍 입문</p>  </div> |
| 내용을 입력하지 않은 경우 | <dib></div>, <audio></audio>, <videa></video> | 
- 참고 : HTML 표기법과 XHTML 표기법
  - 내용을 가질 수 없는 요소의 2가지 표기법
    - HTML 표기법 사용
      - : <요소 이름>만으로 요소를 생성하므로 내용을 가질 수 있는 태그의 시작으로 오해
    - XML(extensible Markup Language) 작성방식을 적용한 XHTML표기법 사용
      - : 명확하게 내용을 가질 수 없는 태그임을 표기할 수 있음
- 
| HTML 표기법 | XHTML 표기법 |
|-------------|-------------|
| <img> | <img /> |
| <br> | <br /> |
| <hr> | <hr /> |

#### 속성
- 속성(attribute)
  - 태그에 추가 정보를 부여할 때 사용하는 것
```
[예시]
            ↓속성이름  ↓속성값
(a)    <hl title="header">Hello HTML5</hl>
        _____속성 블록____

            ↓속성이름  ↓속성값
(b)    <img src="image.png">
       _______속성 블록______

[설명]

(a) title = 속성 이름
(a) "header" = 속성 값
(a) <hl title = "header"> = 속성 블록

(b) src = 속성 이름
(b) "image.png" = 속성 값
(b) <img src="image.png"> = 속성 블록
(b) image.png = 출력할 이미지 정보
```

#### 주석
- 주석(comment)
  - 코드에 대한 설명 기록
```
[얘시]

<!-- 주석 -->

<!DOCTYPE html>
<html>
<head>
    <!-- title 태그 -->
    <title>TITLE</title>
</head>
<body>
    <!-- hl 태그 -->
    <hl>Hello HTML5</hl>
</body>
</html>
```

### HTML% 페이지 구조와 작성법

#### HTML 페이지의 구조
- HTML 구조와 예시
  - <!DOCTYPE html> : HTML5 문서 표기
  - <html> </html> : HTML 페이지 기본요소, 내부에 모든 태그 작성
  - <head> </head> : body태그에 필요한 스타일 시트, 자바스크립트 제공
  - <title> </title> : 웹 브라우저에 표시되는 제목 지정
  - <body> </body> : 사용자에게 실제 보이는 부분을 작성
```
<!DOCTYPE html>-------------------------→ (1) 웹 브라우저에 HTML5 문서라는 것을 알리기 위해 반드시 첫 행에 나와야 함
<html>
<head>----------------------------------→ (2) body 태그에 필요한 스타일시트와 자바스크립트를 제공
    <title>TITLE</title>----------------→ (3) 웹 브라우저에 표시하는 제목을 지정
</head>
<body>----------------------------------→ (4) 사용자에게 실제로 보이는 부분을 작성하는 곳

</body>
</html>---------------------------------→ (5) 모든 HTML 페이지의 기본 요소로, 모든 태그의 이 html 태그 내부에 작성
```
- <html> 태그의 lang 속성
  - 웹 페이지의 사용 언어를 구글 검색 엔진에 제공
  ```
  <html lang="ko">
  ```
- 
| lang 속성 값 | 언어 |
|--------------|------|
| ko | 한국어 |
| en | 영어 |
| ja | 일본어 |
| ru | 러시아어 |
| zh | 중국어 |
| de | 독일어 |
```
[예시]

<!DOCTYPE html>
<html lang="en-US">
```
- <head> 태그의 내부에 입력할 수 있는 태그
  - 아래 표에 지정된 태그만 입력 가능
- 
| 태그 | 설명 |
|------|------|
| meta | 웹 페이지에 추가 정보 전달 |
| title | 페이지 제목 지정 |
| script | 웹 페이지에 스크립트 추가 | 
| link | 웹 페이지에 다른 파일 추가 |
| style | 웹 페이지에 스타일시트 추가 |
| base | 웹 페이지의 기본 경로 지정 |

#### HTML5 페이지의 작성과 실행
- 1 : 새 파일 만들기
  - 비주얼 스튜디오 코드의 [파일]-[새 파일]
  - 또는 단축키 Ctrl + N 사용
  - 또는 Ctrl + Shift + Window + N
- 2 : 코드 작성 후 파일로 저장
  - 아래와 같은 샘플코드 작성
  - [파일]-[다른 이름으로 저장] // 예제작성용 폴더위치에 저장 (예시 : C:\수업)
  - OO.html 또는 OO.htm 형식으로 저장 (예시 : HTMLPage.html)
```
<!DOCTYPE html>
<html>
<head>
    <title>HTML5 Basic</title>
</head>
<body>
    <hl>Hello World..!</h1>
</body>
</html>

- 확장자 자동 설정 : 설정(Ctrl + ,) - [텍스트 편집기][파일]-"Default Language" 항목에 "html" 입력
```
- 3 : 실행
  - 저장한 html파일을 크롬으로 드래그 & 드롭하여 웹 페이지를 실행
    - 예제코드 정상작동 시 'Hello World..!'가 출력됨을 확인
   
#### 스타일시트 작성과 실행
- 내부 스타일
  - (HTML페이지 내부에서) style 태그를 사용해 스타일시트를 직접 입력하는 방법
  - 스타일시트가 짧은 경우 사용
- 외부 스타일
  - 스타일시트를 별도의 파일로 생성
  - (HTML페이지 내부에서)link 태그 href 속성을 사용해 스타일시트를 불러오는 방법
  - 협업 업무나 프로젝트의 규모가 클 경우 유용

#### 예제 2-1 : 내부 스타일시트 작성과 실행
- 코드 2-2 : HTMLPageWithStyle.html
```
<!DOCTYPE html>
<html>
<head>
    <title>HTML5 Basic</title>
    <style>________________________________________| head태그에 style태그 생성(h1 적용)
              hl {                                 |
                      color:white;                 |   
                      background:black;            |
              }                                    |
    </style>_______________________________________|  
</head>
<body>
    <hl>Hello World..!</h1>_________________________ body태그에 제목 지정 (텍스트 입력)
</body>
</html>
```

#### 예제 2-2 : 외부 스타일시트 작성과 실행
- 코드 2-3 : Style.css
```
hl {_____________________________| VS Code [파일]-[새 파일] style.css 파일 작성
        color:white;             | head태그에 들어갈 style태그 작성(hl 적용)
        background:black;        |
}________________________________|
```
- 코드 2-4 : HTMLPageWithLink.html
```
<!DOCTYPE html>
<html>
<head>
          <title>HTML5 Basic</title>
          <link rel="stylesheet" href="Style.css"/>_______________ link태그 사용해 외부 스타일시트(style.css)를 불러오도록 head태그에 지정
</head>                                                            (코드 2-2 변경하고 다른이름으로 저장)
<body>                                                          /
          <hl>Hello World..!</hl>______________________________/
</body>
</html>
```

#### 자바스크립트 작성과 실행
- 내부 자바스크립트
  - (HTML 페이지 내부에서) <script> 태그를 사용해 코드를 직접 작성하는 방법
- 외부 자바스크립트
  - 자바스크립트를 별도의 파일로 생성
  - <script> 태그의 src 속성에 파일 경로를 입력해 HTML 페이지로 불러옴

#### 예제 2-3 : 내부 자바스크립트 작성과 실행
- 코드 2-5 : HTMLPageWithScript.html
```
<!DOCTYPE html>
<html>
<head>
              <title>HTML5 Basic</title>
              <script>___________________________________________| Head 태그에 script 태그를 생성
                            // 경고창을 출력합니다.                | (경고창 출력하는 script)
                            alert('Hello JavaScript..!');        |
              </script>__________________________________________|
</head>
<body>
              <hl>Hello World..!</hl>
</body>
</html>
```

#### 예제 2-4 : 외부 자바스크립트 작성과 실행
- 코드 2-6 : OuterJavaScript.js
```
alert('OuterScript');_______________________ VS Code [파일]-[새 파일] OuterJavaScript.js 파일로 저장하고 다음 코드 작성
```
- 코드 2-7 : HTMLPageWithOuterScript.html
```
<!DOCTYPE html>
<html>
<head>
              <title>HTML5 Basic</title>______________________________| script 태그 사용해 외부 자바스크립트 (OuterJavaScript.js)를 불러오도록 지정
              <script src='OuterJavaScript.js'></script>______________| (코드 2-5 변경하고 다른이름으로 저장)
</head>
<body>
              <hl>Hello World..!</hl>
</body>
</html>
```

### 오류와 검증

#### 검사를 이용한 오류 확인
- 버그(Bug)
  - 프로그램이 원하지 않는 방향으로 동작하는 것
- 디버그(Debug)
  - 버그를 잡근(수정하는) 행위
- 웹 브라우저 검사 기능으로 디버그 수행
  - 크롬을 열고 [F12]
  - 웹 페이지에서 마우스 오른쪽 버튼 클릭해 [검사] 메뉴
- 검사 실행
- [Elements] 탭
  - 현재 HTML 페이지의 계층 구조와 각 태그에 적용된 스타일을 파악할 때 사용
- [Console] 탭
  - 오류를 확인하거나 자바스크립트 코드를 추가로 입력할 때 사용
- 검사 기능을 사용한 계층구조 확인
- 검사를 사용한 오류 확인 예시
  - 오류 발생 원인과 위치를 쉽게 파악할 수 있음
  ```
  ...
  <script>
              alert('Hello World..!');
  </script>
  ...
  ```

##### ✍️작성자: 박지안
##### 🐧실습 환경: Visual Studio Code 
##### 🗓️ 작업일: 2026-10-02
