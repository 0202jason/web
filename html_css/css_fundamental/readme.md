# css
> Cascading Style Sheet

### 적용 방법
1. 인라인(inline) 스타일(비권장)
   - HTML 요소 안에 style 속성 값으로 작성
  ```html
  <h1 style="color: blue; background-color: yellow;">
  ``` 
2. 내부(internal) 스타일
   - head 태그 안에 style 태그에 작성

3. 외부(External) 스타일
   - 별도 css 파일 생성 후 HTML link 태그를 사용해 불러옴

### css 구문
- 선택자(Selector)
  - 누구를 꾸밀지 지정
- 선언(Declaration)
  - 어떻게 꾸밀지
  - 속성과 값이 한 쌍, ; 으로 끝남
- 속성(Property)
  - 바꾸고 싶은 스타일의 종류를 나타냄
- 값(Value)
  - 속성에 적용할 구체적인 설정을 나타냄

### css selector
> HTML 요소를 선택하여 스타일을 적용할 수 있도록 하는 선택자
- 기본 선택자
  - 전체(*)
  - 요소(tag)
  - 클래스(class)
  - 아이디(id)
  - 속성(attr)
- 결합자(Combinators)
  - 자손 결합자(" " (space))
  - 자식 결합자(">")

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    /* 전체 선택자 */
    *{
      color: red;
    }
    /* 요소 선택자 */
    h2 {
      color: orange
    }
    h3,
    h4{
      color: blue
    }
    /* class 선택자 */
    .green {
      color: green
    }
    /* id 선택자 */
    #purple {
      color: purple
    }
    /* 자식 결합자 */
    .green > span {
      font-size: 50px;
    }
    /* 자손 결합자 */
    .green li {
      color: brown
    }
    /* 속성 선택자 */
    [class^="y"] {
      color: yellow;
    }
  </style>
</head>

<body>
  <h1 class="green">Heading</h1>
  <h2>선택자</h2>
  <h3>연습</h3>
  <h4>반가워요</h4>
  <p id="purple">과목 목록</p>
  <ul class="green">
    <li>파이썬</li>
    <li>알고리즘</li>
    <li>웹
      <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>PYTHON</li>
      </ol>
    </li>
  </ul>
  <p class="green">Lorem, <span>ipsum</span> dolor.</p>
  <p class="yellow">TEST</p>
</body>

</html>

```

### 명시도
> 결과적으로 요소에 적용할 CSS 선언을 결정하기 위한 알고리즘

1. Importance
    - !important
2. inline 스타일
3. 선택자
    - id 선택자 > class 선택자 > 요소 선택자
4. 소스 코드 선언 순서


### 선언
- 속성
  - 스타일링 하고 싶은 기능이나 특성
  - font-size, background-color, width, margin, padding 등
- 값
  - 속성에 적용될 구체적 설정
  - 16px, lightgray, 100%, 10rem 등
- 값의 단위
  - 절대 단위: px, pt, cm 등
  - 상대 단위: %, em, rem, vw, vh 등


### 상속
- 상속을 통해 부모 요소의 속성을 자식에게 상속
- 상속되는 속성
  - Text 관련 요소(font, color, text-align), opacity, visibility 등
- 상속X
  - box model 관련 요소(width, height, border, box-sizing ... )
  - position 관련 요소(position, top/right/bottom/left, z-index)


### CSS Box Model
> 웹 페이지의 모든 HTML 요소를 감싸는 사각형 상자 모델

- Content: 실제 내용이 위치하는 영역
- padding: content, border 사이의 내부 여백
- border: content, padding을 감싸는 테두리
- Margin: 이 박스와 다른 요소와의 외부 간격