# 4. DISTRIBUCIONES MUESTRALES Y TEOREMA CENTRAL DEL LÍMITE  
**LIA02 – Ciclo Escolar**  
**Clave de la Asignatura:** ___________

---

## 4.1 Concepto de poblaciones y muestras

### 📘 Teoría

En estadística, se distinguen dos conceptos fundamentales:

### 🔹 Población
Es el **conjunto total de elementos** que se desea estudiar y que comparten una característica común.

Ejemplos:
- Todos los estudiantes de una universidad
- Todas las piezas producidas en una fábrica
- Todos los habitantes de un país

### 🔹 Muestra
Es un **subconjunto de la población**, seleccionado para realizar un estudio estadístico.

> El objetivo de una muestra es **obtener información sobre la población** sin analizar todos sus elementos.

---

### 📐 Parámetros poblacionales

Son valores numéricos que describen a la población:

- Media poblacional:  
\[
\mu = \frac{1}{N} \sum_{i=1}^{N} X_i
\]

- Varianza poblacional:  
\[
\sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (X_i - \mu)^2
\]

---

### 📐 Estadísticos muestrales

Son valores calculados a partir de una muestra:

- Media muestral:  
\[
\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
\]

- Varianza muestral:  
\[
s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2
\]

---

### ✏️ Ejercicio 1 (Paso a paso)

Una población tiene los valores:


#### Paso 1: Identificar población
Todos los datos forman la población, por lo tanto \( N = 5 \).

#### Paso 2: Calcular la media poblacional

\[
\mu = \frac{10 + 12 + 14 + 16 + 18}{5} = \frac{70}{5} = 14
\]

---

## 4.2 Estadísticos y distribuciones muestrales

### 📘 Teoría

Un **estadístico** es cualquier medida calculada a partir de una muestra.

Ejemplos:
- Media muestral (\(\bar{x}\))
- Proporción muestral (\(\hat{p}\))
- Varianza muestral (\(s^2\))

---

### 🔹 Distribución muestral

Es la **distribución de probabilidad** de un estadístico cuando se consideran **todas las muestras posibles** de un tamaño fijo \(n\).

Ejemplo:
- Distribución muestral de la media
- Distribución muestral de la proporción

---

### 📐 Media y varianza de la media muestral

Si la población tiene media \(\mu\) y varianza \(\sigma^2\), entonces:

- Media de la distribución muestral:
\[
E(\bar{x}) = \mu
\]

- Varianza de la media muestral:
\[
Var(\bar{x}) = \frac{\sigma^2}{n}
\]

- Desviación estándar (error estándar):
\[
\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}
\]

---

### ✏️ Ejercicio 2 (Paso a paso)

Una población tiene:
- Media poblacional \(\mu = 50\)
- Desviación estándar \(\sigma = 10\)
- Tamaño de muestra \(n = 25\)

#### Paso 1: Media de la distribución muestral
\[
E(\bar{x}) = 50
\]

#### Paso 2: Error estándar
\[
\sigma_{\bar{x}} = \frac{10}{\sqrt{25}} = \frac{10}{5} = 2
\]

---

## 4.3 Teorema Central del Límite (TCL)

### 📘 Teoría

El **Teorema Central del Límite (TCL)** establece que:

> Si el tamaño de la muestra es suficientemente grande (\(n \geq 30\)), la **distribución de la media muestral** se aproxima a una **distribución normal**, **independientemente de la forma de la población original**.

---

### 📌 Condiciones del TCL

- Muestras aleatorias
- Observaciones independientes
- Tamaño de muestra grande (\(n \geq 30\))

---

### 📐 Distribución normal estándar

Para estandarizar una media muestral se utiliza:

\[
Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}
\]

---

### ✏️ Ejercicio 3 (Paso a paso)

Una población tiene:
- \(\mu = 100\)
- \(\sigma = 20\)

Se toma una muestra de tamaño \(n = 64\).

¿Cuál es la probabilidad de que la media muestral sea mayor que 105?

---

#### Paso 1: Calcular el error estándar

\[
\sigma_{\bar{x}} = \frac{20}{\sqrt{64}} = \frac{20}{8} = 2.5
\]

---

#### Paso 2: Calcular el valor Z

\[
Z = \frac{105 - 100}{2.5} = \frac{5}{2.5} = 2
\]

---

#### Paso 3: Consultar la tabla Z

\[
P(Z > 2) = 0.0228
\]

---

### ✅ Respuesta final

La probabilidad de que la media muestral sea mayor que 105 es:

\[
\boxed{0.0228 \; (2.28\%)}
\]

---

## 📝 Importancia del Teorema Central del Límite

- Permite usar la distribución normal en inferencia estadística
- Fundamenta intervalos de confianza y pruebas de hipótesis
- Facilita el análisis de datos reales

---

📌 **Unidad:** Distribuciones Muestrales y TCL  
🎓 **Nivel:** Universitario  
📚 **Asignatura:** LIA02  



