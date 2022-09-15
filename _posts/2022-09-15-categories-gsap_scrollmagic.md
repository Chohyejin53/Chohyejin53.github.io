---
title: "[JQuery] GSAP을 이용한 Scroll Magic"
excerpt: ""

categories:
  - JQuery
tags:
  - [JQuery, GSAP, scroll-event]

permalink: /JQuery/gsap_scrollmagic/

toc: true
toc_sticky: true

date: 2022-09-15
last_modified_at: 2022-09-15
---

## GSAP
- GrennSock에서 만든 자바스크립트 애니메이션 라이브러리.  

## Scroll Magic
: 스크롤 이벤트를 활용하기에 좋은 라이브러리로 스크롤이벤트보다 간편하게 다양한 모션을 적용할 수 있음

## Setting

### CDN
```html
 <script src="https://code.jquery.com/jquery-2.2.4.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.7/ScrollMagic.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.7/plugins/debug.addIndicators.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/gsap/2.1.3/TweenMax.min.js"></script>
 <script src="//cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.5/plugins/animation.gsap.js"></script>
```

스크립트 순서대로 cdn 경로 입력해주기
1. 제이쿼리 cdn 경로 
2. 스크롤매직 플러그인 cdn 경로
3. 스크롤매직 인디케이터 가이드 표현
4. GSAP TweenMax 플러그인 cdn 경로
5. GSAP 플러그인 cdn 경로


### Download 
[GSAP Installation-download](https://greensock.com/docs/v3/Installation/download)    
[scrollmagic Installation](http://scrollmagic.io/#get-it-now)  


1. zip 파일 설치 
2. html에 경로 입력  

```html
<script src = "/[YOUR_DIRECTORY]/gsap.min.js" ></script> 
```

### npm install
[GSAP Installation - npm](https://greensock.com/docs/v3/Installation/#npm-club) 에서 설치 방법 확인하기 
[scrollmagic Installation - npm](http://scrollmagic.io/)



## Scroll Magic Usage

### 
```html
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
        .addIndicators({ //indicator 추가 (디버깅 후 삭제)
        name: "1"
        });

    }())
```

## More Example

[scrollmagic 공식 사이트](http://scrollmagic.io/examples/index.html)




## 참고
- [greensock](https://greensock.com/) 
- [스크롤매직라이브러리-nana_log](https://nykim.work/30?category=692676)
- [Getting Started : How to use ScrollMagic - github](https://github.com/janpaepke/ScrollMagic/wiki/Getting-Started-:-How-to-use-ScrollMagic)
- [맑은 웹퍼블리싱 블로그](https://www.biew.co.kr/entry/TweenMax%E3%86%8DGSAP-%ED%8A%B8%EC%9C%88%EB%A7%A5%EC%8A%A4-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EB%B0%B0%EC%9A%B0%EA%B8%B0-%EA%B8%B0%EC%B4%881GSAP-%EB%A9%94%EC%84%9C%EB%93%9C?category=314309)
