18-08-2025, 21:41

Tags: [[Integrales Múltiples]]

---
## 1. Definición

La integral doble es una extensión natural de la integral simple a funciones de dos variables. Representa el volumen bajo una superficie sobre una región determinada del plano $xy$. Se define como el límite de una suma doble de Riemann cuando el número de subdivisiones tiende a infinito.
### 1.1. Sobre un rectángulo

Para una función $f(x,y)$ definida sobre $R = [a,b] \times [c,d]$:

$$
\iint\limits_R f(x,y)  dA = \lim_{m,n \to \infty} \sum_{i=1}^m \sum_{j=1}^n f(x_{ij}^*, y_{ij}^*) \Delta x \Delta y
$$
### 1.2. Propiedades fundamentales

$$
\begin{aligned}
&\iint\limits_R [f(x,y) + g(x,y)]  dA = \iint\limits_R f(x,y)  dA + \iint\limits_R g(x,y)  dA  \end{aligned}$$
$$ \begin{aligned} &\iint\limits_R c f(x,y)  dA = c \iint\limits_R f(x,y)  dA \\
\end{aligned}
$$$$ \begin{aligned}&f(x,y) \geq g(x,y) \Rightarrow \iint\limits_R f(x,y)  dA \geq \iint\limits_R g(x,y)  dA
\end{aligned}
$$
## 2. Teorema de Fubini

### 2.1. Para regiones rectangulares

Si $f$ es continua en $R = [a,b] \times [c,d]$:


$$
\iint\limits_R f(x,y)  dA = \int_a^b \int_c^d f(x,y)  dy  dx = \int_c^d \int_a^b f(x,y)  dx  dy
$$
### 2.2. Para funciones separables

Si $f(x,y) = g(x)h(y)$:


$$
\iint\limits_R f(x,y)  dA = \left( \int_a^b g(x)  dx \right) \left( \int_c^d h(y)  dy \right)
$$
## 3. Integrales sobre regiones generales

### 3.1. Región Tipo I

$D = {(x,y) | a \leq x \leq b, g_1(x) \leq y \leq g_2(x)}$


$$
\iint\limits_D f(x,y)  dA = \int_a^b \int_{g_1(x)}^{g_2(x)} f(x,y)  dy  dx
$$
### 3.2. Región Tipo II

$D = {(x,y) | c \leq y \leq d, h_1(y) \leq x \leq h_2(y)}$


$$
\iint\limits_D f(x,y)  dA = \int_c^d \int_{h_1(y)}^{h_2(y)} f(x,y)  dx  dy
$$
## 4. Cambio de Variables

### 4.1. Jacobiano para dos variables

Para $T(u,v) = (x(u,v), y(u,v))$:


$$
J(u,v) = \frac{\partial(x,y)}{\partial(u,v)} = 
\begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix}
$$
### 4.2. Fórmula de cambio de variables


$$
\iint\limits_D f(x,y)  dx  dy = \iint\limits_{D^*} f(x(u,v), y(u,v)) \left| J(u,v) \right|  du  dv
$$
## 5. Coordenadas Polares

### 5.1. Transformación


$$
x = r \cos\theta, \quad y = r \sin\theta
$$
### 5.2. Jacobiano en polares


$$
J(r,\theta) = 
\begin{vmatrix}
\cos\theta & -r \sin\theta \\
\sin\theta & r \cos\theta
\end{vmatrix} = r
$$
### 5.3. Integral doble en polares


$$
\iint\limits_D f(x,y)  dA = \int_\alpha^\beta \int_{r_1(\theta)}^{r_2(\theta)} f(r\cos\theta, r\sin\theta)  r  dr  d\theta
$$
## 6. Aplicaciones de Integrales Dobles

### 6.1. Área de una región


$$
A = \iint\limits_D dA
$$
### 6.2. Volumen bajo una superficie


$$
V = \iint\limits_D f(x,y)  dA
$$
### 6.3. Masa y densidad

Para densidad $\rho(x,y)$:


$$
m = \iint\limits_D \rho(x,y)  dA
$$
### 6.4. Centro de masa


$$
\bar{x} = \frac{1}{m} \iint\limits_D x \rho(x,y)  dA, \quad \bar{y} = \frac{1}{m} \iint\limits_D y \rho(x,y)  dA
$$
### 6.5. Momentos de inercia


$$
I_x = \iint\limits_D y^2 \rho(x,y)  dA, \quad I_y = \iint\limits_D x^2 \rho(x,y)  dA
$$
## 7. Teorema de Green

### 7.1. Forma vectorial


$$
\oint_C \mathbf{F} \cdot d\mathbf{r} = \iint\limits_D \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right)  dA
$$
### 7.2. Forma escalar

$$
\oint_C P  dx + Q  dy = \iint\limits_D \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right)  dA
$$
### 7.3. Área usando Teorema de Green


$$
A = \frac{1}{2} \oint_C x  dy - y  dx
$$

---
## Referencias