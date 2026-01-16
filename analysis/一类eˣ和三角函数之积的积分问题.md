---
tags:
  - "#math"
---

> [!question] 求积分
> $$
> \int e^{ x }\cos x\,dx
> $$

## 1 Integration by Parts
这是两个函数乘起来根据[[求arccosx的积分问题]]普遍的思路，我们可以想到尝试用[[Integration by Parts]]
$$
\begin{aligned}
u = e^{ x },v&=\sin x \\
u'=e^{ x },v'&=\cos x
\end{aligned}
$$

$$
\begin{aligned}
&=e^{ x }\sin x - \int e^{ x }\sin x\,dx \\
&=e^{ x }\sin x - e^{ x }\int e^{ x }\cos x
\end{aligned}

$$




## 2 利用行列式记忆
$$
\int e^{ x }\sin x =
\frac{ 
\left|
\begin{array}{ccc} 
ae^{ ax } & b\cos bx\\
e^{ ax } & \sin bx 
\end{array}
\right| 
}{ 
a^{ 2 } + b^{ 2 }
}
$$

> [!warning]
> 这个好就好在很好记忆，就不用去真的算，比较省时间，**坏处是非常大的，你不知道他弄两次之后可以回到跟原来一样，比较奇技淫巧**


> [!tips] Title
> Contents




## 3 Euler's formula

> [!thinking]
> 我们知道**Euler's formula可以把三角函数和$e^{ x }$l联系起来**，即$e^{ ix }=\cos x+i\sin x$，那么再合并一下就相当于把三角函数和$e^{ x }$合为$e^{ x }$了

$\cos x$为$e^{ ix } = \cos x + i\sin x$的实部，即$\cos x = \mathrm{Re}(e^{ ix }).$

$$
\begin{aligned}
\int e^{ x }\cos x\,dx 
&= \int e^{ x }\cdot \mathrm{Re}(e^{ ix })\,dx\\
&= \mathrm{Re}\left( \int e^{ (1+i)x }\,dx \right)\\
&=\mathrm{Re}\left(\frac{1-i}{2}e^{ (1+i) x } \right)+C\\
&\xlongequal{e^{ ix }=\cos x+i\sin x} \mathrm{Re}\left[ \frac{1-i}{2} e^{ x }(\cos x+i\sin x) \right] + C \\
&=\mathrm{Re}\left[ \frac{e^{ x }}{2}\left[\left(\sin x+\cos x\right)+i\left(\sin x-\cos x\right)\right] +C\right] \\
&= \frac{e^{ x }}{2}(\sin x+\cos x)+C
\end{aligned}
$$4.Tabular 
