17-08-2025, 12:43

Tags: [[Electrostática]]

---

La diferencia de potencial entre dos puntos de un campo electrostático, es igual a la diferencia entre los potenciales de dichos puntos. Si dividimos por $q_{0}$ ambos miembros de la ecuación (43), se obtiene:
$$\frac{EP_{b}}{q_{0}}-\frac{EP_{a}}{q_{0}}=-\int_{a}^{b}E~cos~\theta~ds$$
de donde:
$$V_{b}-V_{a}=-\int_{a}^{b}E~cos~\theta~ds \text{ (51)}$$
O sea que, la diferencia de potencial entre dos puntos es igual al trabajo realizado, por unidad de carga, contra las fuerzas eléctricas, cuando se mueve una carga desde un punto al otro.

Para interpretar la ecuación anterior, recuérdese que $E$ es la fuerza eléctrica, por unidad de carga, sobre una carga de prueba. La integral puede calcularse a lo largo de cualquier trayectoria comprendida entre $a$ y $b$.

Se dice que el punto $b$ está a un potencial superior al de $a$, si se realiza trabajo contra las fuerzas eléctricas para mover una carga positiva desde $a$ hasta $b$ (o si la energía potencial de una carga positiva es mayor en $b$ que en $a$). El potencial en un punto puede considerarse como la diferencia de potencial entre dicho punto y otro a distancia infinita, donde el potencial se supone arbitrariamente cero.

El concepto de diferencia de potencial es extraordinariamente importante, tanto para la electrostática como para los circuitos eléctricos. Por ejemplo, la diferencia de potencial entre los bornes de una batería de automóvil es de $12~V$ (voltios), designándose el borne de potencial más elevado por el signo $+$ y el de menor potencial por el signo $-$. El borne $+$ está cargado positivamente y el borne $-$ negativamente. Existe por lo tanto un campo eléctrico en el espacio que rodea los bornes. Decir que la diferencia de potencial entre los bornes es $12~V$, significa simplemente que si tuviéramos que mover un cuerpo cargado positivamente desde el borne negativo al positivo (por ejemplo, transportar una esfera metálica pequeña, cargada positivamente y sujeta por un hilo aislador, de un punto al otro), el trabajo realizado contra las fuerzas eléctricas del campo existente entre los dos bornes sería de $12~J$ (julios) por culombio de carga transportada.
La diferencia de potencial entre dos puntos $a$ y $b$ se expresa por $V_{ab}$, esto es:
$$V_{ab}=V_{a}-V_{b}$$
Si esta diferencia de potencial es una cantidad positiva, el punto $a$ está a un potencial más alto que $b$. Inversamente, si la diferencia es negativa, el punto $b$ está a un potencial más alto que $a$. Por consiguiente, puesto que $V_{ab}=V_{a}-V_{b}$ y $V_{ba}=V_{b}-V_{a}$, se deduce que: $V_{ab}=-V_{ba}$
En la ecuación (51), si la trayectoria de integración se cierra sobre sí misma, de modo que los extremos coincidan, la diferencia de potencial entre ellos es cero y la integral será por lo tanto nula:
$$\oint E~cos~\theta~ds=0 \text{ (52)}$$

Utilizando la notación vectorial, las ecuaciones (47), (51) y (52) se escriben:
$$V=-\int\vec{E}.\vec{ds}$$
$$V_{b}-V_{a}=-\int_{a}^{b}\vec{E}.\vec{ds}$$
$$\oint\vec{E}.\vec{ds}=0$$
Sabemos que, por simetría, la intensidad del campo eléctrico $E$ entre dos láminas paralelas muy próximas y con cargas iguales y de signos opuestos, es uniforme y perpendicular a las láminas. Nos preguntamos, ¿cuál es la diferencia de potencial entre ellas?

![[Screenshot_2025-08-17-12-48-59-014_com.google.android.apps.docs-edit.jpg]]

Adoptemos un eje $x$ paralelo al campo (figura 39) y consideremos dos puntos $a$ y $b$ en las caras interiores de las láminas. Se tiene:
$$V_{ab}=-V_{ba}=\int_{a}^{b}E~cos~\theta~ds$$
luego, $E=cte.$ ; $cos~\theta=1$; $ds=dx$;
$$V_{ab}=E\int_{x_{a}}^{x_{b}}dx=E(x_{b}-x_{a})=E~d$$
$$E=\frac{V_{ab}}{d} \text{ (53)}$$
La intensidad del campo eléctrico es igual, por consiguiente, a la diferencia de potencial entre las láminas, dividida por la distancia que las separa. Esta ecuación es más útil para expresar la intensidad del campo eléctrico entre láminas paralelas que la ecuación $E=\sigma/\epsilon_{0}$, puesto que la diferencia de potencial $V_{ab}$ puede determinarse experimentalmente de forma más sencilla que la carga por unidad de área.

---
## Referencias
[[Electricidad y Magnetismo.pdf]]