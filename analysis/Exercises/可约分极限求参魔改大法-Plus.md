---
tags:
  - "#math"
  - math_calculus
---
## 天天忘记代入右边的值不是0的问题魔改

> [!example]
> 已知$\lim_{ x \to 2 }{ \frac{ x^{ 3 }+ax+b }{ x-2 } = 8 }$，求常数$a,b.$

> [!tip]+
> 这种东西上面是一个多项式，下面代入$2$之后是0，应该上面可以提取一个公因子$(x-2)$和下面约掉，然后余式代入$2$之后极限为$8$

**这里是魔改的步骤，比较适合自己吧**,有时候就是一直想着代入之后右边等于0，其实不是。
移项变成一个标准的方程
$$
\lim_{ x \to 2 }{ \frac{ x^{ 3 }+ax+b }{ x-2 }  } -8 = 0
$$
因为是三次方用不了韦达定理，你用韦达也不对啊。

> [!tip] 长除法
> 佛了我还打不出这个长除法
> ![[Screenshot_20251214_183933_com.onyx.galaxy.note.png|400]]

^bbdc4a



$$
\lim_{ x \to 2 }{ \left[ x^{ 2 }+2x+(a-4)+\frac{ b+2a+8 }{x-2 } \right] } = 0
$$

$$
\left\{
\begin{array}{ccc}
8+a-4 = 0  \\
b+2a+8 = 0
\end{array}
\right.
$$
$a=-4,b=0$
这样一来即使我不写这个最后等于8我也不会忘hhh


## 保证L'Hospital‘s Rule 为不定型求参

> [!example]
> 若$\lim_{ x \to 0 }{ \frac{1}{x} \left( \frac{a}{x} - \frac{b}{\sin x}\right) } = - \frac{1}{6}$，求出常数$a,b$

简单代入一下发现$\infty -\infty$，按照[[JSC-9E-4.5-Ex54#^83760d]]的思路直接通分【后面居然没有到L'Hospital】
$$
Given = \lim_{ x \to 0 }{ \frac{a\sin x - bx}{x^{ 2 }\sin x} } = -\frac{1}{6}
$$
出来吧等价无穷小，Talor Polynomial....
$$
 -\frac{1}{6} = RHS = \lim_{ x \to 0 }{ \frac{a\left[ x- \frac{1}{6}x^{ 3 }+O(x^{ 3 }) \right]  - bx}{x^{ 3 }}} = \lim_{ x \to 0 }{ \frac{(a-b)x - \frac{a}{6}x^{ 3 } + O(x^{ 3 })}{x^{ 3 }} }  
$$
可以直接除，不需要[[#^bbdc4a |长除法]]
$$
RHS = \lim_{ x \to 0  }{ \left( \frac{a-b}{x^{ 2 }}  - \frac{a}{6} \right) }
$$

> [!warning] 大坑
> **那可不行啊，如果$\lim_{ x \to 0 }{ \frac{(a-b)}{x^{ 2 }} }$无穷大了怎么办，肯定要限制一下。那么只能是这项不存在了，**

$$
a-b = 0
$$
所以啊
$$
RHS = \lim_{ x \to 0 }{ -\frac{a}{6} } = -\frac{1}{6} \implies a = 1
$$
$$
b =a = 1
$$
