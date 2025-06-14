# urock_web

## 소개
- - - - - - - - - - - -
urock_web은 기업 소개 웹사이트, 제품 페이지, 서비스용 홈페이지 등 다양한 웹 템플릿을 모듈식으로 구성한 웹 프레임워크입니다. 컴포넌트 단위의 접근을 통해 효율적인 개발을 위한 CSS/JS 라이브러리를 기반으로 작업, HTML, CSS, JavaScript 기술의 웹 프레임워크입니다.

## 특징
- - - - - - - -
- 빠르고, 모던한 디자인, 제품 페이지, 서비스용, 기업 소개 웹 템플릿 지원
- 모듈식 컴포넌트 기반의 CSS/JS 라이브러리 제공
- 재사용 HTML 구성 요소 시스템(헤더/푸터 등)
- 다양한 환경에서도 호환되는 UI 컴포넌트

## 파일 구조 설명
- - - - - - - - - - - - -
- `css/`: 스타일시트(변수, 컴포넌트, 템플릿용 CSS 파일)
- `js/`: 자바스크립트(기능, 컴포넌트, 템플릿용 JS 파일)
- `html/`: 각 템플릿용 및 컴포넌트용 HTML 파일
- `public/`: 이미지, 아이콘, 로고, 비디오 등 정적 리소스
- `.vscode/`: VS Code 설정 파일

## 시작 및 사용 방법
- - - - - - - - - - - - - - -
1. 저장소를 클론합니다.
2. `index.html`을 브라우저에서 직접 열거나, 로컬 서버(예: Live Server)로 실행합니다.
3. `css/style.css`, `js/index.js`를 통해 모든 스타일과 자바스크립트가 연결되어 있습니다.

## 개발 환경
- - - - - - - -
- HTML5, CSS3, JavaScript(ES6)
- 권장 도구: VSCode
- (선택) Live Server 확장으로 로컬 실행

## 기여 방법
- - - - - - - -
1. 새 브랜치 생성 후에 PR 제출
2. 코드 리뷰 후 메인 구조 및 스타일에 맞는지 확인
3. 웹 표준에만 의존하는 코드 작성

## 라이센스
- - - - - - - -
이 프레임워크는 상업적/비상업적 목적에 모두 자유롭게 사용할 수 있습니다. (별도 라이센스 문서 참조)

## CSS 섹션 통합 가이드
- - - - - - - - - - - - - - -

### Certificate 섹션
`css/section/certificate.css`에 모든 certificate 관련 스타일이 통합되어 있습니다.

**사용 방법:**
```html
<!-- 기본 certificate 섹션 -->
<section class="certificate">
  <div class="cards">
    <div class="card">...</div>
  </div>
</section>

<!-- DFAS Enterprise 페이지 전용 배경 -->
<section class="certificate">
  <div class="cards">
    <div class="card dfas-ent">...</div>
  </div>
</section>
```

### Feature 섹션
`css/section/feature.css`에 모든 feature 관련 스타일이 통합되어 있습니다.

**페이지별 클래스 매핑:**
| 페이지 | CSS 클래스 | 특징 |
|--------|------------|------|
| MCQ-P | `.feature.mcq-p.bg-dark` | 3개 카드, 어두운 배경 |
| MCQ-S | `.feature.mcq-s.bg-dark` | 4개 카드, 어두운 배경 |
| MCQ-G | `.feature.mcq-g` | 3개 카드, 배경 이미지 |
| GM | `.feature.gm` | 단일 이미지, 배경 이미지 |
| GM Pro | `.feature.gm-pro` | 단일 이미지, 패딩, 큰 크기 |
| DFAS Pro | `.feature.dfas-pro` | 단일 이미지, 배경 이미지 |
| DFAS Enterprise | `.feature.dfas-ent` | 단일 이미지, 배경 이미지 |

**사용 방법:**
```html
<!-- MCQ 시리즈 (카드형) -->
<section class="feature mcq-p bg-dark">
  <div class="frames">
    <div class="frame card">
      <h4>Feature 1</h4>
    </div>
    <div class="frame card">
      <h4>Feature 2</h4>
    </div>
    <div class="frame card">
      <h4>Feature 3</h4>
    </div>
  </div>
</section>

<!-- GM 시리즈 (단일 frame) -->
<section class="feature gm">
  <div class="frame"></div>
</section>

<!-- DFAS 시리즈 (단일 frame) -->
<section class="feature dfas-pro">
  <div class="frame"></div>
</section>
```

**장점:**
- 중앙 집중화: 모든 feature 스타일이 한 곳에서 관리됨
- 재사용성: 공통 클래스로 새로운 페이지에서도 쉽게 사용 가능
- 유지보수성: 스타일 변경 시 한 곳만 수정하면 됨
- 일관성: 모든 페이지에서 일관된 feature 스타일 적용

## 프레임워크 디렉토리 구조
=====================

## Typography System
---------

이미지의 텍스트 스타일 스펙에 맞춰 구현된 타이포그래피 시스템입니다.

### 📁 파일 구조

```
css/global/variables.css     # CSS 변수 및 기본 스타일
components/Typography.jsx    # React 컴포넌트
components/Typography.css    # React 컴포넌트 스타일
```

### 🎨 스타일 스펙

| 요소 | 폰트 | 크기 | 굵기 | 설명 |
|------|------|------|------|------|
| H1 | Gmarket Sans | 72px | Medium (500) | 메인 헤딩 |
| H2 | Inter | 64px | Bold Italic (700) | 서브 헤딩 |
| H3 | Pretendard | 36px | Semibold (600) | 섹션 제목 |
| H4 | Pretendard | 24px | Medium (500) | 서브섹션 제목 |
| H5 | Pretendard | 16px | Semibold (600) | 작은 제목 |
| H6 | Pretendard | 16px | Regular (400) | 최소 헤딩 |
| Tab | Pretendard | 20px | Semibold (600) | 탭 메뉴 |
| Card Number | Pretendard | 72px | Medium (500) | 카드 번호 |
| Nav | Pretendard | 18px | Semibold (600) | 네비게이션 |

### 🚀 사용법

#### HTML에서 사용

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="css/global/variables.css">
    <!-- Pretendard 폰트 추가 -->
    <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable.min.css" />
    <link href="https://fonts.googleapis.com/css2?family=Inter:ital,wght@0,300;0,400;0,500;0,600;0,700;1,700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- 기본 헤딩 -->
    <h1>메인 제목</h1>
    <h2>서브 제목</h2>
    <h3>섹션 제목</h3>
    
    <!-- 커스텀 텍스트 -->
    <div class="tab-text">탭 메뉴</div>
    <div class="card-number">01</div>
    <div class="nav-text">네비게이션</div>
</body>
</html>
```

#### React에서 사용

```jsx
import { 
  Heading1, 
  Heading2, 
  Heading3, 
  TabText, 
  CardNumber, 
  NavText,
  Text // 통합 컴포넌트
} from './components/Typography';

function App() {
  return (
    <div>
      {/* 개별 컴포넌트 */}
      <Heading1>메인 제목</Heading1>
      <Heading2>서브 제목</Heading2>
      <TabText active>활성 탭</TabText>
      <CardNumber>01</CardNumber>
      <NavText>네비게이션</NavText>
      
      {/* 통합 컴포넌트 */}
      <Text variant="h1">메인 제목</Text>
      <Text variant="tab" active>활성 탭</Text>
      <Text variant="card-number">02</Text>
    </div>
  );
}
```

### 🎯 컴포넌트 API

#### Heading 컴포넌트 (H1~H6)

```jsx
<Heading1 className="custom-class">
  제목 텍스트
</Heading1>
```

**Props:**
- `children`: 텍스트 내용
- `className`: 추가 CSS 클래스
- `...props`: 기타 HTML 속성

#### TabText 컴포넌트

```jsx
<TabText active onClick={handleClick}>
  탭 메뉴
</TabText>
```

**Props:**
- `children`: 텍스트 내용
- `active`: 활성 상태 (boolean)
- `className`: 추가 CSS 클래스
- `onClick`: 클릭 이벤트 핸들러

#### NavText 컴포넌트

```jsx
<NavText active onClick={handleClick}>
  네비게이션 메뉴
</NavText>
```

**Props:**
- `children`: 텍스트 내용
- `active`: 활성 상태 (boolean)
- `className`: 추가 CSS 클래스

#### CardNumber 컴포넌트

```jsx
<CardNumber>01</CardNumber>
```

**Props:**
- `children`: 숫자 또는 텍스트
- `className`: 추가 CSS 클래스

#### Text 통합 컴포넌트

```jsx
<Text variant="h1" active>
  텍스트 내용
</Text>
```

**Props:**
- `variant`: 스타일 종류 ('h1'~'h6', 'tab', 'card-number', 'nav')
- `active`: 활성 상태 (tab, nav에만 적용)
- `children`: 텍스트 내용
- `className`: 추가 CSS 클래스

### 🎨 CSS 변수 사용

```css
/* 커스텀 스타일에서 변수 사용 */
.my-custom-text {
  font-family: var(--font-h3-family);
  font-size: var(--font-h3-size);
  font-weight: var(--font-h3-weight);
  color: var(--color-dark-text-04-primary);
}
```

### 📱 반응형 디자인

모바일 환경에서는 자동으로 폰트 크기가 조정됩니다:

- H1: 72px → 48px
- H2: 64px → 42px  
- H3: 36px → 28px
- Card Number: 72px → 48px

### 🔧 커스터마이징

#### 색상 변경

```css
:root {
  --color-dark-text-04-primary: #your-color;
  --color-dark-bg-04: #your-bg-color;
}
```

#### 폰트 크기 조정

```css
:root {
  --font-h1-size: 80px; /* 기본값 72px */
  --font-h2-size: 72px; /* 기본값 64px */
}
```

### 🌟 Typography 특징

- ✅ 이미지 스펙에 정확히 맞춘 구현
- ✅ CSS 변수 시스템으로 쉬운 커스터마이징
- ✅ React 컴포넌트와 순수 HTML 모두 지원
- ✅ 반응형 디자인 적용
- ✅ 활성 상태 및 호버 효과
- ✅ 접근성 고려

## CSS 특정 상태 맥락
---------------

### Certificate 특정
`css/section/certificate.css`에서 정의된 certificate 섹션 스타일시트가 있습니다.

**적용 시작:**
```html
<!-- 기본 certificate 특정 -->
<section class="certificate">
    <div class="cards">
        <div class="card">...</div>
    </div>
</section>

<!-- DFAS Enterprise 섹션별 적용 기본 -->
<section class="certificate">
    <div class="cards">
        <div class="card dfas-ent">...</div>
    </div>
</section>
```

### Feature 특정
`css/section/feature.css`에서 정의된 feature 섹션 스타일시트가 있습니다.

**섹션별별 전용스타 맞춤:**
| 섹션별 | CSS 전용스타 | 특징 |
|---------|-------------|------|
| MCQ-P | `.feature.mcq-p.bg-dark` | 3개 전용, 다크모드 코드 |
| MCQ-S | `.feature.mcq-s.bg-dark` | 4개 전용, 다크모드 코드 |
| MCQ-G | `.feature.mcq-g` | 3개 전용, 코드 전용상태 |
| GM | `.feature.gm` | 단일 전용상태, 코드 전용상태 |
| GM Pro | `.feature.gm-pro` | 단일 전용상태, 중앙정렬, 상 폴더 |
| DFAS Pro | `.feature.dfas-pro` | 단일 전용상태, 코드 전용상태 |
| DFAS Enterprise | `.feature.dfas-ent` | 단일 전용상태, 코드 전용상태 |

**적용 시작:**
```html
<!-- MCQ 배경섹션 (전용단위) -->
<section class="feature mcq-p bg-dark">
    <div class="frames">
        <div class="frame card">
            <h4>Feature 1</h4>
        </div>
        <div class="frame card">
            <h4>Feature 2</h4>
        </div>
        <div class="frame card">
            <h4>Feature 3</h4>
        </div>
    </div>
</section>

<!-- GM 배경섹션 (단일 frame) -->
<section class="feature gm">
    <div class="frame"></div>
</section>

<!-- DFAS 배경섹션 (단일 frame) -->
<section class="feature dfas-pro">
    <div class="frame"></div>
</section>
```

**주의:**
- 각각 코드팀: 정의된 feature 스타일시트를 실행 선별된 섹션경우
- 체크업구성: 편상태 전용스타들을 활용모드 섹션별별로 중점된 적용 섹션 섹션
- 섹션상태구성: 스타일 적용 각 실행 말든 운통적설 경우
- 기록 구성: 정의된 섹션별의 기록된 feature 스타일 세팅

## 개발자들 집중토지 폴더
====================

```
urock_web/
├─  README.md
├─  index.html
├─  .stylelintrc
├─  css/
│   ├─  style.css
│   ├─  global/
│   │   ├─  variables.css
│   │   ├─  reset.css
│   │   └─  mixin.css
│   ├─  component/
│   │   ├─  banner.css
│   │   ├─  breadcrumb.css
│   │   ├─  buttons.css
│   │   ├─  cards.css
│   │   ├─  fab.css
│   │   ├─  tab.css
│   │   └─  title.css
│   ├─  section/
│   │   ├─  header.css
│   │   ├─  footer.css
│   │   ├─  hero.css
│   │   ├─  intro.css
│   │   ├─  contents.css
│   │   ├─  description.css
│   │   ├─  feature.css
│   │   ├─  process.css
│   │   ├─  utilization.css
│   │   ├─  effect.css
│   │   ├─  client.css
│   │   ├─  news.css
│   │   ├─  service.css
│   │   └─  certificate.css
│   └─  page/
│           ├─  main.css
│           ├─  company.css
│           ├─  support-01-inquiry.css
│           ├─  support-02-news.css
│           ├─  support-test-index.css
│           ├─  solution-01-dfas-pro.css
│           ├─  solution-02-dfas-ent.css
│           ├─  solution-03-mcq-p.css
│           ├─  solution-04-mcq-s.css
│           ├─  solution-05-mcq-g.css
│           ├─  solution-06-gm.css
│           ├─  solution-07-gm-pro.css
│           ├─  solution-test-index.css
│           ├─  service-01-analysis.css
│           ├─  service-02-authentication.css
│           └─  service-03-education.css
├─  js/
│   ├─  index.js
│   ├─  include.js
│   ├─  global/
│   │   ├─  components.js
│   │   ├─  config.js
│   │   ├─  constants.js
│   │   ├─  events.js
│   │   └─  utils.js
│   ├─  component/
│   │   ├─  cards.js
│   │   ├─  fab.js
│   │   └─  tab.js
│   └─  page/
│           ├─  main.js
│           ├─  company.js
│           ├─  service.js
│           ├─  solution.js
│           └─  support.js
├─  html/
│   ├─  component/
│   │   ├─  tab.html
│   │   └─  title.html
│   ├─  section/
│   │   ├─  header.html
│   │   ├─  intro.html
│   │   └─  footer.html
│   └─  page/
│           ├─  test.html
│           ├─  company.html
│           ├─  support-01-inquiry.html
│           ├─  support-02-news.html
│           ├─  solution-01-dfas-pro.html
│           ├─  solution-02-dfas-ent.html
│           ├─  solution-03-mcq-p.html
│           ├─  solution-04-mcq-s.html
│           ├─  solution-05-mcq-g.html
│           ├─  solution-06-gm.html
│           ├─  solution-07-gm-pro.html
│           ├─  service-01-analysis.html
│           ├─  service-02-authentication.html
│           └─  service-03-education.html
├─  public/
│   ├─  animation/
│   ├─  video/
│   ├─  logo/
│   ├─  icons/
│   └─  images/
│           ├─  solution/
│           ├─  service/
│           ├─  main/
│           ├─  header/
│           ├─  footer/
│           ├─  customer/
│           ├─  company/
│           └─  common/
└─  components/
    ├─  Typography.jsx
    └─  Typography.css
```

- `public` 실형 집중토지 각 `images` 실형 집중토지에서 실형 적용 있습니다. 실형경우 반대내 경유를 폴더실형설으로 합니다.
