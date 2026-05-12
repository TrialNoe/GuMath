---
tags:
  - "#math"
---
## 1 优化形式推导
我们知道Homogenous DE的标准形式如下

> [!equation]
> $$
> \frac{dy}{dx} = \phi\left( \frac{y}{x} \right)
> $$

如果对他进行[[换元法#1 比值换元]]
$$
u=\frac{y}{x},y=ux
$$
那么

> [!summary]
> $$
> \frac{1}{x}\,dx=\frac{1}{\phi(u)-u}\,du
> $$


### 1.1 推导过程
那么
$$
\frac{dy}{dx} = \phi\left(  u \right)
$$
再求导可以知道
$$
\frac{dy}{dx} = x\frac{ du }{ dx }+u
$$
再代入
$$
\phi\left(  u \right) = x \frac{du}{dx}+u
$$
**这里就是优化点，每次都要移动来移动过去非常麻烦，干脆直接算出结果进行记忆就算了**
$$
x\frac{du}{dx} = \phi(u)-u \implies \frac{x}{dx} = \frac{ \phi\left( u \right)-u }{ du }
$$
倒一下

> [!summary]
> $$
> \frac{1}{x}\,dx=\frac{1}{\phi(u)-u}\,du
> $$

得到这个
### 1.2 例子
我们来看一些例子

> [!question] 解方程
> $$
> y^{ 2 }+x^{ 2 } \frac{dy}{dx}=xy \frac{ dy }{ dx }
> $$

这个系数是二次的，显然可以使用[[#1 优化形式推导]]来求解

先进行移项
$$
\begin{align}
(x^{ 2 }-xy) \frac{dy}{dx}  & = -y^{ 2 } \\
\frac{dy}{dx} & =- \frac{y^{ 2 }}{x^{ 2 }-xy}
\end{align}
$$
**上下除一个$x^{ 2 }$就可以构造比值了**
$$
\frac{dy}{dx} = - \frac{\frac{y^{ 2 }}{x^{ 2 }}}{1-\frac{y}{x}} = \frac{\frac{y^{ 2 }}{x^{ 2 }}}{\frac{y}{x}-1} = \frac{u^{ 2 }}{u-1}
$$
这样的话我们就有$\phi(u)=\frac{u^{ 2 }}{u-1}$
代入刚刚的结果公式
$$
\begin{align}
\frac{1}{x}\,dx  & = \frac{1}{\frac{u^{ 2 }}{u-1}-u}\,du=\frac{1}{\frac{u^{ 2 }}{u-1}-\frac{ u(u-1) }{ u-1 }}\,du   = \frac{1}{\frac{u^{ 2 }}{u-1}-\frac{ u^{ 2}-u }{ u-1 }}\,du \\
 & = \frac{ 1 }{ \frac{u^{ 2 }-u^{ 2 }+u}{u-1} }\,du=\frac{1}{\frac{u}{u-1}}\,du
=\frac{u-1}{u}\,du=\left( 1-\frac{1}{u} \right)\,du \end{align}
$$
即（求不定积分 ）
$$
\begin{align}
\int\frac{1}{x}\,dx & =\int\left( 1-\frac{1}{u} \right)\,du \\
\ln \lvert x \rvert  & =u-\ln \lvert u \rvert +\ln \lvert C \rvert \\
 x=C\frac{e^{ u }}{u}  & = \frac{Ce^{ \frac{ y }{ x } }}{\frac{y}{x}} 
\end{align}
$$
结果为
$$
x\cdot \frac{y}{x}=Ce^{ \frac{ y }{ x } }\implies y=Ce^{ \frac{ y }{ x } }
$$
可以看见相对于之后一直移项的操作这种做法更好
![[file-20260512104032558.png|334]]

### 1.3 比值u=x/y的问题
昨天课上做到一个问题

> [!question] 解微分方程
> $$
> (y^{ 2 }-3x^{ 2 })\,dy-2xy\,dx=0
> $$

这个也是二次齐次的，你看系数的次数都是二次，也可以用[[#1 优化形式推导]]来求解
我们先做一下简单的变形
$$
\begin{align}
(y^{ 2 }-3x^{ 2 })\,dy & =2xy\,dx \\
\frac{dy}{dx} & =\frac{2xy}{y^{ 2 }-3x^{ 2 }}  \\
\end{align}
$$
这里上下同时除一个$x^{ 2 }$
$$
\frac{dy}{dx}= \frac{2 \frac{y}{x}}{\frac{y^{ 2 }}{x^{ 2 }}-3}=\frac{2u}{u^{ 2 }-3} = \phi(u)
$$
再次代入
$$
\frac{1}{x}\,dx= \frac{1}{\phi(u)-u}\,du = \frac{1}{\frac{2u}{u^{ 2 }-3}-u}\,du = \frac{1}{\frac{2u}{u^{ 2 }-3}- \frac{ u^{ 3 }-3u }{ u^{ 2 }-3 }}\,du = \frac{ u^{ 2 }-3 }{ 5u-u^{ 3 } }\,du
$$
这完全求不了的，因为你的分母的导数$(5u-u^{ 3 })'=5-3u^{ 2 }$和这个分子$u^{ 2 }-3$压根没有倍数关系..

这里就要尝试不换成$u=\frac{y}{x}$而是换成$v=\frac{x}{y}$了
 因为倒过来了嘛，我们对[[#1 优化形式推导]]进行魔改
 
 
 $$
 x=vy\implies \frac{dx}{dy}=\Phi(v)
 $$
 $$
\begin{align}
  & \frac{dx}{dy} = y \frac{dv}{dy}+v  =\Phi(v)\\ 
\end{align}
 $$

> [!summary]
> $$
> \begin{align}
>  & \int\frac{1}{y}\,dy  =  \int \frac{ 1 }{ \Phi(v) - v }\,dv
> \end{align}
> $$

 

$$
\frac{dy}{dx}  =\frac{2xy}{y^{ 2 }-3x^{ 2 }}=\frac{2\frac{x}{y}}{1-3 \left( \frac{ x }{ y } \right)^{ 2 }} = \frac{2v}{1-3v^{ 2 }}\implies \frac{dx}{dy}= \frac{1-3v^{ 2 }}{2v} =\Phi(v)
$$
所以
$$
\begin{align}
\int \frac{1}{y}\,dy  & = \int \frac{1}{\frac{1-3v^{ 2 }}{2v}-v} \, dv = \int \frac{1}{\frac{1-3v^{ 2 }}{2v}-\frac{ 2v^{ 2 } }{ 2v }} \, dv \\
 & =\int\frac{2v}{1-5v^{ 2 }}\,dv 
\end{align}
$$
SO
$$
\begin{align}
\ln \lvert y \rvert & =-\frac{1}{5}\ln \lvert 1-5v^{ 2 } \rvert +\ln c \\
y & =e^{ -\frac{ 1 }{ 5 }\ln c\lvert 1-5v^{ 2 } \rvert  }= C{(1-5v^{ 2 })^{ - \frac{ 1 }{ 5 } }}
\end{align}
$$


