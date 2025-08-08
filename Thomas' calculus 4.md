---
tags:
  - "#math"
  - thomas_calcculus
---

> [!NOTE] 
>

# Session3

## 极限和导数的区别
以前一直搞混
极限是limit
导数，就是某点切线斜率 tangent slope
若至高中数学书乱教,误人子弟

## Why $sin\frac{1}{x}$ doesn't have limit whenever x approach to 0

> [!NOTE] Title
>  It oscillates too much to have a limit: ƒ(x) has no limit as x S 0 because the func-
tion’s values oscillate between +1 and -1 in every open interval containing 0. The 
values do not stay close to any one number as x S 0 (Figure 2.10c)
![[Pasted image 20250711162955.png]]

这个图真心觉得配的不好，没有我下面的好
这句话理解是因为 趋近0的时候这个函数连成一大块了，在(-1,1)之间震荡，变化的非常快，没有一个固定的值，所以没有极限
![[Pasted image 20250711162717.png]]


## 
![[Pasted image 20250713123658.png]]
![[Pasted image 20250713123708.png]]
true?

## 不会的题
![[Pasted image 20250717150419.png]]

$$
\lim_{x \to 2}\cfrac{f(x)-5}{x-2}=3

$$
因为根据[[利用因式分解求分母为0时的极限]],分子分母可以约掉才是对的
我这里设了$f(x)-5=（ax + b）(x-2)$
这不对的![[Pasted image 20250717151357.png]]
$\cfrac{f(x)-5}{x-2}$不一定线性

Approach0中网友的解答
![[Pasted image 20250717152234.png]]
If $\lim_{x \to 2}\frac{f(x)-5}{x-2}=3$,find $\lim_{x \to 2}f(x)$
$$
\begin{align}
\lim_{x \to 2}f(x) = \lim_{x \to 2}[\frac{f(x)-5}{x-2}(x-2)+5]
\end{align}
$$
since $\lim_{x \to 2}\frac{f(x)-5}{x-2}=3$
$$
 = \lim_{x \to 2}[3(x-2) + 5] = 3·(2-2) + 5 = 5
$$

concluse
$$
if\ \lim_{x \to c}\frac{f(x)}{g(x)} = d\ and\ g(x)=0 
$$
so 
$$
f(x)=0
$$

我一查这是叫做洛必达


