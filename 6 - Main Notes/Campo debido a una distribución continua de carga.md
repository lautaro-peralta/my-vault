15-08-2025, 09:15

Tags: [[Electrostática]]

---
### Hilo conductor cargado

Sea un extenso hilo (con radio lo suficientemente pequeño como para considerarse una línea geométrica) con una carga positiva distribuida uniformemente en todo su largo. Para calcular la magnitud, dirección y sentido del campo eléctrico en un punto $P$, situado a una distancia $r$ del hilo, dividimos el mismo en pequeños segmentos de longitud $dx$ y carga $dq$.  El Campo resultante se tiene mediante la suma vectorial de todos los campos creados por las cargas puntuales. En el punto P, el elemento $dq$ crea un Campo de magnitud: $$dE=k \frac {dq} {s^2}$$
Como ningun otro Campo tiene la misma dirección que $dE$, no podemos calcular la intensidad resultante mediante integración. Trabajemos entonces, con las componentes $x$ e $y$ de $dE$, que sí pueden integrarse separadamente:

$$E_x = \int dE_x= \int dE \sin(\theta)$$
$$E_y = \int dE_y= \int dE \cos(\theta)$$
Representamos por $\lambda$ a la carga por unidad de longitud del hilo. La carga del elemento de longitud $dx$ es: $$dq = \lambda dx$$
De donde: $$dE=k \lambda \frac {dx}{s^2}$$
Sustituyendo $x=r \tan(\theta)$ ; $dx=r \sec^2(\theta)d \theta$ ; $s = r \sec (\theta)$:
$$
E_x = k \frac {\lambda}{r} \int sen(\theta)d\theta
$$
$$

E_y = k \frac {\lambda}{r} \int cos(\theta)d\theta$$
Si el hilo es infinitamente largo, los limites de integracion varían entre $-\frac {\pi}{2}$ y $+ \frac {\pi}{2}$ obteniéndose:$$E_x = 0$$$$E_y = \frac{2k\lambda}{r}$$ 
siempre y cuando la componente $E_y$ sea la perpendicular al hilo y la $E_x$ sea la paralela al hilo. Esto simplemente depende de la configuración de los ejes de coordenadas que se elija al inicio del problema. El resultado físico es el mismo: el campo eléctrico es perpendicular al hilo e inversamente proporcional a $r$, y su magnitud es $$E=\frac{2k \lambda}{r}$$
### Cálculo del campo mediante Gauss

Consideremos una [[Superficie Gaussiana]] en forma de cilindro recto de radio $r$ y longitud $b$, coaxial (mismo eje) con el hilo conductor. Por simetría:

- La dirección del campo es normal al conductor y a la superficie cilíndrica.
- El Campo tiene la misma intensidad en todos los puntos de dicha superficie.

El flujo eléctrico total que atraviesa el cilindro gaussiano hacia afuera es $E(2\pi rb)$ ya que en las bases del mismo, el flujo es nulo.
Por lo tanto, y en virtud de la [[Ley de Gauss]]: $\epsilon_0 E(2\pi r b)= \lambda b$ (recordemos que $\lambda$ es la carga por unidad de longitud) . Luego:
$$E= \frac {1}{2 \pi \epsilon_0} \frac {\lambda}{r} = 2k \frac {\lambda}{r}$$

El resultado es correcto: observemos la simplificación que nos proporciona resolverlo por Gauss.

---
### Anillo circular conductor cargado

Consideremos ahora un anillo circular situado en el plano $xz$, con su centro en el origen, con radio $a$ y cargado de manera uniforme con una carga positiva $q$. Se desea calcular la intensidad del campo en un punto $P$ situado sobre el eje del anillo, a una distancia $b$ del centro. Tomamos un pequeño elemento cuya carga es $dq$, que crea un Campo en $P$ cuya magnitud es $dE = k \frac {dq}{r^2}$. Observamos que si consideramos todos los elementos de un anillo, las componentes perpendiculares al eje se compensan entre sí. En consecuencia, el campo resultante en P es la suma de las componentes $dE \cos(\theta)$: $$E=\int dE \cos(\theta)= k \frac {\cos(\theta)} {r^2} \int dq $$
Ya que la suma de las pequeñas cargas $dq$ da como resultado $q$, y como $\cos(\theta)=\frac {b} {r}$: $$ E=k \frac {q\cos(\theta)} {r^2}=kq\frac {b} {(a^2 + b^2)^{3/2}}$$
En el centro del anillo, $E=0$ por razones de simetría. Para distancias tales que $a$ sea despreciable con respecto a $b$, entonces: $$E=k \frac {q} {b^2}$$
Es decir, a distancias suficientemente grandes, el campo es el mismo que el creado por una carga puntual $q$

---
## Referencias