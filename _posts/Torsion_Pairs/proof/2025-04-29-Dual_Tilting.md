---
title: 对偶 tilting 模的相对分解
author: Chencheng Zhang
layout: post
category: proof
---

## 证明

{% thm %}
(对偶的投射分解). ${_B}T$ 是 tilting 模. 相应地,

1. $A^∙ → T$ 给出 $B$ 的 $𝐚𝐝𝐝 (T)$-相对内射分解 $B → (A^∙)^T$;
2. $A → T^∙$ 给出 $T$ 的 $𝐚𝐝𝐝 (B)$-相对投射分解 $(T^∙ )^T → T$.

{% endthm %}

{% pf %}
先证明以下左 $B$-模复形

1. $(A^∙ → T)^T = [B → (A^∙)^T]$ 与
2. $(A → T^∙)^T = [(T^∙)^T → T]$

是正合复形, 从而构成 $B$ 的 $𝐚𝐝𝐝(T)$-内射分解, 以及 $T$ 的 $𝐚𝐝𝐝(B)$-投射分解.

* 由维数有限, 以及 $\mathrm{Ext}_A^{≥ T}(T,T)=0$. 对如上两条形如 $(X^∙, T)_A$ 的复形使用[一致的正合性条件](Spectral_sequence_filtered#维数移动)即可. 因此, 以上两条 $(X^∙, T)_A$ 确实是正合列.

证明第三条 $\mathrm{Ext}^{≥ 1}_{B^{\mathrm{op}}}(T,T) =0$ 前, 先证明 $A ≃ \mathrm{End}_{B^{\mathrm{op}}}(_BT)$.

* 考虑 $𝐦𝐨𝐝 _A$ 中相对内射分解 $A_A → T_A^∙$, 则 $_BB^∙ → {}_BT$ 是 $𝐦𝐨𝐝_A$ 中的相对投射分解. 考虑 $A$-代数 $A' := \mathrm{End}(_BT)$, 则有相对内射分解 $A'_A → T_A^∙$. 结合范畴等价

  $$
  𝐚𝐝𝐝(A_A)\xrightarrow[∼]{_BT_A} 𝐚𝐝𝐝(_BB)\xrightarrow[∼]{_BT_A} 𝐚𝐝𝐝(A'_A),
  $$

  因此, $A'_A$ 与 $A_A$ 是同构的 $A$-模, 从而 $A ≃ A'$.

这给出范畴等价

\begin{equation}
  𝐚𝐝𝐝 (A_A ⊕ T_A) \xrightarrow[∼]{T_A} 𝐚𝐝𝐝 ({}_B B ⊕ {}_BT).
\end{equation}

回归命题 $\mathrm{Ext}^{≥ 1}_{B^{\mathrm{op}}}(T,T) =0$, 对 $T$ 作 $A$-投射分解或 $B^{\mathrm{op}}$-投射分解. 考虑双模复形的同构 $(B^∙ , T)_{B^{\mathrm{op}}}≃ (A^∙ , T)_A$, 上述两类投射分解在 $(-)^T$ 下是相同的. 相应地, $\mathrm{Ext}^{≥ 1}_A(T,T) = \mathrm{Ext}^{≥ 1}_{B^{\mathrm{op}}}(T,T) = 0$.  

{% endpf %}
