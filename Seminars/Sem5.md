***

# 5-ый МАТ. Семинар 19.03.2026

**Функциональные ряды**

Пусть задана посл-ть ф-ий $u_1(x), u_2(x), \dots$

**Опр.** Ф-рядом н-ся форма записи вида

$\circledast \begin{cases} u_1(x) + u_2(x) + \dots \\ u_1(x) + u_2(x) + \dots + u_n(x) + \dots \text{ — "с общим членом"} \\ \sum_{n=1}^{\infty} u_n(x) \end{cases}$

**Опр.** Областью опр-ия ряда ($D_{\text{опр}}$) наз-ся все числа $x \in \mathbb{R}$, кот. можно подст. одн. во все ф-ции $u_n(x)$,

т.е. $D_{\text{опр}} = \bigcap_{n=1}^\infty D(u_n)$

Напр. $\frac{1}{x} + \frac{1}{x-1} + \frac{1}{x-2} + \dots$

$D_{\text{опр}} = \mathbb{R} \setminus \{0, 1, 2, 3, 4, \dots\} = \mathbb{R} \setminus (\mathbb{N} \cup \{0\}) = \mathbb{R} \setminus \mathbb{N}_+$

$\sqrt{2} \in D_{\text{опр}} \quad 0,5 \in D_{\text{опр}} \quad \frac{\pi^2}{e} \in D_{\text{опр}}$

Если взять конкр. число $x_0 \in D_{\text{опр}}$ и подст. его в ряд $\circledast$

ТО получится числовой ряд $\underbrace{u_1(x_0) + u_2(x_0) + \dots}_{\circledast \circledast} \begin{cases} \text{сх } < \text{усл.} \\ \text{абс.} \\ \text{расх.} \end{cases}$

**Опр.** Обл. сх-ти ряда ($D_{\text{сх}}$) наз-ся мн-во всех чисел $x_0 \in D_{\text{опр}}$, для кот. ряд $\circledast \circledast$ сх-ся

**Опр.** $(D_{\text{расх}})$ — расх-ся

**Опр.** $(D_{\text{абс}})$ — абс. сх-ся

**Опр.** $(D_{\text{усл}})$ — усл. сх-ся

---

**Пример:** Изучить ряд $1 + x + x^2 + x^3 + \dots \quad (D_{\text{сх-ся}}, \dots)$

**Решение:** $x \in \mathbb{R}$

1) Ясно, что $D_{\text{опр}} = \mathbb{R}$

2) Подст. в ряд конкр. число $x_0 \in D_{\text{опр}} = \mathbb{R}$, тогда получим числ. ряд $1 + x_0 + x_0^2 + x_0^3 + \dots$

$1^{\text{ый}}$ сл. $x_0 > 0 \to$ имеем знакопол. ряд $(1 + x_0 + x_0^2 + \dots)$

Применим признак Даламбера $\frac{a_{n+1}}{a_n} = \frac{x_0^n}{x_0^{n-1}} = x_0 \xrightarrow{n \to \infty} x_0 = q$

Значит при $x_0 \in (0, 1)$ ряд будет сх-ся, причем абсолютно

Итак, $(0, 1) \subseteq D_{\text{абс}} \quad \text{***}$

По тем же причинам $(1, +\infty) \subseteq D_{\text{расх}}$

При $x_0 = 1$ имеем ряд $(1+1+1+\dots)$, кот. расх по ДУР

Итак, $1 \in D_{\text{расх}}$ \quad $0 \in D_{\text{абс.}}$ $\nearrow$

$2^{\text{ой}}$ сл: $x_0 = 0 \to$ получаем ряд $(1+0+0+0+\dots)$, кот. сх-ся абсол.

$3^{\text{ий}}$ сл: $x_0 < 0 \to$ в этом случае ряд $(1 + x_0 + x_0^2 + \dots)$ — знакочеред.

Случай 3.1: $-1 < x_0 < 0 \to$ в этом случае $|a_n| = |x_0|^n$ — строго мон. уб. и $\to 0 \Rightarrow$ по пр-ку Лейбница ряд будет сх-ся.

Рассм ряд из модулей $\sum_{n=0}^\infty |x_0^n| = \sum_{n=0}^\infty |x_0|^n \to (-1; 0) \subseteq D_{\text{абс}}$

знакопол. ряд кот. сх ввиду ***

Случай 3.2: $x_0 = -1 \to$ пол. знакочер. $(1-1+1-1+1-\dots)$, который расх-ся в силу ДУР. Итак $-1 \in D_{\text{расх}}$

Случай 3.3: $x_0 < -1$. В этом сл. $|a_n| = |x_0^{n-1}| = |x_0|^{n-1} \to \infty$

$\Rightarrow |a_n| \to +\infty \Rightarrow |a_n| \not\to 0 \Rightarrow a_n \not\to 0 \Rightarrow$ Ряд расх-ся

Итак $(-\infty, -1) \subseteq D_{\text{расх}}$

**Ответ:**

$D_{\text{опр}} = \mathbb{R}$

$D_{\text{сх}} = (-1; 1)$

$D_{\text{расх}} = (-\infty; -1] \cup [1; +\infty)$

$D_{\text{абс}} = (-1; 1)$

$D_{\text{усл}} = \emptyset$
