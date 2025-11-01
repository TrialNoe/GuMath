---
tags:
  - "#math"
  - math_calculus
  - math_analysis
---

> [!question] Cachy mean value theorem
> 如果$f(x),g(x)$满足
> $(1)$在比区间$[a,b]$上面连续；
> $(2)$在开区间$(a,b)$内可导；
> $(3)$对任意的$x \in (a,b),g'(x)\neq0$；$\text{那么在}(a,b)\text{内至少有一点}\xi\in(a,b),\text{使得}\frac{f(a)-f(b)}{g(a)-g(b)} = \frac{f'(\xi)}{g'(\xi)}$
## 1.证明
### 1.1.使用函数绑定进行尝试
> [!fail] trying
> 我们可以仿照[[华南农业大学2015~2016学年第1 学期解答题T2#2.2.2.函数绑定]]的思路，因为是共用一个$\xi$嘛，做成一样才行。但是通过尝试这条路非常复杂走不下去。

### 1.2.利用参数化的思想
如果我们和[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]$f'(\xi) =\frac{f(a)-f(b)}{a-b}$进行对比，从替换的角度来看，不难发现Cauchy mean value theorem是在用$g(a)\to a,g(b)\to b,g'(\xi) \to 1\text{(f'的分母)}$
更像是参数化
参考[[Langrange's Mean Value Theorem(拉格朗日中值定理)]]
$$
h(x)=f(x)-f(a)-\frac{f(a)-f(b)}{a-b}(x-a)
$$

$$
F(x)=f(x)-f(a) -\frac{f(a)-f(b)}{g(a)-g(b)}(g(x)-g(a))
$$
$$
F(a)=F(b)= 0
$$
根据[[Rolle's Theorem(罗尔中值定理)]]
我们可以知道存在$\xi \in (a,b)$使得$F'(\xi)=0$即$\frac{f^{'}(x)}{g^{'}(x)}=\frac{f(a)-f(b)}{g(a)-g(b)}$


### 1.3.历史背景
柯西中值定理首次出现在他1823年的著作《微积分教程摘要》（Résumé des Leçons données à l'École Royale Polytechnique sur le Calcul Infinitésimal）中 [Stack Exchange](https://hsm.stackexchange.com/questions/9831/was-there-a-more-intuitive-early-proof-of-the-generalized-mean-value-theorem)[SOPHIA RARE BOOKS](https://www.sophiararebooks.com/pages/books/5815/augustin-louis-cauchy/resume-des-lecons-donnees-a-l-ecole-royale-polytechnique-sur-le-calcul-infinitesimal-tome-premier)。