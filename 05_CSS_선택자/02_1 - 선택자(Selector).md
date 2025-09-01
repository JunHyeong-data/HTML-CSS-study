# CSS 선택자 기본

## 1. 선택자(Selector)란?

* HTML 문서의 특정 요소를 **선택하여 스타일을 적용**할 수 있도록 하는 방법.
* 즉, "어떤 태그를 꾸밀 것인지"를 지정하는 도구.

---

## 2. 선택자의 종류

### 2.1 전체 선택자 (Universal Selector)

* 문서 내 **모든 요소**를 선택.
* 보통 브라우저의 기본 스타일을 초기화할 때 사용.

```css
* {
  margin: 0;
  padding: 0;
}
```

---

### 2.2 타입 선택자 (Type Selector)

* **태그명으로 요소를 선택**.
* 예: `h2`, `p` 등.

```css
h2 {
  color: green;
}

p {
  color: gray;
  font-weight: 400;
  text-align: center;
}
```

---

### 2.3 클래스 선택자 (Class Selector)

* **`.` + 클래스명**으로 선택.
* 여러 요소에 중복 적용 가능.

```html
<span class="red-text">동해</span>
<span class="red-text">백두산</span>
<span class="blue-text">남산</span>
```

```css
.red-text {
  color: red;
}

.blue-text {
  color: blue;
}
```

---

### 2.4 아이디 선택자 (ID Selector)

* **`#` + 아이디명**으로 선택.
* 문서 내 **단 하나의 요소**에만 적용해야 함 (고유해야 함).

```html
<h1 id="title">애국가</h1>
```

```css
#title {
  font-size: 40px;
  color: darkgray;
  background: yellow;
}
```

---

## 3. 선택자 정리

| 선택자 종류  | 표기법         | 특징          |
| ------- | ----------- | ----------- |
| 전체 선택자  | `*`         | 모든 요소 선택    |
| 타입 선택자  | `h2`, `p` 등 | 태그명으로 선택    |
| 클래스 선택자 | `.클래스명`     | 중복 적용 가능    |
| 아이디 선택자 | `#아이디명`     | 문서 내 고유해야 함 |

---

## 4. 핵심 요약

* 선택자는 HTML 요소를 꾸미기 위해 반드시 알아야 할 개념.
* 기본 선택자:

  * **전체(`*`)**
  * **타입(tag)**
  * **클래스(`.`)**
  * **아이디(`#`)**
* 클래스는 여러 곳에 사용 가능,
  아이디는 고유해야 함.

---
