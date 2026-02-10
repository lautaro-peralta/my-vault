24-08-2025, 11:40

Tags: [[Transformación de un Modelo E-R en Relacional]]

---

Aunque los tres enfoques de conversión de jerarquías sean válidos para todos los casos no siempre serán apropiados o convenientes. Analizaremos a continuación las ventajas y desventajas.

---
### Conversión a jerarquía completa

**Ventajas**
- Mejor uso de espacio de almacenamiento.
- Modelización exacta del dominio.

**Desventajas**
- Para acceder a toda la información de una subclase debe accederse a las tablas de todas sus superclases. Por ejemplo, para obtener toda la información de un ingrediente elaborado, habría que acceder a las tablas de **ARTÍCULOS, INGREDIENTES y ELABORADOS**.
- Requiere coordinación entre las claves primarias de las superclases y subclases.
- Cada nuevo subtipo requiere al menos una nueva tabla y las consultas asociadas a la misma.
- Complejo modelado de las jerarquías solapadas.
- Complejo mecanismo de identificación del tipo de la subclase.

---

#### **Conversión a superclase**

**Ventajas**
- El acceso a cualquier subclase solo requiere acceso a una tabla.
- No requiere coordinación entre las claves primarias de las superclases y subclases.
- Fácil modelado de jerarquías solapadas.
- Rara vez requiere modificaciones en el modelo de datos para agregar una nueva subclase.

**Desventajas**
- Desperdicio de espacio para aquellos atributos de las subclases que no son comunes.
- Complejo mecanismo de identificación del tipo de la subclase.

---

#### **Conversión a subclases**

**Ventajas**
- Fácil mecanismo de identificación de la subclase.
- Uso eficiente de espacio de almacenamiento cuando los atributos comunes de las subclases son pocos.
- Acceso eficiente a todos los datos de una subclase particular.

**Desventajas**
- Uso ineficiente de espacio de almacenamiento cuando los atributos comunes de las subclases son muchos.
- Requiere mecanismos complejos de coordinación de claves primarias para jerarquías solapadas.
- Cada nuevo subtipo requiere una nueva tabla y las consultas asociadas a la misma.
- Complejo modelado de las jerarquías solapadas.
- Mecanismo de identificación de tipo de subclase más complejo.

---

En cada modelo en particular se deberán considerar las ventajas y desventajas de cada enfoque y evaluar en cada caso cuál resulta más conveniente, ya que este tipo de conversión suele tener un impacto importante en el costo de mantenimiento de los sistemas.

---
### EXCEPCIÓN A LOS TRES ENFOQUES: CATEGORÍAS Y RETÍCULAS

El modelo relacional provee un soporte limitado al proceso de generalización-especialización.  
A través de los tres enfoques anteriores pueden modelarse la mayoría de los casos; sin embargo, hay casos particulares donde deben aplicarse otros mecanismos de transformación, en función de las restricciones que plantea el modelo relacional.

Los problemas que surgen de la implementación de este tipo de generalización-especialización son descritos en bibliografía sobre **ORM (Object Relational Mapping),** nombrado como implementación de **herencia múltiple**, y se presentan principalmente en las **categorías y retículas**.

---
#### Categorías

El principal problema surge cuando las entidades que se agrupan son de naturaleza distinta y, por tal motivo, las claves primarias de esas entidades son incompatibles.  
Por ejemplo, si se tiene una entidad **Clientes** que puede representar **clientes particulares o empresas** con cuentas corrientes, las claves primarias de EMPRESAS y PARTICULARES difieren en su dominio.

En estos casos, la alternativa es **transformar las superclases en tablas y agregar las columnas de la subclase a cada superclase**, lo que equivale al enfoque de **conversión a superclase**.

Si las claves primarias no son incompatibles, también podrían usarse los enfoques de conversión de jerarquía completa o conversión a subclases.

En los casos con claves incompatibles, puede agregarse un atributo adicional, como `TipoCliente`, para evitar superposiciones.  
Por ejemplo, la clave primaria podría definirse como:  
**TipoCliente, NroCliente (CP)**

---
#### Retículas

La conversión de una retícula se divide en dos etapas:

1. **Etapa de transformación de jerarquía**:  
    Se considera la superclase de mayor jerarquía hasta las subclases con herencia simple, aplicando los tres enfoques explicados.
    
2. **Etapa de transformación de herencia múltiple**:  
    Aquí se analizan las subclases con herencia múltiple y las superclases de las que heredan, aplicando el mismo análisis que para las categorías.


---
## Referencias
[[BDatos_2_DiseñoBasesDeDatosV2023.01.1.pdf]]