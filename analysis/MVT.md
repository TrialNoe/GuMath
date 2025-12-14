---
tags:
  - "#math"
  - math_calculus
  - math_analysis
  - math_ideas_tools
---
## 0 基本想法
> [!thinking] 基本想法
> MVT主要是利用导数信息去推导原函数信息的工具，主要有[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]、[[Rolle's Theorem(罗尔中值定理)]]、[[Cauchy mean value theorem(柯西中值定理)]]、泰勒中值定理
> 通过这几种MVT的组合啊，代数运算可以对原函数复杂的形式进行说明，技巧性还是挺强的，后面举例子进行详细说明

## 1 解微分方程构造辅助函数（一阶导+原函数/只是一阶导）

> [!tip] Title
> 这一块的原理是Solve differential eqn(解微分方程)F(x)，然后利用MVT证$F'(x)=0$有解

### 例子1 只是一阶导

> [!example]
> 设$f(x)$在$[a,b]$上连续，在$(a,b)$内可导，证明存在$\xi \in (a,b)$，使得
> $$
> 2\xi[f(b) - f(a)] = (b^{ 2 } - a^{ 2 })f'(\xi)
> $$

> [!warning]
> 这里千万不能用[[Cauchy mean value theorem(柯西中值定理)]]
> 因为，你肯定会移项成
> $$
> \frac{f'(\xi)}{g'(\xi)} = \frac{f(b) - f(a)}{g(b) - g(a)} \quad\quad \dots (where\ g(x) = x^{ 2 })
> $$
> 
> 当$(c = 0) \in (a,b),g'(c) = 0$
> 0怎么能做分母呢？？

移项，我们换个思路去证明零点存在
$$
(b^{ 2 } - a^{ 2 })f'(\xi) - 2\xi[f(b) - f(a)] = 0
$$
令$g(x)=(b^{ 2 } - a^{ 2 })f'(x) - 2x[f(b) - f(a)],G'(x)=g(x),C=0$
我们观察$g(x)$他只有导函数而已，直接积分就行了
$$
\begin{aligned}
G(x) &= \int g(x)\, dx \\ 
&= (b^{ 2 } - a^{ 2 })\int f'(x)\,dx - [f(b) - f(a)]\int2x\,dx \\
&= (b^{ 2 }-a^{ 2 })f(x) - [f(b) - f(a)] x^{ 2 }
\end{aligned}
$$
那么我们探一下两个端点
$$
G(a) = b^{ 2 }f(a) - a^{ 2 }f(b) ,G(b) = b^{ 2 }f(a) - a^{ 2 }f(b)
$$
哇,$G(a)=G(b)$，根据[[Rolle's Theorem(罗尔中值定理)]],存在$\xi \in (a,b)$,使得$g(\xi) = 0$
Q.E.D


### 例子2 一阶导+原函数

> [!example]
> 设$f(x)$可导，证明对任意的实数$\lambda$，在$f(x)$的两个零点之间必存在$\lambda f(x) + f'(x)= 0$
> 

> [!thinking] 准备工作
> 不如先把这两个零点显性表示出来即
> $$
> a<b,f(a) = f(b) = 0
> $$
> 改写一下命题，数学化一点
> $$
> \forall \lambda \in R,\exists \xi \in (a,b), \lambda f(\xi) + f'(\xi)= 0
> $$

仿照[[#例子1]]
$$
g(x) = \lambda f(x) + f'(x)
$$
**因为g(x)是linear eqn解微分方程，**
$$
I(x) = e^{ \int \lambda\,dx } = e^{ \lambda x }
$$

$$
h(x) = I(x)\cdot g(x) = e^{ \lambda x }[\lambda f(x) + f'(x)]
$$
积分(都说默认C=0了)
$$
H(x) = \int h(x)\,dx = e^{ \lambda x }f(x)
$$
由于$f(a) = f(b) = 0$,所以 $H(a) = H(b) = 0$
即
$$
\forall \lambda \in R,\exists \xi \in (a,b), g(\xi)= 0
$$
Q.E.D.

## 2 多个点
- [[多个独立点的Lagrange's Mean Value Theorem 问题]]："分割区间"可以做出2个的，效率也很高，但是3个点以上就不太行了；n个点用归纳假设才能做

## 3 二阶导和一阶导