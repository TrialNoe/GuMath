---
tags:
  - "#math"
  - math_calculus
---
> [!question]
> 设$f(x)$在$[0,1]$上连续，在$(0,1)$内可导，且满足条件$f(1)=2\int_{0}^{ \frac{ 1 }{ 2 } }xf(x)\,dx$，试证：存在$\xi \in (0,1)$，使得
> $$
> f(\xi) + \xi f'(\xi) = 0
> $$

我们根据[[MVT]]的思路，应该是让我们去解一个微分方程
$$
f'(x) + \frac{1}{x}f(x)
$$
根据微分方程的几步思路
$$
I(x) = e^{ \int{\frac{ 1 }{ x }\,dx} } = e^{ \ln |x| } = x 
$$
emmm没有一眼看出来，原来这是那个乘法的求导法则
$$
F(x) = xf(x)
$$
就是证明$F(x)$存在Rolle's Point
仿照以前的思路去代入两个端点
$$
F(0) = 0,F(1)=2\int_{0}^{ \frac{ 1 }{ 2 } }xf(x)\,dx
$$
但是发现这两东西都不相等呀，何意味。


**不知道怎么想得MVT for Integrals**
$$
F(1) = 2\int_{0}^{ \frac{ 1 }{ 2 } }xf(x)\,dx = 2 \left( \frac{1}{2}-0 \right)cf(c) = cf(c)
$$
那我们又知道了直接把$c$带进去$F(x)$好像也是这个结果
$$
F(c) = cf(c)
$$
很快哈，根据Rolle's MVT我们可以知道，确实存在这样一个$\xi$使得
$$
f(\xi) + \xi f'(\xi) = 0
$$
Q.E.D.
