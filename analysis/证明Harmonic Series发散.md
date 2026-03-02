---
tags:
  - "#math"
  - math_calculus
---
证明
$$
S_{n}=\sum^{n}_{i=1} \frac{1}{n}
$$
diverge

其实从几何直观去想
```mathematica
ListPlot[Table[{n, 1/n}, {n, 1, 50}]]
```
![[file-20260301223431485.png]]
感觉就是收敛的呀，实际上是发散的。。

级数跟积分好像差不多，差一个底边长

试一下Test for Divergence
$$
\lim_{ n \to \infty }{ \frac{1}{n} } = 0
$$
判断不出来
```mathematica
ListPlot[Table[{n, HarmonicNumber[n]}, {n, 1, 50}]]
```
![[file-20260301224128977.png]]

所以说这个$\frac{1}{n}$也只是接近0,不是真正等于$0$
比如说 
$$
f(n) = 
\left\{
\begin{matrix}
 & \frac{1}{n}, & n\leq50 \\
 & 0, & n>50
\end{matrix}
\right.
$$
$$
\sum^{n}_{i=1} f(n)
$$
是收敛的