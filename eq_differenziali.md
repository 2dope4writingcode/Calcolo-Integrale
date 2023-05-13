# Equazioni Differenziali

### Indice

### Equazione differenziale ordinaria

##### Definizione EDO

**Un'equazione differenziale ordinaria (EDO)** è un'equazione la cui **incognita** è una funzione e almeno uno dei termini che compaiono è una **derivata** qualsiasi della funzione stessa.
Il grado più alto della derivata che compare indica **l'ordine** dell'EDO.

### Problema di Cauchy

Viene definito Problema di Cauchy un sistema matematico da risolvere con all'interno una qualsiasi equazione differenziale di ordine N e delle condizioni iniziali legate ad essa. La soluzione al PDC è sempre solo una. Di seguito un esempio:

$$
(s) = \begin{cases}
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

TODO

### EDO lineari del secondo ordine

TODO


