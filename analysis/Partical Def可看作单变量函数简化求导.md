---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---
## 启发性的题目

> [!question]
> 已知$r=\sqrt{x^{ 2 }+y^{ 2 }+z^{ 2 }}$，并且$u=\frac{1}{r}$，求$du$.
> 

这个如果重复来算是很麻烦的，这个$\sqrt{x^{ 2 }+y^{ 2 }+z^{ 2 }}$重复出现，就有点浪费时间。

这时候就可以使用Chain Rule进行求导

这个怎么看呢

$$
r(x,y,z) = \sqrt{x^{ 2 }+y^{ 2 }+z^{ 2 }}
$$
$u(r(x,y,z)) = \frac{1}{r}$
在求偏导的时候我们通常把另外两个变量fixed
$$
\begin{align}
f(x) = \sqrt{x^{ 2 }+ y^{ 2 } + z^{ 2 }}  \\
g(y) = \sqrt{y^{ 2 } + x^{ 2 } +  z^{ 2 }} \\
h(z) = \sqrt{z^{ 2 }+x^{ 2 }+y^{ 2 }}
\end{align}
$$

$$
u'_x(r(x,y,z)) = [u(f(x))]' =f'(x)u'(f(x))
$$
其他同理
我们试一下
$$
u'_{x}(r) = f'u'(r) = \frac{2x}{2\sqrt{x^{ 2 }+y^{ 2 }+z^{ 2 }}} \cdot \left( -\frac{1}{r^{ 2 }} \right)=\frac{x}{r}\cdot\left( -\frac{1}{r^{ 2 }} \right)
$$

同样的根据轮换对称
$$
\begin{align}
u'_{y}(r) = g'(y)u'(r) = \frac{y}{r}\cdot\left( -\frac{1}{r^{ 2 }} \right) \\
u'_{y}(r) = h'(z)u'(r) = \frac{z}{r}\cdot\left( -\frac{1}{r^{ 2 }} \right)
\end{align}
$$



$$
du = -\frac{x+y+z}{-r^{ 3 }}
$$

