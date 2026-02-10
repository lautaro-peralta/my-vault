---
Comisión: 2k02
Profesor: Sandra Silvester, Del Greco
Año/Semestre: "2025"
Aula: "202"
---
# Lecturas

### 10 de agosto de 2025 — Electrostática (c)

### Campo debido a una distribución continua de carga

Se hace el cálculo por integración de las componentes de:

$dE = k dq / s^2$

$E_x = \int_\ dE_x = \int_\ dE_x * sin(\theta)$ ; $E_y = \int_\ dE_y = \int_\ dE_y *cos(\theta)$

  

### Líneas de Campo Eléctrico

Las **líneas de campo eléctrico** son una representación gráfica del campo eléctrico generado por una o más cargas.

- **Propiedades**:
    - **Dirección**: Las líneas salen de cargas positivas y entran en cargas negativas.
    - **Densidad**: Cuanto más juntas estén las líneas, más intenso es el campo eléctrico en esa región.
    - **No se cruzan**: En un punto dado, el campo eléctrico tiene una única dirección.
    - **Trayectoria de una carga de prueba positiva**: Una carga positiva seguiría la dirección de las líneas de campo si se libera.
- **Ejemplo**:
    - Para una **carga puntual positiva**, las líneas son radiales y salen de la carga.
    - Para un **dipolo eléctrico**, las líneas van de la carga positiva a la negativa.

---

### Momento de Torsión (Torque) en un Dipolo Eléctrico

Un **dipolo eléctrico** consiste en dos cargas iguales y opuestas ($+q$) y ($-q$) separadas por una distancia \(d\).

- **Momento dipolar eléctrico (\(\vec{p}\))**:
    
    \[  
    \vec{p} = q \cdot \vec{d}  
    \]
    
    donde \(\vec{d}\) es el vector que va de \(-q\) a \(+q\).
    
- **Torque (\(\vec{\tau}\)) en un campo eléctrico externo (\(\vec{E}\))**:
    
    Cuando un dipolo se coloca en un campo eléctrico, las fuerzas sobre las cargas generan un torque que tiende a alinear \(\vec{p}\) con \(\vec{E}\):
    
    \[  
    \vec{\tau} = \vec{p} \times \vec{E} = pE \sin\theta \quad (\text{dirección perpendicular al plano de } \vec{p} \text{ y } \vec{E})  
    \]
    
    donde \(\theta\) es el ángulo entre \(\vec{p}\) y \(\vec{E}\).
    
- **Energía potencial (\(U\)) del dipolo**:
    
    \[  
    U = -\vec{p} \cdot \vec{E} = -pE \cos\theta  
    \]
    
    - Mínima cuando \(\vec{p}\) y \(\vec{E}\) están alineados (\(\theta = 0°\)).
    - Máxima cuando están antiparalelos (\(\theta = 180°\)).

---

### **3. Flujo Eléctrico (\(\Phi_E\))**

El **flujo eléctrico** mide el número de líneas de campo que atraviesan una superficie.

- **Definición matemática**:
    
    \[  
    \Phi_E = \int_S \vec{E} \cdot d\vec{A} = \int_S E \cos\theta \, dA  
    \]
    
    donde:
    
    - \(\vec{E}\): Campo eléctrico.
    - \(d\vec{A}\): Vector diferencial de área (perpendicular a la superficie).
    - \(\theta\): Ángulo entre \(\vec{E}\) y \(d\vec{A}\).
- **Caso especial (superficie cerrada, Ley de Gauss)**:
    
    \[  
    \Phi_E = \oint_S \vec{E} \cdot d\vec{A} = \frac{Q_{\text{int}}}{\epsilon_0}  
    \]
    
    - \(Q_{\text{int}}\): Carga neta encerrada.
    - \(\epsilon_0\): Permitividad del vacío.
- **Interpretación**:
    - Si \(\Phi_E > 0\): Más líneas salen que entran (carga neta positiva dentro).
    - Si \(\Phi_E < 0\): Más líneas entran que salen (carga neta negativa dentro).

---

### **Resumen de Fórmulas Clave**

|Concepto|Fórmula|
|---|---|
|**Momento dipolar**|\(\vec{p} = q \vec{d}\)|
|**Torque en dipolo**|\(\vec{\tau} = \vec{p} \times \vec{E}\)|
|**Energía potencial**|\(U = -\vec{p} \cdot \vec{E}\)|
|**Flujo eléctrico**|\(\Phi_E = \int_S \vec{E} \cdot d\vec{A}\)|
|**Ley de Gauss**|\(\oint_S \vec{E} \cdot d\vec{A} = Q_{\text{int}} / \epsilon_0\)|

Espero que esta explicación te ayude. ¿Necesitas algún ejemplo adicional o aclaración? 😊

### 8 de agosto de 2025 — Electrostática (b)

### Carga de un metal por inducción

La carga de un metal por inducción es un proceso donde un objeto metálico neutro adquiere carga eléctrica sin contacto directo con otro objeto cargado. Este fenómeno ocurre en tres pasos principales:

- Un objeto cargado se acerca al metal neutro sin tocarlo
- Las cargas dentro del metal se redistribuyen (las cargas opuestas son atraídas hacia el objeto externo, mientras las del mismo signo son repelidas)
- Si el metal se conecta a tierra mientras está bajo influencia del objeto cargado, y luego se aísla, quedará con carga opuesta a la del objeto inductor

Este método permite cargar objetos metálicos sin transferencia directa de electrones por contacto, y es fundamental en muchas aplicaciones de electrostática.

### Triboelectricidad

La triboelectricidad es un tipo de carga que ocurre cuando ciertos materiales se frotan entre sí. Cuando dos materiales diferentes entran en contacto y luego se separan, se puede producir una transferencia de electrones de un material a otro, resultando en una carga eléctrica. Este fenómeno es responsable de la electricidad estática que experimentamos en la vida cotidiana.

Los materiales pueden ordenarse en una serie triboléctrica, que indica la tendencia de un material a cargarse positiva o negativamente cuando se frota con otro material. Los materiales en extremos opuestos de la serie tienen mayor probabilidad de producir cargas significativas cuando se frotan entre sí.

Ejemplos comunes de triboelectricidad incluyen:

- El cabello que se carga al peinarlo con un peine de plástico
- La ropa que se adhiere entre sí después de secarse en secadora
- Las descargas que sentimos al tocar objetos metálicos después de caminar sobre alfombras sintéticas

  

### Ley de Coulomb

La Ley de Coulomb describe la fuerza electrostática entre dos cargas puntuales. Fue formulada por el físico francés Charles-Augustin de Coulomb en 1785. Esta ley establece que la magnitud de la fuerza electrostática entre dos cargas puntuales es directamente proporcional al producto de las magnitudes de las cargas e inversamente proporcional al cuadrado de la distancia entre ellas.

Matemáticamente, la Ley de Coulomb se expresa como:

F = k·|q₁|·|q₂|/r²

Donde:

- F es la magnitud de la fuerza electrostática
- k es la constante de Coulomb (9×10⁹ N·m²/C²)
- q₁ y q₂ son las magnitudes de las cargas
- r es la distancia entre las cargas

### Campos Eléctricos

Un campo eléctrico es una región del espacio alrededor de una carga eléctrica donde se ejerce una fuerza sobre otras cargas eléctricas. El campo eléctrico es una propiedad del espacio que describe la influencia electromagnética de las cargas eléctricas.

La intensidad del campo eléctrico E en un punto se define como la fuerza F que experimentaría una carga de prueba positiva q₀ colocada en ese punto, dividida por el valor de la carga de prueba:

E = F/q₀

Propiedades importantes de los campos eléctricos:

- Se representan mediante líneas de campo que indican la dirección de la fuerza sobre una carga positiva
- La densidad de las líneas de campo indica la intensidad del campo eléctrico
- Las líneas de campo salen de cargas positivas y entran en cargas negativas
- Las líneas de campo nunca se cruzan

**Calculo de la intensidad de un campo eléctrico**

Para calcular la intensidad del campo eléctrico, se pueden utilizar varios métodos dependiendo de la distribución de carga:

- Para cargas puntuales: E = k·q/r² (en dirección radial desde la carga)
- Para distribuciones continuas: E = ∫dE = k∫(dq/r²) û_r (integración sobre toda la distribución)
- Para cargas con simetría: Aplicación de la Ley de Gauss, E·A = q_encerrada/ε₀

### Campo de un Dipolo

Un dipolo eléctrico consiste en dos cargas de igual magnitud pero signo opuesto, separadas por una pequeña distancia. Los dipolos son fundamentales en el estudio de materiales dieléctricos y moléculas polares.

El campo eléctrico de un dipolo a una distancia r (mucho mayor que la separación entre las cargas) se caracteriza por:

- Decae con 1/r³, más rápidamente que el campo de una carga puntual
- Depende del momento dipolar p = q·l, donde l es el vector de separación
- La expresión para el campo en el eje del dipolo es E = k·2p/r³
- La expresión para el campo en el plano perpendicular al eje es E = k·p/r³

Los dipolos experimentan torque en presencia de campos eléctricos externos, lo que explica la orientación de moléculas polares en solución.

**Campo Eléctrico en Coordenadas Polares**

El cálculo del campo eléctrico se simplifica considerablemente cuando utilizamos coordenadas polares para distribuciones con simetría radial o angular.

En coordenadas polares bidimensionales (r, θ), el campo eléctrico tiene dos componentes:

- Componente radial: E_r (apuntando hacia afuera o hacia adentro)
- Componente angular o azimutal: E_θ (perpendicular a la dirección radial)

Las ventajas de usar coordenadas polares incluyen:

- Simplificación matemática para cargas con simetría radial
- Representación natural de la divergencia del campo desde un punto
- Facilidad para aplicar la Ley de Gauss en sistemas con simetría

Para una carga puntual q en el origen, el campo eléctrico en coordenadas polares es:

E_r = k·q/r²

E_θ = 0

Para distribuciones más complejas, las componentes del campo pueden calcularse mediante:

E_r = ∫(k·dq·cos(α)/r²)

E_θ = ∫(k·dq·sin(α)/r²)

Donde α es el ángulo entre el vector posición r y la línea que conecta el elemento de carga dq con el punto donde se calcula el campo.

Esta aproximación es particularmente útil para calcular el campo de anillos de carga, discos cargados uniformemente y otras geometrías con simetría circular.

### 6 de agosto de 2025 — Electrostática (a)

Introducción:

- Cargas eléctricas
- Estructura de la materia
- Conservación y cuantización de la carga
- Conductores y aisladores
- Electroscopio

# Tarea

---

[[4 - Indexes/Física II/Sin título]]