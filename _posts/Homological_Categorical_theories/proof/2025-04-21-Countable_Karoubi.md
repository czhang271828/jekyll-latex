---
title: 有可数积或可数余积的三角范畴必 Karoubi
author: Chencheng Zhang
layout: post
category: proof
--- 

{% lem %}
(有可数积或可数余积的三角范畴必 Karoubi, <a href = "Countable_Karoubi">证明</a>).
三角范畴 Karoubi 的一个充分条件: 若三角范畴有可数积或可数余积, 则 Karoubi. 
{% endlem %}

{% pf %}
范畴 Karoubi, 当且仅当其反范畴亦然. 不妨假定 $𝒯$ 有可数积, 对幂等自同态 $f ∈ \mathrm{End}(X)$ 定义

$$
∏_ℕX \xrightarrow[:=-e_L] {1-f+fL}∏_ℕX ,\quad ∏_ℕX \xrightarrow[:=-e_R] {1-f+fR}∏_ℕX. 
$$

此处 $L$ 是左移算子 (满), $R$ 是右移算子 (满). 计算知 

$$
e_Le_R = 1,\quad e_Re_L = 1-(f,0,\ldots).
$$

在三角范畴中, $e_L$ 可裂满, 从而 $\ker (e_L)$ 存在, 因此 $(1-f)$ 存在核. 对称地, $𝒯$ Karoubi.  
{% endpf %}

{% note %}
以上实际上是在取 $\cdots → X \xrightarrow f X$ 的同伦极限.
{% endnote %}