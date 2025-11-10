---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---

> [!question]
> 设$h>0$，求证：
> $$
> \frac{h}{1+h^{2}}\leq \arctan h \leq h.
> $$


我们知道$\arctan h$的导数为$\frac{1}{1+h^{2}}$和不等式的左边形式很接近（就差了个$h$），如果让$h=0$的话就同时和左右都很接近，这种**通过导数的信息去推导原函数的信息**可以让我们联想到[[Langrange's Mean Value Theorem(拉格朗日中值定理)#1-数学意义]]

令$f(h) = arctan h,f^{'}(h)=\frac{1}{1+h^{2}}$
通过[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]我们知道，在$(0,h)$内存在$\xi,$使得$f^{'}(\xi)=\frac{f(h)-f(0)}{h-0}=\frac{\arctan h}{h}$
再把$f^{'}(\xi)$进行展开
$$
f^{'}(\xi)=\frac{1}{1+\xi^{2}}=\frac{\arctan h}{h}
$$
$$因为\xi \in(0,h)\implies\xi^{2}\in (0,h^{2}) \implies \frac{1}{1+h^{2}}<\frac{1}{1+\xi^{2}}<1$$
所以再替换一下，很**显然**原不等式就得证了。
$$
\begin{align}
&\quad\quad\frac{1}{1+h^{2}}<\frac{\arctan h}{h}<1 \\
&\implies \frac{h}{1+h^{2}}<\arctan h<h
\end{align}
$$
