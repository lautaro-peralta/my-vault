11-08-2025, 19:02

Tags: [[Electrostática]]

---

La **Ley de Gauss** es una de las cuatro ecuaciones fundamentales del electromagnetismo, formulada por Carl Friedrich Gauss. Establece una relación entre el flujo del campo eléctrico a través de una superficie cerrada y la carga eléctrica encerrada dentro de esa superficie.

### **Enunciado matemático:**
$$
\oint_S \vec{E} \cdot d\vec{A} = \frac{Q_{\text{enc}}}{\varepsilon_0}
$$
Donde:
- $\oint_S$: Integral sobre una superficie cerrada (superficie gaussiana).
- $\vec{E}$: Campo eléctrico.
- $d\vec{A}$: Vector diferencial de área (perpendicular a la superficie).
- $Q_{\text{enc}}$: Carga total encerrada dentro de la superficie.
- $\varepsilon_0$: Permitividad del vacío ($\approx 8.85 \times 10^{-12} \, \text{C}^2/\text{N}\cdot\text{m}^2$).

### **¿Qué establece?**
La Ley de Gauss dice que:
> *"El flujo eléctrico neto a través de cualquier superficie cerrada es proporcional a la carga eléctrica total encerrada dentro de esa superficie."*

### **¿Cómo funciona?**
1. **Flujo eléctrico ($\Phi_E$)**: Mide cuánto campo eléctrico "atraviesa" una superficie.
   - Si el campo es perpendicular a la superficie, el flujo es máximo.
   - Si es paralelo, el flujo es cero.

2. **Superficie gaussiana**: Una superficie imaginaria que se elige de forma simétrica para simplificar el cálculo (ej: esfera, cilindro, plano infinito).

3. **Aplicaciones**:
   - Permite calcular campos eléctricos en configuraciones altamente simétricas (esferas, planos, cilindros).
   - Es útil para demostrar que el campo dentro de un conductor en equilibrio electrostático es cero.

### **Ejemplo: Campo de una carga puntual**
Si elegimos una esfera de radio $r$ alrededor de una carga $Q$, por simetría:
- El campo $\vec{E}$ es radial y constante en magnitud sobre la superficie.
- El flujo es: $\Phi_E = E \cdot (4\pi r^2) = \frac{Q}{\varepsilon_0}$.
- Despejando $E$: $E = \frac{Q}{4\pi \varepsilon_0 r^2}$ (Ley de Coulomb).

### **Limitaciones**
- Solo es útil cuando hay simetría (esférica, cilíndrica o plana).
- No proporciona información directa sobre el campo si no se conoce su dirección de antemano.

### **Relación con otras leyes**
- Es equivalente a la [[Ley de Coulomb]] en electrostática.
- Forma parte de las **Ecuaciones de Maxwell**, que describen completamente los fenómenos electromagnéticos.

---
## Referencias

