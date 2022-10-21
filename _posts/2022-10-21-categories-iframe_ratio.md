---
title: "[HTML&CSS&SCSS] 비율에 맞추어 크기 조절되는 iframe UI"
excerpt: ""

categories:
  - HTML&CSS&SCSS
tags:
  - [HTML/CSS]

permalink: /HTML&CSS&SCSS/iframe_ratio/

toc: true
toc_sticky: true

date: 2022-10-18
last_modified_at: 2022-10-18
---

## 비율에 맞추어 크기 조절되는 iframe UI 

### style
```sass
.wrap {
    margin: 0 auto;
    min-width: 320px;
    max-width: 750px;
}
.video_wrap {
    margin: 0 auto;
    width: 100%;
    height: auto;
    max-width: 750px;
}
.video_box {
    overflow: hidden; /*비디오 컨텐츠가 넘치는 부분은 잘려나감*/
    position: relative;
    width: 100%;
    height: 100%;
    background-color: #32e664;
    padding-top: 56.25%; /* 부모요소 너비를 기준으로 높이 지정*/
    /* 
    다른  비율 계산 16:9가 아닐 경우, 
    사이즈에 맞게 비율을 조정하는 경우에는 calc로 계산 공식을 입력합니다. 
    padding-top {
        calc(세로/가로)*100
    };
    */
}

.video_box iframe {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
}
```
#### 참고
  
### View 
<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="LYmMQVY" data-user="DDol" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/DDol/pen/LYmMQVY">
  iframe ratio</a> by DDol (<a href="https://codepen.io/DDol">@DDol</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


### Note
1. 비디오를 감싸는 영역에 넘치지 않게 overflow: hidden; 처리해주기
2.  **padding-top**은 부모요소 너비를 기준으로 높이 지정
3. **padding-top**으로 비율에 맞게 크기 줄어들 수 있도록 조정해주기 : `calc(세로/가로) * 100`   
  Ex. iframe = 16:9 비율 >>> 따라서 (9/16) * 100 = 56.25%

### Reference
- https://goddino.tistory.com/181
- https://web-development.space/tools/px-to-vw/ 
- https://jocoma.tistory.com/entry/%EA%B0%80%EB%B3%80-%EA%B7%B8%EB%A6%AC%EB%93%9C
