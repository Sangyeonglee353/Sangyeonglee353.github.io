---
layout: post
title:  "[기초문법] Markdown_마크다운"
subtitle:   "[기초문법] Markdown_마크다운"
categories: Summary
tags: Summary
---

# 1. 마크다운에 관하여
## 1.1. 마크다운이란?
마크다운 (Markdown)은 마크업 언어의 일종으로, 존 그루버(John Gruber)와 아론 스워츠(Aaron Swartz)가 만들었다. 온갖 태그로 범벅된 HTML 문서 등과 달리,
읽기도 쓰기도 쉬운 문서 양식을 지원한다. 그루버는 마크다운으로 작성한 문서를 HTML로 변환하는 펄 스크립트도 만들었다.
확장자는 .md또는 .markdown을 쓰지만, 전자가 압도적으로 많이 쓰인다.

## 1.2. 마크다운의 장-단점
### 1.2.1. 장점
```
1. 간결하다
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
5. 텍스트파일이기 때문에 버전관리 시스템을 이용하여 변경이력을 관리할 수 있다.
6. 지원하는 프로그램과 플랫폼이 다양하다.
```
### 1.2.2. 단점
```
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.
```


# 2. 마크다운 사용법(문법)
## 2.1. 헤더_Headers
- 큰 제목: 문서 제목

```
This is an H1
=============
```

This is an H1
=============
  
- 작은 제목: 문서 부제목

```
This is an H2
```

This is an H2
-------------   
  
- 글머리: 1~6까지만 지원

```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
  
## 2.2. 인용문_BlockQuote
이메일에서 사용하는 `>`블럭인용문자를 이용한다.
```
> This is a first blockquote.
> > This is a second blockquote.
> > > This is a third blockquote.
```
> This is a first blockqoute.
> > This is a second blockquote.
> > > This is a third blockquote.

이 안에서는 마크다운 요소를 포함할 수 있다.
> This is a H3
> - List
>   ```
>   code
>   ```

## 2.3 목록_List
- 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 이용한다.

```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

현재까지는 어떤 번호를 입력해도 순서는 자동으로 내림차순으로 정의된다.

```
1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
3. 세번째
2. 두번째

- 순서없는 목록(글러미 기호: `*`, `+`, `-` 지원)

```
* 빨강
  * 파랑
    * 노랑
+ 빨강
  + 파랑
    + 노랑
- 빨강
  - 파랑
    - 노랑
 ```

* 빨강
  * 파랑
    * 노랑
+ 빨강
  + 파랑
    + 노랑
- 빨강
  - 파랑
    - 노랑

> 혼합해서 사용도 가능하다.

```
* 1단계
  - 2단계
    + 3단계
```

* 1단계
  - 2단계
    + 3단계

## 2.4. 코드_Code
4개의 공백(Spacebar) 또는 하나의 탭(Tab)으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

### 2.4.1. 들여쓰기_indent

```
This is a normal paragraph:

  This is an intented sentence.

end intented sentence.
```

***
This is a normal paragraph:
   
    This is an intented sentence.
   
end intented sentence.   
***   

> 줄바꿈을 하지 않으면 인식이 제대로 안되는 문제가 발생한다.

```
This is a normal paragraph:
  This is an intented sentence.
end intented sentence.
```

***
This is a normal paragraph:
  This is an intented sentence.
end intented sentence.   
***   

### 2.4.2 코드 블럭
코드 블럭은 다음과 같이 2가지 방식을 사용할 수 있습니다.

- `<pre><code>{code}</code></pre>` 태그를 이용하는 방법

```
<pre>
<code>
public class BootSpringBootApplication{
  pulic static void main(String[] args){
    System.out.println("Hello, Github");
  }
}
</code>
</pre>
```

<pre>
<code>
public class BootSpringBootApplication {
  pulic static void main(String[] args) {
    System.out.println("Hello, Github");
  }
}
</code>
</pre>


- 코드 블럭 코드(" ``` ")을 이용하는 방법

<pre>
```
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Github");
  }
}
```
</pre>

```
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Github");
  }
}
```

- 깃헙(github)에서는 코드 블럭 코드(' ``` '시작점에 사용하는 언어를 선언하여 [문법강조(Syntax highlighting)](https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting)이 가능하다.

<pre>
```java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Github");
  }
}
```
</pre>

```java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Github");
  }
}
```

## 2.5. 수평선 `<hr/>` 
아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 _페이지 나누기_ 용도로 많이 사용한다.

```
* * *
***
*****
- - -
-------------------------
```

* * *
***
*****
- - -
-------------------------

## 2.6. 링크_Link
- 참조링크

```
키워드에 링크를 넣는 형태 1
// 문법
[link keyword][id]
[id]: URL "Optional Title here"

// 적용코드
Link: [Google][googlelink]
[googlelink]: https://google.com "
```

Link: [Google][googlelink]
[googlelink]: https://google.com "go google"

- 외부링크

```
키워드에 링크를 넣는 형태 2
// 문법
[Title](link)

// 적용코드
Link: [Google](https://google.com, "google link")
```

Link: [Google](https://google.com, "google link")

- 자동연결

```
주소 URL 자체에 링크를 넣는 형태
// 문법
<link>

// 적용코드
* 외부링크: <https://google.com>
* 이메일링크: <address@example.com>
```

* 외부링크: <https://google.com>
* 이메일링크: <address@example.com>

## 2.7. 강조 `<em>`

```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~canceline~~
```

- *single asterisks*
- _single underscores_
- **double asterisks**
- __double underscores__
- ~~canceline~~

> 문장 중간에 사용할 경우에는 앞뒤로 띄어쓰기를 해주는 것이 좋다.

## 2.8. 이미지_Image

```
// 문법
![대체 텍스트](이미지 경로)
![대체 텍스트](이미지 경로 "포인터 텍스트")

// 적용코드
![Programmer](/assets/img/pl_sample.jpg)
![Programmer](/assets/img/pl_sample.jpg "Programmer")
```

![Programmer](/assets/img/pl_sample.jpg)
![Programmer](/assets/img/pl_sample.jpg "Programmer")

> 마크다운 문법에서는 이미지 크기 조절을 따로 지원하지 않는다. 

```
따라서 HTML의 <img src="" width="" height=""> 태그를 이용한다.
// 문법
<img src="이미지 경로" width="가로넓이" height="세로넓이" title="포인터 텍스트" alt="대체 텍스트"></img>

// 적용코드
<img src="/assets/img/pl_sample.jpg" width="450px" height="300px" title="Programmer" alt="Programmer"></img><br/>
<img src="/assets/img/pl_sample.jpg" width="450px" height="300px" title="Programmer" alt="Programmer"></img>
```

<img src="/assets/img/pl_sample.jpg" width="450px" height="300px" title="Programmer" alt="Programmer"></img><br/>
<img src="/assets/img/pl_sample.jpg" width="450px" height="300px" title="Programmer" alt="Programmer"></img>

## 2.9. 줄바꿈 `<br/>`
3칸 이상 띄어쓰기(`   `)를 하면 줄이 바뀐다.

```
* 줄 바꿈을 하기 위해서는 문자 마지막에서 3칸 이상 띄어쓰기를 해야 한다.___ <- 띄어쓰기
줄바꿈 짠!!
```
* 줄 바꿈을 하기 위해서는 문자 마지막에서 3칸 이상 띄어쓰기를 해야 한다.   
줄바꿈 짠!!

## 2.10. 표 `<table>...</table>`
- 기본 구조

```
| name | description | age |
| ---- | ----------- | --- |
| Lee  | You can do it! | 25 |
| Kim  | Simple is the Best! | 30 |
| Yun  | We are the Champions! | 45 |
```

| name | description | age |
| ---- | ----------- | --- |
| Lee  | You can do it! | 25 |
| Kim  | Simple is the Best! | 30 |
| Yun  | We are the Champions! | 45 |

- 표 정렬
  - 왼쪽 정렬 :--
  - 오른쪽 정렬 --:
  - 가운데 정렬 :--:

```
| name | description | age |
| :---- | -----------: | :---: |
| Lee  | You can do it! | 25 |
| Kim  | Simple is the Best! | 30 |
| Yun  | We are the Champions! | 45 |
```

| name | description | age |
| :---- | -----------: | :---: |
| Lee  | You can do it! | 25 |
| Kim  | Simple is the Best! | 30 |
| Yun  | We are the Champions! | 45 |

## 2.11. 주석

> 문법:

```
<!--
마크다운에서 주석 처리하기
-->
```

> 적용예시:

<!--
마크다운에서 주석 처리하기
-->

## 2.12. 각주 `<sup>...</sup>`
본문의 어떤 부분을 설명하거나 보충하기 위해 본문 아래쪽에 별도로 작성하는 간단한 설명문으로서 주로 내용의 출처를 밝힐 때 사용됩니다.

```
최근 스칼라는 매우 인기가 높은 언어이다.[^scala]
[\^scala]: 스칼라는 마틴 오더스크가 개발한 함수형 언어이다.
```

최근 스칼라는 매우 인기가 높은 언어이다.[^scala]

[\^scala] : 스칼라는 마틴 오더스크가 개발한 함수형 언어이다.

## 2.13 목차 생성하기
문서 내에 사용된 헤딩 태그등을 이용하여 '{:toc}'입력 시 목차가 자동 생성된다. 상단 목차 참고.

# 3. 마크다운 사용기
## 3.1. 위지윅(WSYWIG) 에디터
우리가 흔하게 접하는 웹에서 사용되는 에디터(네이버, 다음, 구글 등)이 대부분 위지윅 에디터에 속하며 기본적으로 HTML을 이용하여 스타일을 적용하여 문자을 꾸미는 형태를 취하게 된다. 그래서 하루패드와 같은 마크다운 에디터의 View 영역의 내용을 복사하여 붙여넣기를 하면 대체적으로 View영역에서 보이는 그대로 복사되는 편이다. 다만, 붙여넣기 이후에 문장들을 수정하려고 할 때 문제가 되는데, 이는 스타일이 포함된 태그가 수정과정에서 변형되면서 전체적인 영향을 끼치는 탓이다. 티스토리 블로그에서는 쉽지 않고, 워드프레스의 경우에는 마크다운으로 작성된 포스트를 HTML로 변환해주는 기능을 활용하는 것이 좋다. 결론은 **복사해서 붙여넣기하면 가급적이면 본문은 수정하지 않는 것** 이 좋다.
## 3.2. 깃헙(Github), 비트버킷(Bitbucket)과 요비(Yobi) 등
최근 유행하는 협업개발플랫폼의 경우에는 마크다운을 변환하는 컨버터 기능을 기본탑재하고 있기 때문에 마크다운 문법으로 작성한 텍스트를 그대로 복사해서 붙여넣거나 업로드하는 것만으로 마크다운의 적용이 가능하다.
## 3.3. MS워드 적용
View 영역의 항목을 그대로 붙여넣거나 HTML 내보내기 등으로 생성한 파일을 불러오는 형태로 사용가능하다. 적용한 헤더를 워드가 읽어드리면서 목차에 적용하기 때문에 이를 활용하면 목차까지도 손쉽게 적용이 가능해진다.


