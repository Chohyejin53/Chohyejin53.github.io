---
title: "[JQuery] GSAP"
excerpt: ""

categories:
 - JQuery&Javascript
tags:
  - [JQuery, GSAP]

permalink: /JQuery&Javascript/gsap_basic/

toc: true
toc_sticky: true

date: 2022-09-15
last_modified_at: 2022-09-15
---


## GSAP
- GrennSock에서 만든 **자바스크립트 애니메이션 라이브러리**.  
- 일반적인 애니메이션 효과는 CSS나 제이쿼리를 통해 처리하지만, 더 복잡하고 정교한 애니메이션 구현을 위해 GSAP을 사용함.  
- 프론트엔드 개발자들에게 각광받는 라이브러리.
- GSAP는 제이쿼리보다 20배 이상 퍼포먼스가 좋다고 알려져 훨씬 디테일한 애니메이션 작업이 가능함.
- 유료 라이브러리이나, 일부 무료 플러그인을 지원  


## Setting

### CDN
```html
 <script src="https://code.jquery.com/jquery-2.2.4.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/gsap/2.1.3/TweenMax.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.5/plugins/animation.gsap.js"></script>
```

스크립트 순서대로 cdn 경로 입력해주기
1. 제이쿼리 cdn 경로 
2. GSAP TweenMax 플러그인 cdn 경로
3. GSAP 플러그인 cdn 경로


### Download 
[GSAP Installation-download](https://greensock.com/docs/v3/Installation/download)    

1. zip 파일 설치 
2. html에 경로 입력  

```html
<script src = "/[YOUR_DIRECTORY]/gsap.min.js" ></script> 
```

### npm install
[GSAP Installation - npm](https://greensock.com/docs/v3/Installation/#npm-club) 에서 설치 방법 확인하기 


## Tween
: Tween은 모든 애니메이션이 작동하는 역할을 말함. 
  고성능 속성 설정기라고 생각할 것.
   targets (애니메이션을 적용하려는 개체),duration, properties(속성)을 입력하고 재생 헤드가 새 위치로 이동할 때 해당 지점에서 속성 값이 무엇인지 파악하여 그에 따라 적용하는 원리.

## Syntax  
```Javascript
gsap.to(".box", {x:200}) 
     |     |        |
 method  target    variables
```

- The target (or targets)
: 애니메이션을 적용하려는 개체 

- 



## Methods   
: Tween을 만드는 방법 (이 모든 방법은 Tween 인스턴스를 반환함) 


### gsap.to( )
: 지정한 속성까지(종료 값) 애니메이션 실행
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="wvwEOZL" data-user="GreenSock" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/GreenSock/pen/wvwEOZL">
  GSAP Basic Tween</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>  

### gsap.from( )  
: 시작 값을 설정하여 애니메이션 실행
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="XWrGqvX" data-user="GreenSock" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/GreenSock/pen/XWrGqvX">
  GSAP Basic From Tween</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### gsap.fromTo( )  
: 시작값과 종료 값을 지정하여 애니메이션 실행
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="NWKJzRV" data-user="GreenSock" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/GreenSock/pen/NWKJzRV">
  GSAP Basic fromTo Tween</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### gsap.set()
: 중간의 과정이 없이 바로 애니메이션 이동 후의 결과값을 보여줌 




### etc
※ [더 많은 Methods 보러가기](https://greensock.com/docs/v3/GSAP/gsap.from())


## application
: gsap의 애니메이션은 원하는 속도로 원하는만큼 지정한 시간동안 실행시킬 수 있음. 이 과정이 쉽게 제어되기 때문에, 다양한 스크롤이벤트와 함께 적용하여 다양한 인터렉션을 구현할 수 있음

## Reference
- [greensock docs](https://greensock.com/)
- [Getting Started : How to use ScrollMagic - github](https://github.com/janpaepke/ScrollMagic/wiki/Getting-Started-:-How-to-use-ScrollMagic)
- [맑은 웹퍼블리싱 블로그](https://www.biew.co.kr/entry/TweenMax%E3%86%8DGSAP-%ED%8A%B8%EC%9C%88%EB%A7%A5%EC%8A%A4-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EB%B0%B0%EC%9A%B0%EA%B8%B0-%EA%B8%B0%EC%B4%881GSAP-%EB%A9%94%EC%84%9C%EB%93%9C?category=314309)
- [퍼블리셔와 개발자사이 블로그](https://lpla.tistory.com/106)
