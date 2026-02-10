13-08-2025, 20:26

Tags: [[Modulación de señales]]

---
### Principios Fundamentales

- **Representación**: Datos binarios (1s y 0s)
- **Regla crítica**: Siempre usar patrones **no periódicos** (≠ 101010...). Ya que los patrones periódicos crean componentes espectrales discretas que pueden causar interferencia

---
### Modulación Digital-Analógica

#### Parámetros de la señal

1. **Amplitud**
2. **Frecuencia**
3. **Fase**
---
### Técnicas de Modulación

##### *ASK (Amplitude Shift Keying)*

- Bit '1': Amplitud = portadora
- Bit '0': Amplitud = 0

**¡¡NO SE USA!!** en aplicaciones prácticas debido a alta susceptibilidad al ruido y desvanecimiento

##### *FSK (Frequency Shift Keying)*

- **Principio**: Diferentes frecuencias para '0' y '1'
- **Ventaja**: Mayor robustez al ruido que ASK
- **Aplicación**: Módems de baja velocidad, sistemas de radio

##### *PSK (Phase Shift Keying)*

- **Principio**: Cambio de fase indica transición de bit
- **Ventaja**: Eficiencia espectral superior
- **Variantes**: BPSK, QPSK, 8-PSK, etc.

---
### Análisis Espectral

- **Tren de pulsos no periódico**: Espectro continuo con función sinc(x)
- **Ancho de banda**: Inversamente proporcional a la duración del pulso (1/τ)
- **Espectro del mensaje**: W = ancho de banda de la información

---
### Proceso de Transmisión

1. **Modulación**: Señal digital → Señal analógica
2. **Transmisión**: A través del canal analógico
3. **Demodulación**: Señal analógica → Señal digital
4. **Dispositivo**: **MÓDEM** (**MO**dulator-**DEM**odulator)

---

### Optimización de Velocidad de Transmisión

#### Limitaciones del Enfoque Tradicional

- **Problema**: Aumentar frecuencia de bits (reducir τ) puede causar pérdida de integridad del pulso
- **Solución**: No aumentar la frecuencia de símbolos, sino usar **multinivel** (aumentar μ)

---
## Referencias