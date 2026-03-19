***

# 2-ой МАТ. Семинар 26.02.2025

**Пр.** $\frac{2}{3} - \frac{3}{5} + \frac{4}{7} - ... + (-1)^{n+1} \frac{n+1}{2n+1} + ...$
*(указана общая формула члена $a_n$)*

$a_n = (-1)^{n+1} \frac{n+1}{2n+1}$

Как ведет себя $|a_n|$?
$|a_n| = \frac{n+1}{2n+1} \to 1/2$
$|a_n| \not\to 0$
$a_n \not\to 0 \implies$ по Д.У. Расх (достаточному условию расходимости) ряд расх-ся

> **! Полезный факт**
> $a_n \to 0 \iff |a_n| \to 0$
> $a_n \not\to 0 \iff |a_n| \not\to 0$

---

## Предельный признак сравнения

**Таблица эквивалентностей (при $t \to 0$)**

| Тригонометрия | Степенные/Логарифмы | Многочлены |
| :--- | :--- | :--- |
| $\sin t \sim t$ | $(1+t)^a - 1 \sim a \cdot t$ <br> *(в частности $\sqrt[m]{1+t}-1 \sim \frac{t}{m}$)* | Мн-н, у которого все степени одночленов положительны $\sim$ члену наим. степени. |
| $\arcsin t \sim t$ | $\log_b (1+t) \sim \frac{t}{\ln b}$ <br> *(в частности $\ln(1+t) \sim t$)* | *Напр.* <br> $7t^3 + 2t^2 \sim 2t^2$ |
| $\text{tg} t \sim t$ | $b^t - 1 \sim t \cdot \ln b$ <br> *(в частности $e^t - 1 \sim t$)* | $3t + 5t\sqrt{t} \sim 3t$ |
| $\text{arctg} t \sim t$ | **Условия:** <br> $a \ne 0$ <br> $0 < b \ne 1$ <br> $m = 2, 3, 4...$ | $9t^4 + 4t^{3/5} + 9t^{4/13} \sim 9t^{4/13}$ |
| $1 - \cos t \sim \frac{t^2}{2}$ | | |

---

**Пр. при $n \to \infty$:**

1) $e^{1/n} - 1 \sim 1/n$
   *(пометка $1/n = t \to 0$)*

2) $1 - \cos(\frac{2}{n^3}) \sim \frac{(2/n^3)^2}{2}$
   *(пометка $t \to 0$)*

3) $\sqrt[3]{1 - \frac{1}{n}} - 1 \sim - \frac{1}{3n}$

4) $\arcsin \frac{1}{\sqrt{n}} \sim \frac{1}{\sqrt{n}}$

5) $\ln \frac{n+1}{n} = \log_e (1 + \frac{1}{n}) \sim \frac{1/n}{\ln e} = \frac{1}{n}$

6) $\sqrt{n+1} - \sqrt{n} = \sqrt{n}(\sqrt{\frac{n+1}{n}} - 1) = \sqrt{n}(\sqrt{1+\frac{1}{n}} - 1) \sim \sqrt{n} \cdot \frac{1}{2n} = \frac{1}{2\sqrt{n}}$

***

### Полезный факт №4

$$ \sum_{n=1}^{\infty} \frac{c}{n^p} \quad \begin{cases} \text{сх. при } p > 1 \\ \text{расх. при } p \le 1 \end{cases} $$
*   $c \neq 0$
*   $p > 0$ (const)
*"Ряд Дирихле" / "эталонный ряд"*

---

### Th. (предельный признак ср-ия)
**Пусть**

1) даны 2 ряда $\sum_{n=1}^{\infty} a_n$ и $\sum_{n=1}^{\infty} b_n$;
2) все $a_n > 0$ и все $b_n > 0$
3) $a_n \to 0, \quad b_n \to 0$ — Беск. Мал. Посл.
4) $a_n \underset{n \to \infty}{\sim} b_n$

**Тогда** ряды $\sum_{n=1}^{\infty} a_n$ *(сложный)* и $\sum_{n=1}^{\infty} b_n$ — равносходятся.

---

**Пр.** $\sum_{n=1}^{\infty} (\sqrt{n+1} - \sqrt{n}) \ln \frac{n+3}{n}$

**Возьмём**

$$ a_n = \underbrace{(\sqrt{n+1} - \sqrt{n})}_{\sim \frac{1}{2\sqrt{n}}} \cdot \underbrace{\ln \frac{n+3}{n}}_{\sim \frac{3}{n}} \sim \frac{1}{2\sqrt{n}} \cdot \frac{3}{n} = \frac{(3/2)}{n^{3/2}} = b_n $$

По ППС исх. ряд рав-ся с $\sum_{n=1}^{\infty} \frac{(3/2)}{n^{3/2}}$, а он сход. (ибо $p = 3/2 > 1$)

**Отв.** сх-ся

---

### Th. (признак Раабе [-Дюамеля])
**Пусть**

1) дан ряд $\sum_{n=1}^{\infty} a_n$
2) все $a_n > 0$ (*"знакоположительный"*)
3) $\lim_{n \to \infty} n \left( \frac{a_n}{a_{n+1}} - 1 \right) = q$
    *(! т.к. наоборот спр-ом Даламбера)*
    *(— либо кон. число, либо значок $+\infty$)*

**Тогда**

1) $IF \quad q > 1$, то ряд сх-ся
2) $IF \quad q < 1$, то ряд расх-ся
3) $IF \quad q = 1$, то пр-ак не даёт ответа на вопр. о сх-ти

***

**Прим.** Исследовать на сх-ть ряд $\frac{1}{1\cdot2\cdot3} + \frac{1}{2\cdot3\cdot4} + ...$

$$a_n = ... + \frac{1}{(n+2)(n+1)n}$$

$$ \frac{a_n}{a_{n+1}} = \frac{(n+1)(n+2)(n+3)}{(n+2)(n+1)n} = \frac{n+3}{n} = 1 + \frac{3}{n} $$

$$ \lim_{n \to \infty} n \left( \frac{a_n}{a_{n+1}} - 1 \right) = \lim_{n \to \infty} n \left( 1 + \frac{3}{n} - 1 \right) = 3 = \hat{q} > 1 $$
$\implies$ сх-ся по пр РД (признаку Раабе-Дюамеля)

---

### Th. (признак Гаусса)
**Пусть**

1) дан ряд $\sum_{n=1}^{\infty} a_n$
2) все $a_n > 0$
3) $\frac{a_n}{a_{n+1}} = \alpha + \frac{\beta}{n} + \frac{\gamma_n}{n^s}$, где
   $\begin{cases} \alpha, \beta, s \text{ — некот. конст-ты} \\ s > 1 \\ \gamma_n \text{ — огр. посл-ть} \\ \text{т.е. } \exists A, B \quad \forall n \quad (A < \gamma_n < B) \end{cases}$

**Тогда**

*   $\alpha < 1 \implies$ ряд расх
*   $\alpha > 1 \implies$ ряд сх-ся
*   $\alpha = 1$
    *   $\lor \quad \beta \le 1 \implies$ ряд расх-ся
    *   $\lor \quad \beta > 1 \implies$ ряд сх-ся

*(Справа нарисована схема в виде дерева, дублирующая логику для $\alpha$ и $\beta$):*
*   $\alpha < 1$ (Расх)
*   $\alpha = 1$
    *   $\beta < 1$ (расх)
    *   $\beta = 1$ (расх)
    *   $\beta > 1$ (сх)
*   $\alpha > 1$ (Сх)

---

**Пример.** Исследовать на сх-ть $\sum_{n=1}^{\infty} \frac{1}{n^3}$

$$ \frac{a_n}{a_{n+1}} = \frac{(n+1)^3}{n^3} = \frac{n^3 + 3n^2 + 3n + 1}{n^3} = 1 + \frac{3}{n} + \frac{3}{n^2} + \frac{1}{n^3} $$

$\alpha = 1 \quad \beta = 3 \implies \text{сх-ся}$

$$ \frac{\gamma_n}{n^s} = \frac{3n+1}{n^3} = \frac{3 + 1/n}{n^2} \implies \gamma_n \in (3, 4] $$
*(ограничена)*

$\implies \text{сх-ся}$