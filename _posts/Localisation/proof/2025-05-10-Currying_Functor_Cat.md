---
title: 函子范畴的 Curry 化
author: Chencheng Zhang
layout: post
category: proof
---

## 证明

关于积范畴的定义见[此文](Additive_Localisation).

{% prop %}
对范畴 $𝒜$, $ℬ$ 与 $ℰ$, 以下两个函子范畴同构:

1. $𝐅𝐮𝐧𝐜𝐭 (𝒜 × ℬ, ℰ)$, 即, 积范畴出发的函子范畴;
2. $𝐅𝐮𝐧𝐜𝐭 (𝒜, 𝐅𝐮𝐧𝐜𝐭 (ℬ, ℰ))$, 即, 指向函子范畴的函子范畴.

{% endprop %}

{% pf %}
一方面, 对 $F ∈ 𝐅𝐮𝐧𝐜𝐭 (𝒜 × ℬ, ℰ)$, 有良定义的函子
$$\begin{equation}
𝔉 : 𝒜 → 𝐅𝐮𝐧𝐜𝐭 (ℬ, ℰ),\quad A ↦ F(A, -).
\end{equation}$$
对函子间的自然变换 $θ_{(-,-)} : F ⇒ G$, 以下是自然变换
$$\begin{equation}
[Θ_A : 𝔉(A) ⇒ 𝔊(A)] := [θ_{(A,-)} : F(A, -)⇒ G(A,-)].
\end{equation}$$
由 $θ$ 是双自然变换, 对任意 $φ: A → A'$ 总有交换图
$$\begin{equation}
Θ_{A'} ∘ 𝔉(φ) = θ_{(A', -)} ∘ F(φ , -) = G(φ, -) ∘ θ_{(A, - )} = 𝔊 (φ )∘ Θ_A.
\end{equation}$$

以上完成了对应 $𝐅𝐮𝐧𝐜𝐭 (𝒜 × ℬ, ℰ) ⇒ 𝐅𝐮𝐧𝐜𝐭 (𝒜, 𝐅𝐮𝐧𝐜𝐭 (ℬ, ℰ))$.
\\
\\
另一方面, 对 $𝔉 ∈ 𝐅𝐮𝐧𝐜𝐭 (𝒜, 𝐅𝐮𝐧𝐜𝐭 (ℬ, ℰ))$, 有良定义的函子
$$\begin{equation}
F : 𝒜 × ℬ → ℰ,\quad (A,B) ↦ (𝔉(A))(B).
\end{equation}$$
对函子间的自然变换 $Θ_- : 𝔉 ⇒ 𝔊$, 以下是自然变换:
$$\begin{equation}
[θ_{(A,B)} : F(A,B) → G(A,B)] := [Θ_A(B) : (𝔉(A))(B) → (𝔊(A))(B)]
\end{equation}$$
继而检验自然变换的良定义性, 任取 $(f,g) : (A,B) → (A', B')$,
$$\begin{aligned}
θ_{(A',B')} ∘ F(f,g) & = Θ_{A'}(B')∘ (𝔉(f))(g) \\
& = Θ_{A'}(B') ∘ (𝔉(f)) (\mathrm{id}_{B'}) ∘ (𝔉(\mathrm{id}_{A}))(g)\\
& = (𝔊(f)) (\mathrm{id}_{B'}) ∘ Θ_{A}(B') ∘ (𝔉(\mathrm{id}_{A}))(g)\\
& = (𝔊(f)) (\mathrm{id}_{B'}) ∘ (𝔊(\mathrm{id}_{A}))(g) ∘ Θ_{A}(B)\\
& = (𝔊(f))(g) ∘ Θ_A(B) \\
& = G(f, g) ∘ θ_{(A,B)}.
\end{aligned}$$

由定义, 以上对应是互逆的.
{% endpf %}

{% note %}
以上不区分 $fx$ 与 $f ∘ x$.
{% endnote %}
