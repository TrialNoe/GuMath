---
tags:
  - "#math"
  - math_calculus
---
## 1.JSC5.4 T77
> [!question] 求极限
> $$
> \lim_{ x\to 0 }{ \frac{ 1 }{ x^{2} } \int_{0}^{x} \frac{2t}{\sqrt{ t^{3} + 1 }}dt }
> $$

> [!tip]+
> 根据[[函数的连续性]]我们把0带进去发现分母为$0$，**分子$\int_{0}^{0}f(x)dx = 0$**，所以是一个$\frac{0}{0}$ 

$$
=  \lim_{ x\to 0 }{ \frac{2x}{ 2x \cdot\sqrt{ x^{3} + 1 }} } = \lim_{ x\to 0 }{ \frac{1}{\sqrt{x^{3} + 1}} } = 1
$$



## 2.JSC5.4 T78

> [!question]
> $$
> \lim_{ x \to \infty }{ \frac{1}{x^{2}} \int_{0}^{x} \ln(1+e^{x}) \, dx  }
> $$
> 

我们可以知道$\ln(1+e^{x})$是一个单调增加的函数，从$0$到$\infty$函数图像和$x$轴围成的面积肯定是无穷的。
![[Pasted image 20251109135617.png|300]]

> [!quote] 上面这句话的定理证明
> 反常积分比较判别法
> $$
> \int_{0}^{\infty }\ln(1+e^{x}) \sim \int_{0}^{\infty}\ln(e^{ x }) = \int_{0}^{\infty} x = \infty 
> $$

$$
=\lim_{ x \to \infty }{ \frac{ \ln(1+e^{x}) }{ 2x } } = \lim_{ x \to \infty }{ \frac{e^{ x }}{2(1+e^{x})}}  = \lim_{ x\to \infty }{ \frac{1}{2\left( 1+\frac{1}{e^{x}} \right)} } = \frac{1}{2}
$$

