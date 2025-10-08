---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---

> [!question]
> 求极限
> $$
> \lim_{ x \to 0^{+} } \left( \frac{1}{x}-\frac{1}{\tan^{-1}x} \right)
> $$
> 

## 1.L'Hospital的解法

> [!tip]
> 尝试把$0^{+}$代入，发现是$\infty - \infty$，可以通分，然后使用[[洛必达法则(L'Hospital's Rule)求未定型的极限]]

$$
\begin{align}
 =\lim_{ x \to 0^{+} } \frac{\tan^{-1}x -x }{x \cdot \tan^{-1}x} \dots \dots(1)
\end{align}
$$
这就变成$\frac{0}{0}$了，现在可以用[[洛必达法则(L'Hospital's Rule)求未定型的极限]]了
$$
\begin{align}
 &\xlongequal{H} \lim_{ x \to 0^{+} } \frac{\frac{1}{1+x^{2}}-1}{\tan^{-1}x+\frac{x}{1+x^{2}}} \\
 & = \lim_{ x \to 0^{+} } \frac{-x^{2}}{(1+x^{2})\tan^{-1}x+x}  \\
 & \xlongequal{H} -\lim_{ x \to 0^{+} } {\frac{2x}{2x\cdot \tan^{-1}x+2}} \\
 & = -\lim_{ x \to 0^{+} } {\frac{x}{x\cdot \tan ^{-1}x+1}}  \\
 & =-\lim_{ x \to 0^{+}} {\frac{0}{0+1}} = 0
\end{align}
$$
就是运算量有点大
- 分子分母出现$\frac{1}{1+x^{2}}$之后分子分母同时乘$1+x^{2}$。
- $(1+x^{2})\tan^{-1}x$的求导
## 2.Taylor Polynomial的解法
### 2.1.遇到问题

> [!tip]
> 变化同$(1)$，因为[[Linear Approximation]]的近似解法在[[华南农业大学2022-2023学年第1学期T7#方法2：Linear approximation]]同样是$\frac{0}{0}$有很大成功，不如来尝试一下

$$
\begin{align}
g'(x)  & = \frac{d}{dx}\left( \tan^{-1}x-x \right)=\frac{1}{1+x^{2}}-1=-\frac{x^{2}}{1+x^{2}}\\
h'(x) &  = \frac{d}{dx}(x \cdot \tan^{-1}x)=\tan^{-1}x+\frac{x}{1+x^{2}} \\
\end{align}
$$
在$x=0$处进行进行逼近，
$$
\begin{align}
l_{1} & =g(0)+g'(0)(x-0)=0 \\
l_{2} & = h(0) + h'(0)(x-0) = x
\end{align}
$$

所以说
$$
(1) \sim \lim_{ x \to 0^{+} } {\frac{0}{x}}
$$
更是奇葩一个常数$\frac{0}{\lim_{ x \to 0^{+} } {} }$

> [!fail] 有个问题是现在能不能穿插使用[[洛必达法则(L'Hospital's Rule)求未定型的极限]]?
> 不行
> 1. 这不是$\frac{0}{0}$或$\frac{\infty}{\infty}$型
> 2. 分子是常数$0$，不是趋向于$0$的函数

### 2.2.Taylor Polynomial得增强

> [!tip]
> 我们知道[[Linear Approximation]]是[[Taylor Polynomial]]的$n=1$时的特殊情况，所以说精度丢的有点多有必要进行增强

$$
\begin{align}
g''(x)=-\frac{2x(1+x^{2})-2x\cdot x^{2}}{(1+x^{2})^{2}}=-\dfrac{2\,x}{{x}^{4}+2\,{x}^{2}+1} \\
\end{align}
$$
还是$0$又回去了，得再求啊
$$
g^{(3)}(x)=\dfrac{2\,\left(3\,{x}^{2}-1\right)}{{x}^{6}+3\,{x}^{4}+3\,{x}^{2}+1}
$$
$g^{(3)}(3)=-2$
同样的不知道为什么，$h$也要求$h^{(3)}$
$$
\begin{align}
h''(x)  & = \dfrac{2}{{x}^{4}+2\,{x}^{2}+1} \\
h^{(3)}(x)  & = -\dfrac{8\,x}{{x}^{6}+3\,{x}^{4}+3\,{x}^{2}+1}
\end{align}
$$
$h''(0)=2,h^{(3)}=0$
$$
\begin{align}
p_{1}  & = 0+ 0 -\frac{2}{3!}(x-0)^{3}=-\frac{1}{3}x^{3} \\
p_{2} & =x+\frac{2}{2!}(x-0)^{2} + 0 = x+x^{2} 
\end{align}
$$

$$
\begin{align}
(1) \sim \lim_{ x \to 0^{+} } {}\frac{p_{1}}{p_{2}} & =\frac{-\frac{1}{3}x^{3}}{x+x^{2}} \\
 & = \lim_{ x \to 0^{+} } {} -\frac{x^{2}}{1+x} = 0
\end{align}
$$
**Taylor Polynomial**非常非常麻烦啊，但是如果事先记好了某些展开式应该很容易吧？