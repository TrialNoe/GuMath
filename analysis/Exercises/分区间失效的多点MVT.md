---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---
> [!question]
> 设函数 $f(x)$ 在 $[a, b]$ 上连续，在 $(a, b)$ 内可导，且 $f'(x) \neq 0$，试证：存在 $\xi \in (a,b)$ 且 $\eta \in (a,b)$，使得
> $$
> \frac{f'(\xi)}{f'(\eta)} = \frac{e^{b} - e^{a}}{b - a} \times e^{-\eta}.
> $$
> 

两个点嘛，很自然想到上次的分区间来做

$$
f'(\xi) = \frac{f(c) - f(a)}{c-a},f'(\eta) = \frac{ f(b) - f(c)}{ b-c }
$$
哪来的e没有e
上次也是乘一个$e^{ x }$
$$
g(x) = e^{ x }f(x)
$$

也是没用的

直接用
$$
\begin{aligned}
f'(\xi) = \frac{f(b)-f(a)}{b-a} \\
\frac{f'(\eta)}{e^{ \eta }} = \frac{f(b) - f(a)}{b-a}
\end{aligned}
$$
除一下

Q.E.D.

