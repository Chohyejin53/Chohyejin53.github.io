npm다운그레이드 


npm을 강제로 업그레이드 시키는 만행 저지름 
nvm버전을 올리지않고 냅다 npm install npm i -g npm@latest 실행함 (겁도없이)

이 과정에서 node였나 npm의 뭐가 설정이 바뀜 


해결방법 
delete prefix 입력 이후 이래 링크에서 

```
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
```



```
vi ~/.profile
```
profile 제일 하단에 다음 코드를 추가한다.


```
export PATH=~/.npm-global/bin:$PATH
```

:wq 저장 후 변경된 프로필 내용을 적용 해준다.

```
source ~/.profile
```
끝 


이후 실행 
npm install -g npm@6.9.0

npm 다운그레이드 성공 후 
node도 버전을 맞춰주어야하는데, npm 다운그레이드 전에는 버전이 맞지않아서 계속 nvm default로 가있었음
npm 버전이 맞으니 
alias default 명령어도 실행됨!! 

nvm default로 맞춰주고 버전 맞춘다음 실행함!


https://brtech.tistory.com/124

https://www.google.com/search?q=zsh%3A+command+not+found%3A+gulp&sxsrf=ALiCzsZyHPn3rWBs4-jJsdRj3LF2IBAkOw%3A1663747856155&ei=EMcqY9-CCbzQ2roP3aySuAQ&ved=0ahUKEwjfytjft6X6AhU8qFYBHV2WBEcQ4dUDCA4&uact=5&oq=zsh%3A+command+not+found%3A+gulp&gs_lcp=Cgdnd3Mtd2l6EAMyBQgAEIAEMgQIABAeOgoIABBHENYEELADSgQIQRgASgQIRhgAUNEDWNEDYKsGaAFwAXgAgAHYAYgB2AGSAQMyLTGYAQCgAQKgAQHIAQrAAQE&sclient=gws-wiz
