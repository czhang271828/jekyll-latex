---
title: 关于轨道的若干结论
author: Chencheng Zhang
layout: post
category: caprice
---

## 证明

{% prop %}
([证明](Uniqueness_of_Maximal_Orbit))
以下是一些几何的结论.

1. 极大轨道满足以下等价定义:
   1. $\mathrm{Ext}^1(M,M) =0$;
   2. $[M]$ 是开集;
   3. $\overline{[M]} = 𝐫𝐞𝐩(𝐝𝐢𝐦 \ M)$.
2. 固定 $𝐯$, 极大轨道若存在则必唯一.
3. 极大轨道不存在的必要条件: $q(𝐯) ≤ 0$.
4. (不证明此条). 极小轨道就是半单表示; 等价地, $[X]$ 是闭集.
5. 给定 ses $0 →  X →  Y →  Z →  0$, 该 ses 不可裂当且仅当

   $$
   [X ⊕ Z] \quad ⊆ \quad \overline {[Y]} ∖ [Y]\quad (\text{视作} \ 𝐫𝐞𝐩(\dim Y) \ \text{中的轨道}).
   $$

{% endprop %}

{% prop %}
极大轨道满足以下等价定义:

1. $\mathrm{Ext}^1(M,M) =0$;
2. $[M]$ 是开集;
3. $\overline{[M]} = 𝐫𝐞𝐩(𝐝𝐢𝐦 \ M)$.
{% endprop %}

{% pf %}
由关键公式

$$
\dim 𝐫𝐞𝐩(𝐯) - \dim \ [M] = \dim \mathrm{Ext}^1(M,M) = \dim \mathrm{End}(M) - q(𝐯),
$$

$\dim \mathrm{Ext}^1(M,M) = 0$ 当且仅当 $\dim 𝐫𝐞𝐩(𝐯) = \dim \ [M]$, 即 1 ⟺ 3.

1. (1 ⇒ 2). 若 $\mathrm{Ext}^1(M,M) = 0$, 则 $\overline{[M]} = 𝐫𝐞𝐩(𝐯)$. 由于 $[M]$ 是 $\overline{[M]}$ 中的开集, 得 $[M]$ 是 $𝐫𝐞𝐩 (𝐯)$ 中的开集.
2. (2 ⇒ 1). 若 $[M]$ 是 $𝐫𝐞𝐩 (𝐯)$ 中的开集, 则必是稠密的. 此时 $\dim \ [M] = \dim 𝐫𝐞𝐩(𝐯 )$, 因此 $\mathrm{Ext}^1(M,M) = 0$.
{% endpf %}

{% note %}
由不可约空间, 固定 $𝐯$, 极大轨道若存在则必唯一.
{% endnote %}

{% prop %}
极大轨道不存在的必要条件: $q(𝐯) ≤ 0$.
{% endprop %}

{% pf %}
若 $q(𝐯) ≤ 0$, 则对任意非零 $M$ 都有 $\dim 𝐫𝐞𝐩 (𝐯) > \dim [M]$. 特别地, 此时的轨道数量必无穷.
{% endpf %}

{% prop %}
给定 ses $0 →  X →  Y →  Z →  0$, 该 ses 不可裂当且仅当

$$
[X ⊕ Z] \quad ⊆ \quad \overline {[Y]} ∖ [Y]\quad (\text{视作} \ 𝐫𝐞𝐩(\dim Y) \ \text{中的轨道}).
$$

{% endprop %}

{% pf %}
若 $0 → L \xrightarrow f M \xrightarrow g N → 0$ 可裂, 则 $[L ⊕ N] ⊈ \overline{[M]} ∖ [M]$. 下证明反向, 假定 ses 不可裂.
\\
模的分量由 $Q_0 ∪ Q_1$ 中分量决定的. 对任意 $λ ∈ (Q_0 ∪ Q_1)$, 存在同时分块上三角化

$$
0 → \begin{pmatrix}
L_λ  & O
\end{pmatrix}\xrightarrow{\binom{f_λ }{0}} \begin{pmatrix}
M^1_λ  & M^2_λ  \\ O & M^4 _λ  
\end{pmatrix}\xrightarrow{(0 \ \ g_λ )} \begin{pmatrix}
O \\
N_λ
\end{pmatrix} →  0.
$$

> 此处使用了子表示与商表示的矩阵表述, 也可理解做不变子空间与商空间.

取 $G$ 中元素为

$$
g_t := \begin{pmatrix}
t ⋅  \mathrm{id}_{L_i} & O \\ O & \mathrm{id}_{N_i}
\end{pmatrix},
$$

考虑 $M$ 在单参数子群 $g_t$ 共轭作用下的轨道 $[M]_t$. 由 $k ∖ \{0\}$ 在 $k$ 中稠密, 得

$$
[M]_0 ∈  \overline{\{[M]_t ∣  t ≠  0\}}.
$$
\\
最后说明 $L ⊕  N ≇  M$.

> 即便以上 ses 不可列, 但本命题需要证明 $L ⊕  N ≇  M$.

若 $L ⊕ N ≅ M$, 考虑长正合列

$$
0 → (M,L) → (N,L) → (L,L) → \mathrm{Ext}^1(M,L) \overset δ → \cdots.
$$

带入 $L ⊕ N ≅ M$, 并比较维数, 得

$$
\operatorname{im} \left(\mathrm{Hom}(L, L) \overset δ → \mathrm{Ext}^1(N, L)\right) = 0.
$$

由上述不可裂 ses 正合列是 $δ (\mathrm{id}_L)$, 得矛盾.

{% endpf %}
