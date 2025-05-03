---
title: Happel 的导出等价定理 (第一部分证明)
author: Chencheng Zhang
layout: post
category: proof
---

## 证明

以下 $𝒜$ 是有足够投射的 Abel 范畴.

{% lem %}
若 $T ∈ 𝒜$ 满足 $\mathrm{Ext}^{≥ 1}(T) = 0$, 则局部化 $C^b(𝐚𝐝𝐝 T) ↣ C^b𝒜 → D^b𝒜$ 诱导的态射

$$
K^b(𝐚𝐝𝐝 (T)) → D^b 𝒜
$$

是全忠实的嵌入.

{% endlem %}

{% pf %}

以下使用数学归纳法证明. 记 $P(m,n)$ 是:

* 对一切长度不超过 $m$ 与 $n$ 的复形 $P$ 与 $Q$, 以下是同构

  $$
  (P,Q)_{K^b(𝐚𝐝𝐝 (T))} → (P,Q)_{K^b𝒜} → (P,Q)_{D^b 𝒜}.
  $$

显然 $P(0,0)$ 成立, 因为对轴复形 $X,Y ∈ C^b (𝐚𝐝𝐝(T))$ 总有 $\mathrm{Ext}^{≥ 1}(X,Y) = 0$.
\\
下进行归纳, 假定 $P(≤ m, ≤ n)$ 成立. 对任意长度为 $m+1$ 的 $X$, 考虑强制截断, 则有同伦范畴以及导出范畴的好三角 $LX → X → RX → LX[1]$. 对 $(-,Y)_{K^b(𝐚𝐝𝐝 (T))}$ 与 $(-,Y)_{D^b 𝒜}$ 使用同调代数基本定理, 得交换图

$$
\scriptsize\begin{bmatrix}
( LX[ 1] ,Y)_{K^{b}(\mathbf{add}( T))} & \rightarrow  & ( RX,Y)_{K^{b}(\mathbf{add}( T))} & \rightarrow  & ( X,Y)_{K^{b}(\mathbf{add}( T))} & \rightarrow  & ( LX,Y)_{K^{b}(\mathbf{add}( T))} & \rightarrow  & ( RX[ -1] ,Y)_{K^{b}(\mathbf{add}( T))}\\
\parallel  &  & \parallel  &  & \downarrow  &  & \parallel  &  & \parallel \\
( LX[ 1] ,Y)_{D^{b} 𝒜 } & \rightarrow  & ( RX,Y)_{D^{b} 𝒜 } & \rightarrow  & ( X,Y)_{D^{b} 𝒜 } & \rightarrow  & ( LX,Y)_{D^{b} 𝒜 } & \rightarrow  & ( RX[ -1] ,Y)_{D^{b} 𝒜 }
\end{bmatrix}
$$

此时, 中间箭头是同构. 这完成了归纳 $P(≤ m, ≤ n) ⇒ P(≤ m+1, ≤ n)$. 另一方向同理. 综上, 以上 $K^b(𝐚𝐝𝐝 (T)) → D^b 𝒜$ 是全忠实的.

{% endpf %}
