# HTML 표(Table) 태그 학습

이번 시간에는 **표 태그**에 대해 살펴보겠습니다.  

---

## 1. 표의 기본 구조

- `<table>` : 표 전체  
- `<tr>` : 행(Row)  
- `<td>` : 일반 셀(Cell, Data)  
- `<th>` : 제목 셀(Header)

예시: 3행 3열 표
```html
<table>
  <tr>
    <th>이름</th>
    <th>취미</th>
    <th>특기</th>
  </tr>
  <tr>
    <td>홍길동</td>
    <td>무술</td>
    <td>국지법</td>
  </tr>
  <tr>
    <td>김코딩</td>
    <td>코딩</td>
    <td>디버깅</td>
  </tr>
</table>
````

---

## 2. 표에 테두리와 스타일 적용하기

* 예전에는 `<table border="1">` 같은 속성을 썼지만, 이는 **웹 표준에 맞지 않음**
* 대신 **CSS**를 사용해야 함

```html
<style>
  table, th, td {
    border: 1px solid black;
    border-collapse: collapse; /* 겹치는 선을 하나로 */
  }
  th, td {
    padding: 8px;
    text-align: center;
  }
</style>
```

---

## 3. 표의 주요 태그

### (1) `<caption>`

* 표의 제목/설명을 넣을 때 사용

```html
<table>
  <caption>학생 성적표</caption>
</table>
```

---

### (2) `<thead>`, `<tbody>`, `<tfoot>`

* **그룹화 태그**

  * `<thead>` : 표의 머리글 영역
  * `<tbody>` : 표의 본문 영역
  * `<tfoot>` : 표의 바닥글 영역

```html
<table>
  <thead>
    <tr>
      <th>이름</th><th>국어</th><th>수학</th><th>영어</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>홍길동</td><td>90</td><td>95</td><td>88</td>
    </tr>
    <tr>
      <td>김코딩</td><td>85</td><td>92</td><td>81</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>평균</td><td>87.5</td><td>93.5</td><td>84.5</td>
    </tr>
  </tfoot>
</table>
```

---

### (3) `<colgroup>`, `<col>`

* 열(Column) 단위 스타일 적용 가능

```html
<table>
  <colgroup>
    <col style="width:100px;">
    <col style="background-color:yellow;">
    <col>
  </colgroup>
  <tr>
    <th>이름</th><th>국어</th><th>수학</th>
  </tr>
  <tr>
    <td>홍길동</td><td>90</td><td>95</td>
  </tr>
</table>
```

---

## 4. 병합 속성

* `rowspan` : 행(Row) 병합
* `colspan` : 열(Column) 병합

```html
<table border="1">
  <tr>
    <th rowspan="2">이름</th>
    <th colspan="2">점수</th>
  </tr>
  <tr>
    <th>국어</th>
    <th>영어</th>
  </tr>
  <tr>
    <td>홍길동</td>
    <td>90</td>
    <td>95</td>
  </tr>
</table>
```

---

## 5. 정리

* `<table>` : 표 전체
* `<tr>` : 행
* `<th>` : 제목 셀
* `<td>` : 일반 데이터 셀
* `<caption>` : 표 제목
* `<thead>`, `<tbody>`, `<tfoot>` : 영역 그룹화
* `<colgroup>`, `<col>` : 열 단위 스타일 지정
* `rowspan`, `colspan` : 셀 병합
