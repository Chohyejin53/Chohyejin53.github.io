---
title: "[GITHUB] MarkDown Language"
excerpt: "MarkDown Language"

categories:
  - GIT&GITHUB
tags:
  - [github, markdown]

permalink: /GIT&GITHUB/markdown_language/

toc: true
toc_sticky: true

date: 2022-09-05
last_modified_at: 2022-09-08
---

##  MarkDown Language
Markdown은 텍스트 기반의 마크업언어.
HTML로 변환이 가능.
github의 README.md의 경우 마크다운언어로 작성되며, 최근 협업도구에서도 많이 사용되고 있음. 
github blog와 Readme 파일을 작성할 때 많이 사용되기 때문에 정리를 해두는 것이 좋을 것 같다.


##  MarkDown 장점 
<ol>
  <li>간결성.</li>
  <li>text로 저장되기떄문에 용량이 적음.</li>
  <li>지원하는 프로그램과 플랫폼의 다양성.</li>
</ol>

##  MarkDown 단점  
<ol>
  <li>표준이 없음</li>
  <li>모든 HTML 마크업을 대신할 수 없음.</li>
</ol>


##  MarkDown Language Syntax

### Header
 - 제목은 ```<h1>``` ~ ```<h6>``` 까지 "#"의 개수로 표현
 - `=` `-` 사용

        # <h1> 
        ## <h2>
        ### <h3>
        #### <h4>
        ##### <h5>
        ###### <h6>     

        h1 text
        ===
        h2 text 
        ----
    


###  BlockQuote
   인용문자는 ```>``` 를 이용
    
    > blockqute test.
    >> blockqute test.
    >>> blockqute test.

###  List
  - 순서있는 목록 : ```숫자 + .``` 
  - 순서없는 목록 : ```*```,```+``` ,``` -``` 지원 / 혼합하여 사용가능  
  - 체크박스 : ``` [x] + 텍스트  ``` / ``` [ ] + 텍스트  ```

        1. list test
        2. list test
        3. list teset


        * list test
          * list test
            * list test
        - list test
          - list test
            - list test
        + list teset
          + list teset
            + list teset
            + list teset

        - [x] list teset
        - [x] list teset
        - [ ] list teset

    결과물 :
       1. list test
       2. list test
       3. list teset


      * list test
        * list test
          * list test
      - list test
        - list test
          - list test
      + list teset
        + list teset
          + list teset
          + list teset

      - [x] list teset
      - [x] list teset
      - [ ] list teset


###  Code blocks  
  ####  코드 인용방법
  1. 들여쓰기 (※ 코드의 시작과 끝에 한줄 비우기!!)
  2. ` <pre><code>{code}</code></pre>` 
  3. ` ~~~ ` 
  4. ` ``` ` (코드블럭)
  5. ` `` ` (인라인코드블럭)

  ####  언어에 따른 코드 문법 강조표시 
  코드에 사용된 언어를 ` ``` ` 바로 뒤에 기입하여 사용 

    ``` javascript
    const body = document.querySelector("body");
    
    const IMG_NUMBER = 5;
    
    function randomNumber(){ //랜덤숫자 생성
      return Math.ceil((Math.random()*IMG_NUMBER));
    }

    init();
    
 결과물 :  
  const body = document.querySelector("body");

  const IMG_NUMBER = 5;

  function randomNumber(){ //랜덤숫자 생성
    return Math.ceil((Math.random()*IMG_NUMBER));
  }

  init();  

  
###  수평선 
   
    * * *
    ***
    *****
    - - -
    ---------------------------------------

  결과물 :
  * * *
  ***
  *****
  - - -
  ---------------------------------------
  
###  Link
  
  1. 참조링크 
      
    ['naver'](http://www.naver.com/)
    
   결과물 : ['naver'](http://www.naver.com/)  
   
  2. 외부링크
  
    ['naver'](http://www.naver.com/){: target="_blank" }
  
  결과물 : ['naver'](http://www.naver.com/){: target="_blank" }  
  
  3. url 링크
    
    naver: <http://www.naver.com/>
  
  결과물 : naver: <http://www.naver.com/>  
  
  4. 내부링크 
  html 코드의 idf를 통해 내부링크가 사용가능함
  
  ``` html
    <div id="index">목차</div>
  ```  
  ```
    [링크](#id)
  ``` 

###  emophasis

    *single asterisks*
    _single underscores_
    **double asterisks**
    __double underscores__
    ~~cancelline~~
      
  결과물 :

  *single asterisks*
  _single underscores_
  **double asterisks**
  __double underscores__
  ~~cancelline~~


###  Image
   
    ![Alt text](/path/to/img.jpg)
    ![Alt text](/path/to/img.jpg "Optional title")

    <img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
    <img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
     


###  Table
  ※ 표 생성시 주의사항   
    : 앞뒤로 두줄 이상 띄어야 표로 인식함  
    그렇지 않은 경우에는 텍스트로 인식하여 노출
  
  - table 생성 사이트 : https://www.tablesgenerator.com/markdown_tables

#### table text 중앙정렬 

    | 항목 | 가격 | 개수 |
    |:---:|:----:|:----:|
    | 사과 | 800원 | 10개 |
    | 바나나 | 900원 | 5개 |
    
  결과물 :  
  
  | 항목 | 가격 | 개수 |
  |:---:|:----:|:----:|
  | 사과 | 800원 | 10개 |
  | 바나나 | 900원 | 5개 |
    

#### table text 왼쪽 / 중앙 / 오른쪽 정렬 

    | 항목 | 가격 | 개수 |
    |:----|:----:|-----:|
    | 사과 | 800원 | 10개 |
    | 바나나 | 900원 | 5개 |
    
  결과물 :  
  
  | 항목 | 가격 | 개수 |
  |:----|:----:|-----:|
  | 사과 | 800원 | 10개 |
  | 바나나 | 900원 | 5개 |

###  ASCII code   
  특수문자를 변환되지않고 사용하고싶다면 ASCII code로 입력하기 
  - 참고사이트 : http://www.umsiko.co.za/links/specchar.html

        "(&#34; 또는 &quot;),
        #(&#35;),
        %(&#37;),
        &(&#38; 또는 &amp;),
        '(&#39;),
        *(&#42;),
        <(&#60; 또는 &lt;),
        >(&#62; 또는 &gt;),
        _(&#95;),
        `(&#96;),
        " "(공백)(&nbsp;)


### text-align 
- `{ text-center }` 가운데 정렬
- `{ text-left }` 왼쪽 정렬 
- `{ text-right }` 오른쪽 정렬



### 줄바꿈 
※ 마크다운에서는 Enter 로 줄바꿈이 되지않음.

- `space` X 2번 입력
- `</br>`


### 각주
- `text + [^id]`
- `[^id] + text:des`

결과물 :  

- text + [^id]
- [^id] + text:des

※ github에서는 각주를 지원하지 않음.
