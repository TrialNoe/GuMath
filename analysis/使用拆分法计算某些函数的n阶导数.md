---
tags:
  - "#math"
  - math_calculus
---

> [!question]
> $$
> f(x) = \frac{1}{x^{2} -3x +2},\text{求}f^{(n)}(x)
> $$

> [!thinking]+
> 这个**分母这么复杂还要求这么多次导数**肯定很难做，但是根据[[Partial Fraction Decomposition(部分分式分解)]]，又因为我们有了$\frac{d^{n}}{dx^{n}}\left( \frac{1}{x} \right) = (-1)^{n} \frac{n!}{x^{n+1}}$这个求分式函数高阶导数的工具，问题就迎刃而解了。

$$
f^{(n)}(x) = \frac{d^{n}}{dx^{n}}\left( \frac{1}{x-2} - \frac{1}{x-1} \right)
$$
算一下就是
$$
\begin{align}
f^{(n)}(x) & = \frac{d^{n}}{dx^{n}}\left(\frac{1}{x-2}\right)- \frac{d^{n}}{dx^{n}}\left(\frac{1}{x-1}\right) \\  
 & = (-1)^{n}\frac{n!}{(x-2)^{n+1}} - (-1)^{n} \frac{ n! }{ (x-1)^{n+1} } \\
 & =(-1)^{n} \cdot n! \cdot \left( \frac{ 1 }{ x-2 } - \frac{1}{x-1} \right)^{n+1}
\end{align}
$$
