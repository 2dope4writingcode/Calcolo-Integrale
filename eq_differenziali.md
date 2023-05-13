# Equazioni Differenziali

### Indice

- [Equazione differenziale ordinaria](#Equazione-differenziale-ordinaria)
- [Problema di Cauchy](#Problema-di-Cauchy)
- [EDO lineare omogenea](#Edo-lineare-omogenea)
- [Problema di Cauchy di EDO lineare non omogenea](#Problema-di-Cauchy-di-EDO-lineare-non-omogenea)
- [Equazioni a variabili separabili](#Equazioni-a-variabili-separabili)

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

### EDO lineari del secondo ordine

TODO


