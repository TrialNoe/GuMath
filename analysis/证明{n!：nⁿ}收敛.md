---
tags:
  - "#math"
  - math_calculus
---
## 命题0

> [!question] 证明数列收敛
> $$
> \large
> a_{n} = \frac{n!}{n^{ n } } 
> $$
> 

### 单调性
$$
\frac{a_{n+1}}{a_{n}} = \frac{ \frac{n!}{n^{ n } }  }{ \frac{(n+1)!}{(n+1)^{ n+1 } } } = \frac{n!(n+1)^{ n+1 }}{(n+1)!n^{ n }}
$$
简单约分一下
$$
RHS = \frac{1\cdot(n+1)^{ \cancel{ n+1 }n }}{\cancel{ (n+1) }n^{ n }} =\left( \frac{ n+1 }{ n } \right)^{ n }<1
$$
所以
$$
a_{n}>a_{n+1}
$$
decreasing

### 有界性
$$
a_{n} = \frac{n!}{n^{ n } }  >0
$$
肯定有界，不知道界具体是哪个而已。。
所以$\large{a_{n}}$收敛

#todo
具体的界限是0,不知道怎么求的
## 推广1
[[#命题0]]更像是比值，然后分子和分母竞争。
我们对命题进行修改看看能不能做

> [!question]
> 研究
> $$
> a_{n}  =n^{ n } - n!
> $$
> 的收敛性

仿照[[#单调性]]：
$$
a_{n+1} - a_{n} = (n+1)^{ n+1 } - n^{ n } + (n+1)!-n!
$$
合并下
$$
RHS = (n+1)^{ n+1 }-n^{ n }+n\cdot n!
$$
显然$(n+1)^{ n+1 }-n^{ n } >0,n\cdot n!> 0$
$$
a_{n+1}>a_{n}
$$
单调增加


但是这样做不下去..
$$
\lim_{ n \to \infty }{ (n^{ n } - n!) }
$$
假设事先是不知道$n^{ n }$增长比$n!$快
我们可以利用一下[[#命题0]]，因为是一个$\infty-\infty$，当然要去通分
$$
\lim_{ n \to \infty }{ \left( \frac{ 1-\frac{n!}{n^{ n }} }{ \frac{1}{n^{ n }} } \right) }
$$
**这样做不了。。**
$$
\lim_{ n \to \infty }{ n^{ n }\left( 1-\frac{n!}{n^{ n  }} \right) } = \infty\cdot \left( 1-0 \right) = \infty
$$

在这里反而用不上Monotinic Squence Theorem

