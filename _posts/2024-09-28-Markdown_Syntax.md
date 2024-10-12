---
title: "Markdown Syntax #1 | 마크다운 문법"
author: 'jinjehr'
date: 2024-09-28 20:25:00 +0900
last_modified_at: 2024-09-28 21:25:00 +0900
categories: [Github Blog, Jekyll]
tags: [github, jekyll, chirpy, blog]
img: /assets/post_img/markdown_logo.jpg/
description: Markdown Syntax 
toc: true 
math: true
pin: false
---

<div class="box-info">
<div class="title"> Info </div>
Markdown 문법에 대해 정리한 글입니다.
</div>

## About Markdown

개발쪽에 관심이 있거나 몸을 담고 계신 분들은 `README.md` 파일과 같은 md 파일들을 볼 수 있을 것입니다. 바로 이 파일과 같은 것들이 Markdown을 이용해서 만든 문서입니다. 주변에서 정말 많이 볼 수 있고 사용하기도 편해서 많은 인지도를 가지고 있습니다.

### <u>Markdown의 장점</u>
- 문법이 간단하고 쉽습니다. [Spring Rest Docs](https://spring.io/projects/spring-restdocs)와 같이 더 확장된 기능을 제공하는 `.adoc`형태의 문법도 있지만 더 어렵고 인지도가 적어 제약이 많습니다.
- 지원가능 플랫폼이 많습니다.  필자는 `VScode` 편집기를 이용하지만 `Notion` 등과 같은 대부분의 에디터에서 사용가능합니다.
- 텍스트로 저장되어 용량이 적습니다.
- 언제 어디서든 편집이 가능합니다.(메모장도 가능👍)

### <u>Markdown의 단점</u>
- 모든 HTML 마크업을 대체하지는 못합니다.
- 사진과 같은 파일 업로드시 저장후 경로입력을 해야하는 귀찮음이 있습니다.
- 정해진 표준이 없어 사용자마다 변환방식이나 생성물의 형태가 다를 수 있습니다. 

&nbsp;
&nbsp;

## Syntax

<div class="box-warning">
<div class="title"> Warning </div>
Markdown 문법은 HTML 태그로 변화되어 우리에게 보여지지만, 모든 HTML 태그를 지원하지 않고 일부만 지원하므로 플랫폼과 태그를 꼭 확인해보세요. 또, 이 글은 깃허브 블로그에서 작성되므로 github CSS를 따른다는 점 주의해주세요.
</div>

### <u>제목 (Header)</u>
- Markdown에서 **제목**을 표현하는 방법입니다. 
- `<h1>`부터 `<h6>`까지 나타낼 수 있습니다.
```Markdown
# h1
## h2
### h3
....
###### h6
```

### <u>글자 스타일 (Style)</u>
- Markdown에서는 글자 강조, 이탈릭체, 밑줄, 취소선을 다음과 같이 표현할 수 있습니다.
- Markdown에는 밑줄을 지원하지 않으므로 `HTML 태그`를 사용해야합니다.
```Markdown
**강조**
*이탈릭체*
***강조와 이탈릭체***
~~취소선~~
<u>밑줄</u>
```
> 결과 : **강조**, *이탈릭체*, ***강조와 이탈릭체***,  ~~취소선~~, <u>밑줄</u> 

- 만약 글자 색상이랑 크기를 변화하고 싶다면 `HTML 태그`를 사용할수 있습니다.
```HTML
<span style="font-size: 15px; color: Yellow"></span>
```
> 결과 : <span style="font-size: 15px; color: Yellow">색상과 크기를 변경한 텍스트입니다.</span> 

### <u>기호 출력 (Print Mark)</u> 
- Markdown에서 사용중인 기호를 출력하기 위해서는 `\`를 이용하여 출력할 수 있습니다.
```Markdown
\*
\+
\-
```
> 결과 : \* , \+ , \-

### <u>수평선 (Horizontal Rules)</u> 
- 구분선은 `***`이나 `---`으로 출력할 수 있습니다.

```Markdown
***
---
```

### <u>이모지 출력 (Print Emoji)</u>
- Windows : `Win` + `.`
- Mac : `Commend` + `Control` + `Space`

### <u>목록 (Lists)</u>
- Ordered Lists(순서가 있는 리스트)는 `숫자.`로 시작합니다.
- Unordered Lists(순서가 없는 리스트)는 `-`, `*`, `+`로 시작합니다.
```Markdown
1. Ordered Lists
2. Ordered Lists
3. Ordered Lists

- Unordered Lists
* Unordered Lists
+ Unordered Lists
```
>  결과 : 
> 1. Ordered Lists
> 2. Ordered Lists
> 3. Ordered Lists
>
> - Unordered Lists
> * Unordered Lists
> + Unordered Lists

### <u>줄바꿈 (Change Line)</u>
- 2가지 방법이 존재합니다. 더 편한 방법을 사용하세요. 저는 `<br>`을 더 많이 사용하고 있습니다.

1. HTML 태그인 `<br>`태그를 사용합니다.
```Markdown
줄바꿈 <br> 1번 방법입니다.
```
2. `Space 2번 + Enter` 사용합니다.
```Markdown
줄바꿈 space+space 2번 방법입니다.
```