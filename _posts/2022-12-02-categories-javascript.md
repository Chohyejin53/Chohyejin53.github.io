---
title: "[Javascript] 자바스크립트"
excerpt: ""

categories:
  - HTML&CSS&SCSS
tags:
  - [HTML/CSS, SASS, Javascript]

permalink: /Javascript/responsive_mobile_vh/

toc: true
toc_sticky: true

date: 2022-11-11
last_modified_at: 2022-11-11
---

## 모바일 브라우저 100vh 오류

### 오류 상황 
반응형 페이지 구현 시 모바일 기기에서 100vh가 제대로 적용되지않는 이슈가 있다. 


### 해결방법 
1. javascript로 vh 속성을 재설정해준다. 
```javascript
function setScreenSize() {
            let vh = window.innerHeight * 0.01;
            document.documentElement.style.setProperty('--vh', `${vh}px`);
        }
        setScreenSize();
        window.addEventListener('resize', setScreenSize);
```

2. sass에 코드를 추가해 height 값을 수정해준다. 
```sass
  .wrap {
    height: calc(var(--vh, 1vh) * 100);
  }
   
```

3. 추가로 노치 영역도 대응해주어 사용자가 이용시 콘텐츠를 가리지않도록 작업해준다.
```
  .wrap {
      padding-bottom: calc(constant(safe-area-inset-bottom) + 10px);
      padding-bottom: calc(env(safe-area-inset-bottom) + 10px);}
  }
```


### Note
모바일 환경에서는 상하단 url/nav바, 카카오 인 앱 등 체크하고 대응해야하는 부분이 많다.
꼼꼼히 검수하고 대응해 사용자 친화적 페이지를 구현해야할 필요가 있다.  

### Reference
- https://url.kr/ozh5cw
- https://abcdqbbq.tistory.com/92
