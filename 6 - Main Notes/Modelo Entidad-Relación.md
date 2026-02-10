19-08-2025, 13:36

Tags: [[Modelos de datos]]

---

El enfoque del Modelo E-R simplifica el proceso de modelado desarrollando un diagrama entidad-relación (DER), que es una representación abstracta del dominio analizado y además es independiente del almacenamiento y las consideraciones de eficiencia.
El DER se puede trasladar luego a modelos más apropiados en un sistema de gestión de base de datos (DBMS).

---
### Componentes y Representación

**Entidad** 
Tipo de información que es de interés para la empresa. Puede tener existencia física o conceptual. Denominaciones (depende del autor): Tipo de Entidad, Conjunto de Entidades (aludiendo a que cada instancia que conforma el objeto es una entidad) o simplemente Entidad (entendiendo que se conforma con todas las instancias del objeto).

**Relación**
Correspondencia, conexión o vínculo entre dos o más entidades.

**Atributos**
Caracterizan a la entidad o relación.

$\rightarrow$ *Compuestos vs. Simples:*
- Un atributo puede ser **simple o atómico** cuando admite valores que no pueden subdividirse.
-  Un atributo es **compuesto** cuando puede dividirse en atributos más pequeños.

$\rightarrow$ *Monovaluados vs. Multivaluados:*
- Un atributo es **monovaluado** si solo admite un valor para cada instancia de una entidad en particular.
- Un atributo **multivaluado** asume varios valores para una misma entidad. Pueden tener un límite inferior y superior en el número de valores para una entidad individual.

$\rightarrow$ *Almacenados vs. Derivados:*
- Los atributos **almacenados** son los que deben ser guardados con la entidad ya que no se pueden calcular ni a través de otros atributos de la misma entidad u otras, ni de su relación con otras entidades. 
- Los **derivados**, se calculan en función de otro atributo.

$\rightarrow$ *Valores nulos:*
- En algunos casos, un atributo podría no tener valor para una instancia de una entidad. Dependiendo de si el atributo debería admitir valores nulos o no: NULL o NOT NULL(NN).

$\rightarrow$ *Identificadores o claves:
- cada entidad DEBE TENER un único identificador que permita individualizar cada una de sus instancias. No necesariamente deben ser un único atributo, pueden ser un conjunto de atributos (lo que se denomina una clave compuesta). Todos los atributos que conforman una clave deben ser monovaluados y siempre deben tener valor (son NN). Se completa el concepto de identificadores o claves al referirnos al [[Modelo Relacional]].

---
### Restricciones estructurales

**Razón de cardinalidad**
Número de instancias del vínculo en los que puede participar cada entidad de una relación o vínculo. Al numero de entidades que participan en una relación se lo denomina **grado del vínculo**.

Debido a que no existe una amplia aceptación de un estándar para representar las
cardinalidades en una relación optamos por: ***0..M***. Significa cardinalidad mínima **= 0** y cardinalidad máxima **= M**. Para mencionar la cardinalidad del vínculo lo haremos con sus valores máximos.

**Restricción de participación**
Especifica si la existencia de una entidad depende de que esté relacionada con otra entidad.
Hay dos clases de restricciones de participación: total o parcial.
La restricción de participación total recibe el nombre de dependencia de existencia.

---
### Atributos de las relaciones o vínculos

En los casos de vínculos **1 a 1**, un atributo del mismo podrá ser trasladado a cualquiera de las
entidades que participan del vínculo.
En los casos de vínculos **1 a N** un atributo del mismo sólo se podrá trasladar a la entidad del
lado **N** del vínculo.

---
### Entidades fuertes y entidades débiles

Las entidades fuertes tienen un atributo o conjunto de atributos que identifican a sus
instancias unívocamente, es decir un identificador o clave.

Es posible que una entidad no posea un identificador o clave asociado y su identificación dependa del vínculo con otra entidad. A estas entidades se las llama Entidades Débiles y se dice que hay dependencia de identificación. Al vínculo con la entidad de la que depende su identificación se lo denomina vínculo identificador.

Una entidad débil siempre tiene una restricción de participación total o dependencia de
existencia con otra entidad a través de su vínculo identificador. Sin embargo, no toda dependencia de existencia da lugar a un tipo de entidad débil

---
### Otros tipos de relaciones

$\rightarrow$ **Relaciones recursivas o reflexivas** (cuando una instancia de la entidad se relaciona con otra instancia de la misma entidad).

$\rightarrow$ **Relaciones de grado superior a dos:**
	En varias ocasiones es complicado decidir si una relación deberá ser representada como un tipo de relación de grado N o si debería descomponerse en varios tipos de relación de grados inferiores. Se debe basar la decisión en la semántica o en el significado de la situación particular que se representa. En una relación ternaria las tres entidades deben estar relacionadas. 
	Para minimizar la complejidad del análisis, las cardinalidades mínimas de una relación ternaria las consideraremos siempre 1.
	Las cardinalidades de un vínculo ternario podrán ser todas 1..N, solo podrá existir una con cardinalidad 1..1.
	No necesariamente las entidades que participan de este tipo de relaciones deben ser entidades fuertes.

---

![[Pasted image 20250819184620.png]]

---
## Referencias
[[BDatos_1_ModelosdeDatosV2023.01-1.pdf]]