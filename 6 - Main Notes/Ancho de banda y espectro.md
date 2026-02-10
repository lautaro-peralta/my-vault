13-08-2025, 20:31

Tags: [[Fundamentos de las señales]]

---

### Banda de frecuencia del mensaje
$W=f_{max}-f_{min}$
$W_{AM}= 2 f_{max}$

## Banda de frecuencia de un mensaje

Es el rango de frecuencias que ocupa la señal original (sin modular).  
Si el mensaje contiene frecuencias desde hasta :

$$

\text{Banda de frecuencia} = [f_{\min}, f_{\max}]
$$

Ejemplo:

- Voz telefónica: 300 Hz – 3,4 kHz
- Música Hi-Fi: 20 Hz – 20 kHz

---

## Ancho de banda (BW)

- Es la **diferencia** entre la frecuencia más alta y la más baja que contiene la señal:

$$BW = f_{corteMax} -f_{corteMin}=2Nf_{corteMax}$$

$$

BW = f_{\max} - f_{\min}
$$

- **AM**: (donde es la frecuencia máxima del mensaje)
- **FM/PM**: Se calcula con la **fórmula de Carson**:

$$
    BW \approx 2 \cdot ( \Delta f + f_m )
$$
---
## DSB (Double Sideband) - Modulación de Doble Banda Lateral

Modulación AM donde se conservan ambas bandas laterales pero se puede suprimir o no la portadora.

---
### Variantes:

**DSB-SC (Suppressed Carrier):**

- Se elimina la portadora
- Solo quedan las bandas laterales
- **Eficiencia**: 100% de potencia útil
- **Desventaja**: Detección compleja (requiere portadora de referencia)

**DSB-TC (Transmitted Carrier):**

- Se mantiene la portadora (AM convencional)
- **Eficiencia**: ~33% de potencia útil
- **Ventaja**: Detección simple con diodo

---
### Espectro:

| $f_c-W$ (LSB) | $f_c$ (portadora) | $f_c+W$ (USB) |
| ------------- | :---------------: | ------------- |
| LSB           |     portadora     | USB           |
![[Pasted image 20250813144601.jpg]]
### Comparación práctica:

- **Ancho de banda**: 2W (doble del mensaje)
- **vs SSB**: DSB usa el doble de ancho de banda
- **vs AM**: DSB-SC es más eficiente energéticamente

**Aplicación típica:** Sistemas donde el ancho de banda no es crítico pero se requiere simplicidad en la implementación.

---
## Referencias
