---
tags:
  - "#math"
  - math_calculus
---
## 1.Ex4

> [!question] 求极限
> $$
> \lim_{x\to0^{+}}{(1+x)^{\frac{1}{\sqrt{x}}}}
> $$

> [!tip]
> 想着这个$(1+🤤)^{\frac{1}{🤤}}$结构就想起了[[e的极限表达证明极限存在的构造斜率式证法#^1d7f7f]]的表达式，可以加以利用一下

> [!error]
> 为什么不能做成
> $$
> =\lim_{ t \to +\infty } {\left[\left( 1+\frac{1}{t} \right)^{t} \right]^{\frac{1}{2}}}
> =e^{\frac{1}{2}}
> $$
> 这是不对的，回去重上小学吧
> $$
> \lim_{ t \to +\infty } {\left[\left( 1+\frac{1}{t} \right)^{t} \right]^{\frac{1}{2}}}
> \lim_{ t \to +\infty } {\left[\left( 1+\frac{1}{t} \right)^{\frac{1}{2}} \right]^{t}}
> =\lim_{ t \to +\infty } {\left( 1+\frac{1}{t} \right)^{\frac{1}{2t}}}
> $$
> 

正确的是
$$
=\lim_{ t \to +\infty } {\left[\left( 1+\frac{1}{t} \right)^{t} \right]^{\frac{1}{\sqrt{ t}}}}
=\lim_{ t \to +\infty } {\left[\left( 1+\frac{1}{t} \right)^{t} \right]^{\lim_{ t \to +\infty}{\frac{1}{\sqrt{t}}}}}
=e^{0}
=1
$$



## 2.Ex8(改)

> [!question]
> 已知$\lim_{ x \to 0^{+} } {\left(1+bx\right)^{\frac{1}{x}}}$=3，求$b$的值.

> [!tip]
> **跟上面一样，就是🤤的部分要做成一样的**

$$
\begin{align}
=\lim_{ x \to 0^{+} } {\left[ \left(1+bx\right)^{\frac{1}{bx}} \right]^{b}} & =e^{b} =3  \\
b & =\ln 3
\end{align}
$$


$$
\lim_{ n \to \infty } {3^{n}\sin \frac{\pi}{3^{n-1}}}
$$