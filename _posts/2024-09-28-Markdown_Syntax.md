---
title: "Markdown Syntax #1 | 마크다운 문법"
author: 'jinjehr'
date: 2024-09-28 20:25:00 +0900
last_modified_at: 2024-09-28 21:25:00 +0900
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

> Markdown 문법에 대해 정리한 글입니다.
{: .prompt-info }

## About Markdown
Markdown은 일반적인 텍스트 기반의 가벼운 마크업 언어로, 편집하기 쉬운 목적으로 만들어져 다양한 문서 작성을 위한 형식으로 사용되고 있습니다.  개발쪽에 관심이 있거나 몸을 담고 계신 분들은 `README.md` 파일과 같은 md 파일들을 볼 수 있을 것입니다. 바로 이 파일과 같은 것들이 Markdown을 이용해서 만든 문서입니다. 주변에서 정말 많이 볼 수 있고 사용하기도 편해서 많은 인지도를 가지고 있습니다.

<br>

### <u>Markdown의 장점</u>
- 문법이 간단하고 쉽습니다. [Spring Rest Docs](https://spring.io/projects/spring-restdocs)와 같이 더 확장된 기능을 제공하는 `.adoc`형태의 문법도 있지만 더 어렵고 인지도가 적어 제약이 많습니다.
- 지원가능 플랫폼이 많습니다.  필자는 `VScode` 편집기를 이용하지만 `Notion` 등과 같은 대부분의 에디터에서 사용가능합니다.
- 텍스트로 저장되어 용량이 적습니다.
- 언제 어디서든 편집이 가능합니다.(메모장도 가능👍)

<br>

### <u>Markdown의 단점</u>
- 모든 HTML 마크업을 대체하지는 못합니다.
- 사진과 같은 파일 업로드시 저장후 경로입력을 해야하는 귀찮음이 있습니다.
- 정해진 표준이 없어 사용자마다 변환방식이나 생성물의 형태가 다를 수 있습니다. 

<br>
<br>

## Syntax

> Markdown 문법은 HTML 태그로 변화되어 우리에게 보여지지만, 모든 HTML 태그를 지원하지 않고 일부만 지원하므로 플랫폼과 태그를 꼭 확인해보세요. 또, 이 글은 깃허브 블로그에서 작성되므로 github CSS를 따른다는 점 주의해주세요.
{: .prompt-warning }

### <u>제목 (Header)</u>
- Markdown에서 **제목**을 표현하는 방법입니다. 
- `<H1>`부터 `<H6>`까지 나타낼 수 있습니다.
- H1은 `===`로도 만들 수 있습니다.
H2는 `---`로도 만들 수 있습니다.
```markdown
    This is an H1
    ===
    This is an H2
    ---
    # H1
    ## H2
    ### H3
    #### TH4
    ##### H5
    ###### H6 
```

<br>

### <u>글자 스타일 (Style)</u>
- Markdown에서는 글자 강조, 이탈릭체, 밑줄, 취소선을 다음과 같이 표현할 수 있습니다.
- Markdown에는 밑줄을 지원하지 않으므로 `HTML 태그`를 사용해야합니다.

```markdown
    **강조**
    *이탈릭체*
    ***강조와 이탈릭체***
    ~~취소선~~
    <u>밑줄</u>
```

- 만약 글자 색상이랑 크기를 변화하고 싶다면 `HTML 태그`를 사용할수 있습니다.

```html
    <span style="font-size: 15px; color: brown"></span>
```

<br>

### <u>이스케이프 (Backslash Escape)</u> 
- Markdown에서 사용중인 기호를 출력하기 위해서는 `\`를 이용하여 출력할 수 있습니다.

```markdown
    \*
    \+
    \-
```

<br>


### <u>수평선 (Horizontal Rules)</u> 
- 구분선은 `***`이나 `---`으로 출력할 수 있습니다.

```markdown
    ***
    ---
```

<br>

### <u>이모지 출력 (Print Emoji)</u>
- Windows : `Win` + `.`
- Mac : `Commend` + `Control` + `Space`

<br>

### <u>목록 (Lists)</u>
- Ordered Lists(순서가 있는 리스트)는 `숫자.`로 시작합니다.
- Unordered Lists(순서가 없는 리스트)는 `-`, `*`, `+`로 시작합니다.
- 물론 두가지를 동시에 사용 가능합니다.

```markdown
    1. Ordered Lists
    2. Ordered Lists
    3. Ordered Lists

    - Unordered Lists
    * Unordered Lists
    + Unordered Lists

    1. Ordered Lists
        - Unordered Lists
```

<br>

### <u>줄바꿈 (Change Line)</u>
- 2가지 방법이 존재합니다. 더 편한 방법을 사용하세요. 저는 `<br>`을 더 많이 사용하고 있습니다.

1. HTML 태그인 `<br>`태그를 사용합니다.

```markdown
    줄바꿈 <br> 1번 방법입니다.
```

2. `Space 2번 + Enter` 사용합니다.

```markdown
    줄바꿈 space+space 2번 방법입니다.
```

<br>

### <u>링크 (Links)</u>
- **외부 링크**는 아래와 같이 사용할 수 있습니다. 
- `<>`가 없어도 링크로 인식하고 링크 이름도 아래와 같이 변경 가능합니다.

```markdown
    [Google] (https://www.google.com)

    Google : <https://www.google.com>

    [인터넷 브라우저] (https://www.google.com)
```

- **내부 링크**는 아래와 같이 사용할 수 있습니다.
- `[]`로 묶은 후 `()`안에 헤드 제목을 작성하면 작성한 헤드로 이동합니다.

```markdown
    ex) [마크다운에 대하여] (#about-markdown)
```
> 띄어쓰기는 `-`으로 연결하고, `()`는 없이 작성 및 모두 소문자로 작성해야 하며, 이모지는 `::`제거 후 사용해야 합니다.
{: .prompt-warning }

<br>

### <u>코드 블록 (Code Blocks)</u>
- <code>\`</code>로 3번 이상 입력 후 사용언어를 명시하면 syntax color가 적용됩니다.
- 코드 블록의 <code>\`</code>의 수는 같아야 합니다.
- 사용언어를 안적거나 언어가 아닌 단어를 적어도 코드 블록은 생성됩니다.

```markdown
    ```python
    print('Hello World");
    ```  

    ```bash
    $ npm run git
    ``` 
```

<br>

### <u>체크 리스트 (Check Lists)</u>
- 앞에 `[X]`를 쓰면 완료된 리스트를 표현할 수 있습니다.
- 앞에 `[ ]`를 쓰면 미완료된 리스트를 표현할 수 있습니다.

```markdown
    - [X] complete
    - [ ] incomplete
```

<br>

### <u>주석 (Comments)</u>
- `<!-- -->`를 이용해 주석을 표현할 수 있습니다.

```markdown
    <!-- Comment -->
```