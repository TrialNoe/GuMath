---
tags:
  - "#math"
  - math_calculus
---

> [!NOTE] 主要思想
> 利用sin²x+cos²=1，使得能够让分母为0的式子因公因式约掉


> [!WARNING] 局限性
> 只有三角函数才考虑这个



# Example4

> [!question] Title
> find the limit 
> $$\lim_{x \to 0}\frac{1-\cos{x}}{xsinx}$$

> [!NOTE] Title
>$$
>\begin{align}
>&=\lim_{x \to 0}\frac{1-\cos x}{x \sin x}\cdot \frac{1+\cos x}{1+\cos x}\\
>&=\lim_{x \to 0}\frac{1-\cos ^2x}{x \sin x(1+\cos x)}\\
>\end{align}
>$$
>根据[[三角函数的基本关系]](1-cos²=sin²x)
>$$
>\begin{align}
>&=\lim_{x \to 0}\frac{\sin^2{x}}{x \sin x (1+\cos x)}\\
>&=\lim_{x \to 0}\frac{\sin x}{x} \cdot \lim_{x \to 0}\frac{1}{1+cosx}\\
>&=\lim_{x \to 0}\frac{\sin x}{x}
>\end{align}
>$$
>根据[[洛必达法则]]
>$$
>\begin{align}
>&=\lim_{x\to0}\frac{cosx}{1}=\frac{\cos{0}}{1}=1
>\end{align}
>$$
