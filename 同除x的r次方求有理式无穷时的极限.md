---
tags:
  - "#math"
  - math_calculus
---

> [!NOTE] 关键动机
>同时除以$x^{r}(r>0)$之后变为$\frac{1}{x^{r}}$,利用$\lim_{x \to \pm\infty}\frac{1}{x^{r}}=0$以及[[极限的运算法则]]求极限


> [!NOTE] 重要原则
>1.必须是有理式$\frac{P(x)}{Q(x)}$（可以不齐次）
>2.避免$\pm\frac{\infty}{\infty} or \frac{0}{0}$

^9c5b83

## 1.1.经典例子1

^4d226a

> [!example] 
> 求极限
> $$
> \lim_{x \to \infty}\frac{3x^{2}-x-2}{5x^{2}+4x+1}
> $$
> 

> [!NOTE]
> 考虑到[[同除x的r次方求有理式无穷时的极限#^9c5b83|同除x的n次方求有理式无穷时的极限总要原则]],同时除以$x^2$
> 

> [!done] 
> 
> $$
> 上式=\lim_{x \to \infty}\frac{3-\frac{1}{x}-\frac{2}{x^2}}{5+\frac{4}{x}+\frac{1}{x^2}}=\frac{3}{5}
> $$
> 
#### 为什么不除以x
> [!danger] 
> 如果是除以$x$，就会出现
> $$
> 上式=\lim_{x \to \infty}\frac{3x-1-\frac{2}{x}}{5x+4+\frac{1}{x}}=\frac{\infty-1-0}{\infty+4+0}
> $$
> 无法通过[极限的运算法则](app://obsidian.md/%E6%9E%81%E9%99%90%E7%9A%84%E8%BF%90%E7%AE%97%E6%B3%95%E5%88%99),运算$\frac{\infty}{\infty}$



## 1.2.经典例子2

> [!example] 
> 求极限
> $$
> \lim_{x \to \infty}\frac{x^2+x}{3-x}
> $$

> [!NOTE]
> 依旧考虑[[同除x的r次方求有理式无穷时的极限#^9c5b83|同除x的n次方求有理式无穷时的极限总要原则]]
> 同时除$x而不是x^2$原因同[[同除x的r次方求有理式无穷时的极限#为什么不除以x]]

> [!done] 
> 
> $$
> =\lim_{x \to \infty}\frac{x+1}{\frac{3}{x}-1}=\frac{\infty}{0-1}=-\infty
> $$



## 1.3.有关根式的套娃题

> [!example] 
> 求极限
> $$
> \lim_{x \to -\infty}(\sqrt{x^2+x+1}+x)
> $$
> 

> [!note] 动机1
> 如果直接代入$-\infty$，会出现$\infty-\infty$这种无法运算的情况
> 依据[[使用共轭根式求分母为0时的极限]]的思想，观察结构有这么大个根式，外面和里面一减就没了那个二次项，可以将分子有理化而分母无理化

> [!done] 
> $$
> \begin{align}
> \lim_{x \to -\infty}(\sqrt{x^2+x+1}+x)
> &=\lim_{x \to -\infty}(\sqrt{x^2+x+1}+x)\cdot\frac{\sqrt{x^2+x+1}-x}{\sqrt{x^2+x+1}-x}\\
> &=\lim_{x \to -\infty}\frac{x+1}{\sqrt{x^2+x+1}-x}
> \end{align}
> $$

> [!NOTE] 动机2
> 再次代入$-\infty$，观察结构，又回归到了$\frac{\infty}{\infty}$的问题，借助[[同除x的r次方求有理式无穷时的极限]]的思想，同除x（注意x是负数来的,那个大根号前面要加负号）


> [!done] 
> $$
> \begin{align}
> \lim_{x \to -\infty}\frac{x+1}{\sqrt{x^2+x+1}-x}
> &=\lim_{x \to -\infty}\frac{1+\frac{1}{x}}{-\sqrt{1+\frac{1}{x}+\frac{1}{x^{2}}}-1}
> =\frac{1+0}{-\sqrt{1+0+0} - 1}
> =-\frac{1}{2}
> \end{align}
> $$

> [!danger] 试错
> 直接同除一个x
> $$
> \lim_{x \to -\infty}(\sqrt{x^2+x+1}+x)=\lim_{x\to -\infty}-x(\sqrt{1+\frac{1}{x}+\frac{1}{x^2}}-1)
> $$
> 变成$0 \cdot -\infty$了算不动了

