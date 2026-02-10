22-08-2025, 08:06

Tags: [[Diseño de Bases de Datos]]

---

El modelo relacional es un modelo basado en la lógica de predicados y en la teoría de conjuntos.
Sus fundamentos fueron planteados por Edgard Codd y se constituyó rápidamente en el modelo por excelencia que se trasladó a la implementación de Bases de Datos, en este caso Bases de Datos Relacionales.

---
### Componentes en un Modelo Relacional

**Estructura de Datos: Tablas o Relaciones**. Formalmente, el nombre de Modelo Relacional deriva del uso de relaciones (o tablas) que constan de un conjunto de tuplas (filas de la tabla o registros) constituidas por un conjunto de atributos (columnas de la tabla) cuyos valores pertenecen al dominio. A la cantidad de atributos que constituyen una relación es la denomina grado de la relación.

**Reglas de integridad o Restricciones**:

1. ==*Integridad de Entidad*==  $\rightarrow$ establece que se requiere de la definición de una clave primaria o identificador. Una clave primaria es un atributo o conjunto mínimo de atributos de una relación o tabla que identifica unívocamente al resto de los atributos de la relación. Por ello debe tener un valor único para el conjunto de filas de la tabla, ninguno de sus atributos puede admitir valor nulo y no deben existir atributos que no agreguen información clave (atributos superfluos).
2. ==*Integridad Referencial*== $\rightarrow$ Esta restricción surge de definir una clave foránea en una tabla. Una **clave foránea** es un atributo o conjunto de atributos de una relación o tabla que esta relacionado con la clave primaria de otra relación o tabla. Esta puede admitir valores nulos (todos sus atributos) pero si tiene valor, éste debe ser coincidente con la clave primaria de la tabla con la que está relacionada (se debe indicar con NULL/NN). Con esto se asegura integridad entre la clave foránea de una tabla (hija) y la clave primaria de la tabla (padre) con la que se relaciona.
3. ==*Integridad de Dominio*== $\rightarrow$ Dominio de valores  de los atributos que constituyen la relación o tabla, es decir los valores que pueden admitirse en el atributo. Trabajaremos con el concepto de dominio semántico del atributo (su significado).

---
### Dependencias funcionales y claves

Las dependencias funcionales están ligadas a la búsqueda de claves y es necesaria su comprensión para desarrollar el proceso de normalización y definir el modelo relacional que se implementará luego en una base de datos relacional.
#### Definiciones

**Esquema de Relación**: r = R(T, DF)

donde
**R**: nombre de la relación
**T**: conjunto de atributos que componen la relación: T = {A1, A2, A3, ..., An}
**n**: grado de la relación
**DF**: conjunto de restricciones o dependencias funcionales que se deducen de las reglas del dominio que estamos trabajando: **DF = {DF1; DF2; DF3; ...; DFm}**. Cada **DFi** Se expresa como **X $\rightarrow$ Y,** donde **X** e **Y** son subconjuntos del conjunto de atributos T de R y se denominan descriptores. **X** se denomina determinante e **Y** se denomina determinado.
Se dice que **Y** es funcionalmente dependiente de **X** o que **X** determina funcionalmente a **Y**.
Entonces:
*Sea **R** una relación, **X** e **Y** subconjuntos arbitrarios del conjunto de atributos de **R** a los que denominaremos descriptores. Se dice que **Y** es funcionalmente dependiente de **X** (**X →Y**) si todo valor legal posible de **X** tiene asociado precisamente un único valor de **Y**.*

Diremos que una dependencia funcional (Df1 por ej.) es la clausura de las dependencias funcionales ($DF^{+}$) si a partir de este conjunto de atributos  (que además es mínimo) se pueden obtener todos los atributos de la relación que estamos analizando. Mediante los [[Axiomas de Armstrong]].

#### Dependencia Funcional Parcial 

Una dependencia parcial ocurre cuando un atributo **depende solo de una parte de la clave primaria compuesta**, y no de la clave completa.

**Ejemplo:** Imagina una tabla `EXAMEN` cuya clave primaria es `{NroLegajo, CodAsig, FechaExamen}`. En esta tabla, se dan las siguientes dependencias:
- `NroLegajo → ApellidoyNombres`
- `CodAsig → NombreAsig`
Aquí, `ApellidoyNombres` no necesita la clave completa para ser determinado; le basta con `NroLegajo`. Lo mismo ocurre con `NombreAsig`, que solo necesita `CodAsig`. Estas son dependencias parciales porque no dependen de la clave entera.

#### Dependencia Funcional Transitiva

Una dependencia transitiva ocurre cuando un atributo que **no es parte de la clave** depende de otro atributo que **tampoco es parte de la clave**. Se forma una cadena de dependencias.

**Ejemplo:** Siguiendo con la tabla `EXAMEN`, donde la clave es `{NroLegajo, CodAsig, FechaExamen}`, tenemos estas dependencias:
- La clave `{NroLegajo, CodAsig, FechaExamen}` determina el `LegajoDoc`.
- A su vez,
    `LegajoDoc → NombreDoc`.
Aquí, `NombreDoc` (un atributo no clave) depende de `LegajoDoc` (otro atributo no clave). Esto es una dependencia transitiva.

#### Clave candidata

Atributo o conjunto mínimo de atributos que identifica unívocamente una instancia de una relación o tabla (o conjunto mínimo de atributos tales que su clausura es igual a todos los atributos de la relación).
En función de esto ninguno de los atributos que conforman una clave candidata podrá admitir valores nulos, tampoco los atributos podrán ser superfluos.
De todas las claves candidatas se seleccionará una para utilizarla como clave de la relación y la denominaremos clave primaria.

| Concepto                  | Definición Clave                                                                                                                    | Rol en el Diseño                                                                                                                                                   |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Dependencia Funcional** | Una regla que establece que un conjunto de atributos **determina** unívocamente a otro (X → Y).                                     | Es la **regla fundamental** del universo de tus datos. Son los "hechos" sobre cómo se relacionan los datos entre sí.                                               |
| **Clausura**              | El **conjunto completo de atributos** que pueden ser determinados a partir de un atributo o conjunto de atributos inicial.          | Es la **herramienta de cálculo** para medir el "poder" de un conjunto de atributos. Nos permite ver qué tanto de la tabla podemos "alcanzar" a partir de un punto. |
| **Clave Candidata**       | Un conjunto **mínimo** de atributos cuya clausura es igual a **todos los atributos** de la tabla. Identifica unívocamente una fila. | Es un **identificador potencial** para una fila de la tabla. Puede haber varios "candidatos" para ser la clave principal.                                          |
| **Clave Primaria**        | Es la **clave candidata que se selecciona** para ser el identificador único y principal de la tabla.                                | Es el **identificador oficial y elegido**. Es la clave que se usará para establecer relaciones con otras tablas.                                                   |

No necesariamente se llega a que, dado un dominio y una vez identificados sus atributos y dependencias funcionales, se encuentra un único atributo o conjunto de atributos del cual dependen funcionalmente el resto de los atributos del dominio como en el ejemplo dado. Tanto en estos casos como para evitar otros problemas, una relación puede necesitar ser descompuesta en varias relaciones a través del proceso de **[[Normalización]]**.

---
### Claves foráneas y NULL/NN

- **Si la FK forma parte de la clave primaria (PK)** → **No admite NULL**.
    Las claves primarias nunca pueden contener valores nulos.
- **Si la FK no forma parte de la PK** → Se elige:
    - **`NULL`** → relación opcional con la tabla padre.
    - **`NN` (NOT NULL)** → relación obligatoria con la tabla padre.

---
## Referencias
[[BDatos_2_DiseñoBasesDeDatosV2023.01.1.pdf]]