# Appunti calcolo integrale

# Serie numeriche

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

### Non convergente $\ne$ divergente

- Se una serie è divergente, allora non è convergente; ma esistono
  serie non convergenti e non divergenti.

### Serie geometrica

- Dato $x \in R$, la serie di termine $x^{k}$ viene detta
  **serie geometrica (di ragione $x$)**

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
S_{n} = \sum_{k=1}^{n} \frac{1}{k} = 1 + \frac{1}{2} + \frac{1}{3} + ...
 + \frac{1}{n}
$$

Andando a vedere per $S_{n+1}$ se la serie **converge** o **diverge**
avremo che $\forall n$\:

$$
S_{n} + \frac{1}{n + 1} > S_{n}
$$

e quindi la **serie armonica** per $n \to +∞$ è **divergente**.

#### Serie armonica generalizzata

- Una volta generalizzata la serie armonica sara\:

$$
S_{n} = \sum_{k=1}^{n} \frac{1}{k^\alpha} = 1 + \frac{1}{2^\alpha}
+ \frac{1}{3^\alpha} + ... + \frac{1}{n^\alpha}
$$

Andando a vedere cosa accade in base al valore di $\alpha$\:

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
di una **serie divergente**, ne consegue che anch'essa sisa **divergente**

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
  + ∞ & \text{se $\alpha \leq 1$} \\
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

- Se $S(b_{k})$ **converge**, allora anche $S(b_{k})$ **converge**\:

$$
\text{Se} \ \sum_{k=0} b_{k} < +∞ \implies \sum_{k=0} a_{k} < +∞
$$

- Se $S(b_{k})$ **diverge**, allora anche $S(b_{k})$ **diverge**\:

$$
\text{Se} \ \sum_{k=0} b_{k} = +∞ \implies \sum_{k=0} a_{k} = +∞
$$

### Criterio del confronto asintotico

Siano $0 \leq a_{k}, b_{k}$ tali che\:

$$
\lim_{k} \to +∞ = \frac{a_{k}}{b_{k}} = 1
$$

allora\:

- $S(a_{k})$ converge **se e solo se** $S(b_{k})$ converge\:

$$
\sum_{k=0}^{∞} a_{k} < +∞ \iff \sum_{k=0}^{∞} < +∞
$$

- $S(a_{k})$ diverge **se e solo se** $S(b_{k})$ diverge\:

$$
\sum_{k=0}^{∞} a_{k} = ∞ \iff \sum_{k=0}^{∞} = ∞
$$
