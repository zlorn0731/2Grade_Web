# 연습문제

## 1. 다음 문장에 O X로 답하시오.
- (1) h1 태그가 가장 큰 제목 태그고, h6 태그가 가장 작은 제목 태그입니다. (O)
- (2) a 태그의 링크를 지정할 때는 link 속성을 사용합니다. (X)
- (3) 목록은 ul 태그와 ol 태그 내부에 li 태그를 넣어서 만듭니다. (X)
- (4) 목록 내부에 목록을 중첩할 수도 있습니다. (O)
- (5) th 태그와 td 태그의 rowspan 속성과 colspan 속성을 사용하면 마이크로소프트 워드 등 스프레드시트에 있는 셀 병합 기능처럼 테이블의 셀을 병합할 수 있습니다. (O)
- (6) img 태그, audio 태그, video 태그는 모두 텍스트 등 내용물을 가질 수 없습니다. (X)
- (7) audio 태그, video 태그에 controls 속성을 지정할 때 표시되는 재생 제어 버튼들은 모든 웹 브라우저에서 모양과 형태가 같습니다. (X)

## 2. 다음 중 링크를 생성할 때 사용하는 태그는?
- (1) href 태그
- (2) link 태그
- (3) a 태그 O
- (4) url 태그

## 3. 다음 중 목록 생성과 관련 없는 태그는?
- (1) li 태그
- (2) ol 태그
- (3) ul 태그
- (4) list 태그 O

## 4. 다음 중 이미지를 삽입할 때 사용하는 태그는?
- (1) media 태그
- (2) picture 태그
- (3) graphics 태그
- (4) img 태그 O

## 5. 다음 중 이미지의 대체 문자를 지정할 때 사용하는 속성은?
- (1) text
- (2) alter
- (3) alt O
- (4) imgtxt

## 6. 다음 중 a 태그로 빈 링크를 만들 때, href 속성에 일반적으로 사용되는 기호는?
- (1) # O
- (2) @
- (3) *
- (4) +

## 7. 다음 중 HTML5 표준에 없는 태그는?
- (1) table
- (2) tfoot
- (3) thead
- (4) tcontent O
 
## 8. 다음 중 HTML 표준에 없는 태그는?
- (1) big O
- (2) small
- (3) b
- (4) i

## 9. 다음 중 audio 태그와 video 태그 내부에 넣어 웹 브라우저가 재생할 수 있는 파일 확장자 관련 문제를 해결할 때 사용하는 태그는?
- (1) src
- (2) source O
- (3) content
- (4) media

## 10. 클릭하면 다음 링크로 이동하는 a 태그를 작성하시오.
- (1) 한빛아카데미 웹 사이트(http://www.hanbit.co.kr)
- (2) 네이버 메인 페이지(http://www.naver.com)
- (3) 구글 메인 페이지(http://www.google.com)
- (4) 자신의 대학 웹 사이트(https://www.sungkyul.ac.kr)
```html
(1) - <a href="#">http://www.hanbit.co.kr</a>
(2) - <a href="#">http://www.naver.com</a>
(3) - <a href="#">http://www.google.com</a>
(4) - <a href="#">https://www.sungkyul.ac.kr</a>
```

## 11. 다음과 같이 폴더를 구성했을 때, 이미지를 클릭하면 한빛아카데미 웹 사이트(http://www.hanbit.co.kr)로 이동하도록 태그를 작성하시오
```html
<a href="http://www.hanbit.co.kr"><img src="hanbit_logo.jpg" alt="한빛아카데미"></a>
```

## 12. 다음 과 같은 웹 페이지를 생성하시오.
```html
<!DOCTYPE html>
<html>
    <head>
        <title>제목</title>
    </head>
    <body>
        <h1>HTML5 Basic</h1>
        <h2>ITCookbook - HanbitAcademy</h2>
        <hr>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.,,,,,</p>
    </body>
</html>
```

## 13. 다음 목록을 생성하시오.
```text
. 따뜻한 음료
    1. 커피
    2. 녹차
    3. 둥글레차
. 차가운 음료
    1. 커피
    2. 스무디
    3. 식혜
```
```html
<!DOCTYPE html>
<html>
    <ul>
        <li>따뜻한 음료</li>
        <ol>
            <li>커피</li>
            <li>녹차</li>
            <li>둥굴레차</li>
        </ol>
        <li>차가운 음료</li>
        <ol>
            <li>커피</li>
            <li>스무디</li>
            <li>식혜</li>
        </ol>
    </ul>
</html>
```

## 14. 다음 표를 생성하시오.
```html
<!DOCTYPE html>
<html>
    <table border="1">
        <tr>
            <th colspan="6">한국의 차</th>
        </tr>
        <tr>
            <th rowspan="6">뿌리차</th>
            <td>인삼차</td>
            <th rowspan="9">과일차</th>
            <td>수정과</td>
            <th rowspan="5">잎차</th>
            <td>뽕잎차</td>
        </tr>
        <tr>
            <td>당귀차</td>
            <td>유자차</td>
            <td>감잎차</td>
        </tr>
        <tr>
            <td>생강차</td>
            <td>구기자차</td>
            <td>솔잎차</td>
        </tr>
        <tr>
            <td>칡차</td>
            <td>대추차</td>
            <td>국화차</td>
        </tr>
        <tr>
            <td>둥굴레차</td>
            <td>오미자차</td>
            <td>이슬차</td>
        </tr>
        <tr>
            <td>마차</td>
            <td>매실차</td>
            <th rowspan="4">기타</th>
            <td>두충차</td>
        </tr>
        <tr>
            <th rowspan="3">곡물차</th>
            <td>보리차</td>
            <td>모과차</td>
            <td>영지버섯차</td>
        </tr>
        <tr>
            <td>옥수수차</td>
            <td>산수유차</td>
            <td>귤강차</td>
        </tr>
        <tr>
            <td>현미차</td>
            <td>탱자차</td>
            <td>쌍화차</td>
        </tr>
    </table>
</html>
```