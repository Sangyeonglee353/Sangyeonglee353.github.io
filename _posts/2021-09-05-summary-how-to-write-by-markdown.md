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

혼합해서 사용도 가능하다.
```
* 1단계
  - 2단계
    + 3단계
```
* 1단계
  - 2단계
    + 3단계

## 2.4 코드_Code

    

