***

# 6-ой МАТ. Семинар 02.04.2026

## Равномерная сх-ть ф-го ряда
*(Равномерная сходимость функционального ряда)*

Пусть у нас есть ф-ый ряд $u_1(x) + \dots + u_n(x)$ и задано некот. мн. $D = D_{\text{опр}}$.
Возьмём произв. т. $x_0 \in D$ и подст. её в ряд $\Rightarrow$ получим числ. ряд $u_1(x_0) + u_2(x_0) + \dots$

Тогда $\circledast$ сх-ся в т. $x_0$
$\Updownarrow$
числ. ряд $u_1(x_0) + u_2(x_0) + \dots$ сх.
$\Updownarrow$
посл-ть его част. сумм $S_n(x_0) = u_1(x_0) + u_2(x_0) + \dots$ сх-ся *(к некот. числу $S(x_0)$)*
$\Updownarrow$
$S_n(x_0) \xrightarrow{n \to \infty} S(x_0)$
$\Updownarrow$
$\lim_{n \to \infty} S_n(x_0) = S(x_0)$ *(из 1-го курса)*
$\Updownarrow$
$\forall \varepsilon > 0 \quad \exists N \quad \forall k \geqslant N \quad (|S_k(x_0) - S(x_0)| < \varepsilon)$

**Опр.** Говорят, что ряд ($u_1(x) + \dots$) сх. поточечно на мн-ве $D$ к ф-ции $S(x)$, если $\forall x_0 \in D$ ($S_n(x_0) \xrightarrow{n \to \infty} S(x_0)$), т.е.
$\forall x_0 \in D \quad \forall \varepsilon > 0 \quad \underset{N(x_0, \varepsilon)}{\exists N} \quad \forall k \geqslant N \quad (|S_k(x_0) - S(x_0)| < \varepsilon)$

Поточечная сх-ть гар-ет, что в каждой т-ке $x_0 \in D$ зн-ия $S_n(x_0)$ «подбираются» к $S(x_0)$, но ничего не говорится о «темпе» приближения к числу $S(x_0)$.
А в случае, если мы хотим, чтобы стремление шло примерно «с одинаковым темпом», требуется т.н. равномерная сх-ть.

**Опр.** Говорят, что ($u_1(x) + \dots$) сх-ся равномерно на мн-ве $D$ к ф-ции $S(x)$, если
$\forall \varepsilon > 0 \quad \underset{N(\varepsilon)}{\exists N} \quad \forall k \geqslant N \quad \forall x_0 \in D \quad (|S_k(x_0) - S(x_0)| < \varepsilon)$
В этом случае нер-во вып-ся начиная с номера, унив-го для всех $x_0 \in D$ (т.е. номер $N$ незав. от $x_0$).

**Пр. (хрестоматийный)**
$\underbrace{x}_{u_1(x)} + \underbrace{(x^2 - x)}_{u_2(x)} + \underbrace{(x^3 - x^2)}_{u_3(x)} + \dots, \quad D = [0, 1]$

**Решение:**
**1) К чему дан-ый ряд сх-ся поточечно на $D$?**
Рассм. произв. число $x_0 \in [0, 1]$, подставим:
$x_0 + (x_0^2 - x_0) + (x_0^3 - x_0^2) + \dots$
$S_1(x_0) = x_0$
...
$S_n(x_0) = x_0^n$

$S_n(x_0) \xrightarrow{n \to \infty} S(x_0) = \begin{cases} 0, & 0 \leqslant x_0 < 1 \\ 1, & x_0 = 1 \end{cases}$
*(Подписи рядом: «поточечное стремление», «Поточечный предел $y = S(x)$»)*

**2) А верно ли, что $S_n(x) \overset{[0, 1]}{\rightrightarrows} S(x)$?** *(сходится равномерно)*
Т.е. верно ли что
$\forall \varepsilon > 0 \quad \exists N \quad \forall k \geqslant N \quad \forall x_0 \in [0, 1] \quad (|\overbrace{x_0^k}^{S_k(x_0)} - S(x_0)| < \varepsilon)$

*(Слева нарисован график: оси координат от 0 до 1, показаны кривые $y = S_1(x)$ и $y = S_{10}(x)$, стремящиеся к нулю на промежутке $[0,1)$, но принимающие значение $1$ в точке $x=1$. На оси Y отмечена точка $\varepsilon$.)*

Из стр-ть *(структуры)* гр-в $y = S_k(x)$ видно, что при малых $\varepsilon$ (точнее $0 < \varepsilon < 1$) любой гр-к $y = S_k(x) = x^k$ будет отл-ся *(отличаться)* от $y = S(x)$ больше чем на $\varepsilon$, в т-ах дост. близких к $x=1$.
Следов-но, $\circledast$ неверно, и значит, $S_n(x) \underset{[0, 1]}{\not\rightrightarrows} S(x)$
**(Равном. сх. нет !!)**