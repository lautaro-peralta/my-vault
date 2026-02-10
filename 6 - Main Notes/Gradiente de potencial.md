10-09-2025, 09:43

Tags: [[Electrostática]]

---
La expresión general de la diferencia de potencial entre dos puntos es:

$$
\Delta V = - \int_A^B \vec{E} \cdot d\vec{s}
$$

Cuando la distancia que los separa es infinitesimal, la diferencia de potencial se convierte en $dV$, resultando:

$$
dV = - \vec{E} \cdot d\vec{s}
$$

Esta ecuación puede escribirse:

$$
E_s = - \frac{dV}{ds}
$$

donde $E_s$ es la componente del campo eléctrico en la dirección de $ds$ (figura 41).  %%  %%
La razón $dV/ds$, que es la variación del potencial con la distancia en la dirección $ds$, se denomina **gradiente de potencial**.

Por lo tanto, llegamos al siguiente importante resultado:  
La componente del campo eléctrico en una dirección cualquiera es igual al gradiente de potencial en dicha dirección, cambiado de signo.  

En particular, si la dirección $ds$ es la misma que la del campo eléctrico, entonces el campo eléctrico es igual al gradiente de potencial en la dirección del campo, cambiado de signo.

Las unidades de campo eléctrico y de gradiente de potencial son equivalentes:

$$
1 \, \text{V/m} = 1 \, \text{N/C}
$$

El campo que rodea a un conjunto de cargas cualesquiera es tridimensional.  
En general, el potencial de un punto cualquiera es cierta función de las coordenadas $x, y, z$ del punto.  

Si para la ecuación anterior consideramos las componentes de $d\vec{s}$ en las direcciones de los ejes coordenados, los tres gradientes de potencial dan entonces las tres componentes rectangulares de $\vec{E}$:

$$
E_x = -\frac{\partial V}{\partial x}, \quad
E_y = -\frac{\partial V}{\partial y}, \quad
E_z = -\frac{\partial V}{\partial z}
$$

En rigor, estas expresiones deben escribirse como derivadas parciales.  

El gradiente de una función escalar de $x, y, z$, tal como el potencial $V$, se define como un vector cuyas componentes son las derivadas parciales de la función:

$$
\nabla V = 
\frac{\partial V}{\partial x} \, \hat{i} +
\frac{\partial V}{\partial y} \, \hat{j} +
\frac{\partial V}{\partial z} \, \hat{k}
$$

Se deduce entonces que:

$$
\vec{E} = - \nabla V
$$

---

### Ejemplo: Campo eléctrico en el eje de un anillo cargado

Para ilustrar la simplificación que introduce el uso de gradientes de potencial, calcularemos el campo eléctrico sobre el eje de un anillo cargado (figura 42), problema que ya se resolvió anteriormente (página 24).

Aunque la carga total $q$ sobre el anillo está distribuida en toda su longitud, cada porción de carga se halla a la misma distancia $\sqrt{a^2 + x^2}$ de un punto $P$ del eje.  
Por consiguiente, el potencial en $P$ es:

$$
V = \frac{1}{4 \pi \varepsilon_0} \frac{q}{\sqrt{a^2 + x^2}}
$$

Por razón de simetría, el campo en un punto del eje tiene la dirección de éste, de modo que el gradiente de potencial, cambiado de signo, dará el campo en dicho punto:

$$
E_x = - \frac{\partial V}{\partial x}
= - \frac{1}{4 \pi \varepsilon_0} \frac{q \, (-x)}{(a^2 + x^2)^{3/2}}
= \frac{1}{4 \pi \varepsilon_0} \frac{q \, x}{(a^2 + x^2)^{3/2}}
$$

Este resultado coincide con el que obtuvimos anteriormente, y los cálculos son evidentemente más sencillos.

---

### Ejemplo: Campo eléctrico de un dipolo

Consideremos ahora el campo eléctrico creado por un dipolo, deducido a partir del potencial (figura 43).  
Así comprobaremos las expresiones $E_r$ y $E_\theta$ que se dieron anteriormente sin demostración (página 21).

El potencial en $P$ es:

$$
V = \frac{1}{4 \pi \varepsilon_0} \left( \frac{q}{r_1} - \frac{q}{r_2} \right)
$$

En dirección radial, $ds = dr$.  
En dirección tangencial, $ds$ es perpendicular a $r$, luego es $r \, d\theta$.

Aplicando el gradiente de potencial, se obtienen:

E_r = - \frac{\partial V}{\partial r}, \quad
E_\theta = - \frac{1}{r} \frac{\partial V}{\




---
## Referencias