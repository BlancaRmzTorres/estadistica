# 4. DISTRIBUCIONES MUESTRALES Y TEOREMA CENTRAL DEL LÍMITE

## 4.1 Concepto de poblaciones y muestras

### Población
Es el **conjunto total de elementos** sobre los cuales se desea realizar un estudio estadístico.

**Ejemplos:**
- Todos los estudiantes de una universidad  
- Todas las viviendas de una ciudad  
- Todos los productos fabricados en una semana  

Se denota comúnmente con **N** (tamaño de la población).

---

### Muestra
Es un **subconjunto representativo de la población**, seleccionado para realizar el estudio.

Se denota con **n** (tamaño de la muestra), donde:
\[
n < N
\]

---

### Parámetros vs Estadísticos

| Concepto | Descripción |
|--------|------------|
| Parámetro | Medida numérica de la población |
| Estadístico | Medida numérica de la muestra |

| Parámetro | Estadístico |
|---------|------------|
| Media poblacional $$(\(\mu\))$$ | Media muestral $$(\(\bar{x}\))$$ |
| Varianza poblacional $$(\(\sigma^2\))$$ | Varianza muestral $$(\(s^2\))$$ |
| Desviación estándar $$(\(\sigma\))$$ | Desviación estándar $$(\(s\))$$ |

---

### 🧮 Ejercicio 4.1.1

Una población de 500 empleados tiene un salario promedio real de \$12,000.

Se selecciona una muestra de 50 empleados y se obtiene un salario promedio de \$11,800.

**Identifica:**
- Población  
- Muestra  
- Parámetro  
- Estadístico

### Paso 1: Identificar la población

La **población** es el conjunto total de elementos que se desean estudiar.

En este caso:

$$\[
\text{Población} = 500 \text{ empleados}
\]$$

---

### Paso 2: Identificar la muestra

La **muestra** es un subconjunto representativo de la población.

En este problema:

$$\[
\text{Muestra} = 50 \text{ empleados}
\]$$

---

### Paso 3: Identificar el parámetro

Un **parámetro** es una medida numérica que describe una característica de la **población**.

El salario promedio real de toda la población es:

$$\[
\mu = 12{,}000
\]$$

Por lo tanto:

$$\[
\text{Parámetro} = \mu = 12{,}000
\]$$

---

### Paso 4: Identificar el estadístico

Un **estadístico** es una medida numérica calculada a partir de una **muestra**.

El salario promedio obtenido de la muestra es:

$$\[
\bar{x} = 11{,}800
\]$$

Por lo tanto:

$$\[
\text{Estadístico} = \bar{x} = 11{,}800
\]$$

#### Solución:
- **Población:** 500 empleados  
- **Muestra:** 50 empleados  
- **Parámetro:** $$\(\mu = 12,000\)$$  
- **Estadístico:** $$\(\bar{x} = 11,800\)$$

---

### 🧮 Ejercicio 4.1.2 (caso estadístico)

De una población de 10,000 viviendas se seleccionan 400 para estimar el consumo promedio de agua.

**Pregunta:**  
¿El consumo promedio calculado es un parámetro o un estadístico?

### Explicación paso a paso

1. **La población** está formada por todas las viviendas:
$$\[
\text{Población} = 10{,}000 \text{ viviendas}
\]$$

2. **La muestra** es solo una parte de la población:
$$\[
\text{Muestra} = 400 \text{ viviendas}
\]$$

3. El **consumo promedio de agua** se calcula **únicamente** con los datos de esas 400 viviendas, no con las 10,000.

4. Toda medida numérica que se obtiene a partir de una **muestra** se denomina **estadístico**.

---

### Respuesta final

El consumo promedio calculado es un **estadístico**, porque:

- Se obtiene a partir de una **muestra**
- No describe directamente a toda la población
- Se usa para **estimar** el valor real del parámetro poblacional

Matemáticamente, se representa como:

$$\[
\bar{x} = \text{consumo promedio muestral}
\]$$

---

### Conclusión

Un **estadístico** describe características de una **muestra**, mientras que un **parámetro** describe características de **toda la población**.

En este ejercicio, como el promedio se calcula con solo **400 de las 10,000 viviendas**, el resultado es un **estadístico**.

---

### 🧮 Ejercicio 4.1.3 (caso paramétrico)

#### Enunciado

En una ciudad existen **10,000 viviendas** y se conoce el **consumo promedio real de agua** de **todas** las viviendas.

El consumo promedio registrado es de **250 litros por vivienda al día**.

---

### Paso 1: Identificar la población

La población está formada por **todas las viviendas de la ciudad**:

$$\[
\text{Población} = 10{,}000 \text{ viviendas}
\]$$

---

### Paso 2: Identificar el valor calculado

El consumo promedio de agua fue calculado considerando **a todas las viviendas**, no solo una parte de ellas.

El valor obtenido es:

$$\[
\mu = 250 \text{ litros/día}
\]$$

---

### Paso 3: Clasificación del valor

Como el promedio se obtuvo usando **toda la población**, este valor corresponde a un **parámetro**.

---

### Respuesta final

| Concepto | Valor |
|--------|------|
| **Tipo de medida** | Parámetro |
| **Símbolo** | $$\(\mu\)$$ |
| **Valor** | 250 litros por vivienda al día |

---

### Conclusión

Un **parámetro** describe una característica de **toda la población**, mientras que un **estadístico** describe una característica obtenida a partir de una **muestra**.

En este ejemplo, el consumo promedio de **250 litros diarios** es un **parámetro**, ya que se calculó usando la información de las **10,000 viviendas**.


---

## 4.2 Estadísticos y distribuciones muestrales

### Estadístico
Es una función de los datos muestrales. Algunos ejemplos:

- Media muestral:
$$\[
\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i
\]$$

- Varianza muestral:
$$\[
s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2
\]$$

---

### Distribución muestral
Es la **distribución de probabilidad** de un estadístico cuando se consideran **todas las muestras posibles** de tamaño $$\(n\)$$.

La más importante es la **distribución muestral de la media**.

---

### Propiedades de la media muestral

Si la población tiene media $$\(\mu\)$$ y desviación estándar $$\(\sigma\)$$:

- Media de la media muestral:
$$\[
E(\bar{x}) = \mu
\]$$

- Varianza:
$$\[
Var(\bar{x}) = \frac{\sigma^2}{n}
\]$$

- Desviación estándar (error estándar):
$$\[
\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}
\]$$

---

### 🧮 Ejercicio 4.2.1

Una población tiene:
- $$\(\mu = 70\)$$
- $$\(\sigma = 10\)$$

Se toma una muestra de tamaño $$\(n = 25\)$$.

Calcula:
1. Media de la distribución muestral  
2. Desviación estándar de la media  

#### Solución:

1.  
$$\[
E(\bar{x}) = \mu = 70
\]$$

2.  
$$\[
\sigma_{\bar{x}} = \frac{10}{\sqrt{25}} = \frac{10}{5} = 2
\]$$

---

### 🧮 Ejercicio 4.2.2

Si $$\(\sigma = 12\)$$ y $$\(n = 36\)$$, calcula el error estándar.

#### Solución:

$$\[
\sigma_{\bar{x}} = \frac{12}{\sqrt{36}} = \frac{12}{6} = 2
\]$$

---

## 4.3 Teorema Central del Límite (TCL)

### Enunciado del Teorema Central del Límite

Si se toman muestras aleatorias de tamaño suficientemente grande $$(\(n \ge 30\))$$ de **cualquier población** con media $$\(\mu\)$$ y varianza finita $$\(\sigma^2\)$$, entonces la distribución muestral de la media:

- Se aproxima a una **distribución normal**
- Tiene media $$\(\mu\)$$
- Tiene desviación estándar $$\(\sigma / \sqrt{n}\)$$

$$\[
\bar{x} \sim N\left(\mu, \frac{\sigma}{\sqrt{n}}\right)
\]$$

#### La fórmula se lee "La media muestral se distribuye como una Normal con media μ y desviación estándar σ entre la raíz cuadrada de n."
---

### Importancia del TCL

- Permite usar la **distribución normal** aunque la población no sea normal  
- Es la base de:
  - Intervalos de confianza  
  - Pruebas de hipótesis  
- Justifica la estadística inferencial

---

### 🧮 Ejercicio 4.3.1

El peso promedio de una población es:
- $$\(\mu = 65\)$$ kg
- $$\(\sigma = 8\)$$ kg

Se toma una muestra de $$\(n = 64\)$$.

Calcula:
1. Media de la distribución muestral  
2. Desviación estándar  
3. Probabilidad de que $$\(\bar{x} > 66\)$$

---

#### Solución paso a paso

1.  
$$\[
E(\bar{x}) = 65]$$


## Relación entre $$\(E(\bar{x})\)$$ y $$\(\mu\)$$

En estadística, el valor esperado de la media muestral se expresa como:

$$\[
E(\bar{x}) = \mu
\]$$

### ¿Qué significa esto?

- $$\(E(\bar{x})\)$$ es el **valor esperado de la media muestral**.
- $$\(\bar{x}\)$$ es un **estimador insesgado** de la media poblacional.
- Por lo tanto, cuando tomamos muchas muestras aleatorias, el promedio de todas las medias muestrales converge al valor real de la población, $$\(\mu\)$$.

### Conclusión

La media muestral es un estimador insesgado de la media poblacional, de modo que:

$$\[
E(\bar{x}) = \mu
\]$$

1.  
$$\[
\sigma_{\bar{x}} = \frac{8}{\sqrt{64}} = \frac{8}{8} = 1
\]$$

2. Tipificación:
$$\[
Z = \frac{66 - 65}{1} = 1
\]$$

## Tipificación y cálculo de probabilidad

Queremos calcular la probabilidad:

\[
P(X > 66)
\]

Para una variable normal con media \(\mu = 65\) y desviación estándar \(\sigma = 1\).

---

## 1. Tipificación (transformar a un valor Z)

Aplicamos la fórmula:

\[
Z = \frac{X - \mu}{\sigma}
\]

Sustituimos:

\[
Z = \frac{66 - 65}{1} = 1
\]

---

## 2. Buscar en la tabla normal estándar

Buscamos:

\[
P(Z > 1)
\]

La tabla normalmente da valores de:

\[
P(Z < 1) = 0.8413
\]

Por lo tanto:

\[
P(Z > 1) = 1 - 0.8413 = 0.1587
\]

---

Buscando en la tabla normal:
$$\[
P(Z > 1) = 0.1587
\]$$

Esto significa que hay un **15.87%** de probabilidad de que la variable normal tome un valor mayor que 66.


### Tabla de la distribución normal

<img width="486" height="600" alt="imagen1" src="/assets/tabladistribucion.png" />

---

### 🧮 Ejercicio 4.3.2

Una máquina llena botellas con una media de 500 ml y desviación estándar de 15 ml.  
Se toman muestras de 36 botellas.

Calcula la probabilidad de que el promedio muestral sea menor a 495 ml.

---

#### Solución

1.  
$$\[
\sigma_{\bar{x}} = \frac{15}{\sqrt{36}} = 2.5
\]$$

2.  
$$\[
Z = \frac{495 - 500}{2.5} = -2
\]$$

3.  
$$\[
P(Z < -2) = 0.0228
\]$$

---

## Conclusión

Las distribuciones muestrales y el Teorema Central del Límite son pilares de la estadística inferencial, ya que permiten hacer inferencias confiables sobre poblaciones a partir de muestras.

---
