---
title: 局部 tilting 模诱导的 torsion pair
author: Chencheng Zhang
layout: post
category: proof
---

## 证明

{% thm %}
(局部 tilting 模诱导的 torsion pair). 局部 tilting 模 $T$ 诱导了以下两类 torsion pair.

1. $(𝐠𝐞𝐧(T), T^o)$ 是 torsion pair.
2. $(T^⟂, 𝐜𝐨𝐠(τT))$ 是 torsion pair.
3. $𝐠𝐞𝐧(T) ⊆ T^⟂$.
4. 以上两个 torsion pair, 均有 $T ∈ 𝒯 ∩ {}^⟂𝒯 = 𝒯 ∩ τ⁻¹ ℱ$.
{% endthm %}

{% pf %}
第一问与[此命题](Gen_Eq_T)极其类似. 由 $p.\dim T ≤ 1$, 得 $\mathrm{Ext}^1(-, T)$ 是右正合函子, 因此 $\mathrm{Ext}^1(T,T) = 0$ 蕴含 $𝐠𝐞𝐧(T) ⟂ T$.
\\
第二问同理. 由 $𝐜𝐨𝐠(τT)$ 对扩张封闭, 从而是 torsion-free class. 仅需证明 $T^⟂ = {}^o𝐜𝐨𝐠(τT)$. 由 AR 公式,

$$
\mathrm{Ext}^1(T, M) ≃ D\overline {(M, τ T)} ≃ D(M, τ T).
$$

最后一处同构是因为 $τ M$ 投射 (见 [AR 公式](AR_Formula)).
\\
第三问是直接的, 一般不取等 (若 $T$ 是 tilting 模, 则取等).
\\
第四问是直接的验证, 等价表述见 [$𝐠𝐞𝐧 = 𝐓$ 的充分条件](Gen_Eq_T).
{% endpf %}
