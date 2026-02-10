13-08-2025, 21:30

Tags: [[Fundamentos de las señales]]

---
## ¿Qué son las señales analógicas?

Las señales analógicas son como las ondas del mar: **varían continuamente**. Cuando hablás, tu voz no salta de un volumen a otro - fluye suavemente. Eso es una señal analógica.

**Características principales:**

- Pueden tomar **cualquier valor** dentro de un rango
- Están **siempre cambiando** en el tiempo
- La información está en esas **variaciones suaves**

**Ejemplos:**

- Tu voz cuando hablás
- La música en un disco de vinilo
- La temperatura que marca el termómetro
- El voltaje de una pila que se va gastando

### El gran problema: el ruido se pega para siempre

Imaginate el juego del "teléfono descompuesto". Cada vez que la señal pasa por un amplificador o viaja una distancia larga, se le suma ruido que **no se puede sacar**. Como cuando fotocopiás una fotocopia: cada vez queda peor.

---

## ¿Qué son las señales digitales?

Las señales digitales son como un interruptor de luz: **están prendidas o apagadas**, sin términos medios. Solo pueden tomar valores específicos, generalmente 0 y 1.

**La clave está en la decisión:** Cuando llega una señal medio ruidosa, el receptor puede **decidir** si era un 0 o un 1, y listo - eliminó el ruido. Es como tener un corrector ortográfico automático en cada paso.

**Ejemplos cotidianos:**

- Los archivos de tu computadora
- Los códigos de barras del supermercado
- Las señales de GPS de tu celular
- La música en un CD

---

## Cómo pasar del mundo real al digital

Para convertir algo analógico (como la voz) en digital, hacemos tres pasos:

### 1. Muestreo: "Sacar fotos"

Tomamos "fotografías" de la señal a intervalos regulares. Como hacer un stop-motion de la señal.

**Regla importante:** Tenemos que sacar fotos al menos al doble de velocidad que la frecuencia más alta que queremos capturar ([[Teorema de Nyquist]]).

### 2. Cuantización: "Redondear"

Cada "foto" la redondeamos al valor más cercano de una escala predefinida. Es como aproximar números decimales.

### 3. Codificación: "Ponerle etiquetas"

A cada valor le asignamos una palabra código (secuencia de 0s y 1s).

---

## La comparación práctica

|                                            | Analógica                                 | Digital                     |
| ------------------------------------------ | ----------------------------------------- | --------------------------- |
| **¿Se arruina con ruido?**                 | Sí, para siempre                          | No, se puede "limpiar"      |
| **¿Mantiene calidad a distancia?**         | No, se degrada                            | Sí, se mantiene             |
| **¿Fácil de procesar?**                    | Complicado, necesitás hardware específico | Fácil, con software         |
| **¿Se puede guardar sin que se arruine?**  | No, se degrada con el tiempo              | Sí, copia perfecta infinita |
| **¿Ocupa mucho "espacio" en frecuencias?** | Generalmente menos                        | Generalmente más            |

---
Vivimos en un mundo que es físicamente analógico, pero procesamos casi todo de forma digital.

Hasta la fibra óptica que parece "súper digital" en realidad transmite pulsos de luz analógicos que representan información digital.

**¿Por qué ganó lo digital?** Simple: cada vez que la señal pasa por un repetidor, puede "decidir" qué bit era y mandarlo limpio. En analógico, el ruido se va sumando sin remedio.

Es como la diferencia entre:
- **Analógico:** Pasar un mensaje de boca en boca (se distorsiona)
- **Digital:** Pasar un mensaje escrito que cada persona puede leer bien y volver a escribir claramente

---
## Referencias
