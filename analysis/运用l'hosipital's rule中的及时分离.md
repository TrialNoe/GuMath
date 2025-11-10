---
tags:
  - "#math"
  - math_calculus
---

> [!example]
> 求极限
> $$
> \lim_{ x \to 0 } \frac{\tan x - x}{x^3}
> $$

> [!thinking]
> 这种肯定是可导的，代入$0$之后发现为$\frac{0}{0}$的**indeterminate form**，又无法使用[[同除x的r次方求有理式无穷时的极限]]和[[利用因式分解求分母为0时的极限]]，只好采用[[洛必达法则(L'Hospital's Rule)求未定型的极限]]

根据洛必达法则，我们有
$$
 \begin{align}
\lim_{ x \to 0 } \frac{\tan x - x}{x^3} & =\lim_{ x \to 0 } \frac{\sec^2 x-1}{3x^3} \\
 & = \lim_{ x \to 0 } \frac{2\tan x \sec^2x}{6x} \\
 & = \lim_{ x \to 0 } \frac{\tan x \sec^2x}{3x}
\end{align}
$$

我们知道$\lim_{ x \to 0 }\sec x = 1$，**利用[[极限的运算法则]]分离出来可以是下一步不算这个$\sec$，达到一个简化运算的作用**
就有
$$
\begin{align}
\lim_{ x \to 0 } \frac{\tan x \sec^2x}{3x}  & = \lim_{ x \to 0 } \sec^2 x \cdot \lim_{ x \to 0 } \frac{\tan x}{3x} \\
 & =1 \cdot \lim_{ x \to 0 } \frac{\tan x}{3x} \\
 & =\lim_{ x \to 0 } \frac{\sec^2 x}{3} \\
 & = \frac{1}{3}
\end{align}
$$
