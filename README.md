# CSS layout class

### CSS 스타일링의 두가지 방식을 배우고 각각의 속성을 활용하기

> - display: flex
> - display: grid

## ✅ flex

![alt text](image-1.png)

- `flex-direction` (default : row)
- `align-items`
- `justify-content`
- `flex-flow`
- `oerder` : 상대적 우선순위 (default: 0 / 수치가 작을수록 우선)
- `align-self`
- `flex-warp`
- `align-content`
- `flex` : flex-grow | flex-shrink | flex-basis
  <br/> | 요소 면적 확장 비율 (default: 0)
  <br/>| 요소 면적 축소 비율 (default: 1 / 0이면 줄어들지 않음 / 수치가 클수록 우선적으로 축소)
  <br/>| 주축의 크기 (max 또는 min으로 활용될 수 있음)

## ✅ grid

![alt text](image-2.png)

-
- `grid-template-columns` : [happy] 1fr [lunch] 2fr [box] 1fr [gift]
- `grid-template-rows`: [won] 200px [en] 60px [doller]
- `grid-row`: 1/-1
- `grid-column`: lunch/gift
- `grid-column`: lunch/gift
- `grid-template-areas`: "셀 명"
  <br> | grid templats area
  <br/>/_ 참고 링크 _/
  <br/>https://github.com/nomadcoders/css-layout-masterclass/commit/11367179c514e3f3b7e58a94c14d39e14b0cd973

```css
<사용 예문>
.grid_container {
  display: grid;
  grid-template-columns: [happy] 1fr [lunch] 2fr [box] 1fr [gift];
  grid-template-rows: [won] 200px [en] 60px [doller];
  row-gap: 10px;
  column-gap: 20px;
}

.grid_box {
  background-color: steelblue;
  color: white;
  text-align: center;
  align-content: center;
}

.grid_box:first-child {
  grid-row: 1/-1;
  /* 라인 숫자로 영역 지정한 경우 */
}
.grid_box:last-child {
  grid-column: lunch/gift;
  /* 라인 이름으로 영역 지정한 경우 */
}


- case01
grid-template-areas: "셀 명";
grid-template-rows: 높이;
grid-template-columns: 너비;

- case02
grid-template : "셀 명"  grid-template-rows 높이 ;
                "셀 명"  grid-template-rows 높이 ;
                "셀 명"  grid-template-rows 높이 / grid-columns 너비;


⚠️ 위의 두 가지 경우 태그에 "셀 명 " 지정해줘야 함
.grid_box {
  grid-area: "셀 명";
}
```
