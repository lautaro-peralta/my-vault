22-08-2025, 21:00

Tags: [[Modelo Relacional]]

---
Los axiomas de Armstrong son un conjunto de reglas de inferencia que se utilizan en la teoría de bases de datos para encontrar todas las **dependencias funcionales** que pueden derivarse a partir de un conjunto dado de dependencias. Fueron propuestos por William W. Armstrong en 1974. Estos axiomas son considerados "completos" y "sólidos" (o "sanos"). Son **completos** porque, aplicados repetidamente, pueden generar todas las dependencias funcionales lógicamente implicadas. Son **sólidos** porque no producen dependencias funcionales incorrectas.

El propósito principal de estos axiomas es servir como la base lógica para la **normalización de bases de datos**, ayudando a eliminar la redundancia y asegurar la integridad de los datos. Permiten razonar sobre las relaciones entre los atributos de una base de datos y derivar nuevas dependencias que no estaban explícitamente declaradas.

---
### 1. Axioma de reflexividad
 
Si **∀X ⊇ Y** ⇒ **X $\rightarrow$ Y**
Es decir, si **Y** es subconjunto de **X**, entonces **X** determina funcionalmente a **Y**.
Esto es una dependencia trivial, lo que significa que cualquier conjunto de atributos determina a sus propios atributos o a cualquier subconjunto de ellos.
 
**Ejemplo:**
- $CodArticulo \to CodArticulo$
- $CodBarra\to CodBarra$
- $CodArticulo, ~CodBarra \to CodArticulo$

### 2. Axioma de aumentatividad

Si **{X →Y, Z ⊇ X} ⇒ Z → Y**
Se puede aumentar trivialmente el determinante de una dependencia.

**Ejemplo:**
- $CodArticulo → DescArticulo$
- $CodArticulo, ~CodTalle → DescArticulo$

### 3. Axioma de transitividad (o enlace de DFs)
Si **X→ Y e Y → Z  ⇒ X→ Z**
Éste es el mecanismo básico de funcionamiento del enlace entre tablas o relaciones o claves foráneas.

**Ejemplo:**
- $CodArticulo → CodTalle, Desc Talle$
- $CodTalle → DescTalle$ 
- $CodArticulo → DescTalle$

---
## Reglas de inferencia adicionales (derivan de los axiomas)

### 4. Proyectividad (o descomposición)

**{ X → Y , Z ⊆ Y } ⇒ X → Z**

**Ejemplo:**
$CodArticulo → DescArticulo, CodTalle, CodColor, CodBarra$
Se puede descomponer:
- $CodArticulo → DescArticulo$
- $CodArticulo → CodTalle$
- $CodArticulo → CodColor$
- $CodArticulo → CodBarra$
### 5. Aditividad o Unión

**{ X → Y , Z → V } ⇒ X ∪ Z → Y ∪ V**

**Ejemplo:**
- $CodArticulo → DescArticulo$
- $CodTalle → DescTalle$
- $CodArticulo, CodTalle → DescArticulo, DescTalle$
### 6. Pseudo-transitividad

**{X → Y, W ∪ Y → Z } ⇒ X ∪ W → Z**

**Ejemplo:**
- $CodArticulo → DescArticulo$
- $DescArticulo, CodColor → DescColor$
- $CodArticulo, CodColor → DescColor$

---

Estos axiomas además pueden ser utilizados para:

1. Determinar si una dependencia funcional **X → Y** no indicada inicialmente en un conjunto DF es válida.
2. Determinar si dos representaciones del mismo problema son equivalentes
3. Determinar las claves candidatas y primarias

---
## Referencias
[[BDatos_2_DiseñoBasesDeDatosV2023.01.1.pdf]]