---
title: Github Blog by Chirpy theme (5) Markdown 기본 문법
description: Chirpy theme로 Github Blog 만들기 (2025-01 기준)
author: SemiDS
date: 2025-01-23 20:00:00 +0900
categories: [Blog]
tags: [Markdown]
pin: false
---

## (1). Markdown 이란?
`마크다운(Markdown)`은 존 그루버(John Gruber)가 2004년에 만든 텍스트 기반의 경량 마크업 언어입니다. 간단한 문법으로 사람들이 읽고 쓰기 쉬운 서식 있는 문서를 작성하고 HTML로 변환할 수 있도록 설계되었습니다. 

>Markdown의 주요 특징 (By ChatGPT)
>- 단순함: 직관적인 문법으로 간단하게 서식을 지정할 수 있습니다.
>- 가독성: 서식 문법이 복잡하지 않아, 문법이 포함된 텍스트 자체도 읽기 쉽습니다.
>- 범용성: HTML, PDF, Word 등 다양한 형식으로 변환할 수 있습니다.
>- 확장성: 마크다운 기본 문법 외에도 확장 문법(Markdown Extended)을 지원하여 더 복잡한 서식을 표현할 수 있습니다.

Github blog에 업로드 하는 posting은 Markdown 언어로 작성을 해야하기 때문에, posting을 위해서는 Markdown에 대한 기본 문법을 익히는게 필요합니다.

## (2). 제목 & 줄바꿈 & 수평선
`#`의 갯수로 제목의 중요도를 지정할 수 있습니다. 갯수는 총 6개까지 지원합니다. (HTML에서 h1~h6 tag)

```html
# 제목1
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6
```

줄바꿈을 위해서는 문장 뒤에 `띄어쓰기를 2번` 입력하거나 `<br>` 태그를 사용하면 됩니다.

```html
첫번째줄  # 띄어쓰기(space) 2번 
두번째줄 

첫번째줄<br> 
두번째줄
```

>첫번째줄   
>두번째줄 
>
>첫번째줄<br>
>두번째줄
{: .prompt-tip }

`***`이나 `---`을 입력해서 수평선을 표시할 수 있습니다.
```html
***
---
```

>***
>---

## (3) 강조 (기울기, 두껍게 등)
아래와 같은 형태로 글씨를 강조할 수 있습니다.
```html
_기울기_   
**두껍게**   
**_기울기+두껍게_**
~~취소선~~
<u>밑줄</u>
`배경색`
```

>_기울기_   
>**두껍게**   
>**_기울기+두껍게_**  
>~~취소선~~  
><u>밑줄</u>  
>`배경색`
{: .prompt-tip }

## (4) 목록
순서가 있는 목록은 숫자로, 없는 목록은 `-`로 표시할 수 있습니다. 

```html
1. 1번
2. 2번
3. 3번
    1. 1번
    2. 2번
    3. 3번

- 1번
- 2번
- 2번
```

>1. 1번
>2. 2번
>3. 3번
>    1. 1번
>    2. 2번
>    3. 3번
>
>- 1번
>- 2번
>- 2번
{: .prompt-tip }

## (5) 인용문
`>` 기호로 인용문을 표시할 수 있습니다. 또한 `>`의 갯수로 중첩기능도 제공합니다.
```html
> 인용문을
> 표시하는
> 방법입니다.
>> 인용문 중첩입니다.  
>>> 인용문 중중첩입니다.
```

> 인용문을  
> 표시하는  
> 방법입니다.  
>> 인용문 중첩입니다.  
>>> 인용문 중중첩입니다.
{: .prompt-tip }

jekyll 테마에서는 위와 같은 인용문의 형태를 추가로 강조할 수 있는 방법을 prompt 문법으로 총 4가지를 제공하며, 상황에 따라 매우 유용하게 사용가능합니다.

```html
> .prompt-info
{: .prompt-info }

> .prompt-tip
{: .prompt-tip }

> .prompt-warning
{: .prompt-warning }

> .prompt-danger
{: .prompt-danger }
```

> .prompt-info
{: .prompt-info }

> .prompt-tip
{: .prompt-tip }

> .prompt-warning
{: .prompt-warning }

> .prompt-danger
{: .prompt-danger }

## (6) 코드 블럭 강조
\`\`\` `언어 이름`  
script  
\`\`\`   
형태로 코드 블럭을 표시할 수 있습니다. (html, python, 등)

```python
print("hello world")
```

## (7) 링크 & 이미지
아래와 같은 문법으로 텍스트에 하이퍼 링크를 걸거나 이미지를 삽입할 수 있습니다.

```html
[LINK](https://daeheeseol.github.io/)
![IMAGE](/assets/img/favicons/favicon-96x96.png)
[![IMAGE+LINK](/assets/img/favicons/favicon-96x96.png)](https://daeheeseol.github.io/)
```
-텍스트에 링크 연결

[LINK](https://daeheeseol.github.io/)  

-이미지 삽입

![IMAGE](/assets/img/favicons/favicon-96x96.png){: .left}  

<br><br><br><br>

-이미지에 링크 연결  
[![IMAGE+LINK](/assets/img/favicons/favicon-96x96.png)](https://daeheeseol.github.io/)

## (8) 표
아래와 같은 형태로 표를 삽입할 수 있습니다.
- \-\- or :\-\- (왼쪽 정렬)
- :\-\-: (가운데 정렬)
- \-\-: (오른쪽 정렬)

```html
컬럼1 | 컬럼2 | 컬럼3
--|:--:|--:
값1 | 값2 | 값3
값4 | 값5 | 값6
값7 | 값8 | 값9
```

>컬럼1 | 컬럼2 | 컬럼3
>--|:--:|--:
>값1 | 값2 | 값3
>값4 | 값5 | 값6
>값7 | 값8 | 값9
