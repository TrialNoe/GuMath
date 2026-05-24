---
tags:
  - "#math"
  - math_analysis
  - math_calculus
---
## 1 最基本的定理
我们知道

> [!summary]
> 如果vector function $\mathbf{F}(x,y)=P(x,y)i+Q(x,y)j$满足
> $$
> \frac{ \partial P(x,y) }{ \partial y } = \frac{ \partial Q(x,y) }{ \partial x }  
> $$
> 那么就可以知道，这个$\mathbf{F}$是Conservative Vector Field.有一个很好的性质是The line integral is independent of path

### 1.1 步骤化
1. 设出$P(x,y)$与$Q(x,y)$
2. 验证是否$\frac{ \partial P(x,y) }{ \partial y }=\frac{ \partial Q(x,y) }{ \partial x }$

## 2 3-dimension推广

> [!summary]
> 如果
> $$
> \mathbf{F}(x,y,z) = P(x,y,z)\mathbf{i}+Q(x,y,z)\mathbf{j}+R(x,y,z)\mathbf{k}
> $$
> 那么如果
> $$
> \frac{ \partial P(x,y,z) }{ \partial y } = \frac{ \partial Q(x,y,z) }{ \partial x } , \frac{ \partial P(x,y,z) }{ \partial z } = \frac{ \partial R(x,y,z) }{ \partial x } ,
> \frac{ \partial Q(x,y,z) }{ \partial z } = \frac{ \partial R(x,y,z) }{ \partial y } 
> $$
> 那么$\mathbf{F}(x,y,z)$是Conservative Vector Field

## 3 推广到n-diamension
$$
\mathbf{F}(\vec{x}) = \Delta F(\vec{x})\cdot \vec{n}
$$
是否也是存在这样的
$$
\frac{ \partial \left(\frac{ \partial F }{ \partial x_{i} } \right) }{ \partial x }  = \frac{ \partial F }{ \partial x }  
$$