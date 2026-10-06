# 👨‍💻웹 표준 기술

## 4장 HTML5 기본 태그
- 글자 태그
- 목록 태그
- 테이블 태그
- 미디어 태그

### 글자 태그
- 글자 태그는 페이지에서 가장 큰 비중을 차지

#### 제목과 본문 글자 태그
- 제목 글자 태그
  - 문서의 제목을 표현할 때 사용
  - h는 heading(제목)을 의미
- 본문 글자 태그
  - p는 paragraph(단락)
  - br은 break(줄 바꿈)
  - hr은 horizontal rule(수평 줄)을 의미
- 
| 태그 | - | 설명 |
|------|---|------|
| 제목 글자 | h1 | 첫 번째로 큰 제목 글자 생성 |
| 제목 글자 | h2 | 두 번째로 큰 제목 글자 생성 |
| 제목 글자 | h3 | 세 번째로 큰 제목 글자 생성 | 
| 제목 글자 | h4 | 네 번째로 큰 제목 글자 생성 |
| 제목 글자 | h5 | 다섯 번째로 큰 제목 글자 생성 |
| 제목 글자 | h6 | 여섯 번째로 큰 제목 글자 생성 |
| 본문 글자 | p | 본문 문단 생성 |
| 본문 글자 | br | 줄 바꿈 |
| 본문 글자 | hr | 수평 줄 삽입 |

#### 예제 3-1 : 제목 표현
- 코드 3-1 : text_header.html
```
<!DOCTYPE html>
<html>
<head>
            <title>HTML TEXT Basic Page</title>
</head>
<body>
            <hl>제목 글자 태그 1</hl>
            <h2>제목 글자 태그 2</h2>
            <h3>제목 글자 태그 3</h3>
            <h4>제목 글자 태그 4</h4>
            <h5>제목 글자 태그 5</h5>
            <h6>제목 글자 태그 6</h6>
</body>
</html>
```

#### 예제 3-2 : 본문 단락 구분
- 코드 3-2 : text_paragraph.html
```
<!DOCTYPE html>
<html>
<head>
        <title>HTML NEXT Basic Page</title>
</head>
<body>
        <h1>제목 글자</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Phasellus eros nunc, aliquam nec faucibus vel, rutrum eu neque.</p>
</body>
</html>
```

#### 예제 3-3 : 제목과 본문 태그의 활용
- 코드 3-3 : text_content.html
```
<!DOCTYPE html>
<html>
<head>
            <title>HTML5+CSS3 Text</title>
</head>
<body>
            <h1>홍차</h1>________________________________________________________________________________________________________________________________________________________|
            <hr />                                                                                                                                                               | 
            <h2>정의</h2>                                                                                                                                                        |
            <p>홍차는 백차, 녹차, 우롱차보다 더 많이 발효된 차의 일종이다. 동양에서는 찻물의 빛이 붉기 때문에 홍차라고 부르지만, 서양에서는 찻잎의 색깔 때문에 'black tea'라고 부른다. </p>   |
            <br />                                                                                                                                                               |
            <h2>등급</h2>                                                                                                                                                         |
            <p>홍차는 여러 가지로 등급이 매겨진다. 일반적으로 찻잎의 모양에 따른 등급과 가공 상태에 따른 등급을 조합하여 표시한다.</p>                                                     |   
            <p>- 브로콘 페코</p>                                                                                                                                                  |
            <p>- 브로콘 페코 수송</p>                                                                                                                                              |
            <p>- 브로콘 오렌지 페코 패닝</p>________________________________________________________________________________________________________________________________________|
</body>                                                                                          웹 표준에 따라 br태그는 다른 글자태그 내부에 삽입 가능하나 hr태그는 웹브라우저에 따라 불가함
</html>
```

#### (참고) 특수 문자 표기
- 공백, 괄호 등은 다음 특수 문자를 사용해 화면에 표시할 수 있음
  - 특수 문자 &nbsp; 는 공백을 출력
  - 그 외 &lt; (<), &gt; (>), &amp; (&), &le; (<=), &ge; (>=)을 사용
```
[예시]

<!DOCTYPE html>
<html>
<head>
        <title>HTML5+CSS3 Text</title>
</head>
<body>
        <h1>공백이 있는 글자</h1>
        <h1>공백이&nbsp;&nbsp;&nbsp;있는&nbsp;&nbsp;&nbsp;글자</h1>
</body>
</html>
``` 

#### 앵커 태그
- 하이퍼텍스트(HyperText)
  - 사용자의 선택에 따라 특정 정보로 이동할 수 있도록 조직된 문서
- a 태그(Anchor)
  - 다른 웹 페이지나 웹 페이지 내부의 특정 위치로 이동할 때 사용하는 태그
  - a 태그만으로는 이동하는 웹 페이지를 브라우저에게 알려줄 수 없어 href 사용
    - href(Hyper Reference)
- 
| 태그 | 설명 |
|------|------|
| a | 하이퍼링크 생성 |
```
<a href="http://www.hanbit.co.kr">한밫미디어</a>
           [이동할 웹 페이지]       [출력 글자]
```
- a 태그의 href 속성
  - (1) 절대 경로
    - http://naver.com - 네이버의 메인 페이지
    - /animal.jpg - 현재 웹 사이트 최상위 위치의 animal.jpg 파일
  - (2) 상대 경로
    - animal.jpg - 웹 페이지가 있는 폴더의 animal.jpg 파일
    - image/animal.jpg - 웹 페이지가 있는 폴더에 포함된 image폴더의 animal.jpg 파일
    - ../animal.jpg - 웹 페이지가 있는 폴더의 상위 폴더에 있는 animal.jpg 파일
  - (3) 아이디 경로
    - #name - id 속성이 name인 태그의 위치로 이동
  - (4) 메일 경로
    - maito : hanbit@hanbit.co.kr - 해당 주소로 메일 전송

#### 예제 3-4 : 하이퍼링크 설정
- 1. 특정 웹 페이지에 연결하기
  - 하이퍼링크를 설정한 글자를 클릭하면 해당 웹 페이지로 이동
- 코드 3-5 : text_anchor.html
```
<!DOCTYPE html>
<html>
<head>
        <title>HTML TEXT Basic</title>
</head>
<body>
        <a href="http://hanb.co.kr">한빛미디어</a><br />
        <a href="http://naver.com"/>네이버</a><br />
        <a href="http://daum.com/">다음</a><br />
</body>
</html>
```
- 2. 웹 페이지 내부에 연결하기
  - 하이퍼링크를 설정한 글자를 클릭하면 해당 웹 페이지로 이동
- 코드 3-6 : text_anchorlnner.html
```
<!DOCTYPE html>
<html>
<head>
        <title>HTML TEXT Basic</title>
</head>
<body>
        <a href="#alpha">Alpha 부분</a>
        <a href="#beta">Beta 부분</a>
        <a href="#gamma">Gamma 부분</a>
        <hr />
        <h1 id="alpha">Alpha</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <h1 id="beta">Beta</h1>
        <p>vivamus elementum dictum lobortis. Curabitur ut nunc turpis.</p>
        <h1 id="gamma">Gamma</h1>
        <p>Pharsellus eros nunc, aliquam nec faucibus vel, retrum eu neque.</p>
</body>
</html>
```

#### 글자 모양 태그
- 글자 모양 태그
  - 웹 페이지의 글자에 형태나 의미를 부여하는데 사용하는 태그
- 
| 태그 | 설명 |
|------|------|
| b | 굵은 글자 |
| i | 기울어진 글자 |
| small | 작은 글자 | 
| sub | 아래 첨자 | 
| sup | 위 첨자 | 
| ins | 밑줄 글자 |
| del | 취소선이 그어진 글자 |
- 글자 모양 태그 내부에 제목 글자 태그와 본문 글자 태그는 넣을 수 없음
  - (예시) : 웹 표준을 위반한 글자 모양 태그 사용
```
<i>
      <h1>웹 표준 위반</h1>
      <p>웹 표준 위반</p>
</i>
```

#### 예제 3-5 : 다양한 글자 모양
- 코드 3-7 : text_font.html
```
<!DOCTYPE html>
<html>
<head>
        <title>HTML TEXT Basic Page</title>
</head>
<body>
        <h1><b>Lorem ipsum dolor sit amet</b></h1>
        <h1><i>Lorem ipsum dolor sit amet</i><h1>
        <h1><small>Lorem ipsum dolor sit amet</small></h1>
        <h1>Lorem ipsum dolor <sub> sit amet</sub></h1>
        <h1>Lorem ipsum dolor <sup> sit amet</sup></h1>
        <h1><ins>Lorem ipsum dolor sit amet</ins></h1>
        <h1><del>Lorem ipsum dolor sit amet</del></h1>
        <hr />
        <b>Lorem ipsum dolor sit amet</b><br />
        <i>Lorem ipsum dolor sit amet</i><br />
        <small>Lorem ipsum dolor sit amet</small><br />
        Lorem ipsum dolor <sub> sit amet</sub><br />
        Lorem ipsum dolor <sup> sit amet</sup><br />
        <ins>Lorem ipsum dolor sit amet</ins><br />
        <del>Lorem ipsum dolor sit amet</del><br />
</body>
</html>
```

### 목록 태그

#### 내비게이션 메뉴
- 웹 사이트의 다른 웹 페이지로 이동할 수 있는 버튼
- 목록 태그
  - 내비게이션 메뉴를 만들기 위해 주로 사용되는 목록 태그
- 
| 태그 | 설명 |
|------|------|
| ul | 순서가 없는 목록 생성 |
| ol | 순서가 있는 목록 생성 |
| li | 목록 요소 생성 |

#### 예제 3-6 : 목록 태그 활용
- 1. 순서가 없는 기본(글머리 기호) 목록 만들기
- 코드 3-8 : list_unordered.html
```
<!DOCTYPE html>
<html>
<head>
          <title>HTML List Basic Page</title>
</head>
<body>
      <ul>
            <li>사과</li>
            <li>바나나</li>
            <li>오렌지</li>
       </ul>
</body>
</html>
````
- 2. 순서가 있는 목록 만들기
- 코드 3-9 : list_ordered.html
```
<!DOCTYPE html>
<html>
<head>
          <title>HTML List Basic Page</title>
</head>
<body>
        <ol>
              <li>사과</li>
              <li>바나나</li>
              <li>오렌지<li>
        </ol>
</body>
</html>
```
- 3. 중첩 목록 만들기
- 코드 3-10 : nested_list.html
```
<body>
    <ul>
        <!-- 첫 번째 목록 -->
        <li>
            <b>과일</b>____________________________ 첫 번째 목록 유형 항목
            <ol>
                <li>사과</li>
                <li>바나나</li>
                <li>오렌지</li>
            </ol>
        </li>
        <!-- 두 번째 목록 -->
        <li>
            <b>채소</b>____________________________ 두 번째 목록 유형 항목
            <ol>
                <li>상추</li>
                <li>치커리</li>
                <li>양배추</li>
            </ol>
        </li>
    </ul>
</body>
```

#### 테이블 태그
- 표를 만들 때는 테이블 태그
- 
| 태그 | 설명 |
|------|------|
| table | 표 삽입 |
| tr | 표에 행 삽입 |
| th | 표의 제목 셀 생성 | 
| td | 표의 일반 셀 생성 |

#### 예제 3-7 : 시간표 만들기
- 1. 표 만들기
- 코드 3-11 : table_basic.html
```
<body>
      <table>

      </table>
</body>
```
- 2. 표에 셀 추가하기
- 코드 3-12 : table_basic.html
```
<body>
        <table border="1">_________ border : 표 테두리 두께
              <thead>_________________________________________| 제목 행과 제목 셀 생성
                  <tr>                                        |
                      <th></th>                               |
                      <th>월</th>                             |
                      <th>화</th>                             |
                      <th>수</th>                             |   
                      <th>목</th>                             |   
                      <th>금</th>                             |
                  </tr>                                       |
                </thead>______________________________________|

            <tbody>_________________________________________________| 일반 행과 일반 셀 생성
                <tr>                                                |
                      <td>1교시</td>                                |
                      <td>영어</td>                                 |
                      <td>국어</td>                                 |
                      <td>과학</td>                                 | 
                      <td>미술</td>                                 |
                      <td>기술</td>                                 | 
                </tr>                                               |
                <tr>                                                | 
                      <td>2교시</td>                                |
                      <td>도덕</td>                                 |
                      <td>체육</td>                                 | 
                      <td>영어</td>                                 |   
                      <td>수학</td>                                 |
                      <td>사회</td>                                 |
                  </tr>                                             |
              </tbody>______________________________________________|
            </table>
</body>
```

#### 테이블 태그의 속성
- th와 td에 colspan과 rowspan 속성을 사용하여 표에서 셀이 차지하는 영역을 조절
- 
| 태그 | 속성 | 설명 |
|------|-----|-------|
| table | border | 표의 테두리 두께 지정 |
| th, td | colspan / rowspan | 셀의 너비 지정 / 셀의 높이 지정 |

#### 예제 3-8 : 행, 열 병합 표 생성
- colspan 속성과 rowspan 속성을 적용
- 코드 3-13 : table_span.html
```
<body>
  <table border="1">
        <tr>______________________________________| 1행 : 제목 행, 셀 2개 영역 차지
              <th colspan="2">지역별 홍차</th>     |
        </tr>_____________________________________|
        <tr>____________________________________________| 2행 : 제목 행, 행 3개 영역 차지
              <th rowspan="3">중국</th>                  |
              <td>정산소종</td>                          |
        </tr>                                            | 
        <tr><td>기문</td></tr>                           |  
        <tr><td>운남</td></tr>___________________________|
        <tr>____________________________________________________| 5행 : 제목 행, 행 4개 영역 차지
              <th rowspan="4">인도 및 스리랑카</th>              |
              <td>아삼</td>                                     | 
        </tr>                                                   |
        <tr><td>실론</td></tr>                                  |  
        <tr><td>다질링</td></tr>                                |
        <tr><td>닐기리</td></tr>________________________________|
  </table>
</body>
```

#### 미디어 태그
- 이미지, 오디오, 비디오 등 멀티미디어를 넣을 때 사용
  - 이미지 삽입 : img 태그 사용
  - 음악 삽입 : audio 태그 사용
  - 영상 삽입 : video 태그 사용
- 
| 내용물을 가질 수 있는 태그 | 내용물을 가질 수 없는 태그 |
|---------------------------|----------------------------|
| <audio></audio> / <video></video> | <img> |

#### 미디어 태그 속성 
- 이미지, 오디오, 비디오에 필요한 추가 정보는 속성을 사용
- 
| 태그 | 속성 | 설명 |
|------|-----|-------|
|   | src | 이미지의 경로 지정 |
| img 태그 | alt | 이미지가 없을 때 나오는 글자 지정 |
| <img> | width | 이미지의 너비 지정 |
|   | height | 이미지의 높이 지정 |
| audio 태그 | src | 음악, 비디오 파일의 경로 지정 |
| <audio></audio> | preload | 음악, 비디오를 준비 중일 때 데이터를 모두 불러올지 여부 지정 |
| video 태그 | autoplay | 음악, 비디오의 자동 재생 여부 지정 |
| <video></video> | loop | 음악, 비디오를 반복 여부 지정 |
|   | controls | 음악, 비디오 재생 도구 출력 여부 지정 |
| video | width | 비디오의 너비 지정 |
| <video></video> | height | 비디오의 높이 지정 |

#### 예제 3-9 : 멀티미디어(이미지, 오디오, 비디오) 삽입
- 1. 이미지 삽입하기
  - 이미지 파일 준비 : 준비 파일(이미지.jpg)을 HTML페이지와 같은 폴더에 넣기
  - 코드 3-14 : image_basic.html
```
<body>
      <img src="Penguins.jpg" alt="펭귄" width="300"/>_________________ 웹에 있는 이미지 경로를 넣어도 됨 | <img src="http://www.hanbit.co.kr/images/common/logo_hanbit.png">
                                    ↳ 이미지 파일 : Penguins.jpg / 대체 문구 : 펭귄 / 이미지 너비 : 300 pixel
      <img src="Nothing" alt="그림이 존재하지 않습니다." width="300"/>__________________ 이미지가 없으면 alt 속성에 지정한 글자가 표시됨
</body>
```
- 2. 음악 삽입하기
  - 음악 파일 준비 : 준비 파일(오디오.mp3)을 HTML페이지와 같은 폴더에 넣기
  - 코드 3-15 : audio_basic.html
```
<body>
        <audio src="Kalimba.mp3" controls="controls"></audio>
</body>
```
- 3. 웹 브라우저 제약이 없도록 음악 삽입하기
  - <source> 태그
  - 웹 브라우저마다 지원하는 음악 파일 확장자가 다른 문제 해결
  - <audio> 태그나 <video> 태그 내부에 입력
  - ogg파일 준비 : .ogg 확장자 파일을 HTML페이지와 같은 폴더에 넣기
  - 코드 3-16 : audio_source.html
```
<body>
        <audio controls="controls">____________________________________| type속성을 입력하지 않을 경우, 웹 브라우저가 음악파일 다운로드 후 재생가능 파일인지 확인하는
              <source src="Kalimba.mp3" type="audio/mp3" />            | 작업이 필요하므로 반드시 지정
              <source src="Kalimba.ogg" type="audio/ogg" />            |
        </audio>_______________________________________________________|
</body>
```
- 4. 동영상 삽입하기
  - 동영상 파일 준비 : 준비 파일(동영상.mp4, 동영상.webm)을 HTML페이지와 같은 폴더에 넣기
  - 코드 3-17 : video_basic.html
```
<body>
        <video width="640" controls="controls">
              <source src="wildlife.mp4" type="video/mp4" />
              <source src="wildlife.webm" type="video/webm" />
        </video>
</body>
```
- 5. 동영상을 불러오는 동안 다른 이미지 보여 주기
  - poster 속성
    - <video>태그의 속성
    - 동영상을 불러오는 동안 사용자에게 보여 줄 이미지를 지정
    - 이미지 경로 입력 넣기
  - 코드 3-18 : video_poster.html
```
<body>
        <video controls="controls" poster="https://placketittens.com/300/300">
              <source src="wildlife.mp4" type="video/mp4">
              <source src="wildlife.webm" type="video/webm">
        </video>
</body>
```

##### ✍️작성자: 박지안
##### 🐧실습 환경: Visual Studio Code
##### 🗓️ 작업일: 2026-10-06
