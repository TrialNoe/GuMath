---
tags:
  - "#math"
---

> [!question] 求积分
> $$
> \int \frac{1}{1+e^{x}}\,dx
> $$
> 

## 解法1：拆分Partial Fraction Decomposition
$$
\begin{aligned}
&=\int \frac{e^{ x }\cdot e^{ -x }}{1 + e^{ x }}\,dx  \\
&=\int \frac{1}{u(u-1)}\,du &&& (u=1+e^{ x },du=e^{ x }\,dx) \\
&=\int \frac{1}{u^{ 2 }  - u}\,du
\end{aligned}
$$
然后就做不下去了，问了ai，我猜他的思路是用[[L'hospital Rule解决对分子为不定积分的不定型求极限]]中$\infty-\infty$要通分提供的思路，积分是不是可以反过来去拆分？！
也可是[[使用拆分法计算某些函数的n阶导数]]中，把一个复杂的高次因式，拆成多个简单的一次因式的求和
$$
\begin{align}
& = \int \left[ \frac{1}{u-1} - \frac{1}{u} \right]\,du &&&\\
&= \ln|u-1| - \ln|u| + C &&&\\
&= x - \ln(e^{ x } + 1) + C &&&
\end{align}
$$


## 解法2：“还原”Logistic function

> [!quote] 标准的Logistic function长相是这样的
> $$
> F(t) = \frac{1}{1+e^{ \frac{ -t-\mu }{ \gamma } }}
> $$
> 当$\mu = 1,\gamma = 1$就变成了$F(t) = \frac{1}{1+e^{ -t }}$
> 


$$
\begin{align}
=\int\frac{1}{1+e^{ -x }} \cdot e^{ -x }\,dx & = \int \frac{1}{u}\,du &&\cdots(u=1+e^{ -x },du=e^{ -x }\,dx ) \\
&=\ln|u|+C \\
&=\ln|1+e^{ -x }| + C \\
&=\ln(1+e^{ -x }) + C \\
&=\ln(1+e^{ x }) - x +C
\end{align}
$$
