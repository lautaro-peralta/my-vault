---

---
---
### Definición

Un modelo de datos es un sistema formal y abstracto que permite describir los datos de acuerdo con reglas y convenios predefinidos.
- **Formal** $\rightarrow$ los objetos del sistema se manipulan bajo reglas perfectamente definidas y usando exclusivamente los operadores definidos en el sistema, independientemente de lo que estos objetos y operadores puedan significar.
- **Abstracto** $\rightarrow$ en el modelo solo se representan aquellos aspectos del mundo real que son relevantes para el objetivo del sistema o dominio en estudio.

Un MD es una combinación de tres componentes:
1. una colección de estructuras de datos;
2. una colección de operadores o reglas de inferencia, las cuales pueden ser aplicados para consultar o derivar datos de cualquier parte de estas estructuras en cualquier combinación deseada;
3. una colección de reglas generales de integridad, las cuales explícita o implícitamente definen un conjunto de estados consistentes. Estas reglas algunas veces son expresadas como reglas de insertar-actualizar-borrar.

### Categorías

- **Modelos de datos de alto nivel (o conceptuales)**, muy cercanos al modo como la mayoría de los usuarios percibe los datos. Entre ellos:

	**a.** Basados en objetos:
	1. [[Modelo de Dominio]]
	2. ***[[Modelo Entidad-Relación]]*** $\rightarrow$ [[Modelo E-R extendido]]
	
	**b.** Basados en registros:
	3. Jerárquico: datos en registros, relacionados con punteros y organizados como colecciones de árboles
	4. Redes: datos en registros, relacionados por punteros y organizados como grafos
	5. ***[[Modelo Relacional]]***: datos en tablas relacionados por el contenido de ciertas columnas

- **Modelos de datos de bajo nivel (o físicos)**,  que proporcionan conceptos que describen los detalles sobre como se almacenan los datos en la computadora.