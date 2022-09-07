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
last_modified_at: 2022-09-07
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


## MarkDown Language Syntax

### Header
  제목은 <h1> ~ <h6> 까지 "#"의 개수로 표현
  <pre>
    <code>
      # <h1> 
      ## <h2>
      ### <h3>
      #### <h4>
      ##### <h5>
      ###### <h6>     
    </code>
  </pre>


### BlockQuote
인용문자는 ```>``` 를 이용 
<pre>
    <code>
        > blockqute test.
        >	> blockqute test.
    </code>
  </pre>


### Lst
순서있는 목록 : ```숫자 + .``` 
순서없는 목록 : ```*```,```+``` ,``` -``` 지원 / 혼합하여 사용가능  

<pre>
    <code>
       1. list test
       2. list test
       3. list teset
    </code>
  </pre>

  <pre>
    <code>
      * list test
        + list test
          + list test
            + list test
      * list test
        - list test
          - list test
            - list test
      * list teset
        * list teset
          * list teset
          * list teset
    </code>
  </pre>

결과물 :
* list test
  + list test
    + list test
      + list test
* list test
  - list test
    - list test
      - list test
* list teset
  * list teset
    * list teset
    * list teset


### Code
코드 삽입의 방법은 세가지로 
1. 들여쓰기 (코드의 시작과 끝에 한줄 비우기!!)
2. ```<pre><code>{code}</code></pre>``` 사용
3. "```" 사용 (코드블럭)
4. "``"사용 (인라인코드블럭)



### 수평선 
<pre>
  <code>
    * * *

    ***

    *****

    - - -

    ---------------------------------------
  </code>
</pre>

결과물 :
* * *

***

*****

- - -

---------------------------------------

### Link
1. 참조링크 
2. 외부링크
3. url 노출 링크


### emophasis
<pre>
  <code>
    *single asterisks*
    _single underscores_
    **double asterisks**
    __double underscores__
    ~~cancelline~~
  </code>
</pre>

결과물 :

*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~


### Image
<pre>
  <code>
    ![Alt text](/path/to/img.jpg)
    ![Alt text](/path/to/img.jpg "Optional title")

    <img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
    <img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
  </code>
</pre>


### Table

table 생성 사이트 : https://www.tablesgenerator.com/markdown_tables


### ASCII code 
특수문자를 변환되지않고 사용하고싶다면 ASCII code로 입력하기 
http://www.umsiko.co.za/links/specchar.html

<pre>
  <code>
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

  </code>
</pre>