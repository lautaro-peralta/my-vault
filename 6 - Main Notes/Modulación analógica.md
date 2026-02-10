13-08-2025, 14:29

Tags: [[Modulación de señales]]

---
### AM – Amplitude Modulation

- La **amplitud** de la portadora varía en función de la señal de mensaje.
- La **frecuencia** y **fase** de la portadora se mantienen constantes.
- Ecuación típica:
$$
  s(t) = [A_c + m(t)] \cdot \cos(\omega_c t)
$$

- **Desventajas**: Poco eficiente en potencia y ancho de banda.

### FM – Frequency Modulation

- La **frecuencia instantánea** de la portadora varía en función de la señal de mensaje.
- Amplitud constante, buena inmunidad al ruido.
- Ecuación típica:
$$
  s(t) = A_c \cos\left( \omega_c t + k_f \int m(\tau) d\tau \right)
$$
### PM – Phase Modulation

- La **fase instantánea** de la portadora varía proporcionalmente a la señal de mensaje.
- Muy parecida a FM, pero la modulación se aplica directamente a la fase:

$$

  s(t) = A_c \cos\left( \omega_c t + k_p m(t) \right)
$$
---

![[Pasted image 20250813144359.jpg]]
![[Pasted image 20250813144457.jpg]]

---
## Referencias