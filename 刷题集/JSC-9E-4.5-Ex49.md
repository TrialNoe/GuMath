---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---

> [!question] 求极限
> $$
> \lim_{ x \to 1^{+} } {\ln x \cdot \tan \frac{\pi x}{2}}
> $$


> [!tip] 主要的想法
> 主要是观察到他是$0 \times \infty$所以说要先变化在用洛必达，变成$\frac{0}{0}$还是变成$\frac{\infty}{\infty}$要看哪个熟悉，哪个更好做一点。


> [!note]
> 老生常谈根据[[函数的连续性]]，代入试出来是$0 \times -\infty$
> 肯定要变成[[洛必达法则(L'Hospital's Rule)求未定型的极限]]，把一个变成$\frac{1}{f^{-1}(x)}$就行了

试错哈试了$\ln x$去变化
根据[[一些值得记忆的超越函数的导数]]
$$
\begin{align}
=\lim_{ x \to 1^{+} } \frac{{\tan{\frac{\pi x}{2}}}}{1/\ln x} & =\lim_{x \to 1^{+} } \frac{\frac{\pi}{2}\cdot \sec^{2} \frac{\pi x}{2}}{-\frac{1}{x \cdot \ln^{2} x}}  =- \frac{\pi}{2}\cdot\lim_{ x \to 1^{+} } {\ln^{2}x \cdot \sec^{2} \frac{\pi x}{2}}
\end{align}
$$
离谱的又来了$0 \times -\infty$
所以说用$\ln x$去变换不太可取，试一下用$\tan x$去变换，刚好$\frac{1}{\tan x}=\cot x$，而$\cot x$的导数背诵过的[[一些值得记忆的超越函数的导数]]
$$
\begin{align}
=\lim_{ x \to 1^{+} } {\frac{\ln x}{\cot \frac{\pi x}{2}}}  \xlongequal{H}\lim_{ x \to 1^{+} } {\frac{\frac{1}{x}}{-\frac{\pi}{2} \csc^{2}x}}=-\frac{\pi}{2} \lim_{ x \to 1^{+} } {\frac{1}{x}\cdot \cos^{2} {\frac{\pi x}{2}}} = - \frac{\pi}{2}  \times 1 \times 1 =- \frac{\pi}{2}
\end{align}
$$
我知道了原因是我背过$\frac{d}{dx}\cot x = -\csc^{2}x$

