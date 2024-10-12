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

<br>

## Syntax

> Markdown 문법은 HTML 태그로 변화되어 우리에게 보여지지만, 모든 HTML 태그를 지원하지 않고 일부만 지원하므로 플랫폼과 태그를 꼭 확인해보세요. 또, 이 글은 깃허브 블로그에서 작성되므로 github CSS를 따른다는 점 주의해주세요.
{: .prompt-warning }

### <u>제목 (Header)</u>
- Markdown에서 **제목**을 표현하는 방법입니다. 
- `<h1>`부터 `<h6>`까지 나타낼 수 있습니다.

```Header
# h1
## h2
### h3
....
###### h6
```
