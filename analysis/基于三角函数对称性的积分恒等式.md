---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---

> [!question]
> 若$f(x)$在$[0,1]$上连续，求证
> 1. $\int_{0}^{ \frac{ \pi }{ 2 } }f(\sin x)\,dx =  \int_{0}^{ \frac{ \pi }{ 2 } }f(\cos x)\,dx$.
> 2. $\int_{0}^{ \pi }xf(\sin x)\,dx = \frac{\pi}{2}\int_{0}^{ \pi }f(\cos x)\,dx$.
## 1 解答
### 1.1 Q1
---
第一次做这种真的没有什么灵感，用一下“三板斧”试一下
[[Subsitution Rule]]，准备
Let $t = \sin x,dt = \cos x\,dx$
$\sin0 = 0,\sin \frac{\pi}{2} = 1$
$$
Given = \int_{0}^{ 1 }\frac{ f(t) }{ \sqrt{1-t^{ 2 }} }\,dt
$$

> [!error]+
> 这没有什么明显进展的，而且就接下来也不好做。

---
[[Integration by Parts]]

Let 
	$u = f(\sin x),v=x$
	$u'=f'(\sin x)\cos x,v'=1$
$$
Given = xf(\sin x)-\int_{0}^{ \frac{ \pi }{ 2 } }{f'(\sin x)}\cos x\,dx
$$

> [!error]+
> 越来越复杂了，而且和我们的RHS差了好远

> [!tip]- 互余换角的思路
> **如果我们从$\sin x 和 \cos x$的关系角度去思考，互余的互换，$\sin \left( \frac{\pi}{2}-x \right) = \cos x$**

^180f3a


Let $u = \frac{\pi}{2} - x\,,du=-dx$
$\frac{\pi}{2} -0 = \frac{\pi}{2},\frac{\pi}{2}-\frac{\pi}{2} = 0$
$$
Given 
= \int^{ 0 }_{\frac{ \pi }{ 2 }}f\left( \sin{\left( \frac{\pi}{2}-u \right)} \right)\,(-du) 
= \int_{0}^{ \frac{ \pi }{ 2 } }f(\cos x)\,du
$$
由于那个符号无关的原因
$$
RHS =\int_{0}^{ \frac{ \pi }{ 2 } }\cos x\,dx
$$
Q.E.D

### Q2

> [!tip]
> 第一问告诉，对于这类型$抽象(三角(x))$分部积分，换元的方法都不好用，我们仿照[[#^180f3a]]的思路，我们去想怎么来的$\sin x = \sin x\,,\sin (\pi-x) = \sin x$，这样即可

Let 
	$t=\pi-x\implies x=\pi-t\implies dx=-dt$
	$t_{sub} = \pi-0 = \pi,t_{top} = \pi-\frac{\pi}{2} = \frac{\pi}{2}$
$$
\begin{aligned}
Given 
&= \int_{\pi}^{ \frac{ \pi }{ 2 } }{(\pi-t)f(\sin(\pi-t))\,(-dt)} \\
&= \int_{ \frac{ \pi }{ 2 } }^{ \pi }{(t-\pi)f(\sin \pi)\,dt} \\
&=\int_{ \frac{ \pi }{ 2 } }^{ \pi }{t\,f(\sin \pi)\,dt}
-\int_{ \frac{ \pi }{ 2 } }^{ \pi }{\pi f(\sin \pi)\,dt}\\
&=
\end{aligned} 
$$


> [!thinking]
> 这种技巧是不是要看$\int  \, dx$的上限来做很迷的