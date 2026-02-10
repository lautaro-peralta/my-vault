13-08-2025, 09:37

Tags: [[Magnetostática]]

---

Consideremos una espira circular con  radio $R$, y por la cual circula una corriente $I$. Esta corriente entra y sale de la espira lateralmente por 2 largos conductores. Las corrientes en ellos tienen sentidos opuestos, y sus efectos magnéticos se anulan.
![[Creation_Image_1755090686924_1.png]]

---
### Dirección del campo magnético
Se determina con la regla de la mano derecha:

1. Dobla la mano como si abrazaras la espira.

2. Los dedos siguen el sentido de la corriente.

3. El pulgar extendido indica la dirección del campo en el centro de la espira.

---

### Forma del campo

En el centro de la espira, el campo es perpendicular al plano de la espira.

Las líneas de campo son cerradas y simétricas, parecidas a las de un imán en forma de disco.

Dentro de la espira, las líneas son más concentradas y prácticamente paralelas cerca del centro.

Fuera de la espira, las líneas se expanden y se curvan volviendo a cerrarse.

---

### Módulo del campo en el centro

La intensidad del campo en el centro de la espira se calcula con:

$$B = \frac{\mu_0 \, I}{2R}$$

Donde:

 $B$ → intensidad del campo magnético (teslas, $T$)

 $\mu_0$ → permeabilidad magnética del vacío 

Si la espira tiene $N$ vueltas, se multiplica por :

$$B = \frac{\mu_0 \, N \, I}{2R}$$


### Distribución fuera del centro

El campo no es uniforme en todo el espacio.
En el **eje** de la espira, la simetría es total: todas las contribuciones de cada elemento de corriente suman en la misma dirección. A lo largo del eje, el campo disminuye con la distancia según:


$$B(x) = \frac{\mu_0 I R^2}{2 (R^2 + x^2)^{3/2}}$$
El campo magnético en puntos no situados sobre el eje de la espira puede determinarse por el mismo método, pero los cálculos resultan muy complejos. 

En un **punto fuera del eje**, la simetría se rompe:
- La dirección del vector (desde cada elemento de corriente al punto P) cambia.
- El ángulo que aparece en la **ley de Biot–Savart** varía a lo largo de la espira.

No obstante, cuando las distancias a la espira son grandes comparadas con su radio, las ecuaciones toman una forma sencilla cuando se utilizan coordenadas polares $(r, \theta)$. Similar a como lo hacíamos para un dipolo eléctrico. 

Lejos de la espira, su campo "se ve" como el de un dipolo con momento $m = I π R^2$. Entonces:
$$\boxed{
\begin{aligned}
B_r(r,\theta) &= \frac{\mu_0}{4\pi}\,\frac{2\,m\,\cos\theta}{r^3},\\[4pt]
B_\theta(r,\theta) &= \frac{\mu_0}{4\pi}\,\frac{m\,\sin\theta}{r^3},\\[4pt]
B_\phi &= 0.
\end{aligned}
}$$
Cerca o a distancias comparables a $R$: la aproximación de dipolo ya no alcanza. El cálculo exacto con la [[Ley de Biot–Savart]] lleva a integrales elípticas (no elementales).




---
## Referencias