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

#### Solución:
- **Población:** 500 empleados  
- **Muestra:** 50 empleados  
- **Parámetro:** $$\(\mu = 12,000\)$$  
- **Estadístico:** $$\(\bar{x} = 11,800\)$$

---

### 🧮 Ejercicio 4.1.2

De una población de 10,000 viviendas se seleccionan 400 para estimar el consumo promedio de agua.

**Pregunta:**  
¿El consumo promedio calculado es un parámetro o un estadístico?

#### Solución:
Es un **estadístico**, porque proviene de una **muestra**.

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
Es la **distribución de probabilidad** de un estadístico cuando se consideran **todas las muestras posibles** de tamaño \(n\).

La más importante es la **distribución muestral de la media**.

---

### Propiedades de la media muestral

Si la población tiene media \(\mu\) y desviación estándar \(\sigma\):

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

Si se toman muestras aleatorias de tamaño suficientemente grande (\(n \ge 30\)) de **cualquier población** con media \(\mu\) y varianza finita \(\sigma^2\), entonces la distribución muestral de la media:

- Se aproxima a una **distribución normal**
- Tiene media $$\(\mu\)$$
- Tiene desviación estándar $$\(\sigma / \sqrt{n}\)$$

$$\[
\bar{x} \sim N\left(\mu, \frac{\sigma}{\sqrt{n}}\right)
\]$$

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
E(\bar{x}) = 65
\]$$

2.  
$$\[
\sigma_{\bar{x}} = \frac{8}{\sqrt{64}} = \frac{8}{8} = 1
\]$$

3. Tipificación:
$$\[
Z = \frac{66 - 65}{1} = 1
\]$$

Buscando en la tabla normal:
$$\[
P(Z > 1) = 0.1587
\]$$

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
