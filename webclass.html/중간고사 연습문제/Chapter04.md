# 연습문제

## 1. 다음 문장에 O X를 표시하시오.
- (1) "http://www.google.com/search?q=초콜릿"처럼 데이터를 넣은 것은 POST 방식의 요청입니다. (X)
- (2) label 태그의 for 속성에 "입력 양식 태그의 id 속성"을 넣으면, label 태그를 선택했을 때 입력 양식에 포커스가 갑니다. (O)
- (3) select 태그 내부에 opt 태그를 넣어서 선택할 수 있는 요소를 만듭니다. (X)
- (4) 현대 웹 페이지의 레이아웃을 구성할 때는 테이블을 사용합니다. (X)
- (5) a 태그와 i 태그 등 텍스트는 블록 형식의 태그입니다. (X)
- (6) 모든 검색 엔진은 웹 페이지에 적용된 스타일을 시각적으로 분석하고 의미를 파악합니다. (X)
- (7) 시맨틱 태그는 시맨틱 웹을 구현할 때 사용하는 방법입니다. (O)

## 2. 다음 중 HTML5 표준에 새롭게 도입된 시맨틱 태그는?
- (1) div 태그
- (2) span 태그
- (3) article 태그 O
- (4) em 태그

## 3. 다음 중 HTML5 표준에 새롭게 도입된 시맨틱 태그가 아닌 것은?
- (1) head 태그 O
- (2) nav 태그
- (3) aside 태그
- (4) footer 태그

## 4. 사용자로부터 데이터를 입력받을 때 사용하는 태그는?
- (1) input 태그 O
- (2) data 태그
- (3) field 태그
- (4) collect 태그

## 5. HTML 입력 양식 중에서 여러 개의 선택지 중 하나를 선택하는 종류는?
- (1) text
- (2) checkbox
- (3) radio O
- (4) button

## 6. select 태그 내부에서 각 항목을 만드는 데 사용하는 태그는?
- (1) li 태그
- (2) option 태그 O
- (3) item 태그
- (4) opt 태그

## 7. 다음 중에서 인라인 형식의 태그는?
- (1) h1 태그
- (2) div 태그
- (3) span 태그 O
- (4) p 태그

## 8. form 태그의 method 속성을 GET과 POST로 입력할 때, 버튼을 클릭해 서버로 데이터를 전송한 후 웹 브라우저의 주소 창에 나타나는 URL 변화를 적으시오.
```text
GET : 주소 뒤에 ?이름=값 형태로 데이터가 붙음
POST : 데이터가 요청 본문에 담겨 전송돼서 주소에 표시되지 않음
```

## 9. 다음 입력 양식을 만드시오.
- [Hint] table 태그, th 태그, td 태그로 구조를 잡고, 내부에 글자와 input 태그를 넣습니다.
```html
<form>
    <table>
        <tr>
            <th><label for="id">아이디</label></th>
            <td><input type="text" name="id"></td>
        </tr>
        <tr>
            <th><label for="password">비밀번호</label></th>
            <td><input type="text" name="password"></td>
        </tr>
        <tr>
            <td></td>
            <td><input type="submit" name="제출"></td>
        </tr>
    </table>
</form>
```

## 10. 다음 입력 양식을 만드시오.
```html
<form>
    <b>시작 그룹</b><br>
    <label>
        <input type="radio" name="new" value="new">
        새 탭 페이지 열기
    </label><br>
    <label>
        <input type="radio" name="continue" value="continue">
        중단한 위치에서 계속하기
    </label><br>
    <label>
        <input type="radio" name="zip" value="zip">
        특정 페이지 또는 페이지 모음 열기
    </label><br><br>

    <b>개인정보 및 보안</b><br>
    <label>
        <input type="checkbox" name="service" value="service">
        동기화 및 서비스
    </label><br>
    <label>
        <input type="checkbox" name="login" value="login">
        로그인 허용
    </label><br>
    <label>
        <input type="checkbox" name="payload" value="payload">
        페이지 미리 로드
    </label>
</form>
```

## 11. 다음 입력 양식을 만드시오.
```html
<form>
    <table>
        <h1>글 작성하기</h1><br>
        <tr>
            <th><label for="writer">작성자</label></th>
            <td><input type="text" name="writer"></td>
        </tr>
        <tr>
            <th><label for="id">아이디</label></th>
            <td><input type="text" name="id"></td>
        </tr>
        <tr>
            <th><label for="email">이메일</label></th>
            <td><input type="text" name="email">@<input type="text" name="email"></td>
        </tr>
        <tr>
            <th><label for="phone">휴대폰</label></th>
            <td>
                <select id="phone" name="first_phone">
                    <option>010</option>
                    <option>031</option>
                    <option>02</option>
                    <option>011</option>
                </select>-<input type="text" name="second_number">
                -<input type="text" name="last_number">
            </td>
        </tr>
        <tr>
            <th><label for="story">내용</label></th>
            <td><textarea type="content" name="story" rows="10" cols="30"></textarea></td>
        </tr>
        <tr>
            <td></td>
            <td><input type="submit" name="제출"></td>
        </tr>
    </table>
</form>
```