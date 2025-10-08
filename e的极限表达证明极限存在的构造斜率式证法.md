---
tags:
  - "#math"
  - math_calculus
---
## 天才般的构造原型
$$f(x)=ln(x+1),f'(x)=\frac{1}{x+1}$$
$$\lim_{h \to 0}\frac{f(0+h)-f(0)}{h}=\lim_{h \to 0}\frac{\ln(1+h)-\ln(1)}{h}=\lim_{h \to 0}\ln(1+h)^{\frac{1}{h}}=f'(1)=1$$
$$e^1=e^{\lim_{h \to 0}\ln(1+h)^{\frac{1}{h}}}=\lim_{h \to 0}(1+h)^{\frac{1}{h}}=e$$
稍微换一下字母
$$\lim_{x \to 0}(1+x)^{\frac{1}{x}}=\lim_{n \to \infty}(1+\frac{1}{n})^{n}=e$$


## 1-经典例子

^1d7f7f

> [!question] 
> 证明以下极限存在
> $$
> \lim_{x \to \infty}(1+\frac{x}{n})^{n}=e^{x}
> $$

> [!idea]
> 基本的想法是这个式子和上面[[e的极限表达证明极限存在的构造斜率式证法#天才般的构造原型]]形式很像，唯一区别就是多了个$x$，是不是只要我把形式搞成跟他一模一样就行了，很自然想到[[换元法]]
> 令$t=\frac{x}{n}$就可以变成上面的形式了,$n=\frac{x}{t}$

$$
\begin{align}
\lim_{x \to \infty}(1+\frac{x}{n})^{n}
&=\lim_{t \to 0}(1+\frac{1}{t})^{\frac{x}{t}}\\
\end{align}
$$
外面再套一层ln的壳
$$
\begin{align}
\ln{\lim_{t \to 0}(1+\frac{1}{t})^{\frac{x}{t}}}
=x\lim_{t \to 0}\ln{(1+\frac{1}{t})^{\frac{1}{t}}}
\end{align}
$$
把$e$复合上去
$$
\begin{align}
e^{x\lim_{t \to 0}\ln{(1+\frac{1}{t})^{\frac{1}{t}}}}
=(e^{x})^{1}=e^{x}
\end{align}
$$
