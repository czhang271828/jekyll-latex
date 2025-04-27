---
title: Notes on Classical Tilting Theory
author: Chencheng Zhang
layout: post
category: notes
---

* TOC
{:toc}

## 经典 Tilting: 投射维度 $≤ 1$

### 记号: 对象类

{% def %}
(垂直). 以下使用

1. $⟂_o$ 表示关于 $\mathrm{Hom}(-,-)$ 的垂直,
2. $⟂$ 表示关于 $\mathrm{Ext}^1(-,-)$ 的垂直.

特别地, 使用 $(-)^⟂$, $(-)^o$, $^⟂(-)$ 以及 $^o(-)$ 表示对象类的左右垂直类.

$$
𝒳^⟂ := \{Y ∈ 𝖮𝖻(𝒞) ∣ \mathrm{Ext}^1(X, Y) = 0, ∀ X ∈ 𝒳\}.
$$

{% enddef %}

{% def %}
给定 (非空) 对象类 $𝒳$. 定义

1. $𝐚𝐝𝐝(𝒳)$ 是 $𝒳$ 中对象关于直和与直和项的闭包;
2. $𝐟𝐢𝐥(𝒳)$ 是 $𝒳$ 中对象关于扩张 (合成列) 的闭包;
3. $𝐬𝐮𝐛(𝒳)$ 是 $𝒳$ 中对象关于子对象的闭包;
4. $𝐜𝐨𝐠(𝒳) = 𝐬𝐮𝐛(𝐚𝐝𝐝(𝒳))$ 是 $𝒳$ 中对象关于直和与子对象的闭包;
5. $𝐅(𝒳) = 𝐟𝐢𝐥(𝐬𝐮𝐛(𝒳)) = (^o𝒳)^o$ 是 $𝒳$ 关于子对象和扩张的闭包;
6. $𝐪𝐮𝐨𝐭(𝒳)$ 是 $𝒳$ 中对象关于商对象的闭包.
7. $𝐠𝐞𝐧(𝒳) = 𝐪𝐮𝐨𝐭(𝐟𝐢𝐥(𝒳))$ 是 $𝒳$ 中对象关于直和与商对象的闭包;
8. $𝐓(𝒳) = 𝐟𝐢𝐥(𝐪𝐮𝐨𝐭(𝒳)) = {}^o(𝒳^o)$ 是 $𝒳$ 关于商对象和扩张的闭包.

特别地, 对 $𝐦𝐨𝐝_A$, 对 $𝐚𝐝𝐝$ 封闭的对象类 (1, 2, 4, 5, 7, 8) 都是有限生成的, 从而可以用一个代表元表示. 例如 $𝐜𝐨𝐠(𝒳)$ 必形如某一 $𝐜𝐨𝐠(M)$.

此外, 需要对 $𝐅(𝒳)$ 与 $𝐓(𝒳)$ 的等价定义做一些说明, 见[此处](Def_de_TP).

{% enddef %}

### Torsion Pair 确定的对象类

{% def %}

(Torsion pair 的等价定义, [证明](Def_de_TP)).
称两个对象类 $(𝒯 , ℱ)$ 构成 torsion class, 若以下等价条件满足.

1. $𝒯 ⟂_o ℱ$. 任意对象 $M$ 可嵌入正合列 $0 → tM → M → fM → 0$, 其中 $tM ∈ 𝒯$ 且 $fM ∈ ℱ$.
2. 存在子函子 $t ↪ \mathrm{id}$ 使得 $t^2 ≃ t$, 以及 $t : \operatorname{cok}(t → \mathrm{id}) → 0$. 此时, $\ker t = ℱ$, $\operatorname{im} t = 𝒯$.
3. 存在商函子 $\mathrm{id} ↠ f$ 使得 $f ≃ f^2$, 以及 $f : \operatorname{ker}(f ↠ \mathrm{id}) → 0$. 此时, $\ker f = 𝒯$, $\operatorname{im} f = ℱ$.
4. ${}^oℱ = 𝒯$, 且 $ℱ = 𝒯^o$.
5. $𝒯$ 对商对象与扩张封闭, $ℱ = 𝒯^o$.
6. $ℱ$ 对子对象与扩张封闭, $𝒯 = {}^oℱ$.
7. 任意 $𝐪𝐮𝐨𝐭(𝒯)$-滤过对象属于 $𝒯$, 并取 $ℱ := 𝒯^o$
8. 任意 $𝐬𝐮𝐛(ℱ)$-滤过对象属于 $ℱ$, 并取 $𝒯 := {}^oℱ$.

{% enddef %}

以上 ses 在同构意义下唯一. 依照定义, $tM → N$ 类型的态射通过 $tN ↪ N$ 唯一地分解, 从而 $t$ 是全子范畴嵌入 $𝒯 ↣ 𝒜$ 的右伴随. 特别地,

1. $t$ 是右正合的左伴随函子, $𝒯$ 是余反射的;
2. $f$ 是左伴随的右正合函子, $ℱ$ 是反射的.

Torsion pair 关于 $\mathrm{Hom}$-垂直 (且封闭). 以下是一些关于 $\mathrm{Ext}^1$-垂直的结论.

{% lem %}
(垂直条件, [证明](Torsion_Pair_Ext_Orth)). 以下刻画 torsion pair $(𝒯, ℱ)$ 中满足 $\mathrm{Ext}^1$-垂直的对象. 记 $t$ 与 $f$ 是相应的子函子与商函子.

1. $𝒯 ∩ (^⟂ 𝒯) = 𝒯 ∩ τ ⁻¹ ℱ$.
2. $𝒯 ∩ (𝒯^⟂) = 𝒯 ∩ t(𝐢𝐧𝐣)$.
3. $ℱ ∩ (ℱ^⟂) = ℱ ∩ τ 𝒯$.
4. $ℱ ∩ (^⟂ ℱ) = ℱ ∩ f(𝐩𝐫𝐨𝐣)$.

{% endlem %}

{% lem %}
($𝐠𝐞𝐧$ 与 $𝐜𝐨𝐠$ 中的对象, [证明](gen_and_cog)). 给定对象 $X$ 与 $M$.

1. $M ∈ 𝐠𝐞𝐧(X)$ 当且仅当赋值 $(X, M) ⊗_{\mathrm{End}(X)} X → M$ 是满的.
2. $M ∈ 𝐜𝐨𝐠(X)$ 当且仅当余赋值 $M → ((M, X), X)$ 是单的.
{% endlem %}

{% lem %}
($𝐓$ 与 $𝐅$ 中的对象, 证明见[此定理](Def_de_TP)中 4 ⟺ 5 部分). 给定对象 $X$ 与 $M$.

1. $M ∈ 𝐓(X)$, 当且仅当 $M$ 存在合成列, 合成因子是 $𝐪𝐮𝐨𝐭(X)$.
2. $M ∈ 𝐅(X)$, 当且仅当 $M$ 存在合成列, 合成因子是 $𝐚𝐝𝐝(X)$.

{% endlem %}

{% lem %}
([证明](Gen_Eq_T)). $𝐠𝐞𝐧 = 𝐓$ 或 $𝐜𝐨𝐠 = 𝐅$ 的充分条件.

1. 若 $X ⟂ 𝐠𝐞𝐧(X)$, 则 $(𝐠𝐞𝐧(X), X^o)$ 是 torsion pair.
2. 若 $𝐜𝐨𝐠(X) ⟂ X$, 则 $(^o X, 𝐜𝐨𝐠 (X))$ 是 torsion pair.

{% endlem %}

作为 $𝐜𝐨𝐠$ 与 $𝐠𝐞𝐧$ 中的特例, 定义

{% def %}
(忠实模). 称 $M ∈ 𝐦𝐨𝐝_A$ 忠实, 若以下等价命题成立.

1. 对任意 $a ≠ 0$ 总有 $M ⋅ a ≠ 0$.
2. 同态 $A → \mathrm{End}(M)^{\mathrm{op}}$ 是单的.
3. $A ∈ 𝐜𝐨𝐠(M)$.
4. $DA ∈ 𝐠𝐞𝐧(M)$.

{% enddef %}

### 局部 Tilting 模: 两类 torsion pair

{% def %}
(局部 Tilting 模). 称 $T$ 是局部 tilting 的, 若 $p.\dim T ≤ 1$ 且 $\mathrm{Ext}^1(T,T)=0$.
{% enddef %}

等价地, $T$ 满足自垂直条件 $\mathrm{Ext}^1(T,T)$, 以及

1. $A$ 相对 $𝐚𝐝𝐝(T)$ 的内射分解 (余消解) 是至多 $1$ 维的, 即, 存在 ses

   $$
   0 → A → T' → T'' → 0,
   $$

   其中 $T$, $T''$ 属于 $𝐚𝐝𝐝(T)$.
2. $T$ 相对 $𝐚𝐝𝐝(A)$ 的投射分解 (消解) 是至多 $1$ 维的, 即, 存在 ses

   $$
   0 → P' → P'' → T → 0,
   $$

   其中 $P$, $P'$ 属于 $𝐚𝐝𝐝(A)$.

{% slo %}
由投射维度, $\mathrm{Ext}^1(T,-)$ 与 $\mathrm{Ext}^1(-,T)$ 是右正合函子.
{% endslo %}

{% thm %}
(局部 tilting 模诱导的 torsion pair, [证明](Partial_Tilting_Two_Torsion_pairs)). 局部 tilting 模 $T$ 诱导了以下两类 torsion pair.

1. $(𝐠𝐞𝐧(T), T^o)$ 是 torsion pair.
2. $(T^⟂, 𝐜𝐨𝐠(τT))$ 是 torsion pair.
3. $𝐠𝐞𝐧(T) ⊆ T^⟂$.
4. 以上两个 torsion pair, 均有 $T ∈ 𝒯 ∩ {}^⟂𝒯 = 𝒯 ∩ τ⁻¹ ℱ$.

{% endthm %}

{% note %}
内射模属于 $T^⟂$. 若投射模属于 $𝐠𝐞𝐧(T)$, 则其属于 $𝐚𝐝𝐝(T)$.
{% endnote %}

### Tilting 模诱导的 torsion pair

{% thm %}
([证明待补充](404)). 给定局部 tilting 模 $T$, 以下是 $T$ 成为 tilting 模的等价条件.

1. $A$ 相对 $𝐚𝐝𝐝(T)$ 的内射分解 (余消解) 是至多 $1$ 维的, 即, 存在 ses $0 → A → T' → T'' → 0$, 其中 $T$, $T''$ 属于 $𝐚𝐝𝐝(T)$.
2. $𝐠𝐞𝐧(T) = T^⟂$.
3. $T^o = 𝐜𝐨𝐠(τT)$.
4. 任意 $M ∈ T^⟂$ 存在满的右 $𝐚𝐝𝐝(T)$-逼近 $π : T^n ↠ M$, 且 $\ker π ∈ T^⟂$.
5. $(^⟂𝒯) ∩ 𝒯 = 𝐚𝐝𝐝(T)$, 即 $𝒯 ∩ τ ^{-1} ℱ = 𝐚𝐝𝐝(T)$.

{% endthm %}

前三条等价性的证明是直接的. 后两条定理的证明 (1 ⇒ 4,5) 理应借助 Bongartz 引理.

对 tilting 模, $𝐚𝐝𝐝(T)$ 具有一些神奇的性质. 一般地, 仅有 $({}^⟂𝒯) ∩ 𝒯 = 𝒯 ∩ τ^{-1} ℱ$, 但是,

{% slo %}

对 tilting 模诱导的 torsion pair, $𝒯$ 中被 $τ$ 平移至 $ℱ$ 中的项必是 $T$ 的直和项.

{% endslo %}

{% thm %}
(Bongartz, [证明待补充](404)). 局部 tilting 模是 tilting 模的直和项.
{% endthm %}

暂时将 4 与 5 当作性质使用.

{% prop %}
(Tilting 对象与 torsion pair, [证明](Tilting_Obj_Torsion_Pair)). 对 tilting 对象诱导的 torsion pair $(𝒯, ℱ)$.

1. 对任意 $M ∈ 𝒯$, 存在满的右 $𝐚𝐝𝐝 (T)$-逼近 $T^n ↠ M$ 使得

   $$
   0 → K → T^n → M → 0 \quad ∈ 𝒯.
   $$

2. $(^⟂𝒯) ∩ 𝒯 = 𝐚𝐝𝐝(T)$, 即 $𝒯 ∩ τ ^{-1} ℱ = 𝐚𝐝𝐝(T)$.
3. $M ∈ 𝒯$ 当且仅当配对 $(T, M) ⊗ T → M$ 是同构.

{% endprop %}

{% ex %}
特别地, 存在一列逼近的 ses

$$
0 → K_{k + 1} → T^{N_n} → K_n → 0\quad (n ≥ 0,\quad K_0 = M).
$$

使得有长正合列

$$
θ : \dots → T^{N_2} → T^{N_1} → T^{N_0} → M → 0.
$$

使得 $(T, θ)$ 是 $(T, M)$ 的 $\mathrm{End}(T)$-模投射分解.
{% endex %}

{% note %}
同样地,

1. 内射模属于 $T^⟂$.
2. 若投射模属于 $𝐠𝐞𝐧(T)$, 则其属于 $𝐚𝐝𝐝(T)$.
3. 投射内射模属于 $𝐚𝐝𝐝(T)$.
{% endnote %}

### Brenner-Butler 理论

{% lem %}
考虑函子 $(T,-) : 𝐦𝐨𝐝_A → 𝐦𝐨𝐝_{\mathrm{End}(T)^{\mathrm{op}}}$.

1. $𝐚𝐝𝐝(T) → 𝐩𝐫𝐨𝐣(\mathrm{End}(T)^{\mathrm{op}})$ 给出范畴等价. 此处 $T$ 可以是任意模.
2. $T$ 的直和项无重数, 当且仅当 $\mathrm{End}(T)$ 是基本代数.
3. 若 $T$ 是 tilting 模, 则 $(T,-)\restriction_𝒯$ 是全忠实的.
4. 若 $T$ 是 tilting 模, 则 $\mathrm{Ext}^1(T,-)\restriction_𝒯$ 也是全忠实的.

{% endlem %}

{% def %}

(Tilted 代数). 给定 tilting 模 $T ∈ 𝐦𝐨𝐝_A$, 记 $B:=\mathrm{End}(T)$ 是诱导的 tilted 代数.

一般地, 称 $B$ 是 tilted $k$-代数, 若存在 $k$ 代数 $A$ 上的 tilting 模 $T_A$ 使得 $B ≃ \mathrm{End}(T_A)$.

{% enddef %}

{% lem %}
($A$ 与 $\mathrm{End}(T)$).
$T$ 是 $(B,A)$-双模. 特别地, 代数 $A$ 与 $B$ 的关系如下.

1. $T$ 视作 $B^{\mathrm{op}}$-模也是 tilting 模.
2. 代数同态的合成 $A → B^{\mathrm{op}} → \mathrm{End}(_BT)^{\mathrm{op}}$ 是同构.
3. 中心 $Z(A) ≃ Z(B)$ 同构, 因此 $A$ 与 $B$ 具有相同的连通性.

{% endlem %}

{% thm %}
(对偶 torsion pair).
给定 tilting 模 $T ∈ 𝐦𝐨𝐝_A$, 记 $B:= \mathrm{End}(T_A)$.

1. $𝐦𝐨𝐝_A$ 中的 torsion pair $(𝒯, ℱ)$ 如下:
   1. $𝒯 = 𝐠𝐞𝐧(T_A) = T_A^⟂$,
   2. $ℱ = 𝐜𝐨𝐠 (τ T_A) = T_A^o$.
2. $𝐦𝐨𝐝_B$ 中的 torsion pair $(𝒳, 𝒴)$ 如下:
   1. $𝒳 = D(𝐜𝐨𝐠(τ{}_BT)) = D(_BT^o)$,
   2. $𝒴 = D(𝐠𝐞𝐧(_BT)) = D(_BT^⟂)$.
3. 省略对偶符号, 则
   1. $𝒳 = \ker \mathrm{Hom}_B(-,DT) = \ker (- ⊗_B T)$,
   2. $𝒴 = \ker \mathrm{Ext}_B^1(-, DT) = \ker \mathrm{Tor}_1^B(- , T)$.

{% endthm %}

习惯上, 置 $𝒯 := 𝒯(T_A) ⊆ 𝐦𝐨𝐝_A$ 以及 $𝒳 := 𝒳(T_A) ⊆ 𝐦𝐨𝐝_B$.

{% lem %}

($𝐦𝐨𝐝_B$ 中的 torsion pair). $𝐦𝐨𝐝_B$ 范畴存在对偶的逼近结论.

1. (原). 任意 $M_A ∈ 𝒯$ 存在满的右 $𝐚𝐝𝐝(T_A)$-逼近 $π : T_A^n ↠ M_A$, 且 $\ker π ∈ 𝒯$.
2. (新). 任意 $Y_B ∈ 𝒴$ 存在单的左 $𝐚𝐝𝐝((DT)_B)$-逼近 $ι: Y_B ↪ (DT)_B^m$, 且 $\operatorname{cok}ι ∈ 𝒴$.
3. (原). $M_A ∈ 𝒯$ 的充要条件是典范态射 $(T, M) ⊗ T → M$ 是 $𝐦𝐨𝐝_A$-同构.
4. (新). $Y_B ∈ 𝒴$ 的充要条件是典范态射 $(T, Y ⊗_B T) → Y$ 是 $𝐦𝐨𝐝_B$-同构.

{% endlem %}

{% thm %}

(BB 导出等价). 给定资料 $(A,T,B)$.

1. $\mathrm{Hom}_A(T,-) : 𝒯 ⇆ 𝒴 : (-⊗_BT)$ 是范畴等价 (视作拟逆).
2. $\mathrm{Ext}^1_A(T,-) : ℱ ⇆ 𝒳 : \mathrm{Tor}_1^B(-, T)$ 是范畴等价 (视作拟逆).
3. $𝐑^∙\mathrm{Hom}_A(T,-) : D^b(𝐦𝐨𝐝_A) ⇆ D^b(𝐦𝐨𝐝_B) : 𝐋 ^∙(-⊗_BT)$ 是导出等价.

{% endthm %}

{% thm %}
(BB 同调公式).
给定上述函子.

1. 零次导出的核 (像) 是一次导出的像 (核).
2. $𝐦𝐨𝐝_A$ 中 ses

   $$
   0 → (T,M) ⊗_B T → M → \mathrm{Tor}_1^B(\mathrm{Ext}_A^1(T,M), T) → 0,
   $$

   即, $M$ 的 $(t,f)$-典范 ses.
3. $𝐦𝐨𝐝_B$ 中 ses

   $$
   0 → \mathrm{Ext}_A^1(T, X ⊗ _BT) → X → (T, X ⊗ _BT) → 0,
   $$

   即, $X$ 的 $(t,f)$-典范 ses.

{% endthm %}

### 同调维度

{% lem %}

($𝒯$, $𝒴$ 与投射维数, [证明](T_Y_Dim)). 对 $M ∈ 𝒯$.

1. 若 $p.\dim M ≠ 1$, 则 $p.\dim M = p.\dim (T,M)$.
2. 若 $p.\dim M = 1$, 则 $p.\dim (T,M)$ 为 $0$ 或 $1$.

{% endlem %}

{% thm %}

(整体维数, [证明](Gl_Dim_A_B)). $\|gl.\dim A - gl.\dim B\|≤ 1$.

{% endthm %}

{% thm %}

(Happel 的导出等价定理). 假定 Abel 范畴有足够投射. 某对象 $T$ 满足 $\mathrm{Ext}_𝒜^{≥ 1}(T,T) =0$. 记 $B = \mathrm{End}(T)$.

1. $(T,-)_𝒜: 𝐚𝐝𝐝(T) ⇆ 𝐩𝐫𝐨𝐣(B) : (- ⊗ _BT)$ 是范畴等价.
2. 复合 $K^b(𝐚𝐝𝐝(T)) ↣ K^b (𝒜) → D^b𝒜$ 全忠实.
3. 若任意对象的 $𝐚𝐝𝐝(T)$-余消解维数有限, 则上述复合是等价.
4. 若 $𝒜$ 投射维数有限, 则典范函子 $K^b(𝐩𝐫𝐨𝐣(𝒜)) → D^b(𝒜)$ 是等价. 此时有导出等价 $D^b(𝒜) ≃ D^b(B)$.

{% endthm %}
