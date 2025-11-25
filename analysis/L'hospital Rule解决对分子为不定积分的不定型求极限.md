---
tags:
  - "#math"
  - math_calculus
---
## 1.JSC5.4 T77
> [!question] 求极限
> $$
> \lim_{ x\to 0 }{ \frac{ 1 }{ x^{2} } \int_{0}^{x} \frac{2t}{\sqrt{ t^{3} + 1 }}dt }
> $$

> [!tip]+
> 根据[[函数的连续性]]我们把0带进去发现分母为$0$，**分子$\int_{0}^{0}f(x)dx = 0$**，所以是一个$\frac{0}{0}$ 

$$
=  \lim_{ x\to 0 }{ \frac{2x}{ 2x \cdot\sqrt{ x^{3} + 1 }} } = \lim_{ x\to 0 }{ \frac{1}{\sqrt{x^{3} + 1}} } = 1
$$



## 2.JSC5.4 T78

> [!question]
> $$
> \lim_{ x \to \infty }{ \frac{1}{x^{2}} \int_{0}^{x} \ln(1+e^{x}) \, dx  }
> $$
> 

我们可以知道$\ln(1+e^{x})$是一个单调增加的函数，从$0$到$\infty$函数图像和$x$轴围成的面积肯定是无穷的。
![[Pasted image 20251109135617.png|300]]

> [!quote] 上面这句话的定理证明
> 反常积分比较判别法
> $$
> \int_{0}^{\infty }\ln(1+e^{x}) \sim \int_{0}^{\infty}\ln(e^{ x }) = \int_{0}^{\infty} x = \infty 
> $$

$$
Given=\lim_{ x \to \infty }{ \frac{ \ln(1+e^{x}) }{ 2x } } = \lim_{ x \to \infty }{ \frac{e^{ x }}{2(1+e^{x})}}  = \lim_{ x\to \infty }{ \frac{1}{2\left( 1+\frac{1}{e^{x}} \right)} } = \frac{1}{2}
$$

## 3 华农25级大一期中考的一道求极限题目

> [!question] 求极限
> $$
> \lim_{ x \to 0 }{  }(\cos \sqrt{x})^{ \frac{ 1 }{ x } }
> $$

## 3.1 L'hospital's Rule 的解法
这种是$1^{ \infty }$，取对数之后可以变成$\infty \cdot 0$的形式，再变成$\frac{0}{0} \text{或者} \frac{\infty}{\infty}$的形式
$\large{\text{Let }y = \frac{1}{x}\ln\cos \sqrt{x}}$
$$
\begin{aligned}
&Given = e^{ \lim_{ x \to 0 }{ y } } \\
&\lim_{ x \to 0 }{ y } = \lim_{ x \to 0 }{ \frac{1}{x}\ln \cos \sqrt{x} } \xlongequal{H}\lim_{ x \to 0 }{ \frac{ \frac{ -\frac{1}{2\sqrt{x}}\cdot \sin \sqrt{x} }{ \cos \sqrt{x} } }{ 1 } } =\lim_{ x \to 0 }{ \frac{-\tan \sqrt{x}}{2\sqrt{x}} } \\
\end{aligned}
$$
WC怎么还是$\frac{0}{0}$
再来一次
$$
RHS \xlongequal{H} -\lim_{ x \to 0 }{ \frac{\frac{1}{2\sqrt{x}}\cdot\sec^{ 2 }{\sqrt{x}}}{2\cdot\frac{1}{2\sqrt{x}}} } =-\frac{1}{2}\lim_{ x \to 0 }{ \sec ^{ 2 }x } = -\frac{1}{2}
$$
So
$$
Given = e^{ -\frac{ 1 }{ 2 } }
$$
这种方法用了两次洛必达,还有一堆$\frac{1}{\sqrt{x}}$来打扰不是很方便

## 3.2 
这个$1^{ \infty }$其实等于$e$，是不是可以利用一下，但是它是没有三角函数的，可以用等价无穷小把他变成多项式再说，等价无穷小本质就是[[Taylor Polynomial]]
这个根号太讨厌了
$\large \text{Let } u=\sqrt{x}$(等等是不是$\sqrt{x}$造成的化简了)

$$
\begin{aligned}
&f(u) = \cos u \\
&f(x) = f(0) + \frac{1}{1!}f'(u)(u-0) + \frac{1}{2!}f''(u)(u-0) +O(u)\\
&f(x) = 1-\frac{1}{2}u^{ 2 } + O(x)
\end{aligned}
$$
丢回去
$$
\begin{aligned}
&\cos \sqrt{x} \sim 1-\frac{1}{2}x \\
&Given = \lim_{ x \to 0 }{ \left( 1-\frac{1}{2}x \right)^{ \frac{ 1 }{ x } } } = \lim_{ x \to 0 }{ \left( 1-\frac{x}{2} \right)^{ -\frac{ 2 }{ x }\cdot\left( -\frac{ 1 }2{  } \right) } }=e^{ -\frac{ 1 }{ 2 } }
\end{aligned}
$$

## 3.3 直接换元
在[[#3.2]]中提到，麻烦的是根号，是不是直接把根号弄没了直接做也很简单呢？
$\large \text{Let }u=\sqrt{x}$
$$
Given = \lim_{ u \to 0 }{ (\cos u)^{ \frac{ 1 }{ u^{ 2 } } } }
$$
再洛吗
$$
\lim_{ u \to 0 }{ \frac{\ln \cos u}{u^{ 2 }} } = \lim_{ u \to 0 }{ \frac{ \frac{ \sin u }{ \cos u } }{ 2u } }
$$
没带来什么优势
## 3.4 总结
所以在有三角函数复合的情况下这种$1^{ \infty }$还是转化成$e$好用，比洛必达方便省事，会不会有特例呢

等等不是三角函数行不行
### 3.4.1 非三角函数的推广探索
随便出一道，把$\cos x$改成其他等于$1$的
#### 3.4.1.1 根三次
$$
\lim_{ x \to 0 }{ (\sqrt{1+x^{ 3 }})^{ \frac{ 1 }{ x } } }
$$

##### 3.4.1.1.1 洛
$$
\lim_{ x \to 0 }{  \ln{ (\sqrt{1+x^{ 3 }})^{ \frac{ 1 }{ x } } } }
=\lim_{ x \to 0 }{   \frac{\ln ({1+x^{ 3 })}}{2x} }
\xlongequal{H} \lim_{ x \to 0 }{ \frac{ \frac{3x^{ 2 }}{1+x^{ 3 }} }{ 2 } } = 0
$$
$$
Given = 1
$$
##### 3.4.1.1.2 e
$$
\sqrt{1+x^{ 3 }} = 1+ \frac{1}{1!}\frac{ 3x^{ 2 } }{ 2\sqrt{1+x^{ 3 }} }(x-0) ++ o(x) 
$$
好麻烦
