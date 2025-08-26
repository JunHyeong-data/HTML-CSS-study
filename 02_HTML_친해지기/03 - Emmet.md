# Emmet(에밋) 기본 사용법

안녕하세요. 이번 시간에는 **코드 타이핑 시간을 줄여주는 Emmet**에 대해 살펴보겠습니다.  
이 내용은 스킬 같은 것이므로, 몰라도 코딩을 못하는 건 전혀 아닙니다.  
부담 없이 들어주세요. 시간이 없으신 분은 이 강의를 건너뛰어도 됩니다.  
하지만 영상이 짧으니 한 번 배워 보는 것도 좋습니다.

---

## 1. Emmet이란?
- **Emmet**은 **HTML과 CSS의 자동 완성 기능**을 제공하는 VS Code 확장 기능  
- 작성 시간을 크게 단축시켜줌  
- 실습 파일을 생성하고, 느낌표(`!`)를 입력한 후 `Tab` 키를 누르면 **HTML 기본 문서 구조**가 완성됨  

---

## 2. Emmet 기본 문법

### (1) 자식 노드 생성
- 기호: `>`  
- 예시:  
  ```emmet
  ul>li
  ```

→ `Tab` →

```html
<ul>
  <li></li>
</ul>
```

---

### (2) 형제 노드 생성

* 기호: `+`
* 예시:

  ```emmet
  div>ul+ol+section
  ```

  → `Tab` →

  ```html
  <div>
    <ul></ul>
    <ol></ol>
    <section></section>
  </div>
  ```

---

### (3) 반복 생성

* 기호: `*`
* 예시:

  ```emmet
  ul>li*3
  ```

  → `Tab` →

  ```html
  <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul>
  ```

---

### (4) id 속성 자동 생성

* 기호: `#`

* 예시:

  ```emmet
  span#item
  ```

  → `Tab` →

  ```html
  <span id="item"></span>
  ```

* 태그명을 생략하면 기본값은 `div`

  ```emmet
  #item
  ```

  → `Tab` →

  ```html
  <div id="item"></div>
  ```

---

### (5) class 속성 자동 생성

* 기호: `.`

* 예시:

  ```emmet
  span.title
  ```

  → `Tab` →

  ```html
  <span class="title"></span>
  ```

* 태그명을 생략하면 기본값은 `div`

  ```emmet
  .title
  ```

  → `Tab` →

  ```html
  <div class="title"></div>
  ```

---

### (6) 콘텐츠 삽입

* 기호: `{}`
* 예시:

  ```emmet
  p.container{Hello World}
  ```

  → `Tab` →

  ```html
  <p class="container">Hello World</p>
  ```

---

### (7) 자동 넘버링

* 기호: `$`
* 예시:

  ```emmet
  p.container{Item $}*5
  ```

  → `Tab` →

  ```html
  <p class="container">Item 1</p>
  <p class="container">Item 2</p>
  <p class="container">Item 3</p>
  <p class="container">Item 4</p>
  <p class="container">Item 5</p>
  ```

---

## 3. 마무리

* Emmet을 활용하면 **반복적이고 긴 HTML 마크업을 빠르고 편리하게 작성 가능**
* 모든 문법을 외울 필요는 없음
* 필요할 때마다 구글링해서 찾아 쓰다 보면 자주 쓰는 문법은 자연스럽게 익숙해짐
