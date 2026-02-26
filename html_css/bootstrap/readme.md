# bootstrap

> **css 프론트엔드 프레임워크**: 모바일, 태블릿, 데스크탑 등 다양한 기기 환경에서 웹 페이지가 적절하게 표시될 수 있도록 반응형 웹 디자인을 지원하는 도구(기술)

**프레임워크**: 소프트웨어 개발 시 효율성을 높이기 위해, 공통적으로 필요한 기능과 정해진 구조(뼈대)를 미리 제공해 주는 '반제품' 형태의 개발 환경

## 사용 방법
- **Bootstrap**에는 특정한 규칙이 있는 클래스 이름으로 스타일 및 레이아웃이 미리 작성되어 있음
> {property}{sides}-{size}  
> mt-5  
> -> margin, top, 5
- spacing 표현 법  

|property|sides|size|
|:---|:---|:---|
|m: margin|t: top|0: 0 rem/ 0px|
|p: padding|b: bottom|1: 0.25 rem/ 4px|
||s: left|2: 0.5 rem/ 8px|
||e: right|3: 1 rem/ 16px|
||y: top, bottom|4: 1.5 rem/ 24px|
||x: left, right|5: 3 rem/ 48px|
||blank: 4 sides|auto: auto/ auto|

### Reset CSS
- 모든 HTML 요소 스타일을 일관된 기준으로 재설정하는 간결하고 압축된 규칙 시트
- Normalize CSS

### Typography
> [공식문서](https://getbootstrap.com/docs/5.3/getting-started/introduction/)에 있는 가이드 활용

- 제목, 본문 텍스트, 목록 등에 활용 가능
- 
#### Bootstrap Color System
- Bootstrap이 지정하고 제공하는 색상 시스템
- 일관성 있는 의미론적 관점의 색상을 적용할 수 있게 해 줌
  - blue 대신 primary, red 대신 danger 등
- Text, Background 등에 활용

### Component
> 재사용 가능한 독립적인 부품, 더 크고 복잡한 시스템을 구축하기 위해 사용되는 소프트웨어의 기본 단위

- Alerts, Badges, Cards, Navbar, Carousel, Modal 등이 있음

#### 컴포넌트의 특징, 장점
- 사용성
  - 한번 잘 만들어 둔 컴포넌트는 여러 페이지에서 반복해서 사용할 수 있음
- 독립성
  - 각 컴포넌트는 자체적으로 작동하는 데 필요한 모든 코드(HTML/CSS/JS)를 가지고 있음
  - 따라서 다른 컴포넌트에 미치는 영향을 최소화함
- 유지보수 용이성
  - 특정기능(예: 로그인)을 수정해야 할 때, 전체 코드를 뒤질 필요 없이 해당 컴포넌트만 찾아 수정하면 되므로 관리가 매우 편리

### Semantic Web
> 웹 데이터를 의미론적으로 구조화된 형태로 표현하는 방식

#### HTML Semantic Element
- 기본적인 모양과 기능 이외의 **의미**를 가지는 HTML 요소
- header: 소개 및 탐색에 도움을 줌
- nav: 현재 페이지 내, 또는 다른 페이지로의 링크를 보여줌
- main: 문서의 주요 콘텐츠
- article: 독립적으로 구분해 배포하거나 될 수 있는 구성의 콘텐츠 구획
- section: 문서의 독립적인 구획. 더 적합한 요소가 없을 때 사용
- aside: 문서의 주요 내용과 간접적으로만 연관된 부분
- footer: 가장 가까운 조상 구획(main, article 등)의 작성자, 저작권 정보, 관련 문서

### Semantic in CSS
> CSS를 효율적이고 유지 보수가 용이하게 작성하기 위한 일련의 가이드라인

#### OOCSS(Object Oriented CSS)
> 객체 지향적 접근법을 적용하여 CSS를 구성하는 방법론  

1. 구조와 스킨 분리
   - 구조와 스킨을 분리함으로써 가능성을 높임
2. 컨테이너와 콘텐츠 분리
   - 객체에 직접 적용하는 대신 객체를 둘러싸는 컨테이너에 스타일을 적용
   - 스타일을 정의할 때 위치에 의존적인 스타일을 사용하지 않도록 함
   - 콘텐츠를 다른 컨테이너로 이동시키거나 재배치하라 때 스타일이 깨지는 것을 방지
