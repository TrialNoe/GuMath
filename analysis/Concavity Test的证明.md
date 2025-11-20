---
tags:
  - "#math"
  - math_calculus
---

> [!question]+
> 求证 Concavity Test
> 如果$f''(x)>0$那么$f(x)$是*concave upward*的
> 如果$f''(x)<0$那么$f(x)$是*concave downward*的

## 1 证明
### 1.1 我的证明方法
#### 1.1.1 动机
> [!NOTE]+ 动机
> 根据[[concave upward和concave downward的定义]]要证明concavity test的正确性，就要找到$f''(x) \Rightarrow f'(x) \Rightarrow f(x)$的逻辑链，以及$f(x)$的切线和原函数$f(x)$的关系
> 切线和斜率密切相关，斜率又和导数$f'(x)$相关，归根结底就是要用$f'(x)$的信息去推出$f(x)$，那么就然而然想到[[Langrange's Mean Value Theorem(拉格朗日中值定理)#2 运用Lagrange's Mean Value Theorem#2.1 数学意义]]参与
> 


#### 1.1.2 简化和分析法
先简化假设$f''(x)>0$
由于[concave upward和concave downward的定义](app://obsidian.md/concave%20upward%E5%92%8Cconcave%20downward%E7%9A%84%E5%AE%9A%E4%B9%89)可以得知，就是要证明切线$F(x)$在原函数$f(x)$之下
先构造出$F(x)$
$$
F(x)=f'(t)(x-t)+f(t)
$$
切线$F(x)$在原函数$f(x)$之下,很常用就是[[作差法比较两个数的大小]]



$$
\begin{align}
f(x)-F(x) 
 & =f(x)-[f'(t)(x-t)+f(t)] \\
 & = [f(x)-f(t)]-f'(t)(x-t) \\
 & =(x-t)\left[ \frac{f(x)-f(t)}{x-t} -f'(t)\right] \\
 & = (x-t)[f'(\xi)-f'(t)]
\end{align}

$$

由于$f''(x)>0$ 并且 $t < \xi < x$，根据函数的单调性，很容易比较出$f'(\xi)和f'(t)$的大小

所以有$f(x)-F(x)>0$  即$f(x)>F(x)$

#### 1.1.3 $f''(x) < 0同理$