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

이러한 모델을 밀도 추정 문제에 적용하기 위해서는 관찰된 데이터 집합을 바탕으로 적절한 매개변수의 값을 구하는 과정이 요구된다. 빈도적 관점에서는 어떤 특정 기준을 최적화 하는 방식으로 매개변수를 찾게 된다. 그 예시로는 가능도 함수(Likelihood)가 있다. 이와는 반대로 베이지안 관점에서는 매개변수에 대한 사전 분포를 바탕으로 관측된 데이터 집합이 주어졌을 때의 해당 사후 분포를 계산한다(베이지안 정리를 사용하여).

**켤레**(_conjugate_) 사전 확률이 중요한 역할을 한다는 것도 살펴본다고 한다. 켤레 사전 확률은 사후 확률이 사전 확률과 같은 함수적 형태를 띄도록 만들어 준다.

*	사전분포와 사후분포가 모숫값만 다르고 함수 형태가 같은 확률밀도함수로 표현될 수 있도록 해주는 사전분포를 켤레 사전확률분포라고 한다.

그 결과, 베이지안 분석이 매우 단순해진다. 예를 들어, 다항 분포 매개변수의 켤레 사전 확률은 **디리클레 분포**(_Dirichlet distribution_)이며, 가우시안 분포 평균값의 켤레 사전확률은 또 다른 가우시안 분포이다. 이 분포들은 모두 **지수족**(_exponential family_)에 속한다. 지수족 분포들은 몇몇 중요한 성질들을 가지고 있는데, 이에 대해 추후에 설명한다고 한다.

*	디리클레 분포는 연속 확률분포의 하나로, $k$차원의 실수 벡터 중 벡터의 요소가 양수이며 모든 요소를 더한 값이 1인 경우($k-1$차원 단체(_simplex_)) 에 대해 확률값이 정의되는 분포이다. (_위키백과_)
*	지수족 : 지수함수와 연관되어 있는 특정 확률분포 종류를 가리키는 말로, 정규 분포나 감마 분포, 다항 분포 등 일반적으로 널리 사용되는 분포들이 다수 포함되어 있다.

매개변수적인 접근법의 한계점 중 하나는 분포가 특정한 함수의 형태를 띠고 있다고 가정한다는 것. 이는 몇몇 적용 사례의 경우에는 적절하지 않다. 이럴 땐 **비매개변수적**(_nonparametric_) 밀도 추정 방식이 대안으로 활용될 수 있다고 한다. 비매개변수적 밀도 추정 방식에서는 분포의 형태가 데이터 집합의 크기에 종속적이다. 이러한 모델들은 매개변수를 가지고 있지만, 분포 형태를 결정짓는 것이 아니라 모델 복잡도에 영향을 미친다고 한다. 2장 마지막에서는 히스토그램, 최근점 이웃, 커널을 바탕으로 한 비매개변수적 방법에 대해서 논의할 것이다.

# 2.1 이산 확률 분포

하나의 이진 확률 변수 $x\in\{0,1\}$을 고려해 본다. 예를 들어 $x$는 동전 던지기의 결괏값을 설명하는 확률 변수이다. $x = 0,1$은 동전의 앞,뒤인 경우로 판단하면 될 듯 하다. 만약 동전이 망가져서 앞면이 나올 확률과 뒷면이 나올 확률이 동일하지 않다고 가정해보자. 이때 $x=1$일 확률은 매개변수 $\mu$를 통해 다음과 같이 표현할 수 있다.

```
$p(x = 1|\mu) = \mu$
```



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
