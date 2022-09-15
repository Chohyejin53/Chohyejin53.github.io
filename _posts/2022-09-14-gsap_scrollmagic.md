---
title: "[JQuery] GSAP을 이용한 Scroll Magic"
excerpt: ""

categories:
  - JQuery
tags:
  - [JQuery, GSAP, scroll-event]

permalink: /categories4/gsap_scrollmagic/

toc: true
toc_sticky: true

date: 2022-09-14
last_modified_at: 2022-09-14
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
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.7/ScrollMagic.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.7/plugins/debug.addIndicators.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/gsap/2.1.3/TweenMax.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.5/plugins/animation.gsap.js"></script>
```

### Download
https://greensock.com/docs/v3/Installation/#npm-club

### npm install

스크립트 순서대로 cdn 경로 입력해주기
1. 제이쿼리 cdn 경로 
2. 스크롤매직 플러그인 cdn 경로
3. 브라우저에 인디케이터 가이드 표현
4. GSAP 중 TweenMax 플러그인 cdn 경로
5. 에니메이션 구현을 위한 GSAP 

## Option

```
<script>

    (function () {

    var controller = new ScrollMagic.Controller(); // 1. ScrollMagic 컨트롤러 생성

    var tweenYoyo = TweenMax.fromTo("#animate1", 0.6, { //2. animation object 생성
        backgroundColor: "#666",
        scale: 1,
    }, {
        scale: 2.5,
        backgroundColor: "#dc143c",
        x: 100,
        rotation: 360,
        repeat: -1,
        yoyo: true
    })

    var scene = new ScrollMagic.Scene({ //3. Scene object 생성
        triggerElement: "#trigger1", //스크롤 애니메이션 시작 지점 설정
        duration: 150 //애니메이션 재생 시간 '100%'지정하면 화면 높이에 따라 유동적으로 end위치가 정해짐
        })
        .setTween(tweenYoyo) //4. 2번을 3번에 추가
        .addTo(controller) //5. 1번(controller)을 3번에 추가
        .addIndicators({ //indicator 추가 
        name: "1"
        });

    }())
```

## Example
http://scrollmagic.io/examples/index.html




## 참고
https://frontdev.tistory.com/entry/Greensock-GreenSock-ScrollTrigger-%ED%94%8C%EB%9F%AC%EA%B7%B8%EC%9D%B8
https://frontdev.tistory.com/entry/Greensock-GreenSock-ScrollTrigger-%ED%94%8C%EB%9F%AC%EA%B7%B8%EC%9D%B8
https://nykim.work/30?category=692676
https://github.com/janpaepke/ScrollMagic/wiki/Getting-Started-:-How-to-use-ScrollMagic
