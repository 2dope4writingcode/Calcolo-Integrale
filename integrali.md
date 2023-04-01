# Integrali

### Indice
- [Integrazione secondo Riemann](#Integrazione-secondo-Riemann)
- [Teorema Fondamentale Del Calcolo Integrale](#Teorema-Fondamentale-Del-Calcolo-Integrale)
- [Funzioni primitive](#Funzioni-primitive)
- [Integrale definito e indefinito](#Integrale-definito-e-indefinito)
- [Derivate e Integrali immediati](#Derivate-e-Integrali-immediati)
- [Integrazione per sostituzione](#Integrazione-per-sostituzione)
- [Integrazione per parti](#Integrazione-per-parti)
- [Cosa integrare e cosa derivare?](#Cosa-integrare-e-cosa-derivare-?)

### Integrazione secondo Riemann

Sia $f: [a,b] \to R$ positiva e limitata. Si dice che $f$ è integrabile
secondo Riemann se $\overline{S} = \underline{S}$ dove:

- Il limite per $n \to \infty$ della somma $\underline{S_{n}}$:

$$
\lim_{n \to \infty} \frac{b-a}{2^{n}} \cdot \sum_{k=0}^{2^{n} - 1} 
min_{[x_{k}, x_{k+1}]} f(x) = \underline{S} 
$$
 
- Il limite per $n \to \infty$ della somma $\overline{S_{n}}$:

$$
\lim_{n \to \infty} \frac{b-a}{2^{n}} \cdot \sum_{k=0}^{2^{n} - 1} 
max{[x_{k}, x_{k+1}]} f(x) = \overline{S} 
$$

**L'integrale definito** nell'intervallo $[a,b]$ di $f(x)$ viene
denominato con:

$$
\int\limits_{a}^{b} f(x) \space dx
$$

### Teorema Fondamentale Del Calcolo Integrale

Se $f: [a,b] \to R$ è continua e se definiamo

$$
F(t) = \int\limits_{a}^{t} f(x) \space dx \space \, \forall t \in [a,b] 
$$

allora:

$$
F'(t) = f(t) \space \, \forall t \in [a,b]
$$

Dunque si può dire che l'integrale corrisponde all'operazione matematica
inversa della derivata.

### Funzioni primitive

Se $f(x)$ è una funzione integrabile, allora esistono **infinite
funzioni primitive** $G(x)$ tali che $G'(x) = F(x) + c$, $\forall c \in R$

### Integrale definito e indefinito

Definiamo **integrale definito** il calcolo dell'area al di sotto
di una data funzione $f(x)$ in un intervallo $[a,b]$ come:

$$
\int\limits_{a}^{b} f(x) \space dx= F(x) \Big|_a^b = F(b) - F(a)
$$

Definiamo **integrale indefinito** l'operazione inversa della derivazione, dunque trovare la la primitiva $F(x)$ di una funzione $f(x)$ come:

$$
\int f(x) \space dx = F(x) + c
$$

### Derivate e Integrali immediati

Di seguito due tabelle che elencano le principali derivate immediate e i corrispondenti integrali immediati:

<details closed>
<summary>Derivate immediate</summary>
<center>

| $f(x)$ | $f'(x)$ | 
| :----: | :----:  |
| $x^{\alpha}$ | $\alpha x^{\alpha -1}$ |
| $sin(x)$ | $cos(x)$ |
| $cos(x)$ | $-sin(x)$ |
| $tan(x)$ | $\frac{1}{cos^2(x)}$ |
| $arctan(x)$ | $\frac{1}{1+x^{2}}$ |
| $e^{x}$ | $e^{x}$ |
| $\alpha^{x}$ | $\alpha^{x}ln(\alpha)$ |
| $ln\mid x\mid$ | $\frac{1}{x}$ |

</details>
</center>

<details closed>
<summary>Integrali immediati</summary>
<center>

| $f(x)$ | $f'(x)$ | 
| :----: | :----:  |
| $x^{\alpha}$ | $\frac{x^{\alpha +1}}{\alpha + 1} + c$ |
| $sin(x)$ | $-cos(x) + c$ |
| $cos(x)$ | $sin(x) + c$ |
| $\frac{1}{cos^2(x)}$ | $tan(x) + c$
| $\frac{1}{1+x^{2}}$ | $arctan(x) + c$ |
| $e^{x}$ | $e^{x} + c$ |
| $\alpha^{x}$ | $\frac{\alpha^{x}}{ln(\alpha)} + c$ |
| $\frac{1}{x}$ | $ln\mid x \mid$ + c |

</details>
</center>

### Integrazione per sostituzione

Consideriamo questo esempio:

$$
\int\limits_1^3 e^{2x} \space dx
$$

come prima cosa dobbiamo porre $y=2x$ così da trasformare $f(x) = e^y.$ \
Successivamente anche la variabile d'integrazione dovrà essere modificata:

$$
y = 2x \\
$$

$$
dy = [2x]' dx \\
$$

$$
dy = 2 \space dx \\
$$

$$
\frac{dy}{2} = dx
$$

Una volta fatte queste sostituzioni risolveremo l'integrale indefinito
per poi sostituire alla fine il valore iniziale associato alla $y$ con i
corrispettivi limiti dell'integrale definito (1 e 3). Dunque l'integrale che otteremo sarà:

$$
\int e^y \space \frac{dy}{2} = \frac{1}{2} \int e^y \space dy \\
$$

a questo punto ci basterà risostituire $y = 2x$ e calcolare l'integrale immediato agli estremi  d'integrazione:

$$
\frac{1}{2}\int\limits_1^3 e^y \space dy = \frac{e^{2x}}{2} \Big|_1^3 =
\frac{e^6 - e^3}{2}
$$

### Integrazione per parti

Se il prodotto tra funzioni $f'(x) \cdot g(x)$ è integrabile, allora
l'integrale si può risolvere cona la seguente formula:

$$
\int f'(x) \cdot g(x) = f(x) \cdot g(x) - \int f'(x) \cdot g'(x) \space dx
$$

Consideriamo il seguente integrale:

$$
\int x^3 e^x \space dx
$$

prima di tutto bisogna stabilire quale sia la funzione da derivare e quale
da integrare:

- $f'(x) = e^x \implies f(x) = e^x$
- $g(x) = x^3 \implies g'(x) = 3x^2$

dunque andando ad applicare la formula dell'integrazione per parti avremo:

$$
\int x^3 e^x \space dx = x^3e^x - \int 3x^2 e^x \space dx 
$$

non potendo ancora ricondurci ad un integrale immediato, riapplichiamo 
l'integrazione per parti all'integrale ottenuto:

- $f'(x) = e^x \implies f(x) = e^x$
- $g(x) = 3x^2 \implies g'(x) = 6x$

$$
\int x^3 e^x \space dx= x^3 e^x - \int 3x^2 e^x \space dx \\
$$

$$
= x^3 e^x - \Big[3x^2 e^x - \int 6x e^x \space dx \Big]
$$

applicandola un'ultima volta avremo:

- $f'(x) = e^x \implies e^x$
- $g(x) = 6x \implies 6$

$$
\int x^3 e^x \space dx = x^3e^x - \Big[3x^2e^x - \Big(6xe^x - \int 6e^x
\space dx \Big) \Big] \\
$$

$$
= x^3e^x - 3x^2e^x + 6xe^x - 6e^x + c \\
$$

$$
= e^x (x^3 - 3x^2 + 6x - 6) + c
$$

### Cosa integrare e cosa derivare?

Per quanto riguarda gli integrali del tipo: $\int P(x) \cdot f(x)$ dove 
$P(x)$ rappresenta un polinomio generico, di seguito è rappresentato uno schema:

$$
\circ \space \int P(x) \cdot \begin{cases}
e^{kx} \\
cos(kx) \\
sen(kx) 
\end{cases} dx \\
$$

derivare $P(x)$ ed integrare $f(x)$.

$$
\circ \space \int P(x) \cdot \begin{cases}
ln(x) \\
arctan(x)
\end{cases} dx \\
$$

derivare $f(x)$ ed integrare $P(x)$.

$$
\circ \space \int e^{hx}\cdot \begin{cases}
cos(kx) \\
sen(kx)
\end{cases} dx
$$

integrare per parti 2 volte e poi portare e sinistra l'integrale che
sta a destra dell'uguale.












