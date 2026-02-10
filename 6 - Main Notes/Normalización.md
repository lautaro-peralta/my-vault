23-08-2025, 11:03

Tags: [[Modelo Relacional]]

---
Normalización es el proceso por el cual una relación se descompone en dos o mas relaciones que satisfacen ciertas condiciones denominadas formas normales.

Se normaliza para:
- evitar la redundancia de los datos,
- evitar anomalías de inserción, eliminación y actualización de los datos en las tablas,
- proteger la integridad de los datos, mejorar la independencia de los datos de los programas de aplicación (ver [[Bases de datos relacionales]]).

En el proceso de normalización no se pierde información, por lo que podemos volver siempre a la forma normal desde la que se partió.

---
### Primera forma normal (1NF)

Se dice que una relación (tabla) está en 1NF si cumple la propiedad de que 
> ***"sus atributos o columnas contienen solo valores atómicos (no son multivaluados o compuestos) y pertenecen a un mismo dominio de valores"***

Considerar un atributo como atómico depende de la implementación y de las aplicaciones en que utilizaremos el modelo.

### Segunda forma normal (2NF)

Una relación (tabla) está en 2NF si:
> ***"además de estar en 1NF, cualquiera de sus atributos no-claves dependen completamente de cada una de las claves candidatas de la relación (tabla)"***

La dependencia debe ser completa sobre la totalidad de los atributos que conforman la clave (para claves compuestas) y no para una parte de ella. 2NF se aplica sólo cuando tenemos claves compuestas.

Al descomponer relaciones para obtener la 2NF, se requiere además aplicar el concepto de integridad referencial, es decir, la definición de claves foráneas.

### Tercera forma normal (3NF)

Una relación (tabla) está en 3NF si:
>***"además de estar en 2NF cualquiera de sus atributos no-claves no depende transitivamente de las claves candidatas de la relación (tabla)"***

Es decir, cada atributo no clave debe **depender solo y directamente de la clave primaria**, **no de otro atributo no clave**.

### Forma normal BOYCE-CODD (BCNF)

Una relación (tabla) está en BCNF si:
>***"todo determinante es una clave candidata"***

Es una definición más rígida que la 3NF y aplica en casos donde
1. Una parte de la clave determina otra parte de una clave
2. Un atributo que no conforma parte de la clave determina parte de la clave

---

Es muy común que dado un esquema relacional con sus dependencias funcionales no necesitemos realizar el proceso de normalización completo. Generalmente y sobre todo a partir de la práctica e identificando bien las dependencias funcionales, obtendremos un modelo normalizado, en la 3NF y solo nos restarán agregar algunas relaciones para las dependencias funcionales que no hayan quedado expresadas en el modelo (BCNF).

Además, existen otras formas normales que no derivan de las dependencias funcionales (4NF, 5NF).

---
## Referencias
[[BDatos_2_DiseñoBasesDeDatosV2023.01.1.pdf]]