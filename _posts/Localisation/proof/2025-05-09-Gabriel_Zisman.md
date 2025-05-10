---
title: Gabriel-Zisman 局部化
author: Chencheng Zhang
layout: post
category: caprice
---

{% abs %}
本小节介绍 Gabriel-Zisman 通过路范畴构造局部化的实现方式.
{% endabs %}

## 构造

{% def %}
(范畴的局部化). 范畴 $𝒞$ 关于态射类 $S⊂ 𝖬𝗈𝗋(𝒞)$ 的局部化范畴 $S^{-1}𝒞$ 由以下泛性质决定: 对任意 $𝒟$, 函子 $F:𝒞 → 𝒟$ 映 $S$ 为 $𝒟$ 的同构类, 当且仅当 $F$ 经 $S^{-1}𝒞$ 分解.
$$\begin{equation}
\begin{bmatrix}
𝒞\left[ S^{-1}\right] & \dashrightarrow  & 𝒟\\
\uparrow  &  & ∥ \\
𝒞 & \xrightarrow{F} & 𝒟\\
S & \rightarrow  & \mathrm{Iso}( 𝒟)
\end{bmatrix}
\end{equation}$$

{% enddef %}

{% prop %}
(局部化的存在性: Gabriel-Zisman 的路范畴构造).
给定范畴 $𝒞$ 与态射类 $S$. 以下是将 $S^{-1}$ 形式地加入 $𝖬𝗈𝗋(𝒞)$ 的方式.

1. 由 $𝒞$ 与 $S$ 构造箭图范畴 $𝒬=𝒬(𝒞,S)$, 其对象类与 $𝒞$ 相同, 态射为无交并 $(X,Y)_{𝒬}=\sqcup_{n\geq 0}(X,Y)_n$. 此处
   1. $(X,Y)_0$ 包含 $Y\leftarrow X$ 朝向的长为 $0$ 的路, 非空当且仅当 $X=Y$. 其元素为 $(X,X)_0=\{\mathrm{id}_X\}$.
   2. $(X,Y)_1$ 包含 $Y\leftarrow X$ 朝向的长为 $1$ 的路, 定义作无交并

      $$\begin{equation}
        (X,Y)_1=(X,Y)_{𝒞}\sqcup \{a:Y\to X\mid a\in S\}=:(X,Y)_{1,1}\sqcup (X,Y)_{1,2}.
      \end{equation}$$

   3. $(X,Y)_{n+1}$ 包含 $Y\leftarrow X$ 朝向的长为 $n+1$ 的路. $s\in (X,Y)_{n+1}$ 当且仅当存在 $Z$ 使得 $s\in ((Z,Y)_1\circ (X,Z)_n)$. 此处态射的复合是自由的.

   - 注意: 范畴 $𝒬$ 中的态射是 $𝒞$ 中非恒等态射在忘却复合结构下生成的自由字. 因此, 对象间的 $\mathrm{Hom}$-类未必是小的.
2. 继而考虑 $𝒬$ 上的等价关系. 默认正向箭头的嵌入
   $$\begin{equation}
     𝖬𝗈𝗋(𝒞)\to 𝖬𝗈𝗋(𝒬),\quad [f:X\to Y]\mapsto [f\in (X,Y)_1],\quad \mathrm{id}_X\mapsto \mathrm{id}_X\in (X,X)_0.
   \end{equation}$$
   引入逆向箭头的嵌入为 (方便起见, 假定态射类 $S$ 不包含任一 $\mathrm{id}_X$)
   $$\begin{equation}
     \overline{(-)}:S\to 𝖬𝗈𝗋(𝒬)_1,\quad [f:X\to Y]\mapsto \overline f\quad (f\in (Y,X)_{1,2}).
   \end{equation}$$
   定义范畴 $𝒬$ 中的等价关系 (容易检验):
      1. 自反性, 表述略;
      2. 对 $𝒞$ 中的态射复合 $f\circ g=f\circ_{𝒞} g$, 在 $𝒬$ 中有 $(f\circ_{𝒬} g)\sim (f\circ g)$;
      3. 更一般地, 若 $𝖬𝗈𝗋$ 中有限长的字 $a_1a_2\cdots a_n$ 满足 $a_k=b\circ_{𝒞} c$, 则 $a_1a_2\cdots a_n\sim a_1a_2\cdots a_{k-1}bca_{k+1}\cdots a_n$;
      4. 对 $(f:X\to Y)\in S$, 定义 $(f\circ_{𝒬}\overline f)\sim \mathrm{id}_Y$ 与 $(\overline f\circ_{𝒬}f)\sim \mathrm{id}_X$;
      5. 更一般地, 对任一 $𝖬𝗈𝗋$ 中有限长的字 $a_1a_2\cdots a_n$ 与 $f\in S$, 在可复合的意义下有 $a_1a_2\cdots a_n\sim a_1\cdots a_{i}f\overline fa_{i+1}\cdots a_n$, 以及 $a_1a_2\cdots a_n\sim  a_1\cdots a_{j}\overline f ja_{j+1}\cdots a_n$.

   需要验证以上是范畴的等价关系. 需要对同一律加以说明: 若 $f\sim g$, 则 $f$ 与 $g$ 有相同的来源与去向.
4. $S^{-1}𝒞$ 定义作 $𝒬$ 关于以上范畴等价关系的商范畴. 注: 此处的商由 (未必小的) 滤过余极限, 因此局部化范畴未必是局部小的. 类似 3.2.7 的检验表明 $𝒬/∼ $ 满足局部化范畴 $S^{-1}𝒞$ 应具有的泛性质.

{% endprop %}

## 注记

{% ex %}
依照 Gabriel-Zisman 的构造, 局部化范畴的态射 (等价类的代表元) 形如
$$\begin{equation}
\begin{bmatrix}
X &  &  &  & ⋅  &   & ⋅  &  &  &  & Y\\
 & ↘  &  & ⇙  &  & \cdots &  & ↘  &  & ⇙  & \\
 &  & ⋅  &  &  &  &  &  & ⋅  &  &
\end{bmatrix}
\end{equation}$$

其中的双向箭头属于 $S$. 如锯齿状图所示, 商范畴中态射的等价关系往往难以操作; 引入乘法系重要目的是拉直锯齿图.
{% endex %}

{% ex %}
局部小范畴经 Gabriel-Zisman 局部化后未必是局部小范畴. 考虑范畴 $𝒞$ 如下:

1. 对象是 $X$, $Y$, 以及 $𝖮𝖻 (𝐒𝐞𝐭𝐬)$ (集合范畴的所有对象).
2. 态射规定如下:
   1. 对任意 $P ∈ 𝒞$, $\mathrm{End}(P) = \{\mathrm{id}_P\}$;
   2. 对任意 $P ∈ 𝐒𝐞𝐭𝐬$, 总有
   $$\begin{equation}
     |\mathrm{Hom}(X,P)| = |\mathrm{Hom}(Y, P)| = 1.
   \end{equation}$$
   3. 其他 $\mathrm{Hom}$-集为空.

   总之, 上述范畴非恒等态射形如下图:

   $$\begin{equation}
   \begin{bmatrix}
    &  &  & X &  &  & \\
   \nearrow  & \cdots  & \nearrow  & \uparrow  & \nwarrow  & \cdots  & \nwarrow \\
   \cdots  & S_{i} &  & S_{j} &  & S_{k} & \cdots \\
   \searrow  & \cdots  & \searrow  & \downarrow  & \swarrow  & \cdots  & \swarrow \\
    &  &  & Y &  &  &
   \end{bmatrix}
   \end{equation}$$

记 $S$ 是所有 $S_∙ → X$ 类型的态射. 此时 $\mathrm{Hom}_{𝒞[S^{-1}]}(X, Y)$ 是真类. 尽管 $𝒞[S^{-1}]$ 中仅有两个对象同构类, 该范畴不是局部小的.

{% endex %}
