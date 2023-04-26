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
- [Integrazione di funzioni razionali](#Integrazione-di-funzioni-razionali)
- [Studio di funzioni tramite integrali](#Studio-di-funzioni-tramite-integrali)
- [Integrali impropri](#Integrali-impropri)
- [Convergenza e divergenza di un integrale](#Convergenza-e-divergenza-di-un-integrale)
- [Parallelismo con le serie armoniche generalizzate](#Parallelismo-con-le-serie-armoniche-generalizzate)

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
\int f'(x) \cdot g(x) 
$$

$$
= f(x) \cdot g(x) - \int f'(x) \cdot g(x) \space dx
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
\int x^3 e^x \space dx 
$$

$$
= x^3e^x - \Big[3x^2e^x - \Big(6xe^x - \int 6e^x
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
\end{cases} \space dx \\
$$

derivare $P(x)$ ed integrare $f(x)$.

$$
\circ \space \int P(x) \cdot \begin{cases}
ln(x) \\
arctan(x)
\end{cases} \space dx \\
$$

derivare $f(x)$ ed integrare $P(x)$.

$$
\circ \space \int e^{hx}\cdot \begin{cases}
cos(kx) \\
sen(kx)
\end{cases} \space dx
$$

integrare per parti 2 volte e poi portare e sinistra l'integrale che
sta a destra dell'uguale. \
Infine per integrali del tipo:

$$
\circ \space \int \begin{cases}
cos^k(x) \space dx \\
sen^k(x) \space dx
\end{cases}
$$

dove l'esponente $k$ può essere pari o dispari si procede nel seguente modo:

- $k$ pari $→$ integrazione per parti
- $k$ dispari $→$ integrazione per sostituzione

### Integrazione di funzioni razionali

Nei casi in cui viene richiesto di integrare il **rapporto tra due 
polinomi**, della seguente forma:

$$
\int \frac{P(x)}{Q(x)} \space dx
$$

la risoluzione dipenderà da uno dei seguenti casi:

- **Caso 1** $\rightarrow$ se il rapporto tra polinomi si trova nella seguente forma:

$$
\int \frac{B}{C(x) + D} \space dx
$$

la risoluzione avviene nel seguente modo:

$$
\int \frac{B}{C(x) + D} \space dx = \frac{B}{C} \cdot ln(|C(x) + D|)
$$

- **Caso 2** $\rightarrow$ se il rapporto tra polinomi si trova nella
seguente forma:

$$
\int \frac{A(x) + B}{C(x) + D} \space dx
$$

con $A \neq 0$, è possibile procedere nel seguente modo:

$$
\frac{A(x) + B}{C(x) + D} = \frac{\frac{A}{C}(C(x) + B)}{C(x) + D}
$$

$$
= \frac{\frac{A}{C}(C(x)+D-D) + B}{C(x) + D}
$$

scomponendo in due la frazione al numeratore:

$$
= \frac{\frac{A}{C}(C(x)+D) - \frac{A \cdot D}{C} + B}{C(x) + D}
$$

spezzando in due la frazione principale avremo:

$$
= \frac{\frac{A}{C}(C(x)+D)}{C(x) + D} + \frac{B - \frac{A \cdot D}{D}}
{C(x) + D}
$$

infine semplificando i $C(x) + D$:

$$
\frac{A}{C} + \frac{BC - AD}{C \cdot (C(x) + D)}
$$

Il risultato finale sarà l'integrazione di ciò che abbiamo trovato sopra.

- **Caso 3** $\rightarrow$ se il rapporto tra polinomi si trova nella seguente forma:

$$
\int \frac{1}{A(x)^2 + B(x) +C} \space dx
$$

per prima cosa sarà necessario ricondurlo alla seguente forma:

$$
\frac{1}{A} \int \frac{dx}{x^2 + \alpha(x) + \beta}
$$

dove $\alpha = B/A$ e $\beta = C/A$. Successivamente l'integrale dovrà
essere sviluppato procedendo in base ad uno dei tre casi elencati:

- **Caso 3-a** $\rightarrow$ Calcolando il **delta** del polinomio di secondo grado, se esso sarà uguale a 0 (**$\Delta = 0$**), allora sapendo che le radici sono uguali l'integrale può essere risolto nel seguente modo:

$$
\int \frac{1}{x^2 + \alpha(x) + \beta} = - \frac{1}{x - x_1} + c
$$

  - **Caso 3-b** $\rightarrow$ Se il **delta** è maggiore di 0 (**$\Delta > 0$**), allora le radici saranno diverse dunque l'integrale può essere risolto nel seguento modo:

$$
\int \frac{1}{x^2 + \alpha(x) + \beta}
$$

$$
= \frac{1}{x_1 - x_2} \cdot ln(\Big|\frac{x -x_1}{x-x_2}\Big|) + c
$$

- **Caso 3-c** $→$ Se il **delta** è minore di 0 (**$\Delta < 0$**), allora le radici saranno due numeri complessi diversi, dunque l'integrale potrà essere risolto nel seguente modo:

$$
\int \frac{1}{x^2 + \alpha(x) + \beta} \space dx
$$

$$ 
= \frac{2}{\sqrt{- \Delta}} \cdot arctan \Big( \frac{2x + \beta}{\sqrt{- \Delta}} \Big) + c
$$

- **Caso 4** $\rightarrow$ Se $P(x)$ è un polinomio di grado **maggiore di 2**, allora si dovrà effettura una divisione tra polinomi, così da abbassare il grado di $P(x)$ e poter rientrare in uno dei casi elencati precedentemente.

Sapendo che $P(x) = S(x) \cdot Q(x) + R(x)$, dove $S(x)$ è il risultato 
della divisione $\frac{P(x)}{Q(x)}$ e $R(x)$ il suo resto, allora l'integrale può essere risolto nel seguento modo:

$$
\int \frac{P(x)}{Q(x)} \space dx = \int S(x) \space dx + \int \frac{R(x)}{Q(x)} \space dx
$$

### Studio di funzioni tramite integrali

In alcuni casi, quando non si riesce a trovare una primitiva di una funzione, possiamo comunque trarre delle conclusioni andando a studiare l'integrale senza dover risolverlo.

#### Integrazioni di funzioni pari e dispari

Se $F(x)$ è definita come:

$$
F(t) = \int\limits_0^t f(x) \space dt
$$

- Se $f(x)$ è una funzione pari, allora $F(t)$ è una funzione dispari.
- Se $f(x)$ è una funzione dispari, allora $F(t)$ è una funzione pari.

Se una funzione $f(x)$ è integrata in un intervallo $[-t, t]$, allora:

- Se $f(x)$ è dispari:

$$
\int\limits_{-t}^{t} f(x) \space dx = 0
$$

- Se $f(x)$ è dispari:

$$
\int\limits_{-t}^{t} f(x) \space dx = 2 \int\limits_{0}^t f(x) \space dx
$$

#### Esempio di studio di funzione tramite integrale

Prendiamo il seguente integrale:

$$
F(t) = \int\limits_0^t [x|x| + sen^3(x)] \space dx
$$

1. $F$ è ben definita?
2. $F$ è derivabile?
3. $F(0), \space F'(0), \space F''(0)$ = ?
4. $F(1) > 0$ ?
5. $F$ è pari?
6. $F$ è crescente su $[0, + \infty)$ ?

Queste sono tutte possibili domande di cui si può dare una risposta. Di seguito le soluzioni ad esse:

1. Si perchè $f(x)$ è una funzione continua.
2. Essendo $f(x)$ una funzione continua e limitata è anche derivabile per il Teorema Fondamentale del Calcolo Integrale, infatti sappiamo anche che:

$$
F'(t) = t|t| + sen^3(t), \space \forall t\in R
$$

3. - $F(0) = \int\limits_0^0 f(x) \space dx = 0$
   - $F'(0) = 0 \cdot |0| + sen^3(0) = 0$
   - $F''(0) = t \cdot (segno)t + 3sen^2(t) \cdot cos(t) \rightarrow t = 0 → 0$
4. Andando a sostituire $t =1 \rightarrow$ $\int\limits_0^1 [x |x| + sen^3(x)] \space dx$, dunque sappiamo che:
  
$$
\int\limits_0^1 [x |x| + sen^3(x)] \space dx = \int\limits_0^1 [x^2 + sen^3(x)] \space dx
$$

e quindi andando a studiare il segno delle due funzioni integrande:

- $x^2 \geq 0$
- $sen^3(x) \geq 0$

possiamo concludere che l'integrale, avendo i limiti d'integrazione orientati nel verso giusto, è positivo.

5. Possiamo ricondurci al teorema sull'integrazione delle funzioni pari o dispari in quanto l'integrale è su $[0, t]$, quindi:
  
$$
f(x) = x|x| + sen^3(x)
$$

$$
f(-x) = -x|-x| + sen^3(-x)
$$

$$
= -x|x| + [-sen(x)]^3
$$

$$
= -x|x| + sen^3(x) \rightarrow - f(x)
$$

dunque $f(x)$ è dispari e di conseguenza $F$ è pari.

6. Utilizzando il Teorema Fondamentale Del Calcolo Integrale:

$$
F'(t) = t|t| + sen^3(t) \geq 0, \forall t \geq 0 \space ?
$$

$$
t|t| + sen^3(t) \geq 0, \forall t \geq 0 \space ?
$$

sapendo che la funzione $sen(x)$ oscilla tra -1 ed 1:

$$
-1 \leq sen^3(t) \geq 1
$$

$$
\rightarrow t^2 + sen^3(t) \geq t^2 - 1
$$

e sappiamo che $t \geq 1$ e che tra $[0, 1]$ $F \geq 0$, dunque $f(x) 
\geq 0 \rightarrow$ tra $[0, +∞)$ $F$ è crescente.

### Integrali impropri

Per alcuni tipi di integrali le cui funzione integrande hanno la presenza di alcuni punti di discontinuità, ossia non sono limitate e continue, non possiamo risolverli secondo Riemann. Tuttavia, possiamo andare a studiare il comportamento di una funzione se ci avviciniamo al punto problematico, dunque effettuando il limite.

#### Integrazione in senso improprio

Sia $f(x)$ una funzione con una discontinuità illimitata nel punto $x= b$, sapendo che non è integrabile secondo Riemann in $[a,b]$, possiamo dire che è **integrabile in senso improprio** in $[a,b]$ se l'integrale per $[a, b - \epsilon]$, con $\epsilon \to 0^+$ ammette limite finito (limite $\ne +∞, -∞$ e $\nexists$):

$$
\lim_{\epsilon \to 0^+} \int\limits_{a}^{b - ϵ} f(x) \, dx =
\lim_{\epsilon \to 0^+} F(x)|_a^{b-\epsilon} = l
$$

#### Convergenza e divergenza di un integrale

Data una funzione $f(x)$ e un intervallo illimitato (superiormente o lateralmente), si dice che l'integrale improprio di tale funzione è:

- Convergente se:

$$
\int\limits_{a}^b f(x) < + ∞
$$

- Divergente se:

$$
\int\limits_{a}^b f(x) = \pm ∞
$$

Se l'intervallo è illimitato in più punti è necessario spezzare l'intervallo e studiare il comportamento di ogni sotto-intervallo.
 
#### Criterio del confronto asintotico

Siano $f(x)$ e $g(x)$ due funzioni tali che in $x_0$ ci sia un punto illimitato, se:

$$
\lim_{x \to x_0} \frac{f(x)}{g(x)} = l \in (0, +∞)
$$

allora:

$$
\int\limits_a^{x_0} f(x) \, dx \simeq \int\limits_a^{x_0} g(x) \, dx
$$

e quindi:

- Se $g(x)$ converge, anche $f(x)$ converge
- Se $g(x)$ diverge, anche $f(x)$ diverge

#### Criterio del confronto

Siano $f(x)$ e $g(x)$ due funzioni tali che in $x_0$ ci sia un punto illimitato, se:

$$
0 \leq \int\limits_a^{x_0} f(x) \, dx \leq \int\limits_a^{x_0} g(x) \, dx
$$

allora:


- Se $g(x)$ converge, anche $f(x)$ converge
- Se $f(x)$ diverge, anche $g(x)$ diverge

#### Criterio della convergenza assoluta

Sia $f(x)$ una funzione che in $x_0$ ci sia un punto illimitato, se:

$$
\int\limits_a^{x_0} |f(x)| \, dx < +∞
$$

allora:

$$
\int\limits_a^{x_0} f(x) \, dx < +∞
$$

#### Parallelismo con le serie armoniche generalizzate

Proprio come per le serie numeriche, anche per integrali è possibile stabilire la convergenza o divergenza di funzioni del tipo:

$$
f(x) = \frac{1}{x^\alpha}
$$

Ne seguono due categorie:

$$
\lim_{\epsilon \to 0^+} \int\limits_{\epsilon}^{t} \frac{1}{x^\alpha}
= \begin{cases}
\frac{t^{1 - \alpha}}{1 - \alpha} && \text{se $\alpha < 1$} \\
+ ∞ && \text{se $\alpha \geq 1$}
\end{cases}
$$

$$
\lim_{\epsilon \to 0^+} \int\limits_{t}^{\epsilon} \frac{1}{x^\alpha}
= \begin{cases}
\frac{t^{1 - \alpha}}{1 - \alpha} && \text{se $\alpha > 1$} \\
+ ∞ && \text{se $\alpha \leq 1$}
\end{cases}
$$

[Torna su](#Indice)

