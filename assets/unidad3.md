# Unidad 3. Variables Aleatorias y Distribuciones de Probabilidad

## Introducción

En estadística, muchos fenómenos no pueden predecirse con exactitud, pero sí pueden modelarse mediante probabilidades.  
Las **variables aleatorias** y las **distribuciones de probabilidad** permiten describir matemáticamente estos fenómenos y analizar su comportamiento.

---

## 3.1 Definición y características de variables aleatorias

### ¿Qué es una variable aleatoria?

Una **variable aleatoria** es una función que asigna un valor numérico a cada resultado posible de un experimento aleatorio.

> No es aleatoria en sí misma, sino que depende del azar del experimento.

---

### Tipos de variables aleatorias

| Tipo | Descripción |
|------|-------------|
| Discreta | Toma valores contables (0, 1, 2, 3, …) |
| Continua | Toma valores en un intervalo real |

---

### Ejemplos

**Ejemplo 1 (Variable aleatoria discreta)**  
- Experimento: lanzar un dado  
- Variable aleatoria \( X \): número obtenido  

Valores posibles:

$$\[
X = \{1, 2, 3, 4, 5, 6\}
\]$$

---

**Ejemplo 2 (Variable aleatoria continua)**  
- Experimento: medir el tiempo que tarda un alumno en resolver un examen  
- Variable aleatoria \( X \): tiempo (en minutos)  

$$\[
X \in [0, \infty)
\]$$

---

### Función de probabilidad

- Variables discretas: **función de masa de probabilidad (fmp)**
- Variables continuas: **función de densidad de probabilidad (fdp)**

---

## 3.2 Distribuciones discretas y continuas de probabilidad

---

### Distribuciones discretas

#### Distribución Binomial

Modela el número de éxitos en un número fijo de ensayos independientes.

**Condiciones:**
- Número fijo de ensayos $$\( n \)$$
- Dos resultados posibles (éxito / fracaso)
- Probabilidad constante $$\( p \)$$

---

##### Fórmula

La fórmula de la distribución binomial se escribe así:

$$\[
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}
\]$$

---

Lectura:
**"La probabilidad de que X sea igual a k es igual a n sobre k, multiplicado por p a la k, por uno menos p a la (n menos k)."**

En un problema de distribución binomial, los valores clave son:

- n → número total de ensayos (por ejemplo, número de preguntas)
- p → probabilidad de éxito en un ensayo (por ejemplo, contestar bien)
- k → número de éxitos que queremos calcular

##### Ejemplo (Distribución Binomial)

Un examen tiene 10 preguntas… 
¿Cuál es la probabilidad de contestar correctamente 8 preguntas si la probabilidad de acertar cada una es 0.7?

**Datos:**
- $$\( n = 10 \)$$
- $$\( k = 8 \)$$
- $$\( p = 0.7 \)$$

$$\[
P(X = 8) = \binom{10}{8}(0.7)^8(0.3)^2
\]$$

$$\[
P(X = 8) \approx 0.233
\]$$

---

### Ejemplo para entenderlo mejor

**¿Cuál es la probabilidad de que saques exactamente 7 aciertos?**
→ k sería 7

**¿Cuál es la probabilidad de que aciertes todas (10)?**
→ k sería 10

**¿Cuál es la probabilidad de que solo aciertes 3?**
→ k sería 3


## Ejemplo 2 — Productos defectuosos

Una fábrica produce tornillos con una tasa de defectos de p = 0.05.  
Si se toman 20 tornillos al azar, ¿cuál es la probabilidad de que exactamente **1** sea defectuoso?

Datos:
- n = 20  
- k = 1  
- p = 0.05  

### Sustitución:
P(X = 1) = C(20, 1) * (0.05)^1 * (0.95)^19  
P(X = 1) ≈ 0.377

**Respuesta:** La probabilidad de encontrar 1 tornillo defectuoso es ≈ **0.377**.


## Ejemplo 3 — Moneda equilibrada

Se lanza una moneda 6 veces. ¿Cuál es la probabilidad de obtener exactamente **3 caras**?

Datos:
- n = 6  
- k = 3  
- p = 0.5  

### Sustitución:
P(X = 3) = C(6, 3) * (0.5)^3 * (0.5)^3  
P(X = 3) = 0.3125

**Respuesta:** La probabilidad de obtener 3 caras es **0.3125**.



## Ejemplo 4 — Éxito en llamadas

La probabilidad de que un agente cierre una venta en una llamada es 0.2.  
Si hace 12 llamadas, ¿cuál es la probabilidad de cerrar exactamente **2** ventas?

Datos:
- n = 12  
- k = 2  
- p = 0.2  

### Sustitución:
P(X = 2) = C(12, 2) * (0.2)^2 * (0.8)^10  
P(X = 2) ≈ 0.283

**Respuesta:** La probabilidad de cerrar 2 ventas es ≈ **0.283**.



## Ejemplo 5 — Encuesta

En una encuesta, 60% de los clientes dice estar satisfecho con el servicio.  
Si se eligen 5 clientes, ¿cuál es la probabilidad de que exactamente **4** estén satisfechos?

Datos:
- n = 5  
- k = 4  
- p = 0.6  

### Sustitución:
P(X = 4) = C(5, 4) * (0.6)^4 * (0.4)^1  
P(X = 4) ≈ 0.2592

**Respuesta:** La probabilidad de que 4 clientes estén satisfechos es ≈ **0.2592**.


#### Distribución de Poisson

Modela el número de eventos que ocurren en un intervalo fijo de tiempo o espacio.

##### Fórmula

$$\[
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}
\]$$

---

##### Ejemplo (Distribución de Poisson)

En promedio, llegan 3 personas por minuto a una ventanilla.

**Datos:**
- $$\( \lambda = 3 \)$$
- $$\( k = 5 \)$$

$$\[
P(X = 5) \approx 0.1008
\]$$

---

### Distribuciones continuas

---

#### Distribución Uniforme Continua

Todos los valores del intervalo tienen la misma probabilidad.

##### Función de densidad

$$\[
f(x) =
\begin{cases}
\frac{1}{b - a}, & a \le x \le b \\
0, & \text{en otro caso}
\end{cases}
\]$$

---

##### Ejemplo (Uniforme Continua)

El tiempo de espera de un alumno está entre 5 y 15 minutos.

$$\[
a = 5,\quad b = 15
\]$$

$$\[
P(X < 10) = \frac{10 - 5}{15 - 5} = 0.5
\]$$

---

#### Distribución Normal

Es la distribución continua más importante en estadística.

##### Función de densidad

$$\[
f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}
\]$$

Donde:
- $$\( \mu \) = media$$  
- $$\( \sigma \) = desviación estándar$$  

---

##### Ejemplo (Distribución Normal)

Las calificaciones siguen una distribución normal con:
- $$\( \mu = 75 \)$$
- $$\( \sigma = 10 \)$$

$$\[
Z = \frac{85 - 75}{10} = 1
\]$$

$$\[
P(X > 85) \approx 0.1587
\]$$

---

## 3.3 Exploración de distribuciones discretas y análisis de distribuciones continuas

---

### Valor esperado (media)

##### Fórmula (discreta)

$$\[
E(X) = \sum x_i P(x_i)
\]$$

---

##### Ejemplo

| X | P(X) |
|---|------|
| 0 | 0.2 |
| 1 | 0.5 |
| 2 | 0.3 |

$$\[
E(X) = 1.1
\]$$

---

### Varianza

$$\[
Var(X) = E(X^2) - [E(X)]^2
\]$$

---

### Interpretación gráfica

- Distribuciones discretas: gráficas de barras
- Distribuciones continuas: curvas suaves
- El área bajo la curva representa la probabilidad

---

## Conclusión

Las variables aleatorias y las distribuciones de probabilidad son herramientas fundamentales en estadística para modelar fenómenos aleatorios.  
Su análisis permite comprender el comportamiento de los datos y tomar mejores decisiones en contextos reales.

