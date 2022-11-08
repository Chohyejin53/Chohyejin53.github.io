---
title: "[HTML&CSS&SCSS] for문을 활용한 background-image 처리"
excerpt: ""

categories:
  - HTML&CSS&SCSS
tags:
  - [HTML/CSS, sass, scss]

permalink: /HTML&CSS&SCSS/sass_for/

toc: true
toc_sticky: true

date: 2022-11-04
last_modified_at: 2022-11-04
---

## sass for문을 활용한 background-image 처리 
동일한 이미지와 스타일이 반복되는 스타일링 시 for문을 이용해 배경이미지만 교체하도록 코드를 짜는 것이   
불필요한 코드를 줄여 유지보수에 훨씬 유리하다.

### style
```sass
@for $i from 1 through 6 {
    &.img0#{$i} { 
        width: 200px;
        height: 200px;
        background-image:url(../img/img_0#{$i}.png);
        background-size: 200px 200px;
        -webkit-background-size: 200px 200px;
    }
```


### 반복문 `to`와 `througth` 키워드의 차이
1. `@for $i from 1 to $total`  
: to: ~까지 ($total 전 까지)

2. `@for $i from 1 through $total`
: through: ~끝까지 ($total 포함)



### Reference
- https://webclub.tistory.com/178
