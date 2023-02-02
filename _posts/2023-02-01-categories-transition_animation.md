---
title: "[HTML&CSS&SCSS] CSS 트랜지션과 애니메이션"
excerpt: ""

categories:
  - HTML&CSS&SCSS
tags:
  - [HTML/CSS]

permalink: /HTML&CSS&SCSS/transition_animation/

toc: true
toc_sticky: true

date: 2023-02-01
last_modified_at: 2023-02-01
---

## CSS 트랜지션과 애니메이션
: css에서 평소 애니메이션 효과를 줄 때, 트랜지션과 애니메이션을 모두 사용했었는데 어떤 차이가 있는지, 어떤 기준에 따라 사용하는 것이 맞는지에 대해 알아보고자 정리하였다.

### Transition
#### 특징 및  장점 
- 값의 변경을 갑작스럽지 않고 자연스럽고 끊김없게 만들어줄 때 사용
- duration(지속 시간)을 부여하여 속도를 조절

### code 
```css
transition-property: all;
transition: background-color 0.5s linear 0.5s;
```
- transition 적용할 요소, 지속시간, time function, 딜레이 시간
- 0이어도 유닛(s) 꼭 써주기


### Animation 
#### 특징 및 장점 
- 하나의 줄거리(@keyframes)를 구성하여 줄거리 내에서 세부 움직임을 시간 흐름 단위로 제어

#### code
```css
.shake {
  animation: shake 0.7s linear;
}

@keyframes shake {
  0%,
  100% {
    transform: translateX(0);
  }
  10%,
  30%,
  50%,
  70% {
    transform: translateX(-0.4em);
  }
  20%,
  40%,
  60% {
    transform: translateX(0.4em);
  }
  80% {
    transform: translateX(0.3em);
  }
  90% {
    transform: translateX(-0.3em);
  }
}
```
- animation: keyframe이름 지속시간 timing-function 반복횟수;


### Transition과 Animation의 차이 


  
### View 
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="PoBxxLx" data-user="DDol" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/DDol/pen/PoBxxLx">
  transiton/animation</a> by DDol (<a href="https://codepen.io/DDol">@DDol</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### Note
: 간단한 애니메이션의 구현 혹은 상태값에 따른 변경이 필요할 때는 Transition을 사용해도 좋지만, 디테일한 애니메이션의 구현이 필요한 경우 Animation 속성을 이용해 제어하는 것이 좋은 방법이라고 생각된다. 

### Reference
blogId=minhyupp&logNo=222142052947&parentCategoryNo=&categoryNo=46&viewDate=&isShowPopularPosts=true&from=search)
- [https://web-development.space/tools/px-to-vw/ ](https://til.mmyeon.com/animation/)
- [https://jocoma.tistory.com/entry/%EA%B0%80%EB%B3%80-%EA%B7%B8%EB%A6%AC%EB%93%9C](https://velog.io/@hyemz/%EC%9B%B9-%EC%95%A0%EB%8B%88%EB%A9%94%EC%9D%B4%EC%85%98-%EC%8B%9C%EB%8F%84%ED%95%B4%EB%B3%B4%EA%B8%B0)
