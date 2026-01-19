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

$$\[
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}
\]$$

---

##### Ejemplo (Distribución Binomial)

Un examen tiene 10 preguntas de opción múltiple.  
La probabilidad de contestar correctamente una pregunta es 0.7.

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

