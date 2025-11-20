---
tags:
  - "#math"
  - math_analysis
---

> [!question] 证明
> 已知函数$f(x)$在$[0,1]$上连续，在$(0,1)$内可导，并且$f(0)=0,f(1)=1$
> $(1)$存在$\xi \in (0,1)$,使得$f(\xi)=1-\xi$.
> $(2)$存在两个不同的点$\zeta,\eta \in (0,1)$，使得$f'(\xi)f'(\eta)=1$

## 1.零点存在定理

> [!tip] 
> 这个有个问题是会想成[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]但是，这不是导函数和原函数信息的互推，做不出来的。
> 真正的是两个函数相等的恒等式嘛，很自然会转化成一个函数的零点存在问题。

令$\large g(x) = f(x)+x-1,x \in (0,1)$
很显然根据**间值定理**
$$
\begin{aligned}
&g(0) = f(0) + 0 -1 = -1 < 0\\
&g(1) = f(1) + 1 - 1 = 1 < 0
\end{aligned}
$$
所以
$$
\exists \xi \in (0,1),g(\xi) = 0
$$
即
$$
f(\xi)=1-\xi.
$$
Q.E.D


## 2.Lagrange's Mean Value Theorem


> [!tip]
> 两个单独的变量和[[Cauchy mean value theorem(柯西中值定理)]]推导的时候根本不一样，所以我感觉要用两次[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]
> 
> > [!trick]
> > **一个配套Lagrange's Mean Value Theorem多独立变量的技巧是拆分区间**(应试产物，我是很数学洁癖的)
> 

由[[#1.零点存在定理]]我们可以知道，$f(\xi)=1-\xi$
拆前半段
$$
\exists \zeta \in (0,\xi),f'(\zeta) = \frac{ f(\xi) - f(0) }{ \xi - 0 } = \frac{ 1-\xi }{ \xi }
$$
拆后半段
$$
\exists \eta \in (\xi,1),f'(\eta) = \frac{f(1) - f(\xi)}{1-\xi} =  \frac{\xi}{1-\xi}
$$

所以
$$
f'(\eta)\cdot f'(\zeta) = 1
$$

