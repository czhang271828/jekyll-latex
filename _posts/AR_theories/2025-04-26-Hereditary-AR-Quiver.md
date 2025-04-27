---
title: Notes on AR Quivers over Hereditary Algebras.
author: Chencheng Zhang
layout: post
category: notes
---

## 遗传代数的 AR quiver

### AR 平移, 截面等

先从以下例子开始.

{% ex %}

给定 quiver $Q := [1 → 2 → 3]$. 记代数闭域上的路代数 $A= kQ$, 以及 AR quiver

$$
Γ (A) :=
\begin{bmatrix}
 &  &  &  & A &  &  &  & \\
 &  &  & \nearrow  &  & \searrow  &  &  & \\
 &  & P( 2) &  & \overset τ\dashleftarrow  &  & I( 2) &  & \\
 & \nearrow  &  & \searrow  &  & \nearrow  &  & \searrow  & \\
P( 3) &  & \overset τ\dashleftarrow  &  & S( 2) &  & \overset τ\dashleftarrow   &  & I( 3)
\end{bmatrix}
$$

注意到如下事实.

1. $𝐩𝐫𝐨𝐣 ∩ Γ (A) ≃ Q^{\mathrm{op}} ≃ 𝐢𝐧𝐣 ∩ Γ (A)$.
2. 所有箭头由 $Q^{\mathrm{op}}$ 关于顶点的反射得到.

以上 AR quiver 可视作无限 quiver (点集是 $ℤ × Q^{\mathrm{op}}$) 的一部分, 如下图所示.

$$
\begin{bmatrix}
 &  &  &  & \bullet  & \rightarrow  & \bullet \\
 &  &  & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  & \uparrow  & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  & \uparrow \\
 &  & \bullet  & \rightarrow  & \bullet  & \rightarrow  & \bullet \\
 & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  & \uparrow  & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  & \uparrow  & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  & \\
\textcolor[rgb]{0.29,0.56,0.89}{A} & \textcolor[rgb]{0.82,0.01,0.11}{\rightarrow } & \textcolor[rgb]{0.82,0.01,0.11}{I( 2)} & \textcolor[rgb]{0.82,0.01,0.11}{\rightarrow } & \textcolor[rgb]{0.82,0.01,0.11}{I( 1)} &  & \\
\textcolor[rgb]{0.29,0.56,0.89}{\uparrow } & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  & \textcolor[rgb]{0.82,0.01,0.11}{\uparrow } & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  &  &  & \\
\textcolor[rgb]{0.29,0.56,0.89}{P( 2)} & \textcolor[rgb]{0.82,0.01,0.11}{\rightarrow } & \textcolor[rgb]{0.82,0.01,0.11}{S( 2)} &  &  &  & \\
\textcolor[rgb]{0.29,0.56,0.89}{\uparrow } & \textcolor[rgb]{0.96,0.65,0.14}{⤢ }  &  &  &  &  & \\
\textcolor[rgb]{0.29,0.56,0.89}{P( 3)} &  &  &  &  &  &
\end{bmatrix}
$$

对以上, $P(2) → A$ 通过反射得到 $A → I(2)$.

{% note %}
对子图, 此处沿用子范畴与全子范畴的称呼.

1. 称 $Q' ⊆ Q$ 是子范畴, 若 $Q'$ 是 $Q$ 的子图
2. 称 $Q' ⊆ Q$ 是全子范畴, 若 $Q' ⊆ Q$ 是子图, 且 $\mathrm{Hom}_{Q'}(i,j) = \mathrm{Hom}_{Q}(i,j)$.
{% endnote %}

{% endex %}

假定以下 quiver $Q$ 都是有界连通无环的.

{% def %}
(quiver 的无界化). 给定 $Q$, 定义 $ℤ Q$ 如下.

1. 顶点集是 Catersian 积 $(ℤ × Q_0) := ℤ × Q_0$.
2. 箭头集是 $S_1 ⊔ S_2$. 其中
   1. $S_1 := ℤ × Q_1$, 形如 $(n, α) : (n, x) → (n, y)$.
   2. $S_2$ 中箭头刻画如下: 若 $(n, α) : (n, x) → (n, y)$, 则作

   $$
   θ(n, α) : (n + 1, y) → (n , x).
   $$

简而言之, $(n + 1, y) \xrightarrow[\text{反射}]{θ (n , α)} (n, x) \xrightarrow{(n,α)} (n, y)$. 朝向与 AR quiver 一致:

$$
\begin{bmatrix}
 &  & ( n,x) &  & \\
 & \nearrow  &  & \searrow  & \\
( n+1,y) &  & \overset{\tau }{\dashleftarrow } &  & ( n,y)
\end{bmatrix}
$$

{% enddef %}

{% def %}
定义 $ℤQ$ 上的两类运算.

1. $τ : ℤQ → ℤQ ,\quad (n, -) → (n-1, -)$ 是平移.
2. $θ : ℤQ_1 → ℤQ_1$ 是朝向 $τ$ 的反射.
{% enddef %}

对 $A_3$ 而言, $Q^{\mathrm{op}} = Γ (A) ∩ 𝐩𝐫𝐨𝐣$ 是类似截面的东西. 以下是对 AR quiver 截面的公理化定义.

{% def %}
(截面). 称 $Σ ⊆ ℤ Q$ 是子图, 若

1. (连通无环的全子范畴). $Σ$ 是连通, 无环的全子范畴,
2. (截面). 对任意 $x ∈ Q_0$, 存在唯一的 $n ∈ ℤ$ 使得 $(n, x) ∈ Σ$.
3. (道路封闭). 对 $ℤ Q$ 中的任意道路, 若起点与终点属于 $Σ$, 则道路上的所有点都属于 $Σ$.
{% enddef %}

{% ex %}
$ℤ Γ (k [∙ → ∙ → ∙])$ 的截面可以是 $𝐩𝐫𝐨𝐣 ∩ Γ$, 也可以是

$$
(0, I(1)) → (0, I(2)) → (-1, A).
$$

{% endex %}

{% thm %}
以下是一些组合学的事实, 对后续证明无帮助. 证明从略.

1. $ℤ Q$ 是无环图.
2. 取 $ℤ Q$ 的截面 $Σ$, 则截面的嵌入诱导了同构 $ℤ Σ ≃ ℤ Q$.
3. 记 $T_1$ 与 $T_2$ 是同一棵无向树的两种定向, 则 $ℤ T_1 ≃ ℤ T_2$.
4. 给定环 $C$, 假定其定向是无环的. 此时 $ℤ Q$ 的结构唯一取决于 $C$ 中顺时针箭头个数与逆时针箭头个数, 与具体的排列无关.
{% endthm %}

{% note %}
若除去遗传条件, 则上述定理不再成立. 见[此文中的 $B = \mathrm{End}(T_A)$](Commutative_Diagram_Alg#非-apr-tilting-模).
{% endnote %}

选定 AR quiver $Γ$, 使用

1. $𝔓$ 表示投射对象所在的连通分支.
2. $ℑ$ 表示内射对象所在的连通分支.

对有限表示的遗传代数 (不必选择代数闭域), 下将 $𝔓$ 是截面的事实归纳作如下引理.

{% lem %}
($𝔓$ 是 $ℤ 𝔓$ 的截面, [证明](P_is_Section)).
给定连通, 有限表示表示的遗传代数.

1. $𝔓$ 是 $ℤ𝔓$ 的截面.
2. $Γ$ 是 $ℤ𝔓$ 的子图.
3. $ℤ 𝔓$ 视同 $ℤΓ$ 的全子范畴.

内射对象同理.

{% endlem %}

若去除有限表示条件, 则 $ℤ 𝔓$ 与 $ℤ ℑ$ 是连通分支的子图.
