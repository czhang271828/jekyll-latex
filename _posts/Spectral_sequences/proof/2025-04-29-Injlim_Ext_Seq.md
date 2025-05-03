---
title: $\varprojlim$ 与 $\mathrm{Ext}$ 的正合列
author: Chencheng Zhang
layout: post
category: proof
---

## 证明

{% prop %}
若 $𝒜$ 有正合的滤过余极限, 则逆向塔的 $\varinjlim_{-1}$ 消失. 若进一步假定余积正合, 则有短正合列 ($p ≥ 0$):
\begin{equation}
    0 → \varprojlim {}^1\mathrm{Ext}^p(X_∙, Y) → \mathrm{Ext}^{p+1}(\varinjlim X_∙,Y) → \varprojlim \mathrm{Ext}^{p+1}(X_∙, Y) → 0.
\end{equation}
{% endprop %}

{% pf %}
例行公事地写出谱序列. 由 $\varinjlim^1=0$, 得若干短正合列.
\\
\\
也可以适用同调方法, 大致思路是先使用 $(A, -)$ 构成的四项短正合列, 再用维数移动归纳. 证明时需要使用两个条件: $\mathrm{Ext}^p$ 与 $∐$ 交换, 以及 $∐ → ∐$ 是单射.
{% endpf %}
