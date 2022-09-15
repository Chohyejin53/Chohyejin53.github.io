---
title: "[JQuery] GSAP"
excerpt: ""

categories:
 - JQuery
tags:
  - [JQuery, GSAP]

permalink: /JQuery/gsap_scrollmagic/

toc: true
toc_sticky: true

date: 2022-09-15
last_modified_at: 2022-09-15
---


## GSAP
- GrennSock에서 만든 자바스크립트 애니메이션 라이브러리.  
- 일반적인 애니메이션 효과는 CSS나 제이쿼리를 통해 처리하지만, 더 복잡하고 정교한 애니메이션 구현을 위해 GSAP을 사용함.  
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

## GSAP Usage

### Tween
: Tween은 모든 애니메이션이 작동하는 역할을 말함. 
  고성능 속성 설정기라고 생각할 것.
   targets (애니메이션을 적용하려는 개체),duration, properties(속성)을 입력하고 재생 헤드가 새 위치로 이동할 때 해당 지점에서 속성 값이 무엇인지 파악하여 그에 따라 적용하는 원리.


### gsap Methods   
: Tween을 만드는 방법 (이 모든 방법은 Tween 인스턴스를 반환함) 

1. gsap.to( )
: 지정한 속성까지(종료 값) 애니메이션 실행
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="wvwEOZL" data-user="GreenSock" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/GreenSock/pen/wvwEOZL">
  GSAP Basic Tween</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
2. gsap.from( )  
: 시작 값을 설정하여 애니메이션 실행
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="XWrGqvX" data-user="GreenSock" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/GreenSock/pen/XWrGqvX">
  GSAP Basic From Tween</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

3. gsap.fromTo( )  
: 시작값과 종료 값을 지정하여 애니메이션 실행
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="NWKJzRV" data-user="GreenSock" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/GreenSock/pen/NWKJzRV">
  GSAP Basic fromTo Tween</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

※ [더 많은 예제 보러가기](https://greensock.com/docs/v3/GSAP/gsap.from())


### Tween Methods
: 아직 공부못함



## Example

## 참고
- [greensock](https://greensock.com/) 

- [Getting Started : How to use ScrollMagic - github](https://github.com/janpaepke/ScrollMagic/wiki/Getting-Started-:-How-to-use-ScrollMagic)
- [맑은 웹퍼블리싱 블로그](https://www.biew.co.kr/entry/TweenMax%E3%86%8DGSAP-%ED%8A%B8%EC%9C%88%EB%A7%A5%EC%8A%A4-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EB%B0%B0%EC%9A%B0%EA%B8%B0-%EA%B8%B0%EC%B4%881GSAP-%EB%A9%94%EC%84%9C%EB%93%9C?category=314309)
