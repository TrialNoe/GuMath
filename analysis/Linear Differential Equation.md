---
tags:
  - "#math"
  - math_calculus
---
$$
\frac{dy}{dx} + P(x)y = Q(x)
$$
To solve the linear differential equation $y' + P(x)y = Q(x)$ multiply both sides 
by the integrating factor $I(x) = e^{ \int P(x)\,dx }$ and then integrate both sides.
## 由导数乘法公式构造？
我们知道
$$
[f(x)g(x)]' = f'(x)g(x) + f(x)g'(x)
$$
所以就对上了


## ?
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

## Bernoulli Differential Equation
$$
\frac{dy}{dx} + P(x)y = Q(x)y^{ n }
$$
Let

| $u=y^{ 1-n }$          | $y=u\cdot y^{ n }$            |
| ---------------------- | ----------------------------- |
| $du=(1-n)y^{ -n }\,dy$ | $dy=\frac{1}{1-n}y^{ n }\,du$ |
进行替换
$$
\frac{1}{1-n}y^{ n }\, \frac{ du }{ dx } + P(x)y = Q(x)y^{ n }
$$

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
$$
\frac{ du }{ dx } + (1-n)P(x)u = (1-n)Q(x)
$$
^BDEByUSub

