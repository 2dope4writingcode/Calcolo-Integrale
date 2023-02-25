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

Esempio: Sia $a_{k} = (-1)^{k}$\, la successione delle somme
parziali è\:

$$
S_{1} = -1\\
S_{2} = -1 + 1 = 0\\
S_{3} = -1 + 1 - 1 = -1\\
...\\
S_{n} =
\begin{cases}
  -1 \quad n\; dispari\\
  0 \quad n\; pari\\
\end{cases}
$$

Dato che $S_{n}$ non ammette nè limite finito, nè limite infinito,
la serie $\sum_{k=1}^{∞} (-1)^{k}$ non è nè convergente,
nè divergente.
