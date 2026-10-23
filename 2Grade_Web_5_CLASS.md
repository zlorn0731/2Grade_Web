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
pg13 부터
