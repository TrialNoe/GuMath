---
tags:
  - "#math"
  - math_calculus
---
## 1 

> [!question] Determine Convergence
> $$
> \sum^{\infty}_{n=1} \frac{ \left( \frac{n+2}{n} \right)^{ n^{ 2 } } }{ 2^{ n } }
> $$


这个太多$n$的作为次数了，很自然可以想到用[[Root Test for Series]]



取$n^{ 2 }$居然不行
$$
\lim_{ n \to \infty }{ \sqrt[\Large{n^{ 2 }}]{\frac{ \left( \frac{n+2}{n} \right)^{ n^{ 2 } } }{ 2^{ n } }} } = \lim_{ n \to \infty }{\left( \frac{ n+2 }{ n } \right)\cdot \left( \frac{1}{2} \right)^{ \frac{ 1 }{ n } }} = \lim_{ n \to \infty }{ \left( \frac{1}{2} \right)^{ \frac{ 1 }{ n } } }  = 1
$$

怎么求出个$1$，分子的变化肯定是比分母要快的(这个不知道怎么)，你现在把重要的东西干掉了，剩下一些无关紧要的东西就把问题的本质掩盖了
相当于是把线段压缩嘛，但是压缩过头了，变成一个点了，这个点就不能提供什么有意思的信息。
你本质上其实还是利用p-series：$\frac{1}{n^{ p }}$来做



取$n$才有效
$$
\lim_{ n \to \infty }{ \sqrt[\Large{n}]{\frac{ \left( \frac{n+2}{n} \right)^{ n^{ 2 } } }{ 2^{ n } }} } =\lim_{ n \to \infty }{ \frac{1}{2}\left( \frac{ n+2 }{ n } \right)^{ n } } = \frac{1}{2}\lim_{ n \to \infty }{ \left( 1+\frac{2}{n} \right)^{ \frac{ n }{ 2 }\times2 } } = \frac{e^{ 2 }}{2} > 1
$$
发散的


