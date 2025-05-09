---
title: Kronecker quiver 中预投射与预内射模的维数向量
author: Chencheng Zhang
layout: post
category: proof
---

## 证明

{% lem %}
以下是预投射模与预内射模的的维数向量.

1. 预投射模的维数向量是 $\binom{n}{n + 1}$;
2. 预投射模在同构的意义下形如

   $$
   k^n \ \overset A {\underset B ⇉} \ k^{n+1},\quad A = \binom{I_n}{0}, \ B = \binom{0}{I_n} ∈ k^{n × (n+1)}.
   $$

3. 预内射模的维数向量是 $\binom{n+1}{n}$.
4. 预内射模在同构的意义下形如

   $$
   k^{n+1} \ \overset A {\underset B ⇉} \ k^{n},\quad A = \binom{I_n}{0}^T, \ B = \binom{0}{I_n}^T ∈ k^{(n+1) × n}.
   $$

{% endlem %}

{% pf %}
仅看前两点. 若 $M$ 预投射, 当且仅当 $M$ 在有限次 $C^+$ 后变作零. 记 $𝐝𝐢𝐦 M = mn$, 依照

$$
\begin{pmatrix}
3 & -2 \\ 2 & -1
\end{pmatrix} ^k = \begin{pmatrix}
2k + 1 & -2k \\ 2k & -2k + 1
\end{pmatrix}
$$

得 $𝐝𝐢𝐦 (C^+)^q M = \binom{m + 2q (m-n)}{n + 2q (m-n)}$. 依照预投射的定义, 存在 $q$ 使得 $𝐝𝐢𝐦 (C^+)^q M ∈ \{\binom 01, \binom 12\}$. 容易验证, $M$ 预投射当且仅当 $m + 1 = n$.
\\
往后归纳地计算 $τ^{-k} P(1)$ 与 $τ^{-k} P(2)$ 即可.
{% endpf %}
