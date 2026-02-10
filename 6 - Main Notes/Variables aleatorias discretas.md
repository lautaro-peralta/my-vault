23-09-2025, 18:44

Tags: [[Variables aleatorias y sus distribuciones]]

---

Una variable es discreta cuando el conjunto de valores posibles que puede asumir (rango o recorrido de la variables: $R_{x}$) es un conjunto finito o infinito numerable.

---
### Distribuciones de probabilidad

teniendo en cuenta que los valores que puede asumir la variable aleatoria son resultados de un experimento aleatorio, se le puede asignar una probabilidad a cada valor posible. surge entonces la distribución de probabilidad de una variable.

>***Una distribución de probabilidad es una función que enumera todos los valores posibles que pueda asumir una variable aleatoria, junto con sus probabilidades.***

La distribución de probabilidad describe el comportamiento de la variable en una población. esto significa que las probabilidades se pueden interpretar igual que las frecuencias relativas pero en vez de referirse a una muestra, se refieren a una población.

La función de distribución acumulada $F(x)$ se define como:
$$F(x) = P(X \leq x) = \sum_{i \leq x} P(X = i)$$

### Gráfica de la distribución de la probabilidad

Se utiliza el mismo gráfico que para la distribución de frecuencias de este tipo de variables; el gráfico de bastones.

![[Pasted image 20250923190804.png]]

Como ejemplo se interpretan los valores correspondientes a X=4:
- *Si se elige un día al azar, la chance de que haya 4 clientes insatisfechos es 0,127.*
- *Si se elige un día al azar, la chance de que haya a lo sumo 4 clientes insatisfechos es 0,731*
O también:
- *En el 12,7% de los días (de un período muy largo de días) hubieron 4 clientes insatisfechos.*
- *En el 73,1% de los días (de un período muy largo de días) hubieron a lo sumo 4 clientes insatisfechos.*

A partir de lo estudiado en probabilidad, podemos deducir las sig. propiedades:
- $P_i \geq 0, \, \forall i$
- $\sum_{i \in R_x} P_i = 1$ (condición de cierre).

La distribución de probabilidad debe contener todos los valores posibles que puede tomar una variable aleatoria. Por lo tanto, la suma de las probabilidades debe ser igual a 1.

---
### Parámetros

Son las medidas que resumen la información que brinda una distribución de probabilidad así como los estadísticos resumen información que brinda una distribución de frecuencias.

**Esperanza matemática**

La esperanza matemática es el valor promedio de una variable aleatoria $X$. Se la nota como $E(X)$ o $\mu$.
La fórmula para el cálculo de la esperanza matemática de una variable aleatoria discreta $X$ está dada por: 
$$\mu = \mathrm{E}(X) = \sum_{i=1}^{\infty} X_i \cdot P_i$$
Al igual que para las probabilidades, la esperanza se interpreta como un promedio pero no de un conjunto finito de datos si no de una población.

**Varianza poblacional**

Medida de dispersión, se la nota como $V(X)$ o $\sigma^2$. La fórmula para el calculo de la varianza es:

$$\sigma^2 = V(X) = \sum_i (x_i - \mu)^2 \, p_i$$
**Desviación estándar**

Es la raíz cuadrada positiva de la varianza. Su ventaja es que trabaja con las mismas unidades en las que está expresada la variable.
$$\sigma = \sqrt{V(X)}$$
Las interpretaciones de estos parámetros son las mismas que se utilizan en Estadística Descriptiva pero teniendo en cuenta que, al ser parámetros, hacen referencia a la población.

---
## Referencias
[[Variables aleatorias discretas.pdf]]