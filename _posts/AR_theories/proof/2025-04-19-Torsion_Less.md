---
title: Torsionless 模的等价定义
author: Chencheng Zhang
layout: post
category: proof
---

{% thm %}
(Torsionless 判别法).
给定 $η_M : M → M^{∗ ∗}$. 以下条件等价.
<ol>
<li>
$η_M$ 是单的.
</li>
<li>
$M$ 是 $A^n$ 的子对象.
</li>
<li>
$\mathrm{Ext}^1(\mathrm{Tr}(M), A) = 0$.
</li>
</ol>
{% endthm %}

{% pf %}
考虑四项正合列
$$
0 → \mathrm{Ext}^1(\mathrm{Tr}(M), N) → N ⊗ M → (M^∗, N) → \mathrm{Ext}^1(\mathrm{Tr}(M), N) → 0.
$$
将 $N$ 替换作 $A$, 得 3. 与 1. 等价.
<br>
<br>
若 $η_M$ 单, 则 $M ↪ M^{∗∗} ↪ \mathrm{Hom}_{𝐒𝐞𝐭𝐬}(M^∗, A)$, 因此 $η_M$ 是 $∏ A$ 子空间. 由 <a href = "https://arxiv.org/abs/2105.00701"> Chase 引理</a>, 投射模对任意积封闭当且仅当环是 Artin 的, 从而 $∏_{M^∗} A$ 是投射模. 由 $M$ 有限生成, 其必然是有限生成投射模的子模.
<br>
若 $M$ 是 $A^n$ 的子对象, 记嵌入映射 $ι$. 由 $ι^{∗ ∗ } ∘ η_M = η_{A^n} ∘ ι$ 单, 得 $η_M$ 单.
{% endpf %}

{% note %}
证明 1. 至 2. 可避免使用 Chase 引理. 取 $M^∗$ 的投射盖 $P$, 则
$$
(M^∗, A) ↪ (P,A) ↪ A^n
$$
即为所求之单射.
{% endnote %}