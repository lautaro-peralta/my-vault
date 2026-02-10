19-08-2025, 18:49

Tags: [[Modelos de datos]]

---
### Superclases y subclases

Para casos donde una entidad puede tener varias subagrupaciones adicionales de sus instancias que son significativas y que deben representarse explícitamente dada su importancia para el modelo. Esta posibilidad da mayor carga semántica al modelo, a diferencia del MER básico.

**Herencia de de los atributos**
Todas las instancias de la entidad que es miembro de una subclase heredan todos los atributos de la superclase pero además pueden tener atributos propios.

**¿Para qué usar superclases/subclases?**
$\rightarrow$ Existen atributos que se aplican a algunas instancias de la superclase, no a todas.
$\rightarrow$ Existen relaciones con algunas subclases, no con todas.

---
### Generalización y especialización

**Generalización**
Proceso que implica un refinamiento conceptual ascendente durante el diseño del esquema conceptual (modelo). Comenzamos desde las subclases y a partir del proceso de generalización encontramos las clases o superclases. A efectos prácticos, la generalización pone énfasis en las similitudes y considera que cada instancia de la superclase es también una instancia de las subclases. Es una inversión simple de la especialización.

**Especialización**
Proceso de definir subclases con las instancias de una entidad. Implica un refinamiento conceptual descendente durante el diseño del modelo. Comenzamos con una entidad y definimos subclases de la misma mediante especializaciones sucesivas. pone énfasis en las diferencias y considera que alguna instancia de la superclase puede no ser instancia de ninguna subclase.
Las subclases que forman una especialización se definen a partir de alguna característica distintiva de las instancias de la superclase.
Una especialización puede contener una subclase solamente.

**Especialización definida por atributo**
En algunas especializaciones podemos determinar con exactitud las instancias de la entidad que se convertirán en miembros de cada subclase especificando una condición  en términos del valor de algún atributo de la superclase.
Si todas las subclases de una especialización definen la condición de pertenencia en términos del mismo atributo de la superclase, se dice que la especialización es una especialización definida por atributo, y el atributo se denomina atributo de definición de la especialización.

**Especialización definida por el usuario**
Cuando no tenemos condición que determine la pertenencia a una subclase, es el usuario el que define individualmente la pertenencia a cada entidad y no una condición que pueda ser evaluada de forma automática.

**Restricción de disyunción o solapamiento**
La restricción de disyunción significa que una instancia de la entidad solo puede ser miembro de una de las subclases de la especialización. Si la misma instancia de la entidad puede ser miembro de más de una subclase de especialización existe un solapamiento. 

**Restricción de completitud**
$\rightarrow$ *Total:* toda instancia de la entidad de la superclase debe ser miembro de alguna subclase de la especialización.
$\rightarrow$ *Parcial:* una entidad no pertenece a ninguna de las subclases.

**Tipos de especialización**
- Disyunta, total
- Disyunta, parcial
- Solapada, total
- Solapada, parcial

**Reglas de inserción y eliminación que se aplican a la especialización**
1. Eliminar una instancia de una entidad, de una superclase implica eliminar todas las instancias de las subclases a las que pertenece.
2. Insertar una instancia de una entidad en una superclase de una especialización total implica insertar la misma en por lo menos una de las subclases de la especialización.
3. Insertar una instancia de una entidad en una superclase de una especialización parcial no implica necesariamente insertar la misma en alguna de las subclases de la especialización.

---
### Jerarquías y retículas

Una subclase puede tener más subclases definidas a partir de ella. Cuando la subclase participa de una única relación clase-subclase se dice que forma una Jerarquía.
En las jerarquías las subclases tienen herencia única, es decir heredan los atributos de la clase con la que están relacionadas.
Si una subclase participa en más de una relación clase-subclase se dice que forma una ***retícula*** y a la subclase se la denomina ***subclase compartida***. En las retículas las subclases tienen herencia múltiple (heredan de las clases con las que están relacionadas).

**Regla:** si un atributo que se origina en la superclase se hereda más de una vez a través de diferentes caminos en la retícula debería incluirse solo una vez la subclase compartida. La subclase compartida se considera un subconjunto de la intersección de todas sus superclases (porque debe ser miembro de todas ellas simultáneamente).

---
### Categorías (Unión)

Una categoría es una clase resultante del proceso por el cual varias clases de naturaleza distinta se agrupan (unen) para formar una nueva clase. Proviene de dos o más superclases. Una categoría es un subconjunto de la unión de sus superclases.
Una categoría puede ser parcial o total.
Las superclases de una categoría pueden tener diferentes atributos clave.

---
### Agregación

La agregación es una abstracción a través de la cual las relaciones se tratan como entidades de nivel más alto. Es útil cuando el objeto agregado de más alto nivel se debe relacionar con otro objeto (posteriormente).
- Una agregación hace referencia a la relación ***N a M*** de las entidades que agrega (aunque su nombre puede diferir del nombre de la relación son lo mismo).
- La agregación puede estar haciendo referencia a un vínculo de cualquier grado (por ej. a uno ternario) y las entidades participantes del mismo pueden ser de cualquier tipo
- La agregación puede luego vincularse con otras entidades (fuertes, débiles o también otra agregación) y participar de vínculos de cualquier grado. También puede ser parte de una jerarquía.

---
## Referencias
[[BDatos_1_ModelosdeDatosV2023.01-1.pdf]]