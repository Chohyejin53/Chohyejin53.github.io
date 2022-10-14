---
title: "[JQuery] Tap 전환 UI"
excerpt: ""

categories:
  - JQuery
tags:
  - [HTML/CSS, JQuery]

permalink: /JQuery/tap_switch/

toc: true
toc_sticky: true

date: 2022-10-12
last_modified_at: 2022-10-14
---

## Tap 전환 UI
메뉴 버튼을 클릭하면 컨텐츠 내용이 메뉴에 따라 바뀌는 UI구현

### method / event  

#### const
: text  

- 참고 
  - var
  - let
  
#### .index()
: text  

#### .eq()
: text  

- 참고 
  - :lt()
  - :gt()

  
### View 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="GRdwLvp" data-user="DDol" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/DDol/pen/GRdwLvp">
  tap_switch</a> by DDol (<a href="https://codepen.io/DDol">@DDol</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


### Note
1. 클릭했을 때, 이벤트 발생 
2. 탭의 인덱스 값을 받아오기 
3. 모든 탭의 활성화 클래스 제거 
4. **클릭하여 받아온 인덱스 값에 해당하는 탭만 활성화 클래스 추가해주기**

### Reference
