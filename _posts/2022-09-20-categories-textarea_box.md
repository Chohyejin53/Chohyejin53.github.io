---
title: "[JQuery] 입력값에 따라 높이 자동 조절되는 textarea"
excerpt: ""

categories:
  - JQuery
tags:
  - [HTML/CSS, JQuery]

permalink: /JQuery/textarea_box/

toc: true
toc_sticky: true

date: 2022-09-20
last_modified_at: 2022-09-20
---

## 입력값에 따라 높이 자동 조절되는 textarea 

### method
- .val(); 
  : 양식(form)의 값을 가져오거나 값을 설정하는 메소드

- this 
  : 
  
- height / scrollHeight
  : 
  
- .css 
  :
 
- .on
  :
 
- .change 
  :
  
- .keydown / .keyup 
  :
  
- .paste
  :
  
- .cut
  :
  
- .html
  :
 
- .length
  :
 
- .substring();
  + 문자열에서 기준없이 사용하고 싶은 문자열을 가져오고 싶을 때 사용하는 메소드
  + 시작 인덱스에서부터 끝 인덱스의 하나 전 인덱스까지 가져옴
  + (참고) 문자열을 가져오는 다른 메소드 : split / substr
  
  ```Javascript
  .class.substring(0,10) // 0번째에서 시작하여 10번째 전(9)까지 (0 : 시작 인덱스 , 10 : 마지막 인덱스)
  ```
  
### view
<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="xxjdLPg" data-user="DDol" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/DDol/pen/xxjdLPg">
  Untitled</a> by DDol (<a href="https://codepen.io/DDol">@DDol</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

###Note
- max-height 를 반드시 넣어주어야함.(height 값을 기준으로 영역이 더 커지지 못하게 하기 때문)
