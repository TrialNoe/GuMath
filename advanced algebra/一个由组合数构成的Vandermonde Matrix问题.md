---
tags:
  - "#math"
  - math_advanced_algebra
---

> [!NOTE] 证明
> $$
> \begin{vmatrix}
> 1 & 1 & 1 & \cdots & 1 \\
> 1 & C_2^1 & C_3^1 & \cdots & C_n^1 \\
> 1 & C_3^2 & C_4^2 & \cdots & C_{n+1}^2 \\
> \vdots & \vdots & \vdots & \ddots & \vdots \\
> 1 & C_n^{n-1} & C_{n+1}^{n-1} & \cdots & C_{2n-2}^{n-1}
> \end{vmatrix} 
> = 1
> $$

## 1 证明
> [!tip] 想法
> 一个很自然的思路是这个行列式第一列都是$1$，可以上下相减就可以**做成一列或者一行只有一个元素是$1$然后其他元素是$0$的**，这样就可以通过Method of Reduction of Order来慢慢化简,并且我们注意到用上面的行减下面的行符合**组合数的公式$C_{k}^{ n }-C_{k-1}^{ n-1 } = C_{n-1}^{ k }$(Pascal's rule)**

用$R_{2} - R_{1},R_{3}-R_{2},\cdots,R_{n}-R_{n-1}$

$$
LHS = 
\begin{vmatrix}
1 & 1 & 1 & \cdots & 1 \\
0 & C_1^1 & C_2^2 & \cdots & C_n^1 \\
0 & C_2^2 & C_{3}^2 & \cdots & C_{n+1}^2 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & C_{n-1}^{n-1} & C_{n}^{n-1} & \cdots & C_{2n-3}^{n-1}
\end{vmatrix}
= 
\begin{vmatrix}
1 & 1 & \cdots & C_{n-1}^1 \\
1 & C_{3}^2 & \cdots & C_{n}^2 \\
\vdots & \vdots & \ddots & \vdots \\
1 & C_{n}^{n-1} & \cdots & C_{2n-3}^{n-1}
\end{vmatrix} 
$$

又是一列$1$，同样的配方同样的操作

$$
RHS = 
\begin{vmatrix}
1 & 1 & \cdots & C_{n-1}^1 \\
0 & C_{2}^2 & \cdots & C_{n-1}^2 \\
\vdots & \vdots & \ddots & \vdots \\
0 & C_{n-1}^{n-1} & \cdots & C_{2n-4}^{n-1}
\end{vmatrix} 
$$
展开
$$
RHS = 
\begin{vmatrix}
1 & \cdots & C_{n-1}^1 \\
1 & \cdots & C_{n-1}^2 \\
\vdots & \ddots & \vdots \\
1 & \cdots & C_{2n-4}^{n-1}
\end{vmatrix} 
$$
所以说可以一直展开下去，得到这个**递推公式**
$$
F_{n} = F_{n-1} = F_{n-2} = \dots = F_{1}
$$
一共有$n-1$个等号嘛，那么就要$(2n-2)-(n-1)$
$$
F_{1} = |C_{(2n-2)-(n-1)}^{ n-1 }| = 1
$$
