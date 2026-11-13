# 👨‍💻웹 표준 기술

## CSS3 속성(1)
- 박스 속성
- 가시 속성
- 배경 속성

### 박스 속성

#### 박스 속성
- 박스 속성은 웹 페이지의 레이아웃을 구성할 때 가장 중요
- 
| 속성 | 설명 |
|------|------|
| margin 속성 | 테두리와 다른 태그 사이의 테두리 바깥쪽 여백 |
| border 속성 | 테두리 |
| padding 속성 | 테두리와 글자 사이의 테두리 안쪽 여백, 배경색은 padding 영역까지만 적용 |
| width 속성 | 글자를 감싸는 영역의 가로 크기 |
| height 속성 | 글자를 감싸는 영역의 세로 크기 |
  - Width와 height 속성
    - 글자를 감싸는 영역의 크기 지정
  - border 속성
    - 테두리 두께 지정
  - padding과 margin 속성
    - 테두리 안쪽과 바깥쪽 여백 지정

#### 예제 6-1 : 박스 크기와 패딩 조정
- 1. width와 height 속성 적용하기
- 코드 6-1 box_widthHeight.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            div { 
                width: 100px; height: 100px;
                background-color: red;
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```
- 2. margin과 padding 속성 적용하기
- 코드 6-2 box_marginPadding.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            div {
                width: 100px; height: 100px;
                background-color: red;

                border: 20px solid black;
                margin: 10px; padding: 30px;
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

#### 박스 크기와 여백
- 웹 브라우저에서 검사로 코드 분석
  - 웹 브라우저에서 검사로 코드 분석(width와 height 속성의 적용 범위 비교)
- 태그 전체의 크기 구하기
    - margin, border, padding 속성은 양쪽에 위치하므로 2를 곱함
  - 전체 너비 = width + 2 x (margin + border + padding)
  - 전체 높이 = height + 2 x (margin + border + padding)
- margin과 padding 속성은 두 가지 방법으로 상하좌우 각각 지정 가능
  - margin 속성과 padding 속성의 방향 적용
    - (left, right, top, bottom)
- 
| 속성 | 설명 |
|-------|-----|
| margin-left | 왼쪽 여백 |
| margin-right | 오른쪽 여백 |
| margin-top | 위쪽 여백 |
| margin-bottom | 아래쪽 여백 |
| padding-left | 왼쪽 패딩 |
| padding-right | 오른쪽 패딩 |
| padding-top | 위쪽 패딩 |
| padding-bottom | 아래쪽 패딩 |

#### 예제 6-2 : 박스 여백 부분 조정
- 1. 네 방향 속성 지정하기 : 순서대로 크기 단위 띄어쓰기
- 코드 6-3 box_marginPaddingEachFour.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            div {
                width: 100px; height: 100px;
                background-color: red;

                /* margin: 위 오른쪽 아래 왼쪽 */
                /* padding: 위 오른쪽 아래 왼쪽*/
                margin: 0 30px 0 30px;
                padding: 0 30px 0 30px;
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```
- 2. 두 방향씩 속성 지정하기 : 네 방향을 2개씩 묶어 지정
- 코드 6-4 box_marginPaddingEachTwo.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            div {
                width: 100px; height: 100px;
                background-color: red;

                /* margin: 위아래 왼쪽오른쪽 */
                /* padding: 위아래 왼쪽오른쪽 */
                maring: 0 30px; padding: 0 30px;
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

#### 박스 테두리
- 박스에 테두리를 넣을 때는 두께, 형태, 색상에 해당하는 속성을 사용
  - border-width 속성 : 테두리 두께
  - border-style 속성 : 테두리 형태
  - border-color 속성 : 테두리 색상
- border
  - border-width, border-style, border-color 속성을 한 번에 입력할 수도 있음
  ```html
  <style>
      .box {
            border: thick dashed black;
       }
  </style>
  ```
  - 상하좌우 속성을 각각 입력할 수 있음
  ```html
  .box {
        border-left:
  }
  ```

#### 예제 6-3 : 박스 여백 부분 조정
- 1. 기본 테두리 만들기
- 코드 6-5 border_basic.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            .box {
                border-width: thick;
                border-style: dashed;
                border-color: black;
            }
        </style>
    </head>
    <body>
        <div class="box">
            <h1>Lorem ipsum dolor amet</h1>
        </div>
    </body>
</html>
```
- 2. 둥근 테두리 만들기
- 코드 6-6 border_radius.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            .box {
                border-width: thick;
                border-style: dashed;
                border-color: black;

                border-radius: 20px;
            }
        </style>
    </head>
    <body>
        <div class="box">
            <h1>Lorem ipsum dolor amet</h1>
        </div>
    </body>
</html>
```
- 3. 모서리마다 둥글기를 다르게 적용하기
- 코드 6-7 border_radiusEach.html
```html
<head>
    <title>CSS3 Property Basic</title>
    <style>
        .box {
            border-width: thick;
            border-style: dashed;
            border-color: black;

            /* border-radius: 왼쪽위 오른쪽위 오른쪽아래 왼쪽아래 */
            border-radius: 50px 40px 20px 10px;
        }
    </style>
</head>
<body>
    <div class="box">
        <h1>Lorem ipsum dolor amet</h1>
    </div>
</body>
```

### 가시 속성

#### 가시 속성
- 가시 속성은 태그와 화면에 보이는 방식을 지정
- display 속성
  - 이 속성을 사용하여 인라인 형식, 블록 형식, 인라인-블록 형식으로 설정할 수 있음
- display 속성과 주로 사용하는 키워드
- 
| 키워드 | 설명 |
|--------|------|
| none | 화면에 보이지 않음 |
| block | 블록 박스 형식으로 지정 |
| inline | 인라인 박스 형식으로 지정 |
| inline-block | 블록과 인라인의 중간 형태로 지정 |

#### 예제 6-4 : display 속성
- 1. none 키워드 적용하기. 태그가 화면에서 보이지 않음
- 코드 6-8 display_none.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Display Property</title>
        <style>
            #box {
                display: none;
            }
        </style>
    </head>
    <body>
        <span>더미 객체</span>
        <div id="box">대상 객체</div>
        <span>더미 객체</span>
    </body>
</html>
```
- 2. bloack 키워드 적용하기. #box태그의 display 속성을 block 키워드로 바꿈
- 코드 6-9 display_block.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Display Property</title>
        <style>
            #box {
                display: block;
            }
        </style>
    </head>
    <body>
        <span>더미 객체</span>
        <div id="box">대상 객체</div>
        <span>더미 객체</span>
    </body>
</html>
```
- 3. inline과 inline-block 키워드 비교하기
- 코드 6-10 display_inline.html
```html
<style>
    #box {
        display: inline;
    }
</style>
```
- 코드 6-11 display_inline-block.html
```html
<style>
    #box {
        display: inline-block;
    }
</style>
```

#### inline과 inline-block 키워드 적용
- block 형식, inline-block 형식
  - margin 속성, padding 속성을 상하좌우 네 방향으로 지정할 수 있음
- 코드 6-12 display_inlineWithMargin.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Display</title>
        <style>
            #box {
                display: inline;
                background-color: red;
                width: 100px; height: 50px;
                margin: 10px;
            }
        </style>
    </head>
    <body>
        <p>의미 없는 더미 객체</p>
        <span>더미 객체</span>
        <div id="box">대상 객체</div>
        <span>더미 객체</span>
        <p>의미 없는 더미 객체</p>
    </body>
</html>
```
- inline 형식
  - margin 속성, padding 속성을 왼쪽과 오른쪽으로만 지정할 수 있음
- 코드 6-13 display_inline-blockWithMargin.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Display</title>
        <style>
            #box {
                display: inline-block;
                background-color: red;
                width: 100px; height: 50px;
                margin: 10px;
            }
        </style>
    </head>
    <body>
        <p>의미 없는 더미 객체</p>
        <span>더미 객체</span>
        <div id="box">대상 객체</div>
        <span>더미 객체</span>
        <p>의미 없는 더미 객체</p>
    </body>
</html>
```

### 배경 속성

#### 배경 속성
- 주로 사용하는 배경 속성
- 
| 속성 | 설명 |
|------|------|
| background-image | 배경 이미지 삽입 |
| background-size | 배경 이미지의 크기 지정 |
| background-repeat | 배경 이미지의 반복 형태 지정 |
| background-attachment | 배경 이미지의 부착 형태 지정 |
| background-position | 배경 이미지의 위치 지정 |
| background | 한 번에 모든 배경 속성 입력 |

#### 배경 이미지 삽입과 크기 지정 
- background-image 속성
  - 배경 이미지 지정
  - 스타일 값에는 URL 단위나 그레이디언트 입력
- background-size 속성
  - 배경 이미지 크기

#### 예제 6-5 : 배경 이미지 삽입과 크기 조정
- 1. 배경으로 사용할 이미지 파일 준비하기
  - 배경 이미지와 작성할 HTML 페이지를 같은 폴더에 넣기
    - (실습 시, 배포한 BackgroundFront.png, BackgroundBack.png 파일 사용할 것)
- 2. 배경 이미지 1개 삽입하기
- 코드 6-14 background-image.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            body {
                background-image: url('BackgroundFront.png');
            }
        </style>
    </head>
    <body>
        
    </body>
</html>
```
- 3. 배경 이미지 2개 삽입하기
  - 먼저 입력한 이미지(코드의 왼쪽)가 앞쪽에 위치
- 코드 6-15 background_imageLayer.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            body {
                /* 각각의 그림을 레이어하고 부릅니다. */
                background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
            }
        </style>
    </head>
    <body>
        
    </body>
</html>
```
- 4. 배경 이미지의 너비 조정하기
- 코드 6-16 background_size.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            body {
                background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
            }
        </style>
    </head>
    <body>
        
    </body>
</html>
```
- 5. 배경 이미지 높이 조정하기
- 코드 6-17 background_sizeEach.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            body {
                background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
                background-size: 100% 250px;
            }
        </style>
    </head>
    <body>

    </body>
</html>
```

#### 배경 이미지 반복과 부착 형태, 위치
- background-repeat 속성
  - 배경 이미지의 반복 형태 지정
  - repeat : 이미지를 패턴처럼 표시
  - repeat-x : X축 방향으로만 이미지 반복
  - repeat-y : Y축 방향으로만 이미지 반복
- background-attachment 속성
  - 배경 이미지를 화면에 고정하는 속성
  - scroll : 화면 스크롤에 따라 배경 이미지가 함께 이동(기본 키워드)
- background-position 속성
  - 배경 이미지의 배치 위치 지정
  - background-position: 키워드;
  - background-position: x축 위치;
  - background-position: x축 위치 y축 위치;

#### 예제 6-6 반복과 부착 형태, 위치
- 1. 배경 이미지 반복 없애기
- 코드 6-19 background_repeatNone.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            body {
                background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
                background-size: 100%;
                background-repeat: no-repeat;
            }
        </style>
    </head>
    <body>
        
    </body>
</html>
```
- 2. 스크롤이 가능한 분량의 텍스트 추가하기
- 코드 6-20 background_attachmentScroll.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSS3 Property Basic</title>
        <style>
            body {
                background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
                background-size: 100%;
                background-repeat: no-repeat;
                background-attachment: scroll;
            }
        </style>
    </head>
    <body>
        <h1>Lorem ipsum dolor sit amet</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Proin ut quamfeugiat, tinciduntdolor nec, iaculisdui.</p>
        <p>Fusce elementumpretium diam vitae facilisis.</p>
        <p>Maurisnon lobortislectus. Vestibulum a eros</p>
        <p>Donec ultriciesvolutpatporttitor.</p>
    </body>
</html>
```
- 3. 배경 이미지 화면에 고정시키기
- 코드 6-21 background_attachmentFixed.html
```html
<head>
    <title>CSS3 Property Basic</title>
    <style>
        body {
            background-color: #E7E7E8;
            background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
            background-size: 100%;
            background-repeat: no-repeat;
            background-attachment: fixed;
        }
    </style>
</head>
```

37pg 부터
