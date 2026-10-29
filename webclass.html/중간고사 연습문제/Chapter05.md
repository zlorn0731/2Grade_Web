# 연습문제

## 1. 관련 있는 것끼리 연결하시오.
- (1) 기본 선택자
```text
(1) 전체 선택자   .               . (a) .header
(2) 태그 선택자   .               . (b) #id
(3) 아이디 선택자 .               . (c) *
(4) 클래스 선택자 .               . (d) h1
```
```text
[답]
(1) - (c)
(2) - (d)
(3) - (b)
(4) - (a)
```
- (2) 자손 선택자와 후손 선택자
```text
(1) 선택자A > 선택자B .             . (a) 자손 선택자
(2) 선택자A 선택자B   .             . (b) 후손 선택자
```
```text
[답]
(1) - (a)
(2) - (b)
```

## 2. 다음 문장에 O X를 표시하시오.
- (1) 자손은 후손보다 넓은 개념입니다. (X)
- (2) div > h1, h2는 div 태그 아래의 h1 태그와 h2 태그를 선택하는 선택자입니다. (X)
- (3) CSS도 HTML처럼 <!--주석--> 형태로 주석을 사용합니다. (X)
- (4) 2em은 2배를 나타내는 크기 단위입니다. (O)
- (5) 색상 단위에서 투명도를 지정할 때는 argb() 등을 사용합니다. (X)
- (6) URL을 지정할 때는 url() 형태의 코드를 사용합니다. (O)

## 3. 특정 클래스에 스타일을 적용할 때 사용하는 선택자는?
- (1) #classname
- (2) .classname O
- (3) classname
- (4) *classname

## 4. id가 'header'인 요소에만 스타일을 적용할 때 사용하는 선택자는?
- (1) #header O
- (2) .header
- (3) header
- (4) *header

## 5. 직접적인 자식 요소만을 대상으로 하는 선택자는?
- (1) parent child
- (2) parent > child O
- (3) parent.child
- (4) parent + child

## 6. 모든 요소에 스타일을 적용할 때 사용하는 선택자는?
- (1) * O
- (2) all
- (3) every
- (4) total

## 7. 다음 중에서 CSS에서 사용할 수 없는 크기 단위는?
- (1) cm
- (2) m O
- (3) em
- (4) px

## 8. 다음 코드에서 선택자가 어떤 태그를 선택하는지 설명하시오.
- (1) header a
- (2) header > * > h1
- (3) header > div:first-child > a
- (4) header a:first-child
- (5) div > h1, h2
- (6) .title.card
```text
(1) - header 안에 있는 모든 a
(2) - header 바로 아래 요소들에서 그 바로 아래에 있는 h1
(3) - header의 첫 자식이 div일 때, 그 div 바로 아래 a
(4) - header의 첫 자식인 a
(5) - div 바로 아래의 h1과 페이지의 모든 h2
(6) - title과 card 클래스 둘 다 가진 요소
```

## 9. 다음 HTML 구조에서 음영으로 표시된 태그를 선택할 수 있는 선택자를 3개 이상 만드시오.
```html
<body>
    <table>
        <tr class="head">
            // <td class="head-item">Lorem</td> //
            // <td class="head-item">Ipsum</td> //
        </tr>
        <tr>
            <td>Dolor</td>
            <td>Amet</td>
        </tr>
    </table>
</body>
```
```text
[답]

.head-item
td.head-item
tr.head > td
```

## 10. 다음 코드에서 선택자가 어떤 태그를 선택하는지 적으시오.
```html
<body>
    <header>
        <hgroup>
            <h1><a href="#">Header</a></h1>
        </hgroup>
        <nav>
            <div><a href="#">Item</a></div>
            <div><a href="#">Item</a></div>
            <div><a href="#">Item</a></div>
        </nav>
    </header>
</body>
```
```text
- 선택자 1번 : header a
- 선택자 2번 : header > * > h1
- 선택자 3번 : header > * > *:first-child > a
- 선택자 4번 : header a:first-child

[답]

선택자 1번 : Header a 1개 + Item a 3개 = 총 4개의 a
선택자 2번 : Header a 1개 = 총 1개의 a
선택자 3번 : Header 첫 a 1개 + Item 첫 a 1개 = 총 2개의 a
선택자 4번 : 모든 a = 총 4개의 a
```

## 11. 다음 HTML 구조에서 음영으로 표시된 태그를 선택할 수 있는 선택자를 3개 이상 만드시오.
```html
<body>
    <h1>CSS3 Basic</h1>
    <ul>
        // <li id="first" class="active">CSS3 Selector</li> //
        <li>CSS3 Property</li>
        <li>CSS3 Skill</li>
    </ul>
</body>
```
```text
[답]

#first
.active
li.active
```

## 12. 다음 코드의 실행 결과를 예측하시오
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Selector Basic</title>
        <style>
            li > a:first-child { color: red; }
        </style>
    </head>
    <body>
        <ul>
            <li><a href="#">a 태그</a></li>
            <li><a href="#">a 태그</a></li>
            <li><a href="#">a 태그</a></li>
            <li><a href="#">a 태그</a></li>
            <li><a href="#">a 태그</a></li>
        </ul>
    </body>
</html>
```
```text
[답]

다섯 개의 a 태그 모두 빨간색으로 출력
```