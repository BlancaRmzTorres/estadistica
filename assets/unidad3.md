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

**📊 Ejemplo 1 (Variable aleatoria discreta)**  
- Experimento: lanzar un dado  
- Variable aleatoria \( X \): número obtenido  

Valores posibles:

$$\[
X = \{1, 2, 3, 4, 5, 6\}
\]$$

---

**📊 Ejemplo 2 (Variable aleatoria continua)**  
- Experimento: medir el tiempo que tarda un alumno en resolver un examen  
- Variable aleatoria \( X \): tiempo (en minutos)  

$$\[
X \in [0, \infty)
\]$$

---

# Diferencias entre Variable Aleatoria Discreta y Variable Aleatoria Continua

## Variable Aleatoria Discreta
Una **variable aleatoria discreta** es aquella que solo puede tomar **valores específicos y enumerables**, normalmente finitos o infinitos contables.

### Características
- Toma valores **puntuales** (generalmente enteros).
- Sus valores pueden **enumerarse**.
- Representa **conteos**.
- La probabilidad se asigna a **cada valor individual**.
- Se utiliza una **función de probabilidad** (*Probability Mass Function*, PMF).

### Ejemplos
- Número de llamadas en un día.
- Resultado de un dado (1 a 6).
- Número de fallas en una máquina.

---

## Variable Aleatoria Continua
Una **variable aleatoria continua** puede tomar **cualquier valor dentro de un intervalo**, es decir, **infinitos valores no contables**.

### Características
- Representa **mediciones**.
- La probabilidad no se asigna a un valor exacto, sino a **intervalos**.
- Se describe mediante una **función de densidad** (*Probability Density Function*, PDF).
- La probabilidad de que tome un valor exacto es **0**.

### Ejemplos
- Peso de una persona.
- Tiempo de espera.
- Temperatura ambiente.

---

# Tabla Comparativa

| Característica | Variable Aleatoria Discreta | Variable Aleatoria Continua |
|----------------|------------------------------|------------------------------|
| Tipo de valores | Específicos, enumerables | Infinitos dentro de intervalos |
| Naturaleza | Conteos | Mediciones |
| Probabilidad | A cada valor puntual | A intervalos |
| Función asociada | PMF (función de probabilidad) | PDF (función de densidad) |
| Ejemplos | Resultado de un dado, número de alumnos | Peso, tiempo, temperatura |

---

# 📊 Ejercicio 1: Variable Aleatoria Discreta  
Una tienda recibe llamadas de servicio al día. Sea la variable aleatoria  
\( X = \) número de llamadas por día.  
Se tiene la siguiente distribución de probabilidad:

| x (llamadas) | 0 | 1 | 2 | 3 |
|--------------|---|---|---|---|
| P(X = x)     | 0.1 | 0.3 | 0.4 | 0.2 |

### **a) Verificar que es una distribución válida**

Se comprueba que la suma de probabilidades sea 1:

$$\[
0.1 + 0.3 + 0.4 + 0.2 = 1
\]$$

Sí es una distribución válida.

### **b) Calcular la esperanza \(E[X]\)**

$$\[
E[X] = \sum x \cdot P(X=x)
\]$$

**La fórmula se le la esperanza de X es igual a la suma de cada valor x multiplicado por la probabilidad de que X sea igual a x**

$$\[
E[X] = 0(0.1) + 1(0.3) + 2(0.4) + 3(0.2)
\]$$

$$\[
E[X] = 0 + 0.3 + 0.8 + 0.6 = 1.7
\]$$

**Esperanza: \(E[X] = 1.7\) llamadas por día**

### **c) Calcular la varianza \(Var(X)\)**

Primero calculamos $$\(E[X^2]\)$$:

$$\[
E[X^2] = 0^2(0.1) + 1^2(0.3) + 2^2(0.4) + 3^2(0.2)
\]$$

$$\[
E[X^2] = 0 + 0.3 + 1.6 + 1.8 = 3.7
\]$$

Ahora aplicamos:

$$\[
Var(X) = E[X^2] - (E[X])^2
\]$$

$$\[
Var(X) = 3.7 - (1.7)^2 = 3.7 - 2.89 = 0.81
\]$$

**Varianza: $$\(Var(X) = 0.81\)$$**

**Interpretación:**
- En promedio, la tienda recibe 1.7 llamadas por día.
- La mayor parte del tiempo, la tienda recibirá entre 1 y 2 llamadas, y ese es el nivel típico de demanda.
- Las llamadas recibidas al día son relativamente consistentes.

---

# 📊 Ejercicio 2: Variable Aleatoria Discreta (Binomial)  
Un inspector revisa componentes electrónicos. Cada componente tiene una probabilidad de falla de \(p = 0.1\).  
Se inspeccionan \(n = 4\) componentes.

Sea:  
$$\[
X = \text{número de componentes defectuosos}
\]$$

### **a) Probabilidad de que fallen exactamente 2**

Usamos la distribución binomial:

$$\[
P(X=k) = \binom{n}{k} p^k (1-p)^{n-k}
\]$$

Sustituimos:

$$\[
P(X=2) = \binom{4}{2} (0.1)^2 (0.9)^2
\]$$

$$\[
= 6 \cdot 0.01 \cdot 0.81
\]$$

$$\[
= 6 \cdot 0.0081 = 0.0486
\]$$

**Probabilidad: 0.0486**

### **b) Probabilidad de que falle al menos 1**

$$\[
P(X \ge 1) = 1 - P(X=0)
\]$$

$$\[
P(X=0) = (0.9)^4 = 0.6561
\]$$

$$\[
P(X \ge 1) = 1 - 0.6561 = 0.3439
\]$$

**Probabilidad: 0.3439**

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

### 📊 Ejercicio 1

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


## 📊 Ejercicio 2 — Productos defectuosos

Una fábrica produce tornillos con una tasa de defectos de p = 0.05.  
Si se toman 20 tornillos al azar, ¿cuál es la probabilidad de que exactamente **1** sea defectuoso?

Datos:
- n = 20  
- k = 1  
- p = 0.05  

### Sustitución:
La función de probabilidad de una variable aleatoria binomial  
$$\( X \sim \text{Bin}(n, p) \)$$ está dada por:

$$\[
P(X = k) = \binom{n}{k} p^{k} (1 - p)^{n - k}
\]$$

donde:
- \( n \): número de ensayos  
- \( k \): número de éxitos  
- \( p \): probabilidad de éxito  
- \( \binom{n}{k} \): coeficiente binomial  

---

## Aplicación al ejercicio

Se tiene:
- $$\( n = 20 \)$$
- $$\( k = 1 \)$$
- $$\( p = 0.05 \)$$

Entonces:

$$\[
P(X = 1) = \binom{20}{1} (0.05)^1 (0.95)^{19}
\]$$

---

## Resultado

$$\[
P(X = 1) \approx 0.377
\]$$

---

## Notación completa

La variable aleatoria se puede expresar como:

$$\[
X \sim \text{Bin}(20, 0.05)
\]$$

$$\[
P(X = 1) = \binom{20}{1} (0.05)^1 (0.95)^{19} \approx 0.377
\]$$


**Respuesta:** La probabilidad de encontrar 1 tornillo defectuoso es ≈ **0.377**.


## 📊 Ejercicio 3 — Moneda equilibrada

Se lanza una moneda 6 veces. ¿Cuál es la probabilidad de obtener exactamente **3 caras**?

Datos:
- n = 6  
- k = 3  
- p = 0.5  

### Sustitución:
La función de probabilidad de una variable aleatoria binomial  
$$\( X \sim \text{Bin}(n, p) \)$$ está dada por:

$$\[
P(X = k) = \binom{n}{k} p^{k} (1 - p)^{n - k}
\]$$

donde:
- $$\( n \)$$: número de ensayos  
- $$\( k \)$$: número de éxitos  
- $$\( p \)$$: probabilidad de éxito  

---

## Aplicación al ejercicio

Se tiene:
- $$\( n = 6 \)$$
- $$\( k = 3 \)$$
- $$\( p = 0.5 \)$$

Entonces:

$$\[
P(X = 3) = \binom{6}{3} (0.5)^3 (0.5)^3
\]$$

---

## Resultado

$$\[
P(X = 3) = 0.3125
\]$$

---

## Notación completa

La variable aleatoria se puede expresar como:

$$\[
X \sim \text{Bin}(6, 0.5)
\]$$

$$\[
P(X = 3) = \binom{6}{3} (0.5)^3 (0.5)^3 = 0.3125
\]$$


**Respuesta:** La probabilidad de obtener 3 caras es **0.3125**.



## 📊 Ejercicio 4 — Éxito en llamadas

La probabilidad de que un agente cierre una venta en una llamada es 0.2.  
Si hace 12 llamadas, ¿cuál es la probabilidad de cerrar exactamente **2** ventas?

Datos:
- n = 12  
- k = 2  
- p = 0.2  

### Sustitución:
La función de probabilidad de una variable aleatoria binomial  
$$\( X \sim \text{Bin}(n, p) \)$$ está dada por:

$$\[
P(X = k) = \binom{n}{k} p^{k} (1 - p)^{n - k}
\]$$

donde:
- $$\( n \)$$: número de ensayos  
- $$\( k \)$$: número de éxitos  
- $$\( p \)$$: probabilidad de éxito  

---

## Aplicación al ejercicio

Se tiene:
- $$\( n = 12 \)$$
- $$\( k = 2 \)$$
- $$\( p = 0.2 \)$$

Entonces:

$$\[
P(X = 2) = \binom{12}{2} (0.2)^2 (0.8)^{10}
\]$$

---

## Resultado

$$\[
P(X = 2) \approx 0.283
\]$$

---

## Notación completa

La variable aleatoria se puede expresar como:

$$\[
X \sim \text{Bin}(12, 0.2)
\]$$

$$\[
P(X = 2) = \binom{12}{2} (0.2)^2 (0.8)^{10} \approx 0.283
\]$$


**Respuesta:** La probabilidad de cerrar 2 ventas es ≈ **0.283**.



## 📊 Ejercicio 5 — Encuesta

En una encuesta, 60% de los clientes dice estar satisfecho con el servicio.  
Si se eligen 5 clientes, ¿cuál es la probabilidad de que exactamente **4** estén satisfechos?

Datos:
- n = 5  
- k = 4  
- p = 0.6  

### Sustitución:
La función de probabilidad de una variable aleatoria binomial  
$$\( X \sim \text{Bin}(n, p) \)$$ está dada por:

$$\[
P(X = k) = \binom{n}{k} p^{k} (1 - p)^{n - k}
\]$$

donde:
- $$\( n \)$$: número de ensayos  
- $$\( k \)$$: número de éxitos  
- $$\( p \)$$: probabilidad de éxito  

---

## Aplicación al ejercicio

Se tiene:
- $$\( n = 5 \)$$
- $$\( k = 4 \)$$
- $$\( p = 0.6 \)$$

Entonces:

$$\[
P(X = 4) = \binom{5}{4} (0.6)^4 (0.4)^1
\]$$

---

## Resultado

$$\[
P(X = 4) \approx 0.2592
\]$$

---

## Notación completa

La variable aleatoria se puede expresar como:

$$\[
X \sim \text{Bin}(5, 0.6)
\]$$

$$\[
P(X = 4) = \binom{5}{4} (0.6)^4 (0.4)^1 \approx 0.2592
\]$$


**Respuesta:** La probabilidad de que 4 clientes estén satisfechos es ≈ **0.2592**.


#### Distribución de Poisson

Modela el número de eventos que ocurren en un intervalo fijo de tiempo o espacio.

##### Fórmula

$$\[
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}
\]$$

---
**La probabilidad de que la variable aleatoria X tome el valor k es igual a e elevado a menos lambda, multiplicado por lambda elevado a k, dividido entre 
k factorial.**

---

## Significado de cada elemento

### $$\(P(X = k)\)$$
- Probabilidad de que ocurran exactamente **$$\(k\)$$ eventos**.

---

### $$\(X\)$$
- Variable aleatoria.
- Representa el **número de veces que ocurre un evento** en un intervalo fijo.

---

### $$\(k\)$$
- Número entero no negativo:
$$\[
k = 0, 1, 2, 3, \dots
\]$$

---

### $$\(\lambda\)$$ (lambda)
- **Tasa promedio de ocurrencias**.
- Indica el número esperado de eventos en un intervalo.
- \(\lambda > 0\)

---

### $$\(e\)$$
- Número de Euler:
$$\[
e \approx 2.71828
\]$$

---

### $$\(e^{-\lambda}\)$$
- Probabilidad de que **no ocurra ningún evento** cuando el promedio es \(\lambda\).

---

### $$\(\lambda^{k}\)$$
- Ajusta la tasa promedio al número de eventos deseados.

---

### $$\(k!\) (k factorial)$$
- Factorial de \(k\):
$$\[
k! = k \cdot (k-1) \cdot (k-2) \cdots 1
\]$$

---

## Interpretación general

La distribución de Poisson se utiliza cuando:
- Los eventos ocurren de manera **aleatoria**
- En un **intervalo fijo**
- Con una **tasa promedio constante**
- Los eventos son **independientes**

---

## 📊 Ejemplo

Si el promedio de llamadas por hora es \(\lambda = 3\), la probabilidad de recibir exactamente 2 llamadas es:

$$\[
P(X = 2) = \frac{e^{-3}3^{2}}{2!}
\]$$

---

## Ejercicios – Distribución de Poisson

Recordemos que la función de probabilidad de Poisson es:

$$\[
P(X = k) = \frac{e^{-\lambda}\lambda^{k}}{k!}
\]$$

donde:
- $$\(X\)$$: número de eventos
- $$\(k\)$$: número exacto de eventos
- $$\(\lambda\)$$: tasa promedio de ocurrencias

---

## 📊 Ejercicio 1: Llamadas telefónicas

En promedio llegan **2 llamadas por hora** a un call center.

### ¿Cuál es la probabilidad de que lleguen exactamente 3 llamadas en una hora?

### Datos:
- $$\(\lambda = 2\)$$
- $$\(k = 3\)$$

### Cálculo:
$$\[
P(X = 3) = \frac{e^{-2}2^{3}}{3!}
\]$$

### Resultado:
$$\[
P(X = 3) \approx 0.1804
\]$$

---

## 📊 Ejercicio 2: Errores de escritura

Un documento tiene en promedio **1 error por página**.

### ¿Cuál es la probabilidad de que una página no tenga errores?

### Datos:
- $$\(\lambda = 1\)$$
- $$\(k = 0\)$$

### Cálculo:
$$\[
P(X = 0) = \frac{e^{-1}1^{0}}{0!}
\]$$

### Resultado:
$$\[
P(X = 0) \approx 0.3679
\]$$

---

## 📊 Ejercicio 3: Accidentes de tránsito

En una avenida ocurren en promedio **4 accidentes por mes**.

### ¿Cuál es la probabilidad de que ocurran exactamente 2 accidentes en un mes?

### Datos:
- $$\(\lambda = 4\)$$
- $$\(k = 2\)$$

### Cálculo:
$$\[
P(X = 2) = \frac{e^{-4}4^{2}}{2!}
\]$$

### Resultado:
$$\[
P(X = 2) \approx 0.1465
\]$$

---

## 📊 Ejercicio 4: Llegadas a una tienda

A una tienda llegan en promedio **6 clientes por hora**.

### ¿Cuál es la probabilidad de que lleguen exactamente 5 clientes en una hora?

### Datos:
- $$\(\lambda = 6\)$$
- $$\(k = 5\)$$

### Cálculo:
$$\[
P(X = 5) = \frac{e^{-6}6^{5}}{5!}
\]$$

### Resultado:
$$\[
P(X = 5) \approx 0.1606
\]$$

---

## 📊 Ejercicio 5: Fallas en una máquina

Una máquina presenta en promedio **0.5 fallas por día**.

### ¿Cuál es la probabilidad de que ocurra exactamente 1 falla en un día?

### Datos:
- $$\(\lambda = 0.5\)$$
- $$\(k = 1\)$$

### Cálculo:
$$\[
P(X = 1) = \frac{e^{-0.5}0.5^{1}}{1!}
\]$$

### Resultado:
$$\[
P(X = 1) \approx 0.3033
\]$$

---

## Conclusión

La distribución de Poisson es útil para modelar el número de eventos que ocurren:
- De forma aleatoria
- En un intervalo fijo
- Con una tasa promedio constante


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

##### 📊 Ejemplo (Uniforme Continua)

El tiempo de espera de un alumno está entre 5 y 15 minutos.

$$\[
a = 5,\quad b = 15
\]$$

$$\[
P(X < 10) = \frac{10 - 5}{15 - 5} = 0.5
\]$$

---

## Distribución Uniforme Continua

En una **distribución uniforme continua**, todos los valores del intervalo  
$$\([a, b]\)$$ tienen la **misma probabilidad**.

### Función de densidad

$$\[
f(x) =
\begin{cases}
\frac{1}{b - a}, & a \le x \le b \\
0, & \text{en otro caso}
\end{cases}
\]$$

---

## 📊 Ejercicio 1: Tiempo de espera

El tiempo de espera de un cliente en una tienda está distribuido uniformemente  
entre **5 y 15 minutos**.

### ¿Cuál es la probabilidad de que el cliente espere **menos de 10 minutos**?

### Datos:
- $$\(a = 5\)$$
- $$\(b = 15\)$$

### Cálculo:

$$\[
P(X < 10) = \frac{10 - 5}{15 - 5}
\]$$

### Resultado:

$$\[
P(X < 10) = \frac{5}{10} = 0.5
\]$$

---

## 📊 Ejercicio 2: Temperatura

La temperatura durante el día varía de forma uniforme entre  
**20 °C y 30 °C**.

### ¿Cuál es la probabilidad de que la temperatura sea **mayor a 25 °C**?

### Datos:
- $$\(a = 20\)$$
- $$\(b = 30\)$$

### Cálculo:

$$\[
P(X > 25) = \frac{30 - 25}{30 - 20}
\]$$

### Resultado:

$$\[
P(X > 25) = \frac{5}{10} = 0.5
\]$$

---

## Ejercicio 3: Llegada de un autobús

El tiempo de llegada de un autobús está distribuido uniformemente  
entre **0 y 20 minutos**.

### ¿Cuál es la probabilidad de que el autobús llegue entre  
**5 y 12 minutos**?

### Datos:
- $$\(a = 0\)$$
- $$\(b = 20\)$$

### Cálculo:

$$\[
P(5 \le X \le 12) = \frac{12 - 5}{20 - 0}
\]$$

### Resultado:

$$\[
P(5 \le X \le 12) = \frac{7}{20} = 0.35
\]$$

---

## Conclusión

En la distribución uniforme continua:
- Todas las longitudes de subintervalos tienen la misma probabilidad
- La probabilidad se calcula como la **razón de longitudes**
- No se requieren integrales para casos simples


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

##### 📊 Ejemplo (Distribución Normal)

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

## Distribución Normal

La **distribución normal** es la distribución continua más importante en estadística.
Se caracteriza por su forma de campana y está determinada por dos parámetros:
- $$\( \mu \)$$: media
- $$\( \sigma \)$$: desviación estándar

### Función de densidad

$$\[
f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}
\]$$

---

## 📊 Ejercicio 1: Calificaciones altas

Las calificaciones de un examen siguen una distribución normal con:
- $$\( \mu = 70 \)$$
- $$\( \sigma = 8 \)$$

### ¿Cuál es la probabilidad de que un estudiante obtenga una calificación **mayor a 78**?

### Paso 1: Estandarizar la variable

$$\[
Z = \frac{78 - 70}{8} = 1
\]$$

### Paso 2: Buscar el valor en la tabla Z

$$\[
P(Z > 1) \approx 0.1587
\]$$

### Resultado:

$$\[
P(X > 78) \approx 0.1587
\]$$

---

## 📊 Ejercicio 2: Estatura de personas

La estatura de un grupo de personas sigue una distribución normal con:
- $$\( \mu = 165 \)$$ cm
- $$\( \sigma = 6 \)$$ cm

### ¿Cuál es la probabilidad de que una persona mida entre **159 cm y 171 cm**?

### Paso 1: Calcular los valores Z

$$\[
Z_1 = \frac{159 - 165}{6} = -1
\]$$

$$\[
Z_2 = \frac{171 - 165}{6} = 1
\]$$

### Paso 2: Usar la tabla Z

$$\[
P(-1 < Z < 1) \approx 0.6826
\]$$

### Resultado:

$$\[
P(159 < X < 171) \approx 0.6826
\]$$

---

## 📊 Ejercicio 3: Tiempo de entrega

El tiempo de entrega de un servicio sigue una distribución normal con:
- $$\( \mu = 48 \)$$ horas
- $$\( \sigma = 5 \)$$ horas

### ¿Cuál es la probabilidad de que un pedido tarde **menos de 43 horas**?

### Paso 1: Estandarizar

$$\[
Z = \frac{43 - 48}{5} = -1
\]$$

### Paso 2: Buscar en la tabla Z

$$\[
P(Z < -1) \approx 0.1587
\]$$

### Resultado:

$$\[
P(X < 43) \approx 0.1587
\]$$

---

## Conclusión

Para resolver problemas con distribución normal:
1. Identifica $$\( \mu \)$$ y $$\( \sigma \)$$
2. Convierte la variable a $$\( Z \)$$
3. Usa la tabla Z
4. Interpreta el resultado


## 3.3 Exploración de distribuciones discretas y análisis de distribuciones continuas

---

### Valor esperado (media)

##### Fórmula (discreta)

$$\[
E(X) = \sum x_i P(x_i)
\]$$

---

### Ejemplo

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

## 3.3 Exploración de distribuciones discretas  
### Valor esperado y varianza

---

## Valor esperado (media)

Para una variable aleatoria discreta, el **valor esperado** se define como:

$$\[
E(X) = \sum x_i P(x_i)
\]$$

---

## Varianza

La **varianza** mide la dispersión de los valores respecto a la media y se define como:

$$\[
Var(X) = E(X^2) - [E(X)]^2
\]$$

---

## 📊 Ejercicio 1

Sea la variable aleatoria \(X\) con la siguiente distribución:

| X | P(X) |
|---|------|
| 0 | 0.2  |
| 1 | 0.5  |
| 2 | 0.3  |

### Cálculo del valor esperado

$$\[
E(X) = (0)(0.2) + (1)(0.5) + (2)(0.3)
\]$$

$$\[
E(X) = 0 + 0.5 + 0.6 = 1.1
\]$$

### Cálculo de \(E(X^2)\)

$$\[
E(X^2) = (0^2)(0.2) + (1^2)(0.5) + (2^2)(0.3)
\]$$

$$\[
E(X^2) = 0 + 0.5 + 1.2 = 1.7
\]$$

### Varianza

$$\[
Var(X) = 1.7 - (1.1)^2 = 0.49
\]$$

---

## 📊 Ejercicio 2

Sea la variable aleatoria \(Y\):

| Y | P(Y) |
|---|------|
| 1 | 0.4  |
| 2 | 0.4  |
| 3 | 0.2  |

### Valor esperado

$$\[
E(Y) = (1)(0.4) + (2)(0.4) + (3)(0.2)
\]$$

$$\[
E(Y) = 0.4 + 0.8 + 0.6 = 1.8
\]$$

### $$\(E(Y^2)\)$$

$$\[
E(Y^2) = (1^2)(0.4) + (2^2)(0.4) + (3^2)(0.2)
\]$$

$$\[
E(Y^2) = 0.4 + 1.6 + 1.8 = 3.8
\]$$

### Varianza

$$\[
Var(Y) = 3.8 - (1.8)^2 = 0.56
\]$$

---

## 📊 Ejercicio 3

Sea la variable aleatoria \(Z\):

| Z | P(Z) |
|---|------|
| 2 | 0.3  |
| 4 | 0.5  |
| 6 | 0.2  |

### Valor esperado

$$\[
E(Z) = (2)(0.3) + (4)(0.5) + (6)(0.2)
\]$$

$$\[
E(Z) = 0.6 + 2.0 + 1.2 = 3.8
\]$$

### $$\(E(Z^2)\)$$

$$\[
E(Z^2) = (2^2)(0.3) + (4^2)(0.5) + (6^2)(0.2)
\]$$

$$\[
E(Z^2) = 1.2 + 8.0 + 7.2 = 16.4
\]$$

### Varianza

$$\[
Var(Z) = 16.4 - (3.8)^2 = 1.96
\]$$

---

## Conclusión

- El **valor esperado** representa el promedio teórico de la variable
- La **varianza** mide qué tan dispersos están los valores
- Ambos conceptos son fundamentales para analizar distribuciones discretas

Las variables aleatorias y las distribuciones de probabilidad son herramientas fundamentales en estadística para modelar fenómenos aleatorios.  
Su análisis permite comprender el comportamiento de los datos y tomar mejores decisiones en contextos reales.

