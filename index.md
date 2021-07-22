---
layout: default
---

# 2장 확률분포

1장 리뷰
> 1장에서는 패턴 인식 문제를 해결하는데 있어서 확률론이 얼마나 중심적인 위치를 차지하고 있는지에 대해 공부  
> 2장에서는 몇몇 **확률 분포**의 예시와 성질에 대해서 공부할 예정  
> 또한 확률 분포를 바탕으로 베이지안 추론 등의 중요한 통계적인 개념들을 살펴볼 예정

2장에서 논의할 분포의 역할들 중 하나의 한정된 수의 관찰 집합 $x_{1},...,x_{N}$이 주어졌을 때 확률 변수 $x$의 확률 분포 $p(x)$를 모델링하는 것이다.

2장에서는 목표를 위해 1) 데이터 포인터들은 독립적, 2) 동일하게 분포됨 이라고 가정할 것이다.
사실 밀도 추정 문제는 근본적으로 타당하지 않다고 한다. 제한된 수의 관찰된 데이터 집합으로부터 가능한 모 확률 분포의 가짓수는 무한이기 때문이다. 

*	모비율 : 지지율, 시청률, 실업률 따위와 같이 모집단에서 어떤 사건에 대한 비율
*	모분포 : ...? 같은 뜻인가...?

각각의 데이터 포인트 $x_{1},...,x_{N}$에 대해서 0이 아닌 값을 가지는 어떤 분포 $p(x)$도 모 분포의 후보가 될 수 있다. 이들 중에서 적절한 분포를 선택하는 것은 1장의 다항식 곡선 근사 문제에서 맞닥뜨렸던 모델 선택의 문제와 연관되어 있다. 이는 패턴 인식 문제의 중요 쟁점 사항 중 하나라고 한다.

* 	다항식 곡선 근사 문제에서의 모델 선택 문제 : ...?

저자는 2장에서는 우선 **이산 확률 변수의 이항분포와 다항분포**에 대해 살펴보고, 그 다음엔 **연속 확률 변수의 가우시안 분포**에 대해서 알아본다고 한다. 이 분포들은 **매개변수적** 분포의 예시이다. 이렇게 불리는 이유는 분포들이 작은 수의 조절 가능한 매개변수에 의해 결정되기 때문이라고 한다. 이런 매개변수의 예시로 가우시안 분포의 평균와 분산이 있다고 한다.


Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
