---
tags:
  - "#math"
  - math_calculus
---

> [!NOTE]  主要思想
> 夹挤定理就是要找出上界和下界并且某点上下界的极限（注意是极限相同）相同
> 而三角函数有界性就天然适配这一规则

^a850dd

## 1.1.三角函数有界性经典例子

> [!example] 经典有关正弦函数的极限的例子
$\text{show that }$$$\begin{align}\lim_{x \to 0}x^2 \sin{\frac{1}{x}} = 0\end{align}$$

> [!NOTE] 动机
> 因为没有两个极限相乘的法则,注意到可以利用[[三角函数性质#正余弦函数的有界性]]找出上界和下界，便于我们用夹挤定理

> [!done] 
>因为$-1 \le \sin{\frac{1}{x}} \le 1 \Rightarrow -x^2 \le x^2\sin{\frac{1}{x}} \le x^2$
并且我们知道$\lim_{x \to 0}(-x^2)=\lim_{x \to 0}x^2=0$,根据夹挤定理
$$\lim_{x \to 0}x^2\sin{\frac{1}{x}} = 0$$


## 1.2.有关正弦函数分式求极限的例子

> [!example] 
> 求极限
> $$
> \lim_{x \to \infty}\frac{sin^{2}x}{x^{2}+1}
> $$

> [!NOTE]
> 观察到是一个正弦函数除以一个多项式，分子振荡。
> 相乘和相除应该是相通的，仿照[[夹挤定理（The Squeeze Theorem）和函数有界性的结合的例子#1.1.三角函数有界性经典例子]]，利用夹挤定理

> [!done] 
> 因为$0 \le sin^2x \le 1$则$0\le\frac{sin^2x}{x^2+1}\le \frac{1}{x^2+1}$
> 所以
> $$
> \lim_{x \to \infty}0 \le \lim_{x \to \infty}\frac{sin^{2}x}{x^{2}+1} \le \lim_{x \to \infty}\frac{1}{x^{2}+1}
> $$
> 因为上下界在无穷处极限相等
> $$
> \lim_{x \to \infty}0 =\lim_{x \to \infty}\frac{1}{x^{2}+1}=0
> $$
> 根据夹挤定理，$\lim_{x \to \infty}\frac{sin^{2}x}{x^{2}+1}=0$
> 



## 2.0.那么夹挤定理结合有界性是否只是局限于三角函数呢？

有没有一些函数也有类似的属性呢？
这里我想到和三角函数很相似的双曲函数
### $thx$函数的探究
不过$\sinh x$无界和$\cosh x$只有下界，只有$th x$有上下界符合我们的要求
改一下题目[[#1.2.有关正弦函数分式求极限的例子]]，同样是求极限
$$
\lim_{ x \to \infty } \frac{th^2x}{x^2+1} 
$$

无脑试一下**The Squeeze Theorem**，$0 \leq th^2 x \leq 1$
所以$0\leq\lim_{ x \to \infty }\frac{th^2 x}{x^2 + 1}\leq \lim_{ x \to \infty } \frac{1}{x^2+1}$并且$\lim_{ x \to \infty } \frac{1}{x^2 +1}=0$
根据**The Squeeze Theorem**，$\lim_{ x \to \infty } \frac{th^2 x}{x^2 + 1} = 0$
### 