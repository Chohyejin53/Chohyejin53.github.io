---
title: "[GIT&GITHUB] npm install gulp 오류"
excerpt: ""

categories:
  - GIT&GITHUB
tags:
  - [git, node, gulp, npm]

permalink: /GIT&GITHUB/gulp_error_01/

toc: true
toc_sticky: true

date: 2022-10-28
last_modified_at: 2022-10-28
---

## npm install gulp 오류 
node 버전 확인 후 npm 설치를 진행했다.  
npm install 후 정상적으로 node modules 설치가 된 것을 확인했다. 
그리고 gulp 실행결과 오류가 발생했다. 

결과적으로,  
원인은 gulp의 로컬 설치가 되어있지않았다.   
해결은 gulp를 글로벌로 설치해주어 오류를 해결했다. 
  
### 오류 문구 

오류 문구는 다음과 같다.
```
zsh: command not found: gulp
```
  
gulp를 찾을 수 없다는 에러가 나왔다. 

  
### 해결방법 

1. gulp-cli 설치를 진행한다. 
  ```
  npm i gulp-cli--save--dev
  ```
   > **gulp-cli**  
    Gulp를 콘솔에서 편리하게 실행할 수 있게 해주는 유틸리티 도구
      
   > **--save--dev**  
    `npm install [모듈이름] --save`  
    : package.json에는 설치한 모듈과 버전이 기록 (=dependencies 항목 : 프로젝트에 연관된 모듈들의 목록을 포함)  
    `v--save` 과 `--save--dev` 옵션의 차이  
    : 제품의 릴리즈나 구동시 꼭 필요한 모듈의 경우 --save 옵션 사용 | dependencies 항목에 기록  
      제품의 개발시에 테스트를 위해서 필요 && 실제 릴리즈시에는 필요없는 모듈의 경우 --save-dev 옵션 |  devDependencies 항목에 기록
  
2. 그리고 나서 다음과 같은 명령어가 출력된다.   
   CLI 버전이 2.3.0 으로 설치된 것을 확인할 수있다.  
   그러나 로컬 버전은 확인 할 수 없다.  
  ```
  + gulp-cli@2.3.0
  add 3 packages from 2 contributors in 4,1565
  ...
  run `npm fund` for details 
  ```
  

3. gulp 버전을 확인해본다. 
  ```
  gulp -v
  ```
    
4. gulp 명령어를 찾을 수 없다는 오류가 다시 뜬다. 
  ```
  zsh command not found: gulp
  ```


5. 이번에는 gulp를 글로벌로 전역설치를 진행한다.
  ```
  npm install gulp -g
  ```

6. 다시 걸프 버전을 확인한다. 
  ```
  gulp -v
  ```

7. 그리고 걸프 버전이 로컬에서 제대로 설치되었는지 확인한다. 
   CLI 와 Local 각각 버전정보가 출력된다. 
  ```
  CLI version: 2.3.0 
  Local version: 4.0.2
  ```

8. 끝


### 이후 실행 
이후 혹시 몰라 `npm i` 설치 한번 더 해주고 `gulp` 실행하여 작업 진행.



### Note
지금 사용 중인 node / gulp / webpack에 대해 좀 더 공부해야겠다. 
용어적이해가 부족한 것 같다.

### Reference
- https://haeguri.github.io/2019/03/31/introduction-gulp/
- https://ithub.tistory.com/165
- https://ingorae.tistory.com/1754
