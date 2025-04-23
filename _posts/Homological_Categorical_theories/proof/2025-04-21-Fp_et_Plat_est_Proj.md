---
title: Finitely Presented Flat is Projective
author: Chencheng Zhang
layout: post
---
{% thm %}
(有限表现 + 平坦 = 投射).
给定 Karoubi 的, 本质小的加法范畴 $𝒞$. 若 $F ∈ 𝐦𝐨𝐝_𝒞$ 平坦, 则 $F$ 投射.
{% endthm %}

{% pf %}
记 $F = \mathrm{cok}(h_{X \xrightarrow f Y})$. 考虑对偶

$$
𝔇 : 𝐌𝐨𝐝_{𝒞} → 𝐌𝐨𝐝_{𝒞^{\mathrm{op}}},\quad L ↦ (L(∙), C). 
$$

其中 $C$ 是 $𝐌𝐨𝐝_k$ 中的内射余生成元. 往证 $F$ 提升一切满态射 $α : L → R$, 也就是证明单态射

$$
𝔇 𝖭𝖺𝗍[F, R]\xrightarrow {𝔇 α} 𝔇  𝖭𝖺𝗍[F, L]. 
$$

对可表函子 $h_X$,

$$
𝔇 𝖭𝖺𝗍[h_X, L] ≃ 𝔇LX = (LX, C)≃ h_X(∙) ⊗ (L(∙), C). 
$$

此时,

$$
\begin{bmatrix}
𝔇 (RX) & ≃  & h_{X} ⊗ (R,C) & ↪  & h_{X} ⊗ (L,C) & ≃  & 𝔇 (LX)\\
↓  &  & ↓  &  & ↓  &  & ↓ \\
𝔇 (RY) & ≃  & h_{Y} ⊗ (R,C) & ↪ & h_{Y} ⊗ (L,C) & ≃  & 𝔇 (LY)\\
↓  &  & ↓  &  & ↓  &  & ↓ \\
𝔇 ([F,R]) & ≃  & F⊗ (R,C) & \dashrightarrow  & F⊗ (L,C) & ≃  & 𝔇 ([F,L])
\end{bmatrix}.
$$

依照蛇引理, $𝔇([F,R]) ↪ 𝔇([F,L])$ 是单态射, 从而 $F$ 提升一切满态射. 依照 $F$ 投射, 有限表现, 以及范畴 Karoubi, 得 $F$ 可表.  
{% endpf %}

{% note %}
这一证明完全照抄模范畴的结论.
{% endnote %}