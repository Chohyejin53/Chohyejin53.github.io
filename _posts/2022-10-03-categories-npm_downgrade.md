---
title: "[GIT&GITHUB] npm다운그레이드"
excerpt: ""

categories:
  - GIT&GITHUB
tags:
  - [git, npm, nvm]

permalink: /GIT&GITHUB/npm_downgrade/

toc: true
toc_sticky: true

date: 2022-10-03
last_modified_at: 2022-10-03
---

## npm다운그레이드 

npm을 강제로 업그레이드 시키는 만행 저지름 
nvm버전을 올리지않고 냅다 npm install npm i -g npm@latest 실행함 (겁도없이)
sudo도 입력했던거같고,,, 무튼 아주 강력한 명령어를 통해 되돌릴 수 없게 됨

이 과정에서 node였나 npm의 뭐가 설정이 바뀜 

### 오류 문구 

오류 문구는 다음과 같다.

```
ERRER: npm is known not to run on Node.js v10.16.1
You'11 need to upgrade to a newer Node.js v10.16.1
version of npm. You can find the latest version at https://nodejs.org/
nvm is np compatible with the npm config "prefix" option: currently set to ""
Run `npm config delete prefix` or `nvm use --delete-prefix v10.16.1 --silent` to unset it.
```

system 에 버전이 고정되어있는 문제도 함께 나타났다.

```
nvm alias default 10.16.0
nvm ls 
      v10.15.3
      v10.16.0
      v10.16.1
  ->  system
```


### 해결방법 

1. delete prefix 입력 이후 이래 코드 입력해준다.
  ```
  mkdir ~/.npm-global
  npm config set prefix '~/.npm-global'
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
npm install -g npm@6.9.0

npm 다운그레이드 성공 후 
node도 버전을 맞춰주어야하는데, npm 다운그레이드 전에는 버전이 맞지않아서 계속 nvm default로 가있었음
npm 버전이 맞으니 
alias default 명령어도 실행됨!! 

nvm default로 맞춰주고 버전 맞춘다음 실행함!


### Reference
https://brtech.tistory.com/124

https://www.google.com/search?q=zsh%3A+command+not+found%3A+gulp&sxsrf=ALiCzsZyHPn3rWBs4-jJsdRj3LF2IBAkOw%3A1663747856155&ei=EMcqY9-CCbzQ2roP3aySuAQ&ved=0ahUKEwjfytjft6X6AhU8qFYBHV2WBEcQ4dUDCA4&uact=5&oq=zsh%3A+command+not+found%3A+gulp&gs_lcp=Cgdnd3Mtd2l6EAMyBQgAEIAEMgQIABAeOgoIABBHENYEELADSgQIQRgASgQIRhgAUNEDWNEDYKsGaAFwAXgAgAHYAYgB2AGSAQMyLTGYAQCgAQKgAQHIAQrAAQE&sclient=gws-wiz
