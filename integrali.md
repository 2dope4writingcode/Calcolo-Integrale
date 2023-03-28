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
min_{[x_{k}, x_{k+1}]} f(x) = \overline{S} 
$$

**L'integrale definito** nell'intervallo $[a,b]$ di $f(x)$ viene
denominato con:

$$
\int_{a}^{b} f(x) \, dx
$$

