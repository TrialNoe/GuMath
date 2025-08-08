---
tags:
  - "#math"
  - math_calculus
---

证明
$$
\text{Theorem If f is differentiable at a, then f is continuous at a.}
$$
这里是数学的世界，先通过建模讲出数学语言
命题就是
$$
\begin{align}
&P:\lim_{x\to{a}}\frac{f(x)-f(a)}{x-a}=C\\
&Q:\lim_{x\to{a}}f(x)=f(a)\\
&P\Rightarrow{Q}
\end{align}
$$
通过[[补项法]]，我们可以把$\lim_{x\to{a}}\frac{f(x)-f(a)}{x-a}$和$\lim_{x\to{a}}f(x)=f(a)$联系起来
$$
\begin{align}
\lim_{x\to a}f(x)
&=\lim_{x\to a}(f(x)-f(a)+f(a))\\
&=\lim_{x\to a}[\frac{f(x)-f(a)}{x-a}(x-a)+f(a)]\\
&=f'(a)\cdot\lim_{x\to a}(x-a) +\lim_{x\to a}f(a)\\
&=0\cdot{f'(a)}+f(a)\\
&=f(a)
\end{align}
$$

