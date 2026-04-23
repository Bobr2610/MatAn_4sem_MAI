***

# 4-ый МАТ. Семинар 12.03.2026

Разбор Домашнего задания

**!** №9 $\sum_{n=1}^{\infty} \frac{\sin n}{n}$ — **!** $[ \cos 2 + \cos 7 + \cos 12 + \dots ]$ $\leftarrow$ *Может быть на контрольной работе*

$\frac{(\cos 2 + \dots) \cos \frac{5}{2}}{\cos \frac{5}{2}}$

**признак Дирихле**

1) $a_n = \frac{1}{n}, \quad b_n = \sin n$

2) $a_1 \ge a_2 \ge \dots$

3) $a_n = \frac{1}{n} \to 0$

4) $\forall N \quad |\sin 1 + \dots + \sin N| \le C \text{ — для некоторой конкретной константы}$

*! НЕЛЬЗЯ $1 \cdot N$ т.к. в модуле $\le 1 \to N$ максимальная сумма*

**Искусственный прием:**

Пусть $\alpha \ne 2\pi k$ ($k \in \mathbb{Z}$) $\quad \text{т.к. } \alpha \ne 2\pi \to \frac{\alpha}{2} \ne \pi k$

$\downarrow \to \sin \frac{\alpha}{2} \ne 0$

Рассмотрим $\underbrace{\sin \alpha \quad +}_{+\alpha} \underbrace{\sin 2\alpha \quad +}_{+\alpha} \underbrace{\sin 3\alpha \quad + \dots +}_{+\alpha} \sin(N\alpha) =$

$\uparrow$ *Домножим и разделим на $\sin$ от $\frac{\alpha}{2}$*

$= \frac{\sin \frac{\alpha}{2} (\sin \alpha + \dots + \sin(N\alpha))}{\sin \frac{\alpha}{2}} =$

$= \frac{\sin \alpha \cdot \sin \frac{\alpha}{2} + \dots + \sin(N\alpha) \sin \frac{\alpha}{2}}{\sin \frac{\alpha}{2}} = \quad \quad \begin{cases} \sin \phi \cdot \sin \psi = \\ = \frac{1}{2} (\cos(\phi - \psi) - \\ - \cos(\phi + \psi)) \end{cases}$

$= \frac{\frac{1}{2} \left[ (\cos \frac{\alpha}{2} - \cos \frac{3\alpha}{2}) + \dots + (\cos \frac{2N-1}{2}\alpha - \cos \frac{2N+1}{2}\alpha) \right]}{\sin \frac{\alpha}{2}} =$

Итак $S_n(\alpha) = \sin \alpha + \sin 2\alpha + \dots + \sin(N\alpha) = \frac{\cos \frac{\alpha}{2} - \cos \frac{2N+1}{2}\alpha}{2 \sin \frac{\alpha}{2}}$

$|S_n(\alpha)| = \frac{|\underbrace{\cos \frac{\alpha}{2}}_{[-1; 1]} - \underbrace{\cos \frac{2N+1}{2}\alpha}_{[-1; 1]}|}{|2 \sin \frac{\alpha}{2}|} \le \frac{2}{2 |\sin \frac{\alpha}{2}|} = \frac{1}{|\sin \frac{\alpha}{2}|}$

$\uparrow$ *НЕТ $N$ (верно при всех $N$)*

$\Rightarrow |\sin 1 + \dots + \sin N| \le \frac{1}{\sin \frac{1}{2}}$

---

### Признаки сравнения

[Обычный] признак сравнения

**Теорема** (признак сравнения)

Пусть 1) даны два ряда $\sum a_n$ и $\sum b_n$

2) все $a_n \ge 0$, все $b_n \ge 0$ — "знакоотрицательные ряды"

3) $\forall n \; (a_n \le b_n)$, $\quad \text{major}$

$\hookrightarrow$ говорят, что "$\sum b_n$ — мажорирует ряд $\sum a_n$"

"$\sum b_n$ — мажорирующий для $\sum a_n$"

"$\sum a_n$ — мажорируемый рядом $\sum b_n$"

Тогда 1) Если $\sum b_n$ — сходится, то $\sum a_n$ — сходится.

2) — расходится, — расходится.

**Пример:** Исследовать на сходимость: $\sum_{n=1}^\infty \frac{\arctan(n!)}{n^3}$

Решение: $0 \le a_n = \frac{\arctan(n!)}{n^3} \le \frac{(\pi/2)}{n^3} = b_n \quad \{ \arctan \text{ — не зависит от внутреннего} \}$

Получили мажорирующий ряд $\sum_{n=1}^\infty \frac{\pi/2}{n^3}$, а он сходится

$\Rightarrow$ По признаку сравнения ряд $\sum a_n$ сходится.

**Пример:** —//— : $\sum_{n=1}^\infty \frac{\cos \frac{1}{n}}{n}$

$0 \le a_n = \frac{\cos \frac{1}{n}}{n} \le \dots \frac{1}{n}$ — *НЕЛЬЗЯ Т.К. ГАРМОНИЧЕСКИЙ РАСХОДИТСЯ*

$b_n = \frac{\cos \frac{1}{n}}{n} \ge \frac{\cos 1}{n} \Rightarrow \cos 1 \cdot \sum_{n=1}^\infty \frac{1}{n} \Rightarrow$ гармонический ряд $\Rightarrow$ расходится

$\uparrow$ $a_n$

$\Rightarrow$ По признаку сравнения ряд $\sum b_n$ расходится

---

### Абсолютная и Условная сходимости

**ФАКТ:** $\sum |a_n|$ — сходится $\Rightarrow \sum a_n$ — сходится

$\uparrow$ *ряд из модулей членов*

Примечание. Обратное неверно, т.е. $\not\Rightarrow$

Например, $(1 - \frac{1}{2} + \frac{1}{3} + \dots)$, однако $(1 + \frac{1}{2} + \frac{1}{3} + \dots)$

сходится \quad \quad расходится

**Определение.** Если $\sum |a_n|$ сходится, то ряд $\sum a_n$ **абсолютно** сходится $\left[ \sum \frac{1}{n^2} \right]$

**Определение.** Если $\sum |a_n|$ расходится, то сам ряд $\sum a_n$ сходится,

то ряд $\sum a_n$ — **условно** сходится $\left[ 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \dots \right]$

Упражнения:

① $1 - \frac{1}{\sqrt{2}} + \frac{1}{\sqrt{3}} - \frac{1}{\sqrt{4}} + \dots$

Сходится по Лейбницу $\Rightarrow$ сходится условно

Но по модулям расходится

② $\frac{1}{2} + \frac{2}{4} - \frac{3}{8} - \frac{4}{16} + \frac{5}{32} + \frac{6}{64} + \dots$

ряд из модулей сходится $\Rightarrow$ абсолютно сходится

$\sum \frac{n}{2^n}$ $\leftarrow$ сходится по радикальному признаку Коши
