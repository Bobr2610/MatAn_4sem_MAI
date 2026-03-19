***

# 3-ий МАТ. Семинар 05.03.2026

**№9 (из Д/З)**

$$ (1+t)^p = 1 + \underbrace{\frac{p}{1!}}_{C_p^1}t + \underbrace{\frac{p(p-1)}{2!}}_{C_p^2}t^2 + \underbrace{\frac{p(p-1)(p-2)}{3!}}_{C_p^3}t^3 + \underbrace{...}_{\text{коварно}} $$

при любых $p \in \mathbb{R}$

**Методичка по борьбе с многоточием**

**I.** Ряд Маклорена можно оборвать на любом члене.

**II.** Если последний оставшийся член содержащий $t^m$, то вместо отброшенных членов записать $+ \bar{o}(t^m) \rightarrow$ остаточный член в форме Пеано.

$$ (1+t)^p = 1 + \frac{p}{1!}t + \bar{o}(t) \equiv 1 + pt + t \cdot \beta(t), \text{  } \beta(t) \to 0 $$

$$ (1+t)^p = \text{--------- // ---------} + \frac{p(p-1)}{2!}t^2 + \bar{o}(t^2) \equiv $$

**III.** Ост. член вида $\bar{o}(\varphi(\xi))$ можно заменить на произведение $\varphi(\xi) \cdot \alpha(\xi)$ и дописать, что $\alpha(\xi) \to 0$

$$ \equiv 1 + pt + \frac{p(p-1)}{2}t^2 + t^2 \cdot \alpha(t), \text{ где } \alpha(t) \to 0 $$

---

**№9 (Призн. Гаусса)** $\frac{1}{1 \cdot 2} + \frac{1}{2 \cdot 3} + \frac{1}{3 \cdot 4} + ...$

$$ \sum_{n=1}^{\infty} \frac{1}{\sqrt[3]{n}} $$

$$ \frac{a_n}{a_{n+1}} = \sqrt[3]{1+\frac{1}{n}} = \{t = \frac{1}{n}\} = 1 + \frac{1}{3}t + \frac{1/3(-2/3)}{2!}t^2 + \frac{1/3(-2/3)(-5/3)}{3!}t^3 + ... = $$

$$ = 1 + \frac{1}{3}t - \frac{1}{9}t^2 + \bar{o}(t^2) = 1 + \frac{1}{3n} - \frac{1}{9n^2} + \bar{o}\left(\frac{1}{n^2}\right) = $$

$$ = 1 + \frac{1}{3n} - \frac{1}{9n^2} + \frac{1}{n^2}\omega(n), \text{ где } \omega(n) \xrightarrow{n \to \infty} 0 $$

по п. Гаусса :

$$ 1 + \frac{(1/3)}{n} + \frac{\omega(n) - (1/9)}{n^2} $$

$$ \gamma_n = (\omega(n) - 1/9) \xrightarrow{n \to \infty} -\frac{1}{9} \Rightarrow \text{огр-на} $$

$$ \alpha = 1 \Rightarrow \beta = 1/3 \Rightarrow \quad < 1 \Rightarrow \text{расх-ся} $$

**Th. из 1го сем-ра:** If посл-ть сх-ся $\Rightarrow$ она огр-на.

***

### {Признак Лейбница}

**Опр.** Ряд наз-ся знакочередующимся, если любые два соседних члена имеют <u>разные знаки</u>.

**Пр.** $1 - 1 + 1 - 1 + ... \quad ; \quad +\frac{1}{2} - \frac{1}{3} + \frac{1}{4} - \frac{1}{5} + ...$

**Th.** (признак Лейбница) $\ast$

Пусть 1) дан знакочер. ряд $(p_1 - p_2 + p_3 - ...)$ или $(-p_1 + p_2 - p_3 + ...)$

2) все $p_n > 0$

3) посл-ть $p_n$ <u>строго монотон. уб-т</u> , т.е. $p_1 > p_2 > p_3 > ... > p_n$

Тогда $\ast$ сх-ся $\Leftrightarrow p_n \to 0$

**Пр.**

① $1 - \frac{1}{2} + \frac{1}{3} - ... \quad [= \ln 2]$

$p_n = |a_n| = \frac{1}{n} > 0$

$1 > 1/2 > 1/3 > ...$

$p_n = \frac{1}{n} \to 0 \Rightarrow$ ряд сх-ся

② $1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + ... \quad[= \frac{\pi}{4}]$ — ряд Лейбница

$p_n = |a_n| = \frac{1}{2n-1} > 0$

$1 > 1/3 > 1/5 > ...$

$p_n = \frac{1}{2n-1} \xrightarrow{n \to \infty} 0 \Rightarrow$ ряд сх-ся

---

### {Признак Дирихле и Абеля}

**Th.** (признак Дирихле)

Пусть 1) дан ряд $\sum_{n=1}^{\infty} (a_n b_n)$

2) пос-ть $a_n$ нестрого монотонна, т.е. $\begin{array}{l} \text{либо } a_1 \le a_2 \le a_3 \le ... \\ \text{либо } a_1 \ge a_2 \ge a_3 \ge ... \end{array}$

3) $a_n \to 0$

4) т.е. $\exists C > 0 \quad \forall N \quad (|b_1 + ... b_N| < C)$

Тогда ряд $\sum_{n=1}^{\infty} (a_n b_n)$ сход-ся

**Примечание:**

Пр-к Дирихле и Абеля даёт список усл-ий, которые заведомо дают сходимость ряда.

При этом если хотя бы одно неверно то и про пов-ие ряда сказать ничего нельзя.

**Th. (признак Абеля)**

Пусть 1) и 2) --- // --- Дирихле

3) посл-ть $a_n$ огрн., т.е. $\exists C > 0 \quad \forall n(|a_n|<C)$

4) $\sum_{n=1}^{\infty} b_n$ сх-ся

Тогда $\nearrow$

**Задача**

Иссле-ть на сх-ть

$$ \underbrace{1}_{a_1 b_1} + \underbrace{\frac{1}{\sqrt{2}}}_{a_2 b_2} - \underbrace{\frac{1}{\sqrt{3}}}_{a_3 b_3} - \frac{1}{\sqrt{4}} + \frac{1}{\sqrt{5}} + \frac{1}{\sqrt{6}} $$

пр. Дирихле

2) $a_n = \frac{1}{\sqrt{n}} \Rightarrow \quad \frac{1}{\sqrt{1}} \ge \frac{1}{\sqrt{2}} \ge ... \quad b_n = 1, 1, -1, -1, ...$

3) $a_n \xrightarrow{n \to \infty} 0$

4) $C=3 > 0 \quad |1+1-1-1+...| < 3 \Rightarrow |S_k| < 3$

$\Rightarrow$ ряд сх-ся
