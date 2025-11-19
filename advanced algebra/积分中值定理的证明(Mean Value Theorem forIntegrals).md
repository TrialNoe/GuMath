---
tags:
  - "#math"
  - math_analysis
---
求证
$$
\int_{a}^{ b }f(t)\,dt=f(\xi)(b-a),(a<b)
$$

对于$\int_{a}^{ b } f(x)\,dx$而言$f(x)$是他的导数，这不就是原函数和导数的信息互推吗，自然而然可以想到[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]，但是要把那个形式做出来
我们可以让$G'(x)=f(x)$,那么
$$
LHS = G(b)-G(a)
$$
根据[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]
我们可以知道
$$
\exists \xi \in (a,b), \frac{ G(b)-G(a) }{ b-a } = f(\xi)
$$
移项
$$
G(b) - G(a) = f(\xi)\cdot(b-a)
$$
$$
LHS =\int_{a}^{ b }f(x)\,dx= f(\xi)\cdot(b-a)
$$
Q.E.D
