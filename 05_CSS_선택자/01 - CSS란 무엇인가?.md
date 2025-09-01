# CSS 기초 강의 정리

## 1. CSS란?

* **CSS (Cascading Style Sheets)**
* HTML 문서를 꾸밀 때 사용하는 스타일시트 언어.
* HTML → 웹페이지 뼈대,
  CSS → 디자인/스타일 적용.

---

## 2. CSS 구조

```css
선택자 {
  속성명: 속성값;
}
```

* **선택자** : 꾸밀 HTML 요소(h1, p, a 등)
* **속성명** : 변경할 스타일 항목(color, background 등)
* **속성값** : 적용할 값(red, 16px 등)

👉 CSS를 배운다는 것은 속성명과 속성값을 차근차근 배워가는 것.

---

## 3. CSS 적용 방법 (3가지)

### 3.1 인라인 스타일 (Inline Style)

* HTML 태그 안에 `style` 속성으로 직접 지정.
* 잘 사용하지 않지만, 꼭 필요한 경우만 활용.

```html
<h1 style="color: blue; font-size: 20px;">제목</h1>
```

---

### 3.2 내부 스타일 (Internal Style Sheet)

* `<head>` 안에 `<style>` 태그를 사용.

```html
<head>
  <style>
    h1 { color: red; }
    .content { border: 1px solid red; background: yellow; }
  </style>
</head>
```

---

### 3.3 외부 스타일 (External Style Sheet) ✅ 가장 많이 사용

* `.css` 파일을 따로 만든 뒤 `<link>` 태그로 연결.

```html
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

* `style.css` 예시:

```css
h1 {
  color: blue;
}

.article {
  border: 1px solid black;
  padding: 30px;
}
```

---

## 4. CSS 주석

* 메모를 남길 때 사용.

```css
/* 이것은 주석입니다 */
h1 {
  color: red; /* 빨간색 적용 */
}
```

* 단축키:

  * macOS : `Command + /`
  * Windows : `Ctrl + /`

---

## 5. CSS 출처와 우선순위

### 출처

1. **제작자 스타일**: 우리가 작성한 CSS (인라인, 내부, 외부 스타일 등)
2. **사용자 스타일**: 사용자가 시스템/브라우저에서 지정한 설정 (예: 고대비 모드)
3. **브라우저 기본 스타일**: 각 브라우저가 기본 제공하는 스타일

---

### 우선순위

* `!important` → 최우선 적용
* 제작자 스타일 → 그다음 적용
* 브라우저 기본 스타일 → 마지막 적용

예시:

```css
a {
  color: red !important; /* 무조건 우선 적용 */
}
```

---

## 6. "Cascading"의 의미

* **Cascading = 폭포처럼 흐른다**
* 여러 스타일이 겹쳤을 때 **우선순위 규칙에 따라 순서대로 적용**됨을 의미.

---

## 7. 핵심 요약

* CSS = HTML을 꾸미는 스타일 언어
* 구조: **선택자 + 속성명 + 속성값**
* 적용 방법: **인라인 / 내부 / 외부 (외부 방식 선호)**
* 주석: `/* ... */`
* 출처: 제작자 / 사용자 / 브라우저
* 우선순위: `!important` > 제작자 > 브라우저
* CSS 학습 = 속성명/속성값을 하나씩 알아가는 과정

---
