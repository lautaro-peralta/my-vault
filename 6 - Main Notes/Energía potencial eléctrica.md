17-08-2025, 12:22

Tags: [[Electrostática]]

---

## Energía Potencial Eléctrica

Sabemos que el trabajo realizado para separar un cuerpo de la superficie de la Tierra, aumenta la energía potencial gravitatoria del sistema cuerpo-Tierra; además, también sabemos que cuando las dos partes se juntan, esta energía potencial gravitatoria se libera convirtiéndose en otras formas de energía. Es decir, el trabajo realizado al separar dos partes de un sistema que se atraen mutuamente, puede ser recuperado. Exactamente las mismas ideas pueden aplicarse a cualquier sistema compuesto de cuerpos que se atraen o rechazan entre sí, como ocurre en el caso de las cargas eléctricas. Para separar una carga positiva de una negativa hay que realizar un cierto trabajo, y este trabajo puede recuperarse cuando se permite a las dos cargas aproximarse entre sí. Para aproximar dos cargas del mismo signo hay que realizar un cierto trabajo, y este trabajo puede recuperarse cuando se permite a dichas cargas separarse.

En síntesis, cuando dos cargas distintas se separan, o cuando dos cargas iguales se aproximan, aumenta la energía potencial del sistema y el cambio de energía potencial eléctrica se define como el trabajo realizado para efectuar la separación o la aproximación.

---

Generalizando, podemos mover un cuerpo cargado en el campo creado por un número cualquiera de cargas. Sin especificar la posición, magnitud o signo de estas cargas, sea $E$ el campo eléctrico creado por ellas en un punto cualquiera. La fuerza sobre un pequeño cuerpo de prueba que posee una carga positiva $q_{o}$ es entonces $q_{o} E$. Para mantener el cuerpo en reposo o para desplazarlo sin rozamiento o aceleración, se requiere una fuerza opuesta $F=-q_{o}E$. El trabajo necesario para dar al cuerpo de prueba un desplazamiento $ds$ se define como $dW=F~cos~\theta$ ds, siendo $\theta$ el ángulo formado por $F$ y $ds$. Dado que $F=-q_{o}E,$ es:
$$dW=-q_{o}E~cos~\theta~ds$$
donde $\theta$ es ahora el ángulo formado por $E$ y $ds$. Para un desplazamiento finito desde el punto $a$ al punto $b$, el trabajo necesario es:
$$W_{a\rightarrow b}=-q_{0}\int_{a}^{b}E~cos~\theta~ds \text{ (39)}$$

Esta es la expresión general del trabajo necesario para desplazar la carga de prueba, desde un punto cualquiera $a$ hasta otro punto cualquiera $b$, en un campo eléctrico.

---
![[Screenshot_2025-08-17-12-34-19-732_com.google.android.apps.docs-edit.jpg]]

Consideremos ahora el caso especial del campo creado por una sola carga puntual fija $q$ como la de la figura 37. En este caso sencillo:
	$ds~cos~\theta=dr$
	$E=k\frac{q}{r^{2}}$
	$W_{a\rightarrow b}=-k~qq_{0}\int_{r_{a}}^{r_{b}}\frac{dr}{r^{2}}$
$$W_{a\rightarrow b}=k~qq_{0}(\frac{1}{r_{b}}-\frac{1}{r_{a}})=k\frac{qq_{0}}{r_{b}}-k\frac{qq_{0}}{r_{a}} \text{ (40)}$$

Como el resultado depende solamente de las distancias inicial y final de los puntos $a$ y $b$ a la carga $q$, se deduce que el trabajo es el mismo para cualquier trayectoria que pase por estos puntos (o entre un par cualquiera de puntos situados a las distancias $r_{a}$ y $r_{b}$ de la carga $q$). Además, si la carga de prueba vuelve del punto $b$ al punto $a$ a lo largo de cualquier trayectoria, el trabajo realizado para moverla desde $a$ hasta $b$ puede recuperarse totalmente. Por consiguiente, la fuerza eléctrica es una fuerza conservativa y está justificado considerar el trabajo realizado sobre la carga de prueba, como un incremento de su energía potencial.

En el segundo miembro de la ecuación (40), el primer y segundo término representan, respectivamente, la energía potencial de la carga de prueba a las distancias $r_{b}$ y $r_{a}$ de la carga $q$.
Dado que las distancias $r_{a}$ y $r_{b}$ son arbitrarias, la energía potencial de una carga puntual $q_{o}$ a una distancia cualquiera $r$ de una carga puntual $q$ es:
$$EP=k\frac{qq_{0}}{r} \text{ (41)}$$
---


![[Screenshot_2025-08-17-12-36-09-856_com.google.android.apps.docs-edit.jpg]]


Supongamos ahora que el campo es creado por una distribución arbitraria de cargas puntuales $q_{1}$, $q_{2}$,... ubicadas a las distancias $r_{1}$, $r_{2}$,... de una carga de prueba $q_{o}$ colocada en el punto $a$. Puesto que la energía es una magnitud escalar, la energía potencial de la carga de prueba $q_{o}$ es la suma algebraica de sus energías potenciales respecto a todas las otras cargas:
$$EP_{a}=k~q_{0}\sum\frac{q}{r} \text{ (42)}$$

En un segundo punto $b$, la energía está dada por la misma expresión, excepto que $r_{1}$, $r_{2}$,... representan ahora las distancias de las cargas respectivas al punto $b$. El trabajo necesario para desplazar la carga de prueba desde $a$ hasta $b$ a lo largo de cualquier trayectoria, es igual a la diferencia de sus energías potenciales en $b$ y en $a$. Por consiguiente:
$$W_{a\rightarrow b}=-\int_{a}^{b}q_{0}E~cos~\theta~ds=EP_{b}-EP_{a} \text{ (43)}$$
Por lo tanto, el trabajo puede calcularse hallando el valor de la integral en el caso de que $E$ sea conocido en todos los puntos de la trayectoria, o bien calculando las energías potenciales solamente en los puntos extremos y restando una de otra.

De la ecuación (42) deducimos que, el nivel de referencia de la energía potencial eléctrica en el cual la misma es nula, es aquel para el cual todas las distancias $r_{1}$, $r_{2}$,... son infinitas. Es decir, la energía potencial de la carga de prueba es nula cuando está muy alejada de todas las cargas que crean el campo. Si la carga de prueba se trae desde el infinito a un punto cualquiera del campo, el trabajo realizado contra la fuerza ejercida sobre ella por el campo es igual a la energía potencial en el punto. Si suponemos el punto $a$ en el infinito y hacemos $EP_{a}=0$, la ecuación (43) se convierte en:
$$EP_{b}=-\int_{\infty}^{b}q_{0}E~cos~\theta~ds$$
El punto $b$ puede ser un punto cualquiera del campo. Podemos por lo tanto suprimir el subíndice y los límites de integración:
$$EP=-\int q_{0}E~cos~\theta~ds \text{ (44)}$$
donde se entiende que es una integral curvilínea desde el infinito al punto en cuestión. Físicamente, la energía potencial de una carga de prueba en cualquier punto de un campo eléctrico, es igual al trabajo realizado contra la fuerza ejercida sobre ella por el campo, cuando se traslada la carga desde el infinito al punto.

La ecuación (42) da la energía potencial asociada con la presencia de la carga de prueba $q_{0}$ en el campo $E$ producido por $q_{1}$ $q_{2}$, $q_{3},...$. Pero también interviene una energía potencial en el acto de reunir estas cargas. Si en un principio las mismas están todas separadas unas de otras por distancias infinitas y luego las juntamos de modo que la distancia entre $q_{i}$ y $q_{j}$ sea $r_{ij}$, la energía potencial total $EP_{t}$ es la suma de las energías potenciales de interacción de cada par de cargas. Esto se puede escribir como
$$EP_{t}=k\sum_{i<j}\frac{q_{i}q_{j}}{r_{ij}}$$
Esta suma se extiende a todos los pares de cargas. No se hace que $i=j$ (porque eso sería una interacción de una carga consigo misma) y se incluyen sólo términos con $i<j$ para asegurar que se cuente cada par sólo una vez. Así, para tener en cuenta la interacción entre $q_{3}$ y $q_{4}$ se incluye un término con $i=3$ y $j=4$, pero no un término con $i=4$ y $j=3$.

---
## Referencias
