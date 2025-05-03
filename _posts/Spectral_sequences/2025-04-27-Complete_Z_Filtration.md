---
title: 完备化, 滤过复形
author: Chencheng Zhang
layout: post
category: caprice
---

## $\mathrm{Gr}_∙$ 与完备化

以下命题都是对模范畴 $𝐌𝐨𝐝_R$ 而言的.

{% def %}
(Cauchy 列). 对滤过模 $\cdots ⊃ F^s M ⊃ \cdots$, 取 $M$ 为全空间, 诸 $F^p M$ 的陪集为开集. 称 $(x_n)_{n ∈ ℕ} ∈ ∏_ℕ M$ 是 Cauchy 列, 当且仅当

\begin{equation}
    ∀ p, \  ∃ N ∈ ℕ, \ ∀ (m,n) (n > m ≥ N), ((x_m - x_n) ∈ F^pM).
\end{equation}
{% enddef %}

{% note %}
简单地说, 此处的拓扑基是的所有 $F^s M$ 的陪集.
{% endnote %}

{% def %}
对满射系统 (一般理论见[导出极限](Spectral_sequence_filtered#导出极限)) $\cdots ↠ \frac{M}{F^{p+1} M} ↠ \frac{M}{F^p M} ↠ \cdots$ 做三点定义:

1. 称之穷竭, 当且仅当 $\varinjlim \frac{M}{F^p M} = 0$, 即 $M=  ⋃ F^p M$;
2. 称之 Hausdorff, 当且仅当 $\varprojlim F^p M = ⋂ F^p M = 0$.
3. 称之完备, 当且仅当 $\varprojlim \frac{M}{F^p M} = M$.

{% enddef %}

{% note %}
简单地看,

1. 所谓穷竭, 即是说原点处基本开球 $F^pX$ 的覆盖范围 (随 $p →- ∞$) 趋向全空间.
2. 所谓 Hausdorff, 就是说开球可以任意小, 使得能区分任意不同的两点.
3. 所谓完备, 就是说收敛数列存在极限.
{% endnote %}

{% thm %}
对模范畴中 $ℤ$-指标的塔, 导出极限 $\varprojlim {}^1$ 消失.
{% endthm %}

{% lem %}
([证明](Complete_Filtration))
完备蕴含 Haussdorff. 完备当且仅当 $\varprojlim ^{0,1} F^p M = 0$.
{% endlem %}

{% def %}
(完备化). 滤过 $F^∙ M$ 的完备化旨在函子地补全 Cauchy 列的收敛终点. 此处定义做
\begin{equation}
  𝐅^p 𝐌 = \varprojlim \ \ \frac{F^p M}{F^{≥ p} M}.
\end{equation}
{% enddef %}

{% note %}
将极限视作积对象的子对象, $𝐅^p𝐌$ 确实是滤过. 亦可通过 $\varprojlim$ 的左正合性质说明单射 $𝐅^{p+1}𝐌 ↪ 𝐅^p𝐌$.
{% endnote %}

{% prop %}
([证明](FFX_vs_FX)). 滤过完备化具有如下重要的性质:

1. $\frac{𝐌}{𝐅 ^p𝐌} ≃ \frac{M}{F^p M}$ 是同构, 作为推论, $\frac{𝐅^{p-r} 𝐌}{𝐅 ^p𝐌} ≃ \frac{F^{p-r}M}{F^p M}$.
2. $𝐅^p𝐌$ 穷竭当且仅当 $F^p M$ 穷竭.
3. $𝐅^p 𝐌$ 是完备的 Hausdorff 的滤过.
{% endprop %}

{% thm %}
(同构的完备化等价于同构的分次态射. [证明](Gr_Iso_is_Complete_Iso)).
$\mathrm{Gr}(f)$ 是同构当且仅当完备化态射 $𝐟$ 是同构.

{% endthm %}
