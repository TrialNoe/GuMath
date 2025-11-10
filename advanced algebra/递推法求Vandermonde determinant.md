---
tags:
  - "#math"
---

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
> 这个东西有个特点，就是前面一列和后面一列差了一个次方，前面的次方加一，再拿后面的去减

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


& = (-1)^{n+1}
\left|
\begin{array}{ccc}
x_{1}-x_{n} & x_{1}^{2}-x_{1}x_{n} & \dots & x_{1}^{n-1}-x_{1}^{n-2}x_{n} \\
x_{2}-x_{n} & x_{2}^{2}-x_{2}x_{n} & \dots & x_{2}^{n-1}-x_{2}^{n-2}x_{n} \\
\vdots & \vdots & \vdots & \ddots & \vdots   \\
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
& = (x_{n}-x_{1})(x_{n}-x_{2})\dots(x_{n}-x_{n-1})V_{n-1} \\
& = \prod_{1\leq i<j\leq n}(a_{i}-a_{j})
\end{aligned}
$$
so
$$
V_{n} = \prod_{1\leq i<j\leq n}(a_{j}-a_{i})
$$

如果是降次排列呢？
 $$
 \hat{V_{n}} = 
\left|
\begin{array}{ccc}
x_{1}^{n-1} & x_{1}^{n-2} & x_{1}^{n-3} & \dots & x_{1} & 1 \\
x_{2}^{n-1} & x_{2}^{n-2} & x_{2}^{n-3} & \dots & x_{2} & 1 \\
\vdots & \vdots & \vdots  & \vdots      & \ddots&  \vdots    \\ 
x_{n}^{n-1} & x_{n}^{n-2} & x_{n}^{n-3} & \dots & x_{n} & 1
\end{array}
\right|
 $$
这个想法就是变成第一种升次的，使用“交换算法”相邻两个进行交换就行了。
经过$\frac{n(n-1)}{2}$次交换我们可以得到
$$
\hat{V_{n}} = (-1)^{\frac{n(n-1)}{2}}V_{n} = (-1)^{\frac{n(n-1)}{2}}\prod_{1\leq i<j<n}(a_{j}-a_{i}) 
$$
其实$\frac{n(n-1)}{2}$就是$C_{n}^{2}$嘛，在这个$\prod_{1\leq i<j<n}$也是有$C_n^{2}$项，一样的
所以(小指标减大指标)
$$
\hat{V_{n}} = \prod_{1\leq i < j \leq n}(a_{i} - a_{j})
$$