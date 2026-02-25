## css box model

> 박스 타입에 따라 페이지에서의 배치 흐름 및 다른 박스와 관련하여 박스가 동작하는 방식이 달라짐

1. **block**
   - 항상 새로운 행으로 나뉨(한 줄 전체를 차지, 너비 100%)
   - width, height, margin, padding 속성 모두 사용 가능
   - width 지정하지 않으면 inline 방향으로 사용 가능한 공간 모두 차지
   - h1~6, p, div, ul, li 등
2. **inline**
    - 줄 바꿈이 일어나지 않음(콘텐츠 크기만큼 영역 차지)
    - width, height 사용 불가
    - padding, margin, border가 적용되지만 상하로는 다른 요소를 못 밀어냄
    - a, img, span, strong 등


### 기타 속성

1. **inline-block 타입**
   - block과 inline의 특징 합침(줄 바꿈 없음, 크기 지정 가능)
   - width, height 사용가능
   - padding, margin, border로 인해 다른 요소가 상자에서 밀려남
2. **none** 타입
   - 요소를 화면에 표시하지 않고, 공간조차 부여되지 않음
3. **flex**

## css position

### css layout
- 각 요소의 위치와 크기를 조정, 웹 페이지의 디자인 결정
- 요소들을 상하좌우로 정렬하고 간격을 맞추고 전체적인 페이지의 뼈대 구성
- 핵심 속성: display(block, inline, flex, grid, ...)

### css position
- 요소를 **normal flow**에서 제거하여 다른 위치로 배치
- 다른 요소 위에 올리기, 화면의 특정 위치에 고정시키기
- 핵심 속성: position(static, relative, absolute, fixed, sticky, ...)
- 네 가지 방향 속성(상, 하, 좌, 우)을 이용해 요소의 위치를 조절할 수 있음
- 겹치는 요소의 쌓이는 순서를 조절할 수 있음(Z Axis)

### position 유형

1. **static**
   - 요소를 Normal flow에 따라 배치
   - top, right, bottom, left 속성이 적용되지 않음
2. **relative**
   - 요소를 Normal flow에 다라 배치
   - 자신의 원래 위치(static)을 기준으로 이동
   - top, right, bottom, left 속성으로 위치를 조정
   - 다른 요소의 레이아웃에 영향을 주지 않음
3. **absolute**
   - 요소를 Normal Flow에서 제거
   - 가장 가까운 relative 부모 요소를 기준으로 이동
     - 만족하는 부모 요소가 없다면 body 태그를 기준으로 함
   - top, right, bottom, left 속성으로 위치를 조정
   - 문서에서 요소가 차지하는 공간이 없어짐(원래 있던 자리 사라짐)
4. **fixed**
   - 요소를 Normal Flow에서 제거
   - 현재 화면영역(viewpoint)을 기준으로 이동
   - 스크롤해도 항상 같은 위치에 유지됨
   - top, right, bottom, left 속성으로 위치를 조정
   - 문서에서 요소가 차지하는 공간이 없어짐
5. **sticky**
   - relative와 fixed의 특성을 결합한 속성
   - 스크롤 위치가 임계점에 도달하기 전에는 relative처럼 동작
   - 스크롤 위치가 임계점에 도달하면 fixed처럼 화면에 고정
   - 다음 sticky 요소가 나오면 이전 sticky 요소의 자리를 대체

### z-index

> 요소의 쌓임 순서를 정의하는 속성  

- 정수 값을 사용해 z축 순서를 지정
- 값이 클수록 요소가 위에 쌓이게 됨
- static이 아니 ㄴ요소에만 적용됨
- 기본값은 auto, 부모 요소의 z-index 영향을 받음
- 같은 부모 내에서만 z-index 값을 비교, 값이 같으면 HTML문서 순서대로 쌓임
- 부모의 z-index가 낮으면 자식의 z-index가 아무리 높아도 부모보다 위로 올라갈 수 없음

## CSS Flexbox(중요)

> 요소를 행과 열 형태로 배치하는 1차원 레이아웃 방식

### 구성요소
- **main axis**
  - flex item들이 배치되는 기본 축
  - main start -> main end 방향으로 배치(기본 값)
- **cross axis**
  - main axis에 수직인 축
  - cross start -> cross end 방향으로 배치
- **flex container**
  - display: flex; 혹은 display: inline-flex; 가 설정된 부모 요소
  - 이 컨테이너의 1차 자식 요소들이 Flex Item이 됨
  - flexbox 속성 값들을 사용하여 자식 요소 Flex Item들을 배치하는 주체
- **flex item**
  - flex container 내부에 레이아웃 되는 항목

###  Flexbox 속성
- **Flex Container**
  - Flex Container: display 속성을 flex 로 설정하면, Flex Container로 지정됨
  - flex item은 기본적으로 행으로 나열
  - 주 축의 시작선에서 시작
  - 교차 축의 크기를 채우기 위해 늘어남
- **flex-direction**
  - flex item이 나열되는 방향을 지정
  - row: 아이템을 가로 방향으로, 왼쪽에서 오른쪽으로 배치
  - column: 아이템을 세로 방향으로, 위에서 아래로 배치
  - "-reverse"로 지정하면 flex item  배치의 시작 선과 끝 선이 서로 바뀜
- **flex-wrap**
  - flex item 목록이 flex container의 한 행에 들어가지 않을 경우, 다른 행에 배치할지 여부 설정
  - nowrap(기본 값): 줄 바꿈을 하지 않음
  - wrap: 여러 줄에 걸쳐 배치될 수 있게 설정 (위에서 아래로 쌓임)
  - wrap: 여러 줄에 걸쳐 배치되나, 줄이 쌓이는 방향이 반대(역순)으로 설정
- **justify-content**
  - 주 축을 따라 flex item 들을 정렬하고 간격을 조정
  - flex-start(기본값): 주 축의 시작점으로 정렬
  - center: 주 축의 중앙으로 정렬
  - flex-end: 주 축의 끝점으로 정렬
- **align-content**
  - 컨테이너에 여러줄의 flex item이 있을 때, 그 줄들 사이의 공간을 어떻게 분배할지 지정
    - wrap 또는 wrap-reverse로 설정된 여러 행에만 적용(두 줄 이상일때만 의미 있음)
    - stretch(기본값): 여러 줄을 교차 축에 맞게 늘려 빈 공간을 채움
    - center: 여러 줄을 교차 축의 중앙에 맞춰 정렬
    - flex-start: 여러 줄을 교차 축의 시작점(보통 위쪽)에 맞춰 정렬
    - flex-end: 여러 줄을 교차 축의 끝점(보통 아래쪽)에 맞춰 정렬
- **align-items**
  - 컨테이너 안에 있는 flex item 들의 교차 축 정렬 방법을 지정
  - stretch(기본값): 아이템을 교차 축 높이를 꽉 채우도록 늘어남
  - center: 아이템을 교차 축의 중앙에 맞춰 정렬
  - flex-start: 아이템을 교차 축의 시작점(가로 방향일 경우 위쪽)에 맞춰 정렬
  - flex-end: 아이템을 교차 축의 끝점(가로 방향일 경우 아래쪽)에 맞춰 정렬
- **align-self**
  - 컨테이너 안에 있는 flex item 들을 교차 축을 따라 개별적으로 정렬
  - auto(기본값): 부모 컨테이너의 align-items 속성 값을 상속
  - stretch: 해당 아이템만 교차 축 방향으로 늘어나 컨테이너를 꽉 채우도록 정렬
  - center: 해당 아이템만 교차 축의 중앙에 정렬
  - flex-start: 해당 아이템만 교차 축의 시작점(가로 방향일 경우 위쪽)에 정렬
  - flex-end: 해당 아이템만 교차 축의 끝점(가로 방향일 경우 아래쪽)에 정렬
- **flex-grow**
  - 남는 행 여백을 비율에 따라 각 flex item 에 분배
  - flex item이 컨테이너 내에서 확장하는 비율을 지정 