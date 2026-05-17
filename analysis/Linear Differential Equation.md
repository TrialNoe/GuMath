---
tags:
  - "#math"
  - math_calculus
---

> [!question]
> $$
> \frac{dy}{dx} + P(x)y = Q(x)
> $$
> To solve the linear differential equation $y' + P(x)y = Q(x)$ multiply both sides 
> by the integrating factor $I(x) = e^{ \int P(x)\,dx }$ and then integrate both sides.

^d39348

## 1 由导数乘法公式构造？
我们知道

> [!question]
> $$
> [f(x)g(x)]' = f'(x)g(x) + f(x)g'(x)
> $$

所以就对上了
## 2 判断是否为Linear Differential Equation
比方说我们举例子

> [!question]
> $$
> \begin{align}
> 2y\,dx+(y^{ 3 }-x)\,dy &  = 0 \tag{1}\\
> (y-x^{ 3 })\,dx -2x\,dy  & = 0 \tag{2}
> \end{align}
> $$

> [!summary]
> 有一种方法是，如果我们只看$x$或者只看$y$，看看是不是只有一次方（有三角函数、对数、指数等都不包括）的

- 比如$(1)$中，我们如果只看$y$，可以看到$y$有$y,y^{ 3 }$显然不符合[[#^d39348]]，但是我们只看$x$，可以发现只有$-x$这一项,那么这个就是以$x$为因变量，$y$为自变量的Linear DE.
- 如$(2)$，如果我们只看$y$，那么也只有$y$这一项，显然是以$y$为因变量，$x$为自变量的Linear DE.
接下来用Integeral Factor来求解就好了.
## 3 ?
很容易有误区 我们暂时借用编程语言的等于和赋值来区分
这里只考虑$y=0$
$$
4x^{ 3 }y+ x^{ 4 } y' == \sin ^{ 3 }x\tag{1}
$$
很显然如果$x =0$是可以保证方程成立的
但是这个
$$
2xy'+ y == 2\sqrt{x}\tag{2}
$$
如果$x=0$,方程变成了$y==0$，但是$y$你又不知道，不能重新赋进去吧
问题来了，这里$x==0$真的有可能是成立的吗？？？


看了一下答案$(1)$是不用考虑$x==0$这种情况的。。。为什么？？？？

## 4 Bernoulli Differential Equation

> [!equation]
> $$
> \frac{dy}{dx} + P(x)y = Q(x)y^{ n }
> $$
> Let
> 
> | $u=y^{ 1-n }$          | $y=u\cdot y^{ n }$            |
> | ---------------------- | ----------------------------- |
> | $du=(1-n)y^{ -n }\,dy$ | $dy=\frac{1}{1-n}y^{ n }\,du$ |
> 进行替换
> $$
> \frac{1}{1-n}y^{ n }\, \frac{ du }{ dx } + P(x)y = Q(x)y^{ n }
> $$
> 

> [!tip]
> 这里用到一个很关键的$y=u\cdot y^{ n }$，怎么想的呢，因为两边都有这个$y^{ n }$，结论式又没有这个，当然想到是可以约去的，所有就有了这么一出

$$
\frac{1}{1-n}y^{ n }\, \frac{ du }{ dx } + P(x)u\cdot y^{ n } = Q(x)y^{ n }
$$
约分
$$
\frac{1}{1-n}\, \frac{ du }{ dx } + P(x)u = Q(x)
$$
做乘法

> [!equation]
> $$
> \frac{ du }{ dx } + (1-n)P(x)u = (1-n)Q(x)
> $$

^BDEByUSub

