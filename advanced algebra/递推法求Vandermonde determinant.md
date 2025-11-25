---
tags:
  - "#math"
---
## 1.1 Vandermonde determinant升次排列
> [!question]
> $$
> V_{n} = 
> \left|
> \begin{array}{ccc}
> 1 & x_{1} & x_{1}^{2} & \dots & x_{1}^{n-1} \\
> 1 & x_{2} & x_{2}^{2} & \dots & x_{2}^{n-1} \\
> \vdots & \vdots & \vdots & \ddots & \vdots \\
> 1 & x_{n} & x_{n}^{2} & \dots & x_{n}^{n-1}
> \end{array}
> \right|
> $$


> [!tip]+
> 因为是从$0$开始计，最后一个是$n-1$次方
> Vandermonde Determinant的特点是在每一行（是不是有可能倒置）中后一项比前一项高一次方。此时可以用前一项乘底数减去后一项，做出有一行是单位向量。
> 好处就是下面的行都能提取公因式，原因还是**后一项比前一项高一次方**，然后可以发现可以迭代

$$
\begin{aligned}
V_{n} & = 
\left|
\begin{array}{ccc}
1 & x_{1}-x_{n} & x_{1}^{2}-x_{1}x_{n} & \dots & x_{1}^{n-1}-x_{1}^{n-2}x_{n} \\
1 & x_{2}-x_{n} & x_{2}^{2}-x_{1}x_{n} & \dots & x_{2}^{n-1}-x_{2}^{n-2}x_{n} \\
\vdots & \vdots & \vdots & \ddots & \vdots   \\
1 & x_{n-1}-x_{n} & x_{n-1}^{2}-x_{1}x_{n} & \dots & x_{n-1}^{n-1}-x_{n-1}^{n-2}x_{n} \\
1 & 0 & 0 & \dots & 0
\end{array}
\right| \\ \\


& \xlongequal{按第n行进行展开} (-1)^{n+1}
\left|
\begin{array}{ccc}
x_{1}-x_{n} & x_{1}^{2}-x_{1}x_{n} & \dots & x_{1}^{n-1}-x_{1}^{n-2}x_{n} \\
x_{2}-x_{n} & x_{2}^{2}-x_{2}x_{n} & \dots & x_{2}^{n-1}-x_{2}^{n-2}x_{n} \\
\vdots & \vdots & \vdots & \ddots    \\
x_{n-1}-x_{n-1}x_{n} & x_{n-1}^{2}-x_{n-1}x_{n} & \dots & x_{n-1}^{n-1}-x_{n-1}^{n-2}x_{n} \\
\end{array}
\right| 

\end{aligned}
$$

根据[[n阶行列式性质3：提取某一行（列）公因子不变性]]，提一下
$$
\begin{aligned}
V_{n}
& = (-1)^{n+1}(x_{1}-x_{n})(x_{2}-x_{n})\dots(x_{n-1}-x_{n})
\left|
\begin{array}{ccc}
1 & x_{1} & \dots & x_{1}^{n-2} \\
1 & x_{2} & \dots & x_{2}^{n-2} \\
\vdots & \vdots & \ddots & \vdots    \\
1 & x_{n-2} & \dots & x_{n-2} \\
\end{array}
\right| \\
& = (-1)^{n+1}(-1)^{n-1}(x_{n}-x_{1})(x_{n}-x_{2})\dots(x_{n}-x_{n-1})V_{n-1} \\
& = (x_{n}-x_{1})(x_{n}-x_{2})\dots(x_{n}-x_{n-1})\Large{V_{n-1}} \\
& = \prod_{1\leq i<j\leq n}(a_{i}-a_{j})
\end{aligned}
$$
so
$$
V_{n} = \prod_{1\leq i<j\leq n}(a_{j}-a_{i})
$$

> [!tip] 写成二重连乘直观一点
> $$
> {
> \prod_{1\leq i < j \leq n}
> =\prod_{i=1}^{ n-1 } \prod_{j = i+1}^{ n }(a_{j}-a_{i})
> 
> }
> $$
> 

## 1.2 Vandermonde Determinant 降次排列
如果是降次排列呢？

> [!example]
>  $$
> \hat{V_{n}} = 
> \left|
> \begin{array}{ccc}
> x_{1}^{n-1} & x_{1}^{n-2} & x_{1}^{n-3} & \dots & x_{1} & 1 \\
> x_{2}^{n-1} & x_{2}^{n-2} & x_{2}^{n-3} & \dots & x_{2} & 1 \\
> \vdots & \vdots & \vdots  & \vdots      & \ddots&  \vdots    \\ 
> x_{n}^{n-1} & x_{n}^{n-2} & x_{n}^{n-3} & \dots & x_{n} & 1
> \end{array}
> \right|
>  $$

> [!tip]
> 这个想法就是变成第一种升次的排列，变成解决过的问题，使用“交换算法”相邻两个进行交换就行了。
> 经过$\frac{n(n-1)}{2}$次交换我们可以得到

$$
\hat{V_{n}} = (-1)^{\frac{n(n-1)}{2}}V_{n} = (-1)^{\frac{n(n-1)}{2}}\prod_{1\leq i<j<n}(a_{j}-a_{i}) 
$$
其实$\frac{n(n-1)}{2}$就是$C_{n}^{2}$嘛，在这个$\prod_{1\leq i<j<n}$也是有$C_n^{2}$项，一样的
所以(小指标减大指标)
$$
\hat{V_{n}} = \prod_{1\leq i < j \leq n}(a_{i} - a_{j})
$$
$$
\prod_{1\leq i<j\leq n}(a_{i}-a_{j}) = \prod_{i=1}^{ n-1 }\prod_{j=i+1}^{n}(a_{i} - a_{j}) 
$$
