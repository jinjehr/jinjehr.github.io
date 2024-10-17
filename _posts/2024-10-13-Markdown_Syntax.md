---
title: "Markdown Syntax | 마크다운 문법"
author: 'jinjehr'
date: 2024-10-13 23:51:00 +0900
last_modified_at: 2024-10-17 12:51:00 +0900
categories: [Markdown, Syntax]
tags: [Markdown, Syntax]
description: Markdown Syntax 
toc: true 
math: true
pin: false
image:
  path: /assets/post_img/markdown_logo.jpg
  alt: Markdown
---

> Markdown 문법에 대해 정리한 글입니다. ~~사실 제가 보려고 정리한 글입니다.~~
{: .prompt-info }

## About Markdown
Markdown은 일반적인 텍스트 기반의 가벼운 마크업 언어로, 편집하기 쉬운 목적으로 만들어져 다양한 문서 작성을 위한 형식으로 사용되고 있습니다.  개발쪽에 관심이 있거나 몸을 담고 계신 분들은 `README.md` 파일과 같은 md 파일들을 볼 수 있을 것입니다. 바로 이 파일과 같은 것들이 Markdown을 이용해서 만든 문서입니다. 주변에서 정말 많이 볼 수 있고 사용하기도 편해서 많은 인지도를 가지고 있습니다.

<br>

### <u>Markdown의 장점</u>
- 문법이 간단하고 쉽습니다. [Spring Rest Docs](https://spring.io/projects/spring-restdocs)와 같이 더 확장된 기능을 제공하는 `.adoc` 형태의 문법도 있지만 더 어렵고 인지도가 적어 제약이 많습니다. ~~언젠가 `.adoc` 도 정리해보겠습니다.~~
- 지원가능 플랫폼이 많습니다.  필자는 `VScode` 편집기를 이용하지만 `Notion` 등과 같은 대부분의 에디터에서 사용가능합니다.
- 텍스트로 저장되어 용량이 적습니다.
- 언제 어디서든 편집이 가능합니다.(메모장도 가능👍)

<br>

### <u>Markdown의 단점</u>
- 모든 HTML 마크업을 대체하지는 못합니다.
- 사진과 같은 파일 업로드시 저장후 경로입력을 해야하는 귀찮음이 있습니다.
- 정해진 표준이 없어 사용자마다 변환방식이나 생성물의 형태가 다를 수 있습니다. 

<br>

![Markdown Editor](/assets/post_img/2024-10-13-1.png)
_Markdown in VSCode_

<br>
<br>

## Syntax

> Markdown 문법은 HTML 태그로 변화되어 우리에게 보여지지만, 모든 HTML 태그를 지원하지 않고 일부만 지원하므로 플랫폼과 태그를 꼭 확인해보세요. 또, 이 글은 깃허브 블로그에서 작성되므로 github CSS를 따른다는 점 주의해주세요.
{: .prompt-warning }

### <u>제목 (Header)</u>
- Markdown에서 **제목**을 표현하는 방법입니다. 
- `<H1>` 부터 `<H6>` 까지 나타낼 수 있습니다.
- H1은 `===` 로도 만들 수 있습니다.
- H2는 `---` 로도 만들 수 있습니다.

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6 

This is an H1
===
This is an H2
---
```

<br>

### <u>글자 스타일 (Style)</u>

#### 글씨체(Font)
- Markdown에서는 글자 강조, 이탈릭체, 밑줄, 취소선을 다음과 같이 표현할 수 있습니다.

```markdown
**강조**
*이탈릭체*
***강조와 이탈릭체***
~~취소선~~
```

> Preview : 
**강조**, *이탈릭체*, ***강조와 이탈릭체***, ~~취소선~~

<br>

#### 밑줄(Underline)
- Markdown에는 밑줄을 지원하지 않으므로 `HTML 태그` 를 사용해야합니다.

```html
<u>밑줄</u>
```
> Preview : 
<u>밑줄</u>

<br>

#### 색상과 크기(Color, Size)
- 만약 글자 색상이랑 크기를 변화하고 싶다면 `HTML 태그` 를 사용할수 있습니다.

```html
<span style="font-size: 15px; color: skyblue"></span>
```

> Preview : 
<span style="font-size: 15px; color: skyblue">색상과 크기를 변화한 텍스트입니다.</span>

<br>

### <u>수평선 (Horizontal Rules)</u> 
- 구분선은 `***` 이나 `---` 으로 출력할 수 있습니다.

```markdown
***
---
```

> Preview : 
***

<br>

### <u>이스케이프 (Backslash Escape)</u> 
- Markdown에서 사용중인 기호를 출력하기 위해서는 `\` 를 이용하여 출력할 수 있습니다.

```markdown
\*
\+
\-
```

> Preview : 
\*, \+, \-

<br>

### <u>체크 리스트 (Check Lists)</u>
- 앞에 `[X]` 를 쓰면 완료된 리스트를 표현할 수 있습니다.
- 앞에 `[ ]` 를 쓰면 미완료된 리스트를 표현할 수 있습니다.

```markdown
- [X] complete
- [ ] incomplete
```

> Preview : 
>- [X] complete 
>- [ ] incomplete

<br>

### <u>이모지 출력 (Print Emoji)</u>
- Windows : `Win` + `.`
- Mac : `Command` + `Control` + `Space` 로 하거나 `Fn` 단일키

> Preview : 😁

<br>

### <u>줄바꿈 (Change Line)</u>
- 2가지 방법이 존재합니다. 더 편한 방법을 사용하세요. 저는 `<br>` 을 더 많이 사용하고 있습니다.

<br>

#### HTML 태그
-  HTML 태그인 `<br>` 태그를 사용합니다.

```markdown
줄바꿈 <br> 1번 방법입니다.
```
> Preview : <br> 줄바꿈 <br> 1번 방법입니다.

<br>

#### 공백 줄바꿈
- `Space 2번 + Enter` 사용합니다.

```markdown
줄바꿈 space+space 2번 방법입니다.
```
> Preview : <br> 줄바꿈  
2번 방법입니다.

<br>

### <u>인용문 (Blockquotes)</u>
- 본문에 인용구를 삽입할 때 `>` 를 이용해 작성합니다.
- `>` 의 개수는 최대 3개까지 사용해 중첩 인용문을 사용할 수 있습니다.   
- 인용문 안에는 리스트나 제목 등을 삽입할 수 있습니다.

```markdown 
> 첫번째 인용문
    >> 두번째 인용문
        >>> 세번째 인용문
```

> Preview :
>
> 첫번째 인용문
>> 두번째 인용문
>>> 세번째 인용문

<br>

### <u>목록 (Lists)</u>

#### 순서가 있는 리스트(ordered Lists)
- 말 그대로 순서를 볼 수 있는 리스트입니다.
- `숫자.` 로 시작합니다.

```markdown
1. Ordered Lists
2. Ordered Lists
3. Ordered Lists
```

> Preview :
>1. Ordered Lists
>2. Ordered Lists
>3. Ordered Lists

<br>

#### 순서가 없는 리스트(Unordered Lists)
- 말 그대로 순서가 없는 리스트입니다.
- `-` , `*` , `+` 로 시작합니다.

```markdown
- Unordered Lists
* Unordered Lists
+ Unordered Lists
```
> Preview :
>- Unordered Lists
>* Unordered Lists
>+ Unordered Lists

<br>

#### 혼합 리스트(Mixed Lists)
- 물론 위의 리스트 두가지를 동시에 사용 가능합니다.
```markdown
1. Ordered Lists
    - Unordered Lists
- Ordered Lists
    1. Unordered Lists
```
> Preview :
>1. Ordered Lists
>    - Unordered Lists
>- Ordered Lists
>    1. Unordered Lists

<br>

### <u>인라인 코드 블록 (Inline Code)</u>
- `Backtick` 을 양끝에 추가하면 그 부분만 강조한 텍스트를 만들 수 있습니다.

```markdown
`인라인 코드 블록` 입니다.
```

> Preview : `인라인 코드 블록` 입니다.

<br>

### <u>코드 블록 (Code Blocks)</u>
- `Backtick` 이나 `~`로 3번 이상 입력 후 사용언어를 명시하면 syntax color가 적용됩니다.
- 코드 블록의 `Backtick` 이나 `~` 의 수는 같아야 합니다.
- 사용언어를 안적거나 언어가 아닌 단어를 적어도 코드 블록은 생성됩니다.
- [Support Language List] (https://docs.readme.com/rdmd/docs/code-blocks)에서 지원 언어 태그를 확인하실 수 있습니다.

~~~markdown
```python
print('Hello World')
```  

```bash
$ npm run git
``` 
~~~

> Preview :
>```python
>print('Hello World')
>```  
>
>```bash
>$ npm run git
>``` 

<br>

### <u>링크 (Links)</u>

#### 외부링크(External Link)
- `<>` 가 없어도 링크로 인식하고 링크 이름도 아래와 같이 변경 가능합니다.

```markdown
[Google](https://www.google.com)

Google : <https://www.google.com>

[인터넷 브라우저](https://www.google.com)
```

> Preview : <br>
> [Google](https://www.google.com) <br>
> Google : <https://www.google.com> <br>
> [인터넷 브라우저](https://www.google.com)

<br>

#### 내부링크(Internal Link)
- `[]` 로 묶은 후 `()` 안에 헤드 제목을 작성하면 작성한 헤드로 이동합니다.
- 띄어쓰기는 `-` 로 연결해야 합니다.
- `()` 는 없이 모두 소문자로 작성해야 합니다.
- 이모지는 `::` 제거 후 사용해야 합니다.

```markdown
[마크다운에 대하여](#about-markdown)
```

> Preview : [마크다운에 대하여](#about-markdown)

<br>

### <u>테이블 (Tables)</u>

#### 표(Creating Tables)
- 본문에 표를 삽입할 때 사용합니다.
- 테이블의 헤더와 셀은 3개 이상의 `-` 으로 구분할 수 있습니다.
- 양끝의 `|` 은 생략할 수 있습니다.

```markdown
Create Tables

H1|H2|H3
---|---|---
C1|C2|C3 
C4|C5|C6
```

> Preview : <br>
>Create Tables
>
>H1|H2|H3
>---|---|---
>C1|C2|C3 
>C4|C5|C6

<br>

#### 정렬된 표(Sorted Tables)
- 헤더와 셀을 구분할 때 `:` 으로 셀의 내용을 정렬할 수 있습니다.
- `:---` 는 좌측정렬, `:---:` 는 중앙정렬, `---:` 는 우측정렬이다.

```markdown
Create Sorted Tables

H1|H2|H3
:---|:---:|---:
Left|Mid|Right
C1|C2|C3
C4|C5|C6
```

> Preview : <br>
>Create Sorted Tables
>
> H1|H2|H3
> :---|:---:|---:
> Left|Mid|Right
> C1|C2|C3
> C4|C5|C6

<br>

### <u>주석 (Comments)</u>
- `<!-- -->` 를 이용해 주석을 표현할 수 있습니다.

```markdown
<!-- Comment -->
```

<br>

### <u>이미지 (Image)</u>
- 가장 앞에 `!` 를 붙여 사용합니다.
- 인라인 이미지와 링크 이미지는 아래와 같이 사용합니다.

```markdown
![text](이미지 파일 경로.png) //png, jpg, jpeg 등등 가능
![text](이미지 파일 URL)
![text](이미지 파일 URL "링크 설명")
```

- 이미지에 링크를 추가하기 위해서는 아래와 같이 마크다운의 이미지 문법을 링크 문법 코드로 덮어줍니다.

```markdown
[![설명](이미지 링크)](https:// ~~ "링크 설명")

[![Philog](/favicon.ico)](https://jinjehr.github.io/)
```


- 이미지의 크기 조절은 `HTML 태그`를 이용한다.

```html
<img src="이미지 파일 경로" width="???px" height="???px" title="px 고정크기 값" alt="설명"></img>

<img src="이미지 파일 경로" width="??%" height="??%" title="px %크기 값" alt="설명"></img>
```

- 이미지 정렬 조절 역시 `HTML 태그`를 이용한다.

```html
<p align="center"><img src="이미지 파일 경로" width="???px" height="???px" title="px 고정크기 값" alt="설명"></img> // center, right, left 등등
```

<br>

### <u>요약 (Summary)</u>
- Markdown은 아니지만 유용하게 사용했던 기억이 있어서 같이 설명합니다.
- `HTML 태그`를 이용하여 하위 내용을 접거나 펼쳐서 볼 수 있게 만들어줍니다.

```html
<details><summary>보여지는 텍스트</summary>
숨겨지는 텍스트
</details>    
```
> Preview : 
> <details><summary>Click Here</summary>Hello World!</details> 


<br>

## Reference
- [Basic Syntax : The Markdown elements outlined in the original design document.](https://www.markdownguide.org/basic-syntax/) <sup>site</sup>
- [Support Language List in Markdown](https://docs.readme.com/rdmd/docs/code-blocks)<sup>site</sup>