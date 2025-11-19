---
tags:
  - "#math"
  - math_calculus
---

> [!question] 求积分
> $$
> \int \arccos x\,dx
> $$

> [!thinking]
> 主要的想法是知道这个复杂的东西的导数，然后就把这个换成u，另一个看成$v=x,v'=1$，这样就转化成了求另一个积分$\int u'\cdot x\,dx$，只要这个积分比以前好求就成功了，不好求也没关系，没变复杂就行


这个可以看成$1\cdot \arccos x$
$$
\begin{aligned}
u=\arccos x,v &= x  \\
u'=-\frac{1}{\sqrt{1-x^{ 2 }}},v'&=1
\end{aligned}
$$
根据[[Integration by Parts]]

$$
\int \arccos x\,dx = x\arccos x - \int \left( -\frac{x}{\sqrt{1-x^{ 2 }}} \right)\,dx
$$
这个$\int-\frac{x}{\sqrt{1-x^{ 2 }}}\,dx$**符合积分核$\int f(g(x))g'(x)\,dx$**，直接[[Subsitution Rule]]
$$
t = 1-x^{ 2 },dt = -2x\,dx,dx=\frac{1}{-2x}\,dt
$$
$$
\int \left( -\frac{x}{\sqrt{1-x^{ 2 }}} \right)\,dx 
= \int - 
\left[ 
\frac{x}{\sqrt{t}} \cdot \left(  \frac{1}{-2x}\,dt \right)
\right]  
= \int \frac{1}{2\sqrt{t}}\,dt 
= \sqrt{t} + C_{1}=\sqrt{1-x^{ 2 }}+C_{1}
$$



是不是$\arcsin x$也可以做呢？$\arctan x$呢

> [!question]
> $$
> \int \arcsin x\,dx
> $$

先来一手[[Integration by Parts]]

$$
\begin{aligned}
u=\arcsin x, v&=x\\
u'=\frac{1}{\sqrt{1-x^{ 2 }}},v'&=1
\end{aligned}
$$
$$
\int 1\cdot \sin x\,dx
= x\arcsin x - \int \frac{x}{\sqrt{1-x^{ 2 }}}\,dx
+C_{1}
$$
根据[[Subsitution Rule]]
$$
\int \frac{x}{\sqrt{1-x^{ 2 }}}\,dx = \int \frac{x}{\sqrt{u}}\cdot \frac{1}{-2x}\,du
= -\int \frac{1}{2\sqrt{u}}\,du = -\sqrt{1-x^{ 2 }} +C_{2}
$$

所以

$$
\int \sin x\,dx = x\arcsin x+\sqrt{1-x^{ 2 }}+C
$$
