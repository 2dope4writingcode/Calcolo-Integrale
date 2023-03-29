# Integrali

### Indice
- [Integrazione secondo Riemann](#Integrazione-secondo-Riemann)

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

Di seguito una tabella che elenca le principali derivate immediate e i corrispondenti integrali immediati:

<center>
<table>
<tr><th>Derivate immediate </th><th>Integrali immediati</th></tr>
<tr><td>

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

</td><td>


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

</td></tr> </table>
</center>






