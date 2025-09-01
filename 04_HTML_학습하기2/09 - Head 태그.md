# HTML `<head>` 태그 정리

## 1. `<head>` 태그란?

* **문서 정보(metadata)** 를 담는 영역.
* 브라우저 화면에 직접 보이지 않음.
* 예시:

  * 파비콘(favicon)
  * 문서 제목(title)
  * SNS/카카오톡 미리보기 시 보이는 이미지, 설명 등

---

## 2. `<head>` 안에 올 수 있는 주요 태그

### 2.1 `<title>`

* 브라우저 상단 탭에 표시되는 문서 제목.

```html
<head>
  <title>헤드 태그 예제</title>
</head>
```

---

### 2.2 `<base>`

* 문서 내 상대 경로(URL)의 기준(base URL)을 지정.
* 상대 경로 → 절대 경로처럼 동작하도록 기준을 바꿀 수 있음.

```html
<head>
  <base href="/assets/images/">
</head>
```

---

### 2.3 `<link>`

* 외부 리소스와의 관계를 명시.
* 주로 CSS 파일, 파비콘을 연결할 때 사용.

```html
<head>
  <!-- CSS 연결 -->
  <link rel="stylesheet" href="style.css">

  <!-- 파비콘 연결 -->
  <link rel="icon" href="./favicon.ico">
</head>
```

---

### 2.4 `<style>`

* 문서 내부에 직접 CSS를 작성할 때 사용.

```html
<head>
  <style>
    body { font-family: Arial; }
  </style>
</head>
```

---

### 2.5 `<meta>`

* 문서의 메타데이터(추가 정보)를 담음.
* 예시:

  * 인코딩 방식
  * 검색엔진 키워드
  * SNS 미리보기 정보(Open Graph, Twitter Card 등)

```html
<head>
  <!-- 인코딩 -->
  <meta charset="UTF-8">

  <!-- 설명 -->
  <meta name="description" content="이 웹사이트는 HTML 학습 예제입니다.">

  <!-- Open Graph (SNS 공유 최적화) -->
  <meta property="og:title" content="웹사이트 제목">
  <meta property="og:description" content="웹사이트 설명">
  <meta property="og:image" content="thumbnail.png">
</head>
```

---

### 2.6 `<script>`

* 자바스크립트 코드를 문서에 포함.

```html
<head>
  <script src="script.js"></script>
</head>
```

---

## 3. 파비콘(favicon) 설정 실습

1. 파비콘 생성 사이트에서 `.ico` 파일 생성.
2. 프로젝트 폴더에 `favicon.ico` 저장.
3. `<head>` 안에 `<link>` 태그 추가.

```html
<head>
  <title>파비콘 테스트</title>
  <link rel="icon" href="./favicon.ico">
</head>
```

* `./favicon.ico` → **상대 경로**
* `<base>` 태그 사용 시 기준 경로가 바뀔 수 있음.

---

## 4. 핵심 요약

* `<head>` 태그는 **문서의 보이지 않는 정보**(메타데이터)를 정의.
* 주요 구성 요소:

  * **`<title>`** : 문서 제목
  * **`<base>`** : 상대경로 기준 URL
  * **`<link>`** : 외부 리소스 연결 (CSS, 파비콘 등)
  * **`<style>`** : 내부 CSS 정의
  * **`<meta>`** : 문서 정보, SNS 공유용 데이터
  * **`<script>`** : 자바스크립트 코드 삽입
* 몰라도 웹사이트 제작 가능하지만, 알면 **검색엔진 최적화(SEO), SNS 공유, 파비콘 등**에 활용할 수 있음.

---
