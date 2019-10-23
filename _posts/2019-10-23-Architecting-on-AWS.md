---
layout: post
title: "Architecting on AWS 정리"
comments: true
description: "Quick review purpose"
keywords: "Cloud, AWS, Solutions Architect, Associate"
---

# What is Cloud?

>> Cloud Computing
Computing resource를 대여해서 사용하는 것.
Internet에 연결되어 있다면 언제든지 사용가능.
'Pay as you go'기 때문에 전략을 바꿀때 민첩성에 힘을 실어줌.

6가지 benefit from cloud computing

1. CapEX --> VarEX
2. 규모의 경제
3. 용량 추정 불필요
4. Agility & Fast
5. 중요한 문제(Business)에 집중
6. Go global in minuites

# AWS Well-Architected Framework

>> _AWS의 설계 원칙 목표_ 는 보안, 안정성, 비용 최적화, 성능 효율성 그리고 운영 우수성으로 나뉜다.

1. **보안**
    정보를 보호하고 손해를 최소화하는 목표.
    Architecture level에서 자격 증명 기반, traceability activation, 모든 layer에 security rule 적용, security best practice 자동화, 전송 및 저장 시 데이터 암호화 등의 basic security guide line 적용. 이를 통해 보안 강화.

2. **안정성**
    기존 환경에서는 안정성을 보장하기가 어려움. 단일 장애 지점, 자동화 미비, 탄력성 부족에서 문제가 발생합니다. 안정성 핵심 요소의 아이디어를 적용하면 이러한 문제를 다수 방지할 수 있습니다. HA Architecture, fault tolerance and overall duplication 을 통해서 안정성 취할 수 있음

3. **Cost Optimization**
    Production의 수명 내내 정교화되고 개선되어야 함. 현재 Architecture

## Typography Elements in One

Let's start with a informative paragraph. **This text is bolded.** But not this one! _How about italic text?_ Cool right? Ok, let's **_combine_** them together. Yeah, that's right! I have code to highlight, so `ThisIsMyCode()`. What a nice! Good people will hyperlink away, so [here we go](#) or [http://www.example.com](http://www.example.com).

<div class="divider"></div>

## Headings H1 to H6

# H1 Heading

## H2 Heading

### H3 Heading

#### H4 Heading

##### H5 Heading

###### H6 Heading

<div class="divider"></div>

## Footnote

Let's say you have text that you want to refer with a footnote, you can do that too! This is an example for the footnote number one [[^1]]. You can even add more footnotes, with link! [[^2]]

<div class="divider"></div>

## Blockquote

> Start by doing what's necessary; then do what's possible; and suddenly you are doing the impossible. --Francis of Assisi

**NOTE:** This theme does NOT support nested blockquotes.

<div class="divider"></div>

## List Items

1. First order list item
2. Second item

* Unordered list can use asterisks
- Or minuses
+ Or pluses

<div class="divider"></div>

## Code Blocks

```javascript
var modularpattern = (function() {
    // your module code goes here
    var sum = 0 ;

    return {
        add:function() {
            sum = sum + 1;
            return sum;
        },
        reset:function() {
            return sum = 0;    
        }  
    }   
}());
alert(modularpattern.add());    // alerts: 1
alert(modularpattern.add());    // alerts: 2
alert(modularpattern.reset());  // alerts: 0
```

```python
s = "Python syntax highlighting"
print s
```

```
No language indicated, so no syntax highlighting.
But let's throw in a <b>tag</b>.
```

<div class="divider"></div>

## Table

### Table 1: With Alignment

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

### Table 2: With Typography Elements

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

<div class="divider"></div>

## Horizontal Line

The HTML `<hr>` element is for creating a "thematic break" between paragraph-level elements. In markdown, you can create a `<hr>` with any of the following:

* `___`: three consecutive underscores
* `---`: three consecutive dashes
* `***`: three consecutive asterisks

renders to:

___

---

***

<div class="divider"></div>

## Media

### YouTube Embedded Iframe

<div class="video-container"><iframe src="https://www.youtube.com/embed/n1a7o44WxNo" frameborder="0" allowfullscreen></iframe></div>

### Image

![Minion](http://octodex.github.com/images/minion.png)

---
Footnote:

[^1]: 1: Footnote number one yeah baby!

[^2]: 2: A footnote you can link to - [click here!](#)
