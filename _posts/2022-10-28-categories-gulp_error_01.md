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



### 오류 문구 

오류 문구는 다음과 같다.

```
zsh: command not found: gulp
```

gulp를 찾을 수 없다는 에러가 나왔다. 

  
### 해결방법 

1. delete prefix 입력 이후 이래 코드 입력해준다.
  ```
  npm i gulp-cli--save--dev
  ```

  ```
  vi ~/.profile
  ```

2. profile 제일 하단에 다음 코드를 추가한다.
  ```
  export PATH=~/.npm-global/bin:$PATH
  ```

3. :wq 저장 후 변경된 프로필 내용을 적용 해준다.
  ```
  source ~/.profile
  ```

4. 끝 


### 이후 실행 
`npm i` 설치 한번 더 해주고 `gulp` 실행하기 


### Reference
- https://haeguri.github.io/2019/03/31/introduction-gulp/
- https://ithub.tistory.com/165