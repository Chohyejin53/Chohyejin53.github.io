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
last_modified_at: 2022-10-17
---

## Tap 전환 UI
메뉴 버튼을 클릭하면 컨텐츠 내용이 메뉴에 따라 바뀌는 UI구현

### method / event  

#### const
: (ES6) 
- const는 상수(변하지 않는 값)를 위해 사용
- 변수 재할당 금지
- 객체 타입 변수 선언 시 const를 사용 지향

- 참고 
  - var : (ES5) 
    - 변수를 선언하는 유일한 방법 
    - 함수 레벨 스코프(Function-level scope)
    - var 키워드 생략가능 (암묵적 전역변수 생산가능성의 문제)
    - 변수 중복 선언 허용 
    - 변수 호이스팅

  - let : (ES6) 
    - 함수 레벨 스코프(Function-level scope)를 따르는 자바스크립트에서, `**블록 레벨 스코프(Block-level scope)**`를 따르는 변수를 선언하기 위해 let 키워드 사용.
    - let 키워드로 선언된 변수는 선언 단계와 초기화 단계가 분리되어 진행
    - 변수 중복선언 금지
    - 변수 재할당이 자유로움
    - 호이스팅 가능
  
  - 정리
  1.  ES6를 사용한다면 var 키워드는 사용하지 않는다.
  2. 재할당이 필요한 경우에 한정해 let 키워드를 사용한다. 이때 변수의 스코프는 최대한 좁게 만든다.
  3. 변경이 발생하지 않는(재할당이 필요 없는 상수) 원시 값과 객체에는 const 키워드를 사용한다. const 키워드는 재할당을 금지하므로 var, let 보다 안전하다.
  
#### .index() 
:   선택된 해당요소의 index 값을 반환   
:   같은 레벨에서 몇번째 요소인지 찾을 떄 사용  

#### .eq()
: 선택한 요소의 인덱스 번호에 해당하는 요소를 반환  
  (숫자는 0 부터 시작함, 마이너스 값이 있다면, 역순)


  ※ .eq()와 .get()의 차이 
  둘다 선택한 요소중 N번째요소를 반환하지만,  
  불러오는 방식으로 eq()의 경우 jQuery객체로 반환하며, get()은 DOM 개체로 반환합니다. 전자는 jQuery 매서드로 사용가능하지만, 후자는 불가능하다.

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
- https://poiemaweb.com/es6-block-scope
- https://log.designichthus.com/m/61
- https://mylife365.tistory.com/m/221

