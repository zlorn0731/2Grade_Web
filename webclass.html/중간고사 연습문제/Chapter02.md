# 연습문제

## 1. 다음 문장에 O X를 표시하시오
- (1) HTML 태그는 반드시 내부에 무언가를 포함해야 합니다. (X)
- (2) HTML 태그 내부에는 텍스트만 입력할 수 있습니다. (X)
- (3) html 태그의 lang 속성은 구글 등 검색 엔진에 문서의 언어 정보를 알려 줄 때 사용됩니다. (O)

## 2. 다음 HTML 요소의 속성 이름과 속성 값, 태그 이름을 모두 적으시오.
```html
<img title="바다" alt="sea" src="sea.png">
```
```text
[답]

속성 이름 : title, alt, src
속성 값 : 바다, sea, sea.png
태그 이름 : img
```

## 3. 다음 중 head 태그 내부에 입력할 수 없는 태그는?
- (1) style 태그
- (2) meta 태그
- (3) base 태그
- (4) header 태그 O

## 4. HTML5 기본 페이지 형태는 다음과 같다. 빈칸에 들어갈 알맞은 내용을 적으시오.
```html
<  (1)  >
<  (2)  >
<  (3)  >
    <title>HTML5 Basic</title>
</ (3)  >
<  (4)  >

</ (4)  >
</ (2)  >
```
```text
[답]

(1) - !DOCTYPE html
(2) - html
(3) - head
(4) - body
```

## 5. 다음 코드에서 잘못된 부분을 찾아 바르게 수정하시오.
```html
<!DOCTYPE html>
<html>
    <head>
        <title>HTML5 Basic</title>
        <style src="outer_stylesheet.css"></style>
        <script src="outer_javascript.js"></script>
    </head>
    <body>

    </body>
</html>
```
```text
[답]

<style src="outer_stylesheet.css"></style> 부분이 잘못 됨

<link rel="stylesheet" href="outer_stylesheet.css"> 으로 고쳐야됨
```

## 6. 아직 어떤 HTML 태그가 어떤 기능을 하는지 배우지 않았지만, 기본 예제를 입력하면서 h1이라는 태그를 사용하면 크고 굵은 글씨를 출력할 수 있음을 알았을 것이다. 이를 활용해서 간단한 생각을 표현해 보시오.
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Document</title>
    </head>
    <body>
        <h1>다음 장부터 HTML5를 공부해봅시다.</h1>
        <h1>처음에는 외울 것이 많다고 생각해서 어렵게 느껴지겟지만</h1>
        <h1>차근차근 공부해봐요...!</h1>
    </body>
</html>
```
