---
tags:
  - "#math"
  - math_advanced_algebra
---
## 0.证明
> [!quote]
> 
> $$
> |A| = 
> \left|
> \begin{array}{ccc}
> a_{11}  & a_{12} & \cdots  & a_{1r} & \cdots  & a_{1n} \\
> a_{21}   & a_{22} & \cdots & a_{2r} & \cdots & a_{2n} \\
> \vdots  & \ddots  & \vdots & \ddots &  \vdots \\
> a_{n1} & a_{n2} & \cdots & a_{nr} & \cdots &  a_{nn}
> \end{array}
> \right|
> $$
> 
> $$
> |A| = (-1)^{r+1}a_{1r}M_{1r}+(-1)^{r+2}a_{2r}M_{2r} + \cdots + (-1)^{r+n}a_{nr}M_{nr}
> $$


## 1.证明

> [!NOTE]
> 我们定义里面**只有按第一列展开**的omg，但是我们学了[[n阶行列式性质4：对换两行（列）变成相反数]]，做一些**对调就能把第$r$列弄到第一列去**进行展开了。这里我们选择相邻两列两行进行对调类似“冒泡算法”，这样**不受影响的列就是从小到大排序**的了。

> [!tip]
> 数次数
> ![[n阶行列式可以按第r列进行展开：数对调的次数.png]]
> 假设进行了$r-1$次对调。

我们有
$$
|B| = 
\left|
\begin{array}{ccc}
a_{1r} &  a_{11} & a_{12} & \cdots  & a_{1n} \\
a_{2r}  &  a_{21}  & a_{22}& \cdots & a_{2n} \\
\vdots  &  \vdots & \ddots &  \vdots \\
a_{nr} &  a_{n1} & a_{n2} & \cdots &  a_{nn}
\end{array}
\right|
 = (-1)^{r-1}|A|
 $$
 小小展开一下
 $$
\begin{aligned}
|B| & = a_{1r}N_{1r} - a_{2r}N_{2r} + \cdots + (-1)^{n+1}a_{nr}N_{nr} \\
\end{aligned}
$$
![[n阶行列式可以按第r列进行展开：比较图B.png|400]]
![[n阶行列式可以按第r列进行展开：比较图A.png|400]]
可以比较一下干掉之后的，其实是一模一样的，即$N_{i,r} = M_{i,r}$
所以
$$
\begin{aligned}
|A| & =(-1)^{r-1}|B|\\ 
& = a_{1r}M_{1r} - a_{2r}M_{2r} + \cdots + (-1)^{n+1}a_{nr}M_{nr} \\
& = (-1)^{r-1}\left[a_{1r}M_{1r} - a_{2r}M_{2r} + \cdots + (-1)^{n+1}a_{nr}M_{nr}\right]\\
& = (-1)^{r+1}a_{1r}M_{1r}+(-1)^{r+2}a_{2r}M_{2r} + \cdots + (-1)^{r+n}a_{nr}M_{nr}
\end{aligned}
$$
确实如此
