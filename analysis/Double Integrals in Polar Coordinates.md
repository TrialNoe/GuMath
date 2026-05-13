---
tags:
  - "#math"
  - math_calculus
---

> [!summary]
> 比较常用该方法就是底座的轨迹是一个圆，三叶草，Fermat's spiral ($r=\sqrt{\theta}$)，或者是给定的一些极坐标方程

## 1 流程化
1. 写出替换式$x=r\cos\theta,y=r\sin\theta$
2. 找到$r$ 和 $\rho$的范围
3. 补$r$


## 2 1

> [!question]
> $$
> \iint_{D}e^{ -x^{ 2 }-y^{ 2 } }\,dA
> $$
> D是由`y-axis`和$x=\sqrt{4-y^{ 2 }}$围成的面积.

我们看到这个$x=\sqrt{4-y^{ 2 }}$是一个半圆，很自然可以想到换成极坐标系比较容易做
$$
r\in[0,2],\rho\in [-\pi,\pi]
$$

$$
\int_{-\pi}^{ \pi }\int_{0}^{ 2 }re^{ -r^{ 2 } }\,dr\,d\theta
$$
换元积分
$$
\begin{align}
  t=-r^{ 2 }, & t(0)=0,t(2)=-4 \\
 & dt=-2r\,dr
\end{align}
$$
$$
\begin{align}
\int_{-\pi}^{ \pi }\int_{0}^{ 4 }-\frac{1}{2}e^{ t }\,dt\,d\theta & =-\frac{1}{2}\int_{-\pi}^{ \pi }\left[e^{ t }\right]_{0}^{ 4 }\,d\theta=-\frac{1}{2}\int_{-\pi}^{ \pi }(e^{ 4 }-1)\,d\theta=-\frac{1}{2}(e^{ 4 }-1)\int_{-\pi}^{ \pi }\theta \\
 & =-\frac{1}{2}(e^{ 4 }-1)\cdot2\pi \\
 & =\pi(1-e^{ 4 })
\end{align}
$$

## 3 