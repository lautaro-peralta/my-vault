
---
Las **integrales múltiples** generalizan el concepto de la integral definida de una variable a funciones de varias variables.  
Mientras que en una dimensión una integral representa el área bajo una curva, en dos o más dimensiones las integrales múltiples permiten calcular áreas, volúmenes, masas, momentos de inercia y otras magnitudes físicas o geométricas.

---
## Idea general

Sea $f: \mathbb{R}^n \to \mathbb{R}$ una función continua definida sobre una región acotada $D \subset \mathbb{R}^n$. La **integral múltiple de $f$ sobre $D$** se escribe como:
$$\int_{D} f(\mathbf{x}) \, d\mathbf{x}$$
donde:

- $n = 2$: se habla de [[Integrales dobles]], $\iint_{D} f(x,y)\, dx\,dy.$
- $n = 3$: se habla de [[Integrales triples]], $∭_{D}f(x,y,z) dx dy dz$.

En general: se habla de **integral múltiple de orden $n$**.

## Significado geométrico

- En $n=2$: representa el volumen bajo la superficie $z=f(x,y)$ y sobre la región $D$ del plano.
- En $n=3$: representa el “hipervolumen” bajo la hipersuperficie en $\mathbb{R}^3$.
- Más allá de la interpretación geométrica, las integrales múltiples sirven como herramienta para acumular valores de una función sobre un dominio multidimensional.
## Propiedades básicas

Las integrales múltiples heredan las propiedades de la integral definida en una variable.

**Linealidad**:
$$\int_{D} \big( af + bg \big) = a \int_{D} f + b \int_{D} g$$

**Aditividad** respecto de la región:  
>Si $D = D_1 \cup D_2$ y son disjuntos,
$$\int_{D} f = \int_{D_1} f + \int_{D_2} f$$

**Positividad**:  
>Si $f(x) \geq 0$ en $D$, entonces $\int_D f \geq 0$.

## Evaluación práctica

En la práctica, las integrales múltiples se calculan como **integrales iteradas**, es decir, resolviendo una integral a la vez:
$$\iint_{D} f(x,y)\, dx\,dy = \int_{a}^{b} \left( \int_{g_1(x)}^{g_2(x)} f(x,y)\, dy \right) dx$$

Este procedimiento se extiende a tres o más variables.

---
## Referencias