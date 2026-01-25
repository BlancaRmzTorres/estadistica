# 4. DISTRIBUCIONES MUESTRALES Y TEOREMA CENTRAL DEL LÍMITE  
---

## 4.1 Concepto de poblaciones y muestras

En estadística, se distinguen dos conceptos fundamentales:

### Población
Es el **conjunto total de elementos** que se desea estudiar y que comparten una característica común.

Ejemplos:
- Todos los estudiantes de una universidad
- Todas las piezas producidas en una fábrica
- Todos los habitantes de un país

### Muestra
Es un **subconjunto de la población**, seleccionado para realizar un estudio estadístico.

> El objetivo de una muestra es **obtener información sobre la población** sin analizar todos sus elementos.

---

### Parámetros poblacionales

Son valores numéricos que describen a la población:

- Media poblacional:  
$$\[
\mu = \frac{1}{N} \sum_{i=1}^{N} X_i
\]$$

- Varianza poblacional:  
$$\[
\sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (X_i - \mu)^2
\]$$

---

### Estadísticos muestrales

Son valores calculados a partir de una muestra:

- Media muestral:  
$$\[
\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
\]$$

- Varianza muestral:  
$$\[
s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2
\]$$

---

### Ejercicio 1: Identificación de población y muestra

### Enunciado
Un investigador desea estudiar el **promedio de horas de estudio** de los alumnos de una preparatoria que tiene **800 estudiantes**.  
Para el estudio selecciona **50 estudiantes al azar**.

### Solución paso a paso

- **Población:**  
  Todos los **800 estudiantes** de la preparatoria.

- **Muestra:**  
  Los **50 estudiantes seleccionados**.

### Conclusión
- Población → 800 estudiantes  
- Muestra → 50 estudiantes  

---

## Ejercicio 2: Cálculo de la media poblacional (μ)

### Enunciado
Dada la siguiente población de datos:

$$\[
X = \{4, 6, 8, 10, 12\}
\]$$

Calcular la **media poblacional**.

---

### Paso 1: Fórmula

$$\[
\mu = \frac{1}{N}\sum_{i=1}^{N} X_i
\]$$

---

### Paso 2: Número de datos

$$\[
N = 5
\]$$

---

###  Paso 3: Suma de los valores

$$\[
\sum X_i = 4 + 6 + 8 + 10 + 12 = 40
\]$$

---

### Paso 4: Sustitución

$$\[
\mu = \frac{40}{5} = 8
\]$$

---

### Resultado

$$\[
\mu = 8
\]$$

---

## Ejercicio 3: Varianza poblacional (σ²)

### Enunciado
Usando la misma población del ejercicio anterior:

$$\[
X = \{4, 6, 8, 10, 12\}
\]$$

Calcular la **varianza poblacional**.

---

### Paso 1: Media poblacional

$$\[
\mu = 8
\]$$

---

### Paso 2: Cálculo de las diferencias al cuadrado

| $$\(X_i\)$$ | $$\(X_i - \mu\)$$ | $$\((X_i - \mu)^2\)$$ |
|--------|---------------|------------------|
| 4 | \(4 - 8 = -4\) | 16 |
| 6 | \(6 - 8 = -2\) | 4 |
| 8 | \(8 - 8 = 0\) | 0 |
| 10 | \(10 - 8 = 2\) | 4 |
| 12 | \(12 - 8 = 4\) | 16 |

---

### Paso 3: Suma de los cuadrados

$$\[
\sum (X_i - \mu)^2 = 16 + 4 + 0 + 4 + 16 = 40
\]$$

---

### Paso 4: Aplicar la fórmula

$$\[
\sigma^2 = \frac{40}{5} = 8
\]$$

---

### Resultado

$$\[
\sigma^2 = 8
\]$$

---

## Ejercicio 4: Población y muestra en un contexto real

### Enunciado
Una fábrica produce **2,000 piezas al día**.  
El departamento de calidad revisa **120 piezas**.

---

### Solución

- **Población:**  
  $$\[
  N = 2000 \text{ piezas}
  \]$$

- **Muestra:**  
  $$\[
  n = 120 \text{ piezas}
  \]$$

---

### Conclusión
La muestra permite analizar la calidad sin revisar toda la producción.

---

## Ejercicio 5: Parámetro poblacional vs estadístico muestral

### Enunciado
Clasifica los siguientes valores:

1. La **media de edad de todos los habitantes** de una ciudad  
2. El **promedio de edad de 100 personas** seleccionadas

---

### Solución

1. **Parámetro poblacional**  
   $$\[
   \mu \rightarrow \text{describe a toda la población}
   \]$$

2. **Estadístico muestral**  
   $$\[
   \bar{x} \rightarrow \text{calculado a partir de una muestra}
   \]$$

---

## Resumen

- **Población:** conjunto total de elementos  
- **Muestra:** subconjunto representativo  
- **Parámetros poblacionales:**  
  - Media → $$\( \mu \)$$
  - Varianza → $$\( \sigma^2 \)$$  
- Se usan cuando se analiza **toda la población**


## 4.2 Estadísticos y distribuciones muestrales

### Teoría

Un **estadístico** es cualquier medida calculada a partir de una muestra.

Ejemplos:
- Media muestral $$(\(\bar{x}\))$$
- Proporción muestral $$(\(\hat{p}\))$$
- Varianza muestral $$(\(s^2\))$$

---

### Distribución muestral

Es la **distribución de probabilidad** de un estadístico cuando se consideran **todas las muestras posibles** de un tamaño fijo \(n\).

Ejemplo:
- Distribución muestral de la media
- Distribución muestral de la proporción

---

### Media y varianza de la media muestral

Si la población tiene media $$\(\mu\)$$ y varianza $$\(\sigma^2\)$$, entonces:

- Media de la distribución muestral:
$$\[
E(\bar{x}) = \mu
\]$$

- Varianza de la media muestral:
$$\[
Var(\bar{x}) = \frac{\sigma^2}{n}
\]$$

- Desviación estándar (error estándar):
$$\[
\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}
\]$$

---

### Ejercicio 2 (Paso a paso)

Una población tiene:
- Media poblacional $$\(\mu = 50\)$$
- Desviación estándar $$\(\sigma = 10\)$$
- Tamaño de muestra $$\(n = 25\)$$

#### Paso 1: Media de la distribución muestral
$$\[
E(\bar{x}) = 50
\]$$

#### Paso 2: Error estándar
$$\[
\sigma_{\bar{x}} = \frac{10}{\sqrt{25}} = \frac{10}{5} = 2
\]$$

---

## 4.3 Teorema Central del Límite (TCL)

### Teoría

El **Teorema Central del Límite (TCL)** establece que:

> Si el tamaño de la muestra es suficientemente grande $$(\(n \geq 30\))$$, la **distribución de la media muestral** se aproxima a una **distribución normal**, **independientemente de la forma de la población original**.

---

### Condiciones del TCL

- Muestras aleatorias
- Observaciones independientes
- Tamaño de muestra grande (\(n \geq 30\))

---

### Distribución normal estándar

Para estandarizar una media muestral se utiliza:

$$\[
Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}
\]$$

---

### Ejercicio 3 (Paso a paso)

Una población tiene:
- $$\(\mu = 100\)$$
- $$\(\sigma = 20\)$$

Se toma una muestra de tamaño $$\(n = 64\)$$.

¿Cuál es la probabilidad de que la media muestral sea mayor que 105?

---

#### Paso 1: Calcular el error estándar

$$\[
\sigma_{\bar{x}} = \frac{20}{\sqrt{64}} = \frac{20}{8} = 2.5
\]$$

---

#### Paso 2: Calcular el valor Z

$$\[
Z = \frac{105 - 100}{2.5} = \frac{5}{2.5} = 2
\]$$

---

#### Paso 3: Consultar la tabla Z

$$\[
P(Z > 2) = 0.0228
\]$$

---

### Respuesta final

La probabilidad de que la media muestral sea mayor que 105 es:

$$
0.0228 \quad (2.28\%)
$$
---

## Importancia del Teorema Central del Límite

- Permite usar la distribución normal en inferencia estadística
- Fundamenta intervalos de confianza y pruebas de hipótesis
- Facilita el análisis de datos reales

---




