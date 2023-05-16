# Equazioni Differenziali

### Indice

- [Equazione differenziale ordinaria](#Equazione-differenziale-ordinaria)
- [Problema di Cauchy](#Problema-di-Cauchy)
- [EDO lineare omogenea](#Edo-lineare-omogenea)
- [Problema di Cauchy di EDO lineare non omogenea](#Problema-di-Cauchy-di-EDO-lineare-non-omogenea)
- [Equazioni a variabili separabili](#Equazioni-a-variabili-separabili)
- [EDO lineari non omogenee del secondo ordine](#EDO-lineari-non-omogenee-del-secondo-ordine)

### Equazione differenziale ordinaria

##### Definizione EDO

**Un'equazione differenziale ordinaria (EDO)** è un'equazione la cui **incognita** è una funzione e almeno uno dei termini che compaiono è una **derivata** qualsiasi della funzione stessa.
Il grado più alto della derivata che compare indica **l'ordine** dell'EDO.

### Problema di Cauchy

Viene definito Problema di Cauchy un sistema matematico da risolvere con all'interno una qualsiasi equazione differenziale di ordine N e delle condizioni iniziali legate ad essa. La soluzione al PDC è sempre solo una. Di seguito un esempio di come si presenta il sistema:

$$
(p) = \begin{cases}
y''(t) = g \\
y'(0) = 0 \\
y(0) = 0
\end{cases}
$$

### EDO lineare omogenea

Questo tipo di EDO presenta al suo interno termini di grado 0 o 1 ed essendo omogenea non contiene termini costanti aggiuntivi indipendenti dalla funzione $y(t)$. Dunque possiamo dire che dato il caso generico:

$$
\begin{cases}
y'(t) = a(t) \space y(t) \\
y(t_0) = y_0
\end{cases}
$$

la soluzione sarà:

$$
y'(t) = a(t) \space y(t) \rightarrow y(t) = Ce^{A(t)}
$$

dove $A(t)$ è l'integrale di $a(t)$ nell'intervallo $[t_0, t]$.

### Problema di Cauchy di EDO lineare non omogenea

Dato un Problema di Cauchy di un'EDO lineare non omogenea del tipo:

$$
\begin{cases}
y'(t) = a(t) \space y(t) + b(t) \\
y(t_0) = y_0
\end{cases}
$$

l'unica soluzione sarà:

$$
y(t) = e^{A(t)} \left[y_0 + \int\limits_{t_0}^{t} b(t) \space e^{-A(t)} \space dt \right]
$$

### Equazioni a variabili separabili

Questo tipo di equazioni non sono lineari e quindi non vale il principio dell'omogeneità. Dunque la risoluzione di un Problema di Cauchy con equazioni a variabili separabili sarà molto diversa rispetto ai precedenti metodi risolutivi. Il sistema si presenta nel seguente modo:

$$
\begin{cases}
y'(t) = f(y(t)) \space g(t) \\
y(t_0) = y_0
\end{cases}
$$

Per prima cosa occorrerà andare a sostituire $y_0$ all'interno della funzione con argomento $y(t)$. I casi sono due:

- Se $f(y_0) = 0$ allora la soluzione sarà: $y(t) = y_0$
- Se $f(y_0) \neq 0$ la risoluzione proseguirà come segue:

Sapendo che $f(y(t)) \neq 0 \space \forall t$ allora con certezza possiamo dire che $y(t) \neq 0 \space \forall t$.
Come primo passo occorrerà isolare a destra la $g(t)$ e quindi portare a sinistra tutto ciò che dipende da $y(t)$, cioè dalla funzione incognita.
Questo metodo viene anche definito "separazione di variabili":

$$
\frac{y'(t)}{f(y(t))} = g(t)
$$

successivamente si integra a sinistra e a destra nell'intervallo $[t_0, s]$:

$$
\int\limits_{t_0}^{s} \frac{y'(t)}{f(y(t))} \space dt = 
\int\limits_{t_0}^{s} g(t) \space \space dt
$$

a destra l'integrale è immediato e quindi avremo una primitiva $G(t)$ calcolata in $[t_0, s]$, mentre a sinistra procedendo con la sostituzione $z = y(t)$, avremo che $dz = y'(t) \space dt$ e quindi l'integrale con i corrispettivi nuovi limiti sarà:

$$
\int\limits_{y_0}^{y(s)} \frac{dz}{f(z)} = F(z) \Big|_{y_0}^{y(s)}
$$

concludendo la soluzione sarà data dall'uguaglianza:

$$
F(y(s)) - F(y_0) = G(s) - G(t_0)
$$

e se $F^{-1}$ esiste si può trovare $y(s)$, che sarà quindi l'unica soluzione al Problema di Cauchy con equazioni a variabili separabili.

Esempio:

$$
\begin{cases}
y'(t) = 1 + y^2(t) \\
y(0) = 0
\end{cases}
$$

Sappiamo che $f(s) = 1 + s^2$ e $g(t) = 1$. Procedendo con la separazione di variabili e l'integrale da entrambe le parti avremo:

$$
\int\limits_{t_0 = 0}^{s} \frac{y'(t)}{1 + y^2(t)}  \space dt =
\int\limits_{t_0 = 0}^{s} 1 \space dt
$$

svolgendo l'integrale a destra e con la sostituzione $z = y(t)$, da cui $dz = y'(t) \space dt$:

$$
\int\limits_{0}^{y(s)} \frac{dz}{1 + z^2} = s
$$

$$
 arctan(z) \Big|_{0}^{y(s)} = s
$$

$$
arctan(y(s)) = s
$$

infine applicando la funzione inversa $F^{-1} (arctan) = tan$ a sinistra e a destra:

$$
y(s) = tan(s)
$$

che è la soluzione del Problema di Cauchy di un EDO a variabili separabili.

### EDO lineari non omogenee del secondo ordine

Come dice il nome, sono equazioni dfferenziali ordinare di ordine due, dove quindi compare la derivata seconda della funzione incognita. Il Problema di Cauchy associato si presenta nella forma:

$$
\begin{cases}
y''(t) + Ay'(t) + By(t) = g(t) \\
y'(t_0) = y_0 \\
y(t_0) = y_1
\end{cases}
$$

Le soluzioni dell'EDO sono infinite e dipendenti da 2 parametri. Esse sono date da:

$$
y(t) = y_0(t) + \bar y(t)
$$

dove $y_0(t)$ è la soluzione dell'EDO omogenea associata e $\bar y(t)$ la soluzione particolare.

#### Risoluzione EDO lineare omogenea associata

Come prima cosa per risolvere un'EDO lineare non omogenea del secondo ordine, bisogna passare all'EDO omogenea associata che si presenta come segue:

$$
y''_0 + Ay'_0 + By_0 = 0
$$

per poi riscriversi il Polinomio Caratteristico associato all'EDO del secondo ordine:

$$
\lambda ^2 + A \lambda + B \lambda = 0
$$

Naturalmente essendo un polinomio di secondo grado, possiamo cadere in uno dei seguenti 3 casi:

- **Caso 1** → ( $\lambda _1 \neq \lambda _2$ ) Tutte le soluzioni sono date da:
$$
y_0(t) = Ce^{\lambda _1 t} + De^{\lambda _2 t}
$$

- **Caso 2** → ( $\lambda _1 = \lambda _2$ ) Tutte le soluzioni sono date da:

$$
y_0(t) = (C + Dt) \space e^{\lambda _1 t}
$$
 
- **Caso 3** →  ( $\lambda _{1,2} = \alpha \pm i \beta$ ) Tutte le soluzioni  sono date da:

$$
y_0(t) = e^{\alpha t} \left[ C \cdot cos(\beta t) + D \cdot sen(\beta t)\right]
$$

Se l'EDO di partenza è lineare ed omogenea, allora nel caso di un Problema di Cauchy, bisogna derivare $y_0(t)$ e poi andare ad assegnare le condizioni iniziali per risolvere il sistema a due incognite $C$ e $D$, che daranno la soluzione definitiva al PDC.

#### Trovare la soluzione particolare

Nel caso si trattasse di un Problema di Cauchy con un'EDO lineare non omogenea, allora dobbiamo trovare la soluzione particolare $\bar y(t)$. In base a come si presenta la funzione a destra dell'uguale, cioè $g(t)$, la soluzione da cercare sarà dello stesso tipo e cambierà in base ad uno dei seguenti casi:

- **Se $g(t)$ è un polinomio** si dovrà cercare una soluzione del tipo:

$$
\bar y(t) = Qt + R
$$

per poi andare a fare le derivate di $\bar y(t)$ e andare a sostituire i corrispettivi valori all'interno dell'EDO iniziale così da determinare i valori di $Q$ ed $R$ tramite un sistema.

- **Se $g(t)$ è un esponenziale** si dovrà cercare una soluzione del tipo:

$$
\bar y(t) = Qe^{t}
$$

e avendo calcolato precedentemente il Polinomio Caratteristico, la soluzione particolare sarà data da:

$$
\bar y(t) = Q \cdot P(\alpha) \space e^{\alpha  t}
$$

- **Se $g(t)$ è trigonometrica** si dovrà cercare una soluzione del tipo:

$$
\bar y(t) = Q \cdot cos(t) + R \cdot sen(t)
$$

dunque calcolando le derivate e sostituendo all'interno dell'EDO troveremo un sistema in $Q$ ed $R$ da determinare.

**Osservazione**. Naturalmente ognuno di questi 3 casi è valido solo se la soluzione particolare è diversa dalla soluzione dell'EDO associata. Nel caso non lo fosse allora è necessario trovarla in una delle forme precedenti ma moltiplicandola per $t$.

[Torna su](#Indice)

