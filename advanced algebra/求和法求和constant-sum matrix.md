---
tags:
  - "#math"
  - math_advanced_algebra
---

> [!question] 求值
> $$
> |A| = 
> \left|
> \begin{array}{ccc}
> x & a & a & \dots & a & a \\
> a & x & a & \dots & a & a \\
> \vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
> a & a & a & \dots & a & x
> \end{array}
> \right|
> $$

> [!tip]+
> 这个矩阵有个特点，**每一列加起来都是$x+(n-1)a$，每一行加起来都是$x+(n-1)a$，那么把下面的行全部加到第一行就能凑出一个整个行（列）都相等的了，不就可以利用[[n阶行列式性质3：提取某一行（列）公因子不变性]]吗**

![[Screenshot_20251109_195412_com.onyx.galaxy.note.png|300]]
$$
\begin{aligned}
|A| 
&= 
\left|
\begin{array}{ccc}
x+(n-1)a & x+(n-1)a & x+(n-1)a & \dots & x+(n-1)a & x+(n-1)a \\
a & x & a & \dots & a & a \\
\vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
a & a & a & \dots & a & x
\end{array}
\right|\\
&=
[x+(n-1)a]
\left|
\begin{array}{cccc}
1 & 1 & 1 & \dots & 1 & 1 \\
a & x & a & \dots & a & a \\
a & a & x & \dots & a & a  \\
\vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
a & a & a & \dots & a & x 
\end{array}
\right| \\ \\




\end{aligned}
$$

**再用第一行的$a$倍往其他行加，消掉没有用的$a$**
$$
|A| = 
[x-(n-1)a]
\left|
\begin{array}{ccc}
1 & 1 & 1 & \dots & 1 & 1 \\
0 & x-a & 0 & \dots & 0 & 0 \\ 
0 & 0 & x-a & \dots & 0 & 0 \\ 
0 & 0 & 0 & x-a & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \dots & 0 & x-a
\end{array}
\right| 
$$

这不就是上三角行列式吗,根据[[n阶上下三角行列式的性质证明]]我们可以知道
$$
|A| = 
[x-(n-1)a](x-a)^{n-1}
$$
