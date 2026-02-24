# html

> HyperText Markup Language
- HyperText: 웹 페이지를 다른 페이지로 연결하는 링크
- Markup Language: 태그 등을 이용하여 문서나 데이터의 구조를 명시하는 언어


### HTML Element(요소)

- 하나의 요소는 여는 태그와 닫는 태그, 내용으로 구성됨
- 닫는 태그는 태그 이름 앞에 슬래시가 포함
  - 닫는 태그가 없는 태그도 존재
```html
<p>My cat is very grumpy</p>
```

### HTML Attributes(속성)

- 사용자가 원하는 기준에 맞도록 요소를 설정하거나 다양한 방식으로 요소의 동작을 조절하기 위한 값
- 목적
  - 나타내고 싶지 않지만 추가적인 기능, 내용을 담고 싶을 때 사용
  - CSS에서 스타일 적용을 위해 해당 요소를 선택하기 위한 값으로 활용됨
- 작성 규칙
  - 속성은 요소 이름과 속성 사이에 공백이 있어야 함
  - 하나 이상의 속성들이 있는 경우엔 속성 사이에 공백으로 구분함
  - 속성 값은 열고 닫는 따옴표로 감싸야 함
```html
<p class="editor-note">My cat is very grumpy</p>
```

### 구조 예시 코드

```html
<!-- 해당 문서가 html로 문서라는 것을 나타냄 -->
<!DOCTYPE html>

<!-- 전체 페이지의 콘텐츠를 포함 -->
<html lang="en">

<!-- HTML 문서에 관련된 설명, 설정 등
 컴퓨터가 식별하는 메타데이터를 작성
 사용자에게 보이지 않음 -->
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- 브라우저 탭, 즐겨찾기 시 표시되는 제목 -->
  <title>Document</title>
</head>

<!-- HTML 문서의 내용을 나타냄
 페이지에 표시되는 모든 콘텐츠를 작성
 한 문서에 하나의 body만 존재 -->
<body>
  <!-- <p> paragragh. 텍스트 문단을 만드는 태그 -->  
  <p>My page</p>

  <!-- <a> Anchor. 다른 페이지로 이동시키는 하이퍼링크 태그 -->
  <a href="https://www.google.com">Google</a>

  <!-- <img src="images/sample.png" alt="샘플 이미지"> -->
  <img src="https://picsum.photos/200/300" alt="">
  
  <!-- <h1> 텍스트를 크게, 현재 문서의 최상위 제목이라는 의미 부여 -->
  <h1>메인 대제목</h1>
  <h2>중제목</h2>

  <!-- <strong> 강조 글자 굵게, <em> 강조, 글자 기울임 -->
  <p>안녕<strong>하세요</strong> <em>박재현</em>입니다.</p>
  <p>반갑습니다. <b>누구누구</b>입니다</p>

  <!-- ordered list. 리스트 생성 -->
  <ol>
    <li>파이썬</li>
    <li>알고리즘</li>
    <li>웹</li>
  </ol>

  <!-- unordered list. 리스트 생성 -->
  <ul>
    <li>파이썬</li>
    <li>알고리즘</li>
    <li>웹</li>
  </ul>
</body>
</html>
```
