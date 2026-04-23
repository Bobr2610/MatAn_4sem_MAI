***

# 9-ый Семинар 16/04/2025
N09 из Домашнего задания  *{ На контрольной работе могут быть сложные синусы }*

$\sum_{n=1}^{\infty} \frac{\sin(2nx)}{n+x} \quad D = [\pi/4, 3\pi/4]$

$a_n(x) = \frac{1}{n+x}$
$\forall x_0 \in D \quad a_1(x_0) \ge a_2(x_0) \ge ...$
$a_n(x) \overset{D}{\rightrightarrows} 0 \quad \forall x_0 \in D$
Так как $\frac{1}{n+x_0} < \varepsilon \Rightarrow n > \frac{1}{\varepsilon} - x_0$
$N(\varepsilon) = \left[ \frac{1}{\varepsilon} - \frac{\pi}{4} \right] + 10, \quad 0 < \varepsilon < 1$

$b_n(x) = \sin(2nx)$
$\forall n \; \forall x_0 \quad |b_1(x) + b_2(x) + ...| \le \frac{1}{|\sin x_0|}$
Так как $\frac{\sin\frac{\alpha}{2}\sin\alpha + \sin\frac{\alpha}{2}\sin 2\alpha + ... + \sin\frac{\alpha}{2}\sin n\alpha}{\sin\frac{\alpha}{2}} =$
$= \frac{-\frac{1}{2}\left[\cos\left(\frac{3}{2}\alpha\right) - \cos\frac{1}{2}\alpha + ... + \cos\frac{2n+1}{2}\alpha - \cos\frac{2n-1}{2}\alpha\right]}{\sin\frac{\alpha}{2}} = ... \le \frac{1}{|\sin\frac{\alpha}{2}|}$ (где $\alpha = 2x$)
$\Rightarrow$ По признаку Дирихле сходится

$\Rightarrow \forall \varepsilon > 0 \; \exists N \; \forall n \ge N \; \forall x_0 \in D \quad |a_n(x_0)| < \varepsilon$

---

## Отрицание определений поточечной и равномерной сходимости

1) $S_n(x) \xrightarrow{D} S(x)$ *(поточечная сходимость)*
   $\forall x_0 \in D \; \forall \varepsilon > 0 \; \exists N : \forall n \ge N$
   $(|S_n(x_0) - S(x_0)| < \varepsilon)$
2) неверно, что $S_n(x) \xrightarrow{D} S(x)$
   $\exists x_0 \in D \; \exists \varepsilon > 0 \; \forall N \; \exists n \ge N$
   $(|S_n(x_0) - S(x_0)| \ge \varepsilon)$

## Степенные ряды

*Определение.* Степенным рядом называется функциональный ряд вида
$c_0 + c_1(x-x_0) + c_2(x-x_0)^2 + c_3(x-x_0)^3 + ...$
где $c_1, c_2, c_3$ - заданные числа (называются коэффициентами степенного ряда), $x_0$ - заданное число (называется центром).

*Примеры:*
1) $1 + (x-2) + \frac{(x-2)^2}{2!} + \frac{(x-2)^3}{3!} + ...$
   Центр: $x_0 = 2$
   Коэффициенты: $c_0 = 1, \; c_1 = \frac{1}{1!}, \; ... \; c_n = \frac{1}{n!}$

2) $x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + ... = [\sin x]$
   Центр: $x_0 = 0$
   Коэффициенты: $c_0 = 0, \; c_1 = \frac{1}{1!}, \; c_2 = 0, \; c_3 = -\frac{1}{3!}, \; c_4 = 0 ...$

Если в степенной ряд подставить $x=x_0$, то получится ряд $c_0 + 0 + 0 + ...$
Это означает, что всегда $x_0$ лежит в области сходимости.

*Факт:* У степенных рядов область сходимости может быть 6-ти видов:
1) $D_{cx} = \{x_0\} \Rightarrow R_{cx} = 0$
2) $D_{cx} = (x_0-R; x_0+R)$
3) $D_{cx} = [x_0-R; x_0+R]$
4) $D_{cx} = (x_0-R; x_0+R]$
5) $D_{cx} = [x_0-R; x_0+R)$
*(Для 2-5 радиус сходимости $R_{cx} = R$)*
6) $D_{cx} = (-\infty; +\infty) \Rightarrow R_{cx} = +\infty$
($R_{cx}$ - радиус сходимости)

---

Если знать $R_{cx}$, то можно в первом приближении записать область сходимости ряда.
Например, если $x_0 = 5, \; R_{cx} = 2$, то область сходимости это промежуток $\langle 5-2; 5+2 \rangle$, т.е. $\langle 3; 7 \rangle$.

**Как найти $R_{cx}$ степенного ряда?**
1 способ: $1/R_{cx} = \lim_{n \to \infty} \left| \frac{c_{n+1}}{c_n} \right|$  `*`
2 способ: $1/R_{cx} = \lim_{n \to \infty} \sqrt[n]{|c_n|}$ - формула Коши-Адамара `**`

`*` обе допускают значения $R_{cx} = 0$ и $R_{cx} = +\infty$ (формулы символические)
`**` этими формулами можно пользоваться в том случае, если среди коэффициентов $(c_0, c_1, c_2...)$ либо нет нулевых, либо конечное число нулевых.

**Факт 1-ый:** Если $R_{cx} \neq 0$, то степенной ряд сходится равномерно на любом конечном отрезке, который целиком укладывается в $D_{cx}$.
**Факт 2-ой:** Если $R_{cx} \neq 0$, то на интервале/прямой степенной ряд сходится абсолютно.

*Пример:* $\sum_{n=2}^{\infty} \frac{(x+7)^n}{\sqrt{n}}$
$x_0 = -7 \quad c_0 = 0 \quad c_1 = 0 \quad c_2 = \frac{1}{\sqrt{2}} \quad c_3 = \frac{1}{\sqrt{3}} \Rightarrow \begin{cases} 0, & n=0,1 \\ \frac{1}{\sqrt{n}}, & n \ge 2 \end{cases}$

Нулевых конечное число $\Rightarrow 1/R_{cx} = \lim_{n \to \infty} \frac{1/\sqrt{n+1}}{1/\sqrt{n}} = \lim_{n \to \infty} \sqrt{\frac{n}{n+1}} = 1$
$\Rightarrow R_{cx} = 1$
$D_{cx} = \langle -7-1; -7+1 \rangle = \langle -8; -6 \rangle$ *(непонятно какие скобки)*

*   $x = -8 \Rightarrow \sum_{n=2}^{\infty} \frac{(-1)^n}{\sqrt{n}}$ - сходится условно
*   $x = -6 \Rightarrow \sum_{n=2}^{\infty} \frac{1}{\sqrt{n}}$ - расходится как ряд Дирихле

---

$D_{\text{опр}} = (-\infty; +\infty)$
$D_{cx} = [-8; -6)$
$D_{\text{абс}} = (-8; -6)$
$D_{\text{усл}} = \{-8\}$
$D_{\text{расх}} = (-\infty; -8) \cup [-6; +\infty)$

---

**Как быть, если среди чисел $c_0, c_1, c_2, \dots$ бесконечное количество нулей?**

**Ответ:** надо сделать замену, которая устранила бы эту проблему.

**Пример:** $\circledast \sum_{n=2}^{\infty} \frac{3^n \cdot (x-2)^{2n}}{n}$ — найти $D_{\text{опр}}$ и т.д.

**Решение:**
1) Ясно, что $D_{\text{опр}} = (-\infty; +\infty)$
2) Центр ряда $x_0 = 2$
3) Коэффициенты ряда:
   $c_0 = 0, \; c_1 = 0, \; c_2 = 0, \; c_3 = 0, \; c_4 = \frac{3^2}{2}, \; c_5 = 0, \; c_6 = \frac{3^3}{3}, \dots$

   То есть
   $c_n = \begin{cases} 0, & \text{если } n=0; 2 \\ 0, & \text{если } n=2k-1, \; k \ge 1 \\ \frac{3^k}{k}, & \text{если } n=2k, \; k \ge 2 \end{cases}$

Итак, среди коэффициентов бесконечное число нулевых $\Rightarrow$ применять формулы для $R_{cx}$ нельзя $\Rightarrow$ нужно делать замену!!!

Замена $\tilde{x} = (x-2)^2$ приводит к вспомогательному ряду

$\circledast\circledast \sum_{n=2}^{\infty} \frac{3^n}{n} \cdot \tilde{x}^n$ — это тоже степенной ряд!

У него уже другие коэффициенты:
$\tilde{c}_0 = 0$
$\tilde{c}_1 = 0$
$\tilde{c}_n = \frac{3^n}{n}, \quad n \ge 2$

Среди чисел $\tilde{c}_0, \tilde{c}_1, \dots$ конечное число нулевых $\Rightarrow$ применять формулы можно:

$\frac{1}{\tilde{R}_{cx}} = \lim_{n \to \infty} \sqrt[n]{|\tilde{c}_n|} = \lim_{n \to \infty} \sqrt[n]{\frac{3^n}{n}} = \lim_{n \to \infty} \frac{3}{\sqrt[n]{n}} = \frac{3}{1} = 3$

Значит, у вспомогательного ряда $\circledast\circledast$ радиус сходимости равен $\tilde{R}_{cx} = \frac{1}{3}$.
Значит, $\tilde{D}_{cx} = \left\langle 0 - \frac{1}{3}, 0 + \frac{1}{3} \right\rangle = \left\langle -\frac{1}{3}, \frac{1}{3} \right\rangle$
*(стрелочки указывают на угловые скобки с подписью: "пока неясно, какие скобки")*

Исследуем поведение ряда $\circledast\circledast$ на правом конце $\tilde{x} = \frac{1}{3}$:
$\sum_{n=2}^{\infty} \frac{3^n}{n} \cdot \left(\frac{1}{3}\right)^n = \sum_{n=2}^{\infty} \frac{1}{n}$ — это хвост гармонического ряда, значит, он расходится.

Исследуем поведение ряда $\circledast\circledast$ на левом конце $\tilde{x} = -\frac{1}{3}$:
$\sum_{n=2}^{\infty} \frac{3^n}{n} \cdot \left(-\frac{1}{3}\right)^n = \sum_{n=2}^{\infty} \frac{(-1)^n}{n}$ — этот ряд сходится (по признаку Лейбница), причем, очевидно, условно.

Значит, для вспомогательного ряда $\circledast\circledast$
$\tilde{D}_{cx} = \left[-\frac{1}{3}; \frac{1}{3}\right)$
$\tilde{D}_{\text{абс}} = \left(-\frac{1}{3}; \frac{1}{3}\right); \quad \tilde{D}_{\text{усл}} = \left\{-\frac{1}{3}\right\}$

Обратная замена:

1) Исходный ряд $\circledast$ сходится
   $\Updownarrow$
   $(x-2)^2 \in \tilde{D}_{cx} = \left[-\frac{1}{3}; \frac{1}{3}\right)$
   $\Updownarrow$
   $-\frac{1}{3} \le (x-2)^2 < \frac{1}{3}$
   $2 - \frac{1}{\sqrt{3}} < x < 2 + \frac{1}{\sqrt{3}}$

2) Исходный ряд $\circledast$ сходится абсолютно
   $\Updownarrow$
   $(x-2)^2 \in \tilde{D}_{\text{абс}} = \left(-\frac{1}{3}; \frac{1}{3}\right)$
   $\Updownarrow$
   $-\frac{1}{3} < (x-2)^2 < \frac{1}{3}$
   $2 - \frac{1}{\sqrt{3}} < x < 2 + \frac{1}{\sqrt{3}}$

3) Исходный ряд $\circledast$ сходится условно
   $\Updownarrow$
   $(x-2)^2 \in \tilde{D}_{\text{усл}} = \left\{-\frac{1}{3}\right\}$
   $\Updownarrow$
   $(x-2)^2 = -\frac{1}{3}$
   $\Updownarrow$
   $x \in \emptyset$

**Ответ:**
$D_{\text{опр}} = (-\infty; +\infty)$
$D_{cx} = \left(2 - \frac{1}{\sqrt{3}}; 2 + \frac{1}{\sqrt{3}}\right)$
$D_{\text{абс}} = \left(2 - \frac{1}{\sqrt{3}}; 2 + \frac{1}{\sqrt{3}}\right)$
$D_{\text{усл}} = \emptyset$
$D_{\text{расх}} = \left(-\infty; 2 - \frac{1}{\sqrt{3}}\right] \cup \left[2 + \frac{1}{\sqrt{3}}; +\infty\right)$