---
tags:
  - "#math"
  - math_advanced_algebra
---
## 1.例子
### 1.1 一般的例子
> [!example]
> 问$\vec{u}$是否在$A$张成的$Span$内，并且证明
> $$
> A = \begin{bmatrix}
> 3 & -5 \\
> -2 & 6 \\
> 1 & 1
> \end{bmatrix}
> \quad
> \vec{u} = \begin{bmatrix}
> 0 \\
> 4 \\
> 4
> \end{bmatrix}
> $$

> [!NOTE]+ 动机
> 想法是很自然的，我们想要得到一个[[linear combination#Linear Combination的理解]]，能够完成下面的。
> $$
> x_{1}\begin{bmatrix}3 \\-2 \\1\end{bmatrix}
> +x_{2}\begin{bmatrix}-5 \\6 \\1\end{bmatrix}
> =\begin{bmatrix}0 \\4 \\4\end{bmatrix}
> $$
> 又根据[[linear combination#$A vec{x}= vec{b}$有解]],只要解出来增广矩阵，自然而然想到[[高斯消元法 Gaussian Elimination]]
> $$
> \begin{bmatrix}
> 3 & -5 & 0 \\
> -2 & 6 & 4 \\
> 1 & 1 & 4
> \end{bmatrix}
> $$
> 

$$
\begin{bmatrix}
3 & -5 & 0 \\
-2 & 6 & 4 \\
1 & 1 & 4
\end{bmatrix}
\sim
\begin{bmatrix}
 1 & 1 & 4\\
-2 & 6 & 4 \\
3 & -5 & 0
\end{bmatrix}
\sim
\begin{bmatrix}
1 & 0 & \frac{5}{2}\\
0 & 1 & \frac{3}{2} \\
0 & 0 & 0
\end{bmatrix}
$$
### 1.2 共线的例子

> [!example]
> 题目同[[#1.1 一般的例子]]
> $$
> A =
> \begin{bmatrix}
> 2 & -1 \\
> -6 & 3 
> \end{bmatrix}
> \quad 
> \vec{u}=
> \begin{bmatrix}
> b_{1} \\
> b_{2}
> \end{bmatrix}
> $$

#### 1.2.1 共线的角度

> [!NOTE]+ 动机
> 根据[[linear combination]]可以得出$A$由一下两个$vector$组成
> $$
> \vec{a_{1}}=\begin{bmatrix}2 \\-6\end{bmatrix}
> \quad
> \vec{a_{2}}=\begin{bmatrix}-1 \\3\end{bmatrix}
> $$
> 

显而易见的是$\vec{a_{1}}=-2\vec{a_{2}}$,明显共线，无法张成一个平面，只有在同一线上才有解
而这条线就是$b_{1}和b_{2}$成倍数关系$(-1:3)$,$b_{1}=-3b_{2}$
#### 1.2.2 Gaussian的角度

> [!NOTE]+
> 道理同[[#1.1 一般的例子|1.1 一般的例子的动机]]

$$
\begin{bmatrix}
2 & -1 & b_{1} \\
-6 & 3 & b_{2}
\end{bmatrix}
\sim
\begin{bmatrix}
2 & -1 & b_{1} \\
0 & 0 & b_{2}+3b_{2} 
\end{bmatrix}
$$

$b_{2}+3b_{2}=0$就可以把下面做成零行了