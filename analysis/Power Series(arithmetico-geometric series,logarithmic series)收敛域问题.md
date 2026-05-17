---
tags:
  - "#math"
---
我们经常看见这样的问题

> [!equation] arithmetico-geometric series
> $$
> \sum^{\infty}_{n=k} a_{n}x^{ n },a_{n}=n\,q^{ n }
> $$


或者说是

> [!equation] logarithmic series
> $$
> \sum^{\infty}_{n=k} a_{n}x^{ n },a_{n}=\frac{q^{ n }}{n}
> $$

很自然就产生一个问题，到底是**什么样的约束条件(q)**\,才能满足让原来的Series收敛呢？他的收敛域又是一个什么情况呢？

## 1 我们先研究arithmetico-geometric series

> [!equation] arithmetico-geometric series
> $$
> \sum^{\infty}_{n=k} a_{n}x^{ n },a_{n}=n\,q^{ n }
> $$

很自然地我们根据[[Power Series#1 一般化的步骤]]，我们先求Radius of convergence
$a_{n}=nq^{ n }$
$$
R= \left\lvert \frac{a_{n}}{a_{n+1}} \right\rvert =\left\lvert \frac{nq^{ n }}{(n+1)q^{ n+1 }} \right\rvert 
=\left\lvert \frac{n}{n+1} \frac{1}{q} \right\rvert 
=\left\lvert \frac{1}{1+\frac{1}{n}} \frac{1}{q}\right\rvert\to \left\lvert \frac{1}{q} \right\rvert 
$$
as $n\to \infty$
那么我们下面对这个边界进行讨论
这个$\frac{1}{q}$带个绝对值，太麻烦了，我们分类进行讨论吧
### 1.1 q=0
这个时候原来的$Serie$就是
$$
\sum^{\infty}_{n} 0 = 0
$$
显然是收敛的。

### 1.2 q>0
when $x=\left\lvert \frac{1}{q} \right\rvert = \frac{1}{q}$
$$
\sum^{\infty}_{n}nq^{ n }\left(\frac{1}{q} \right)^{ n } = \sum^{\infty}_{n=1} \frac{1}{n}
$$
回到了[[证明Harmonic Series发散]]，那就是Divergent.

when $x=- \frac{1}{q}$
$$
\sum^{\infty}_{n}nq^{ n }\left(-\frac{1}{q} \right)^{ n } = \sum^{\infty}_{n=1} (-1)^{ n }\frac{1}{n}
$$
变成了alternating series，显然是Convergent.
那么这个时候的收敛域就是$x \in [-\frac{1}{q}, \frac{1}{q})$

### 1.3 q<0
when $x =  \left\lvert \frac{1}{q} \right\rvert = -\frac{1}{q}$
$$
\sum^{\infty}_{n}nq^{ n }\left(-\frac{1}{q} \right)^{ n } = \sum^{\infty}_{n=1} (-1)^{ n }\frac{1}{n}
$$
Convergent


when $x= -\left\lvert \frac{1}{q} \right\rvert = \frac{1}{q}$
