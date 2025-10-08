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

## 2.Ex7

> [!question]
> 设$x_{1}=10$，$x_{n+1}=\sqrt{ x_{n}+6 }(n\geq1)$，证明数列${x_{n}}$存在，并求此极限.

### 2.1.一些尝试
### 2.1.1.两边平方处理
$$
x^{2}_{n+1} = x_{n}+6
$$
做不下去的，想求通项的，没工具处理这种通过$x^{2}_{n+1}$和$x_{n}$的关系求通项emm

### 2.1.2.直接看单调性
虽然我带了$n=1,2,3,4$猜出来他是单调减的，后面的极限应该是$3$，但是没办法做
$$
x_{n+1}-x_{n}=\sqrt{ x_{n}+6 } - x_{n} \tag{1}
$$
没救了，
$$
(1)=\frac{-x^{2}_{n}+x_{n}+6}{\sqrt{x_{n}+6}+x_{n}}
=\frac{(3-x_{n})(x_{n}+2)}{\sqrt{x_{n}+6}+x_{n}}
$$
$x_{n}$肯定是**非负数**，这么大个根号。所以这么大一串**只用看$(3-x_{n})$的正负**，看不了啊，虽然知道他最终极限是$3$就是没有工具去说明啊！！


## 3.Ex8(改)

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