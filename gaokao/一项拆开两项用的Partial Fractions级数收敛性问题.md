---
tags:
  - "#math"
  - math_calculus
  - math_gaokao
---
> [!question] 求收敛性
> $$
> \sum^{\infty}_{n=2} \frac{1}{n^{ 3 }-n}
> $$

对于这么高的次数，但是又是多项式。很自然地想把下面的结构进行因式分解
根据[[Partial Fraction Decomposition(部分分式分解)]]
$$
Given = \frac{1}{2}\sum^{\infty}_{n=2} \left( \frac{1}{n+1}+\frac{1}{n-1}-\frac{2}{n} \right)
$$

> [!fail]
> 这里第一次做的时候踩了坑，因为三个都是Harmonic Series，然后直接救下定论他是Divergent了
> 其实这个和L-Hospital's Rule是一个道理，他们的相互作用之下，可能会变成Convegent

注意观察这里$\frac{2}{n}$是两个$\frac{1}{n}$，拆开刚好可以和其他两个配对
$$
RHS = \frac{1}{2}\sum^{\infty}_{n=2} \left[\left(\frac{1}{n+1}-\frac{1}{n}\right) + \left(\frac{1}{n-1}-\frac{1}{n} \right)  \right]
$$
这不就是一个经典的$\sum^{n}_{i=?}(f(n)-f(n+k))$问题吗，此时即可根据[[高考中裂项求和问题]]的方法进行求导


$$
s_{n} >1+ \sum^{n}_{i=2}  \frac{1}{i}
$$