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
입력 값에 따라 글자를 카운트 하여 100자 이내의 텍스트만 입력가능하고, 텍스트영역이 한줄에서 여러줄로 가변되는 UI 구현.


### method / event

#### this 
: 변수, 선택자의 역할을 함
  
#### height(); / scrollHeight(); 
- height();
  : 요소의 높이 값을 반환

- scrollHeight(); 
  : scroll되어 나타나는 부분까지 높이 값 반환
  
 ※ height/innerHeight 와 scrollHeight와 차이
 : height/innerHeight는 가시화면에 해당하는 높이 값을 반환하지만, scrollHeight는 스크롤되어 나타는 영역, 즉 overflow: scroll / overflow-y: auto 처리되는 부분까지의 높이를 반환함
 
#### .css();  
: 선택한 요소의 css 속성값을 가져오거나 style 속성 추가

```javascript

$( ".textarea_box" ).css( "background-color" ); // .textarea_box의 background-color 속성값을 가져옴
$( ".textarea_box" ).css( "background-color", "green" ); // .textarea_box의 background-color 속성 값을 추가하여 스타일 변경

```
 
#### .on(); 
: jQuery는 특정 요소에 이벤트 바인딩(event binding)하기 위해 사용

- 기본형  

  ```javascript

    $("p").on("click", function(){
   alert("문장이 클릭되었습니다.");
  });

  ```
- 이벤트 핸들러 하나에 여러 이벤트 설정  
  
  ```javascript

  $("p").on("change keydown keyup", function() {  // change keydown keyup 의 요소변경 이후에 이벤트 발생
  });
  
  ```

- 특징
1. 선택한 요소에 모든 타입의 이벤트 연결 가능
2. 하나의 이벤트 핸들러에 여러 개의 이벤트를 동시에 연결 가능
3. 선택한 요소에 여러 개의 이벤트 핸들러와 여러 개의 이벤트를 같이 연결 가능
4. 사용자 지정 이벤트(custom event)를 위해 이벤트 핸들러로 데이터를 넘길 수 있음
5. 차후에 다루게 될 요소를 이벤트에 바인딩 가능

+ (참고) 관련 이벤트 바인딩 메소드 : .off() / .one() 

#### .change();  
: 요소 변경이 끝난 후 발생, 텍스트 입력 요소인 경우에는 요소 변경이 끝날 때가 아니라 포커스를 잃을 때 이벤트 발생
  
#### .keyup(); / .keydown(); 
- .keyup();  
  : 키보드를 누른 이후에 실행
- .keydown();  
  :  키보드를 눌렀을 때 실행 (누르고 있는 한번만 실행)
  
+ (참고) 관련 키보드 이벤트 : .keypress (키보드를 눌렀을 때 실행, 키보드를 누르고 있을떄 계속해서 실행)
  
#### .cut(); / .paste();
: 각각 값을 잘라내기, 붙여넣기 할 때 발생하는 이벤트
  
  
#### .html(); 
: 선택한 요소 안의 내용을 가져오거나, 다른 내용으로 수정

+ (참고) 
    = .text()와 비슷하지만 태그의 처리에 차이가 있음

```javascript

var test = $( 'h1' ).html(); // <h1> 요소의 내용을 test 변수에 저장
.html( htmlString ) // htmlString로 텍스트 내용 수정

```

#### .val(); 
: 양식(textarea)의 값을 가져오거나 값을 설정하는 메소드
 
#### .length(); 
: 선택한 요소의 개수를 반환
 
#### .substring();
  + 문자열에서 기준없이 사용하고 싶은 문자열을 가져오고 싶을 때 사용하는 메소드
  + 시작 인덱스에서부터 끝 인덱스의 하나 전 인덱스까지 가져옴
  + (참고) 
    = html에서 textareadml maxlenth 속성을 사용하여 글자 수를 제한하는 방법도 있음
    = 문자열을 가져오는 다른 메소드 : split / substr  
    
```Javascript

.class.substring(0,10); // 0번째에서 시작하여 10번째 전(9)까지 
                        // (0 : 시작 인덱스 , 10 : 마지막 인덱스)

```
  
### View
<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="xxjdLPg" data-user="DDol" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/DDol/pen/xxjdLPg">
  Untitled</a> by DDol (<a href="https://codepen.io/DDol">@DDol</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### Note
- 구현한 부분의 3가지 핵심
  1. 텍스트 입력 양에 따라 1-3줄 가변
  2. 3줄이 넘어갈 때, scroll 생성
  3. 글자수 100자 제한  
    
- max-height 를 반드시 넣어주어야함.(height 값을 기준으로 영역이 더 커지지 못하게 하기 때문)
- textarea에 'resize: none;'을 넣어주어 사이즈 조절 방지 

### 참고
- http://daplus.net/jquery-overflow-hidden-%EB%98%90%EB%8A%94-overflow-scroll-div%EC%9D%98-%EC%8B%A4%EC%A0%9C-height-%EB%8A%94-%EC%96%B4%EB%96%BB%EA%B2%8C-%EC%96%BB%EC%8A%B5%EB%8B%88%EA%B9%8C/
- https://wonjuman.tistory.com/20
