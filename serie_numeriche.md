# Serie numeriche

### Indice

- [Definizione serie numerica](#Definizione-serie-numerica)
- [Serie convergenti](#Serie-convergenti)
- [Serie divergenti](#Serie-divergenti)
- [Serie non convergenti](#Serie-non-convergenti)
- [Serie geometrica](#Serie-geometrica)
- [Serie armonica](#Serie-armonica)
- [Serie armonica generalizzata](#Serie-armonica-generalizzata)
- [Condizione necessaria](#Condizioni-necessarie-per-convergenza-di-una-serie)
- [Serie a termini di segno costante](#Serie-a-termini-di-segno-costante)
- [Criterio del confronto](#Criterio-del-confronto)
- [Criterio del confronto asintotico](#Criterio-del-confronto-asintotico)
- [Criterio del rapporto](#Criterio-del-rapporto)
- [Criterio della radice](#Criterio-della-radice)
- [Ordini di grandezza delle successioni](#Ordini-di-grandezza-delle-successioni)
- [Formula di Stirling](#Formula-di-Stirling)
- [Criterio di Leibniz](#Criterio-di-Leibniz)
- [Convergenza assoluta](#Convergenza-assoluta)

## Definizione serie numerica

- Data la successione di **termine generico** $a_{k}$,

$$
a_{1} + a_{2} + ... = \sum_{k=1}^{n} a_{k}
$$

- Data la serie di termine generico $a_{k}$\,
  si fissa _n_ naturale, si calcola la somma dei primi _n_ numeri
  della sequenza, si passa al limite per $n \to +∞$

$$
n \to S_{n} := \sum_{k=1}^{n} a_{k} \to \sum_{k=1}^{∞}
a_{k} := \lim_{n \to {+∞}} S_{n}
$$

La successione $S_{n}$ è detta **successione delle somme parziali.**

### Serie convergenti

- Definizione

Se la successione delle somme parziali $S_{n}$ converge a $l$,
la serie numerica è **convergente** e la sua **somma** è $l$\:

$$
  \sum_{k=1}^{∞} a_{k} = l
$$

Ad esempio, la serie $\sum 1/k(k+1)$ è convergente e

$$
  \sum_{k=1}^{∞} \frac{1}{k(k+1)} = 1
$$

### Serie divergenti

- Definizione

Se la successione delle somme parziali $S_{n}$ diverge a
$+∞$, la serie numerica è **divergente** a $+∞$ e si scrive\,

$$
  \sum_{k=1}^{∞} a_{k} = +∞
$$

Analogamente, se $S_{n} \to -∞$, la serie diverge a $-∞$.

### Serie non convergenti

- Se una serie è divergente, allora non è convergente; ma esistono
  serie non convergenti e non divergenti.

### Serie geometrica

- Dato $q \in R$, la serie di termine $q^{k}$ viene detta
  **serie geometrica (di ragione $q$)**

La **Serie geometrica** è definita come\:

$$
S_{n} = \sum_{k=0}^{n} q^{k} = \begin{cases}
  \frac{1-q^{n+1}}{1-q} & \text{se $q \ne 1$}\\
  n+1 & \text{se q = 1}
\end{cases}
$$

$$
\lim_{n \to +∞} S_{n} = \sum_{k=0}^{∞} q^{k} = \begin{cases}
  \frac{1}{1-q} & \text{se $-1 < q < 1$} \\
  +∞ & \text{se $q \geq 1$} \\
  \nexists & \text{se $q \leq -1$}
\end{cases}
$$

### Serie armonica

- Prendendo in considerazione una successione del tipo\:

$$
a_{n} = \frac{1}{n+1}
$$

Essa viene chiamata **successione armonica**. La serie finita di successione
corrisponderà dunque a\:

$$
S_{n} = \sum_{k=1}^{n} \frac{1}{k} = 1 + \frac{1}{2} + \frac{1}{3} + ...+
\frac{1}{n}
$$

Studiando per $S_{n+1}$ se la serie **converge** o **diverge**
avremo che $\forall n$\:

$$
S_{n} + \frac{1}{n + 1} > S_{n}
$$

e quindi la **serie armonica** per $n \to +∞$ è **divergente**.

#### Serie armonica generalizzata

- Una volta generalizzata la serie armonica sarà\:

$$
S_{n} = \sum_{k=1}^{n} \frac{1}{k^\alpha} = 1 + \frac{1}{2^\alpha} +
\frac{1}{3^\alpha} + ... + \frac{1}{n^\alpha}
$$

Studiando cosa accade in base al valore di $\alpha$\:

- Se $\alpha < 1$\:

$$
\frac{1}{k^\alpha} > \frac{1}{k}
$$

dunque segue che\:

$$
\sum_{k=1}^{n} \frac{1}{k^\alpha} > \sum_{k=1}^{n} \frac{1}{k} \implies
\sum_{k=1}^{n} \frac{1}{k^\alpha} > +∞
$$

e poichè la **serie armonica generalizzata** per $\alpha < 1$ è maggiore
di una **serie divergente**, ne consegue che anch'essa sia **divergente**

- Se $\alpha > 1$\:

$$
\frac{1}{k^\alpha} < \frac{1}{k}
$$

dunque segue che:

$$
\sum_{k=1}^{n} \frac{1}{k^\alpha} < \sum_{k=1}^{n} \frac{1}{k} \implies
\sum_{k=1}^{n} \frac{1}{k^\alpha} < +∞
$$

e poichè la **serie armonica generalizzata** per $\alpha > 1$ è minore di una
**serie divergente**, ne consegue che essa sia **convergente**

La **Serie armonica generalizzata** è definita come\:

$$
\lim_{n \to +∞} S_{n} = \sum_{k=1}^{∞} \frac{1}{k^\alpha} = \begin{cases}
  +∞ & \text{se $\alpha \leq 1$} \\
  < + ∞ & \text{se $\alpha > 1$}
\end{cases}
$$

### Condizioni necessarie per convergenza di una serie

- Se una serie è **convergente** per $n \to +∞$, allora $a_{k} \to 0$\:

$$
\sum_{k=0}^{∞} a_{k} < +∞ \implies a_{k} \to 0
$$

- Negazione della condizione di **convergenza**\:

Se per $n \to +∞$ si verifica che $a_{k} \not\to 0$, allora la serie
**non può essere convergente**\,

$$
a_{k} \not\to 0 \implies \sum_{k=0}^{∞} a_{k} \quad \text{non è convergente}
$$

### Serie a termini di segno costante

- Se $a_{k} \geq 0, \forall k \in N$, allora la serie **converge**
  oppure **diverge positivamente**\:

$$
S_{n} = \sum_{k=0}^{∞} a_{k} = \begin{cases}
  < +∞ \\
  +∞
\end{cases}
$$

- Se $a_{k} \leq 0, \forall k \in N$, allora la serie **converge**
  oppure **diverge negativamente**\:

$$
S_{n} = \sum_{k=0}^{∞} a_{k} = \begin{cases}
  < -∞ \\
  -∞
\end{cases}
$$

### Criterio del confronto

Siano $0 \leq a_{k} \leq b_{k}, \forall k \in N$\,

- Se $S(b_{k})$ **converge**, allora anche $S(a_{k})$ **converge**\:

$$
\text{Se} \ \sum_{k=0} b_{k} < +∞ \implies \sum_{k=0} a_{k} < +∞
$$

- Se $S(a_{k})$ **diverge**, allora anche $S(b_{k})$ **diverge**\:

$$
\text{Se} \ \sum_{k=0} a_{k} = +∞ \implies \sum_{k=0} b_{k} = +∞
$$

### Criterio del confronto asintotico

Siano $0 \leq a_{k}, b_{k}$ tali che\:

$$
\lim_{k \to +∞} \frac{a_{k}}{b_{k}} = l
$$

se $l \geq 1$ allora\:

- $S(a_{k})$ converge **se e solo se** $S(b_{k})$ converge\:

$$
\sum_{k=0}^{∞} a_{k} < +∞ \iff \sum_{k=0}^{∞} b_{k}< +∞
$$

- $S(a_{k})$ diverge **se e solo se** $S(b_{k})$ diverge\:

$$
\sum_{k=0}^{∞} a_{k} = ∞ \iff \sum_{k=0}^{∞} b_{k}= ∞
$$

### Criterio del rapporto

Sia $a_{k} \geq 0$, se si verifica che \:

$$
\lim_{k \to +∞} \frac{a_{k+1}}{a_{k}} = l
$$

allora se\:

- $0 \leq l < 1$ la serie **converge**
- $l > 1$ la serie **diverge**
- $l = 1$ **non sappiamo** se la serie converga o diverga

Se la serie $a_{k}$ presenta un termine del tipo $k!$ allora conviene
utilizzare questo criterio.

### Criterio della radice

Sia $a_{k} \geq 0$, se si verifica che \:

$$
\lim_{k \to +∞} \sqrt[k]{a_{k}} = l
$$

allora se\:

- $0 \leq l < 1$ la serie **converge**
- $l > 1$ la serie **diverge**
- $l = 1$ **non sappiamo** se la serie converga o diverga

Se la serie $a_{k}$ presenta un termine del tipo $x^{k}, \space x \in R$ allora conviene
utilizzare questo criterio.

### Ordini di grandezza delle successioni

Per la risoluzione di alcuni limiti può essere utile ricordare gli
**ordini di grandezza delle successioni**\:

$$
c \prec \log^{k}(n) \prec \sqrt[b]{n} \prec n^{k} \prec A^{k}
\prec k! \prec k^{k}
$$

### Formula di Stirling

Per la risoluzione di alcune serie con il **Criterio della radice** è
necessario ricodarsi l'esistenza di un **limite notevole** nel quale ci si
imbatte spesso, ossia\:

$$
\lim_{k \to +∞} \sqrt[k]{k} = 1
$$

In alcuni casi però può risultare utile la **Formula di Stirling**,
descrivente il comportamento asintotico delle seguenti funzioni\:

$$
\lim_{k \to +∞} \frac{k!}{k^{k} \space  \cdot e^{-k} \space \cdot
\sqrt{2\pi k}}
$$

dunque per $k \to +∞$ si ha che\:

$$
k! \sim k^{k} \space \cdot e^{-k} \space \cdot \sqrt{2\pi k}
$$

### Criterio di Leibniz

Sia $a_{k} = (-1)^{k} \cdot b_{k}$, se $b_{k}$ soddisfa le seguenti
**tre condizioni**, allora la serie a termine generico $a_{k}$ è **convergente**\:

$$
\sum_{k = 0}^{+∞} (-1)^{k} \cdot b_{k} < +∞
$$

Se e solo se\:

- $b_{k} \geq 0$
- $b_{k+1} \leq b_{k} \space \forall k$
- $b_{k} \to 0 \space \text{per} \space n \to +∞$

### Convergenza assoluta

La serie di termine generico $a_{k}$ si dice **convergente assolutamente**
se e solo se la serie di termine generico $|a_{k}|$ è **convergente**

$$
\sum_{k = 0}^{∞} a_{k} < +∞ \iff \sum_{k=0}^{∞} |a_{k}| < +∞
$$
