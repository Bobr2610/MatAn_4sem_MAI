***

# 7-ой МАТ. Семинар 06.04.2026

## Равномерная сходимость (продолжение)

**Определение равномерной сходимости:**
$$S_n(x) \overset{D}{\rightrightarrows} S(x)$$
$$\forall \varepsilon > 0 \ \exists N : \forall k \ge N \ \forall x_0 \in D \quad (|S_k(x_0) - S(x_0)| < \varepsilon)$$

Раскроем модуль в неравенстве:
$$-\varepsilon < S_k(x_0) - S(x_0) < \varepsilon$$
$$S(x_0) - \varepsilon < S_k(x_0) < S(x_0) + \varepsilon$$

Таким образом, определение можно переписать в следующем виде:
$$\underbrace{\forall \varepsilon > 0}_{\text{какую бы $\varepsilon$-труб. вокруг гр. } y=S(x) \text{ мы ни взяли}} \quad \underbrace{\exists N \ \forall k \ge N}_{\text{начиная с некоторого номера}} \quad \forall x_0 \in D \quad \underbrace{\left( S(x_0) - \varepsilon < S_k(x_0) < S(x_0) + \varepsilon \right)}_{(\ast)}$$

**Геометрический смысл $(\ast)$:** все графики $y = S_k(x)$ лежат в $\varepsilon$-трубке графика $y = S(x)$.

**Что такое $\varepsilon$-трубка графика $y = S(x)$ на множестве $D$?**
Это множество точек плоскости $Oxy$, которые заметаются графиком $y = S(x)$ (при $x \in D$), когда он смещается вверх и вниз на $\varepsilon$. Границы трубки определяются кривыми $y = S(x) + \varepsilon$ и $y = S(x) - \varepsilon$.

---
**Из примера прошлого занятия:**
Рассмотрим последовательность $S_k(x) = x^k$ на интервале $x \in [0; 1)$.
*(По графику видно)*, что при малых $\varepsilon \in (0; 1)$ вообще все графики $y = S_k(x) = x^k$ выходят за пределы $\varepsilon$-трубки графика $y = S(x) \equiv 0$.
При этом, если $\varepsilon \ge 1$, то все графики $y = S_k(x)$ целиком лежат в $\varepsilon$-трубке $y = S(x)$.

**Вывод:** равномерной сходимости нет, $S_k(x) \underset{D}{\not\rightrightarrows} S(x)$.

***

### Пример 2
Дан функциональный ряд, частичная сумма (ч.с.) которого равна:
$$S_n(x) = \frac{\text{tg} x}{n}$$

**а) К чему поточечно сходится этот ряд на $D = \left(0; \frac{\pi}{2}\right)$?**
При фиксированном $x \in \left(0; \frac{\pi}{2}\right)$:
$$\lim_{n \to \infty} \frac{\text{tg} x}{n} = \lim_{n \to \infty} \frac{\text{tg} x}{\infty} = 0 \implies S(x) = 0 \quad \text{при } x \in \left(0; \frac{\pi}{2}\right)$$

**б) Есть ли равномерная сходимость на $D = \left(0; \frac{\pi}{2}\right)$?**
Так как предельная функция $S(x) = 0$ непрерывная, то, возможно, будет равномерная сходимость. Проверим это.
Рассмотрим графики первых частичных сумм: $S_1(x) = \text{tg} x$, $S_2(x) = \frac{\text{tg} x}{2}$ и т.д. При приближении $x \to \frac{\pi}{2}$ графики уходят в бесконечность.

**Вывод:** Какую бы $\varepsilon$-трубку (вокруг $y=0$) мы ни взяли, все $S_k(x)$ уйдут за её границы в $\infty \implies S_k(x) \not\rightrightarrows S(x)$ (равномерной сходимости нет).

---
*(Примечание: далее разобран фрагмент нахождения $N(\varepsilon)$ для другой функции, судя по виду вычислений, для функции, содержащей экспоненту).*

**3. б)** Графики $S_n(x)$ располагаются целиком в $\varepsilon$-трубке (начиная с некоторого номера) $\implies S_k(-1) < \varepsilon$

*Вычисления:*
$$e^{-k+1} < \varepsilon$$
$$-k + 1 < \ln \varepsilon$$
$$k > -\ln \varepsilon + 1$$
$$k > \ln \frac{1}{\varepsilon} + 1$$

Отсюда берем номер (округляя вверх):
$$N(\varepsilon) = \left\lceil \ln \frac{1}{\varepsilon} + 1 \right\rceil$$

***

### Пример 5
Дана последовательность:
$$S_k(x) = x^k, \quad D = \left[0; \frac{1}{2}\right]$$

**а) Найти поточечную сходимость $S_k(x) \xrightarrow{D} S(x)$**
При $x \in \left[0; \frac{1}{2}\right]$:
$$\lim_{k \to \infty} S_k(x) = \lim_{k \to \infty} x^k = 0 \quad (\text{т.к. } 0 \le x < 1)$$
$\implies S(x) = 0$ при $x \in \left[0; \frac{1}{2}\right]$.

**б) Исследовать на равномерную сходимость $S_k(x) \overset{D}{\rightrightarrows} S(x)$**
Да, равномерная сходимость есть, т.к. $\forall \varepsilon > 0$ график $y = S_k(x)$ будет целиком лежать в $\varepsilon$-трубке графика $y = S(x) \equiv 0$.
Наибольшее значение на отрезке функция принимает в правой точке:
$$S_k\left(\frac{1}{2}\right) < \varepsilon$$
$$\Updownarrow$$
$$\frac{1}{2^k} < \varepsilon$$
$$\frac{1}{\varepsilon} < 2^k$$
$$k > \log_2 \frac{1}{\varepsilon}$$

*(Пометка: просто взять $N(\varepsilon) = \left\lceil \log_2 \frac{1}{\varepsilon} \right\rceil$ нельзя, т.к. при больших $\varepsilon$ может получиться отрицательное число).*

**в) Найти $N(\varepsilon)$**
Для корректного задания номера распишем его кусочно:
* Если $\varepsilon > \frac{1}{2}$, то берем $N(\varepsilon) = 1$
* Если $\varepsilon \le \frac{1}{2}$, то берем $N(\varepsilon) = \lceil \log_2 \frac{1}{\varepsilon} \rceil + 10$ *(с запасом)*

Итак, искомый номер $N(\varepsilon)$ задается системой:

$N(\varepsilon) = 1$, если $\varepsilon > \frac{1}{2}$
$N(\varepsilon) = \lceil \log_2 \frac{1}{\varepsilon} \rceil + 10$, если $\varepsilon \le \frac{1}{2}$

*(Скобки $\lceil ... \rceil$ означают округление до целого числа вверх).*