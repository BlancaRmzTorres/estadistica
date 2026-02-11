# 6. REGRESIÓN LINEAL Y ANÁLISIS DE VARIANZA (ANOVA)

La regresión y el análisis de varianza son herramientas fundamentales de la **estadística inferencial** que permiten analizar relaciones entre variables, explicar fenómenos y tomar decisiones basadas en datos.

---

## 6.1 Modelos de regresión lineal simple y múltiple

La **regresión lineal** estudia la relación entre una variable dependiente y una o más variables independientes.

---

### 6.1.1 Regresión lineal simple

Se utiliza cuando existe **una variable independiente**.

#### Modelo matemático

$$\[
Y = \beta_0 + \beta_1 X + \varepsilon
\]$$

**Y es igual a una constante (beta cero) más un coeficiente (beta uno) multiplicado por la variable X, más un término de error épsilon.**

Donde:
- $$\(Y\)$$: variable dependiente  
- $$\(X\)$$: variable independiente  
- $$\(\beta_0\)$$: intercepto (ordenada al origen)  
- $$\(\beta_1\)$$: pendiente  
- $$\(\varepsilon\)$$: error aleatorio  

---

### Estimación de los parámetros

$$\[
\beta_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}
\]$$

**Beta uno es igual a la suma de los productos de las desviaciones de X respecto a su media por las desviaciones de Y respecto a su media, dividido entre la suma de los cuadrados de las desviaciones de X respecto a su media.**

$$\[
\beta_0 = \bar{y} - \beta_1 \bar{x}
\]$$

**Beta cero es igual a la media de Y menos beta uno multiplicado por la media de X**

- **β₁ = pendiente**
  - Indica cuánto cambia Y cuando X aumenta en 1 unidad.

- **β₀ = intercepto**
  - Es el valor de Y cuando X = 0.

---

## Ejercicio 1: Cálculo de $$\( \beta_1 \)$$ y $$\( \beta_0 \)$$

Se tienen los siguientes datos para ajustar un **modelo de regresión lineal simple**:

### Datos

| X | Y |
|---|---|
| 1 | 2 |
| 2 | 3 |
| 3 | 5 |
| 4 | 4 |

---

## 1. Cálculo de las medias

### Media de $$\( X \)$$

$$\[
\bar{x} = \frac{1 + 2 + 3 + 4}{4} = 2.5
\]$$

### Media de $$\( Y \)$$

$$\[
\bar{y} = \frac{2 + 3 + 5 + 4}{4} = 3.5
\]$$

---

## 2. Cálculo de $$\( \beta_1 \)$$

### Fórmula

$$\[
\beta_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}
\]$$

---

### Tabla de cálculos

| $$\(x_i\)$$ | $$\(y_i\)$$ | $$\(x_i - \bar{x}\)$$ | $$\(y_i - \bar{y}\)$$ | $$\((x_i-\bar{x})(y_i-\bar{y})\)$$ | $$\((x_i-\bar{x})^2\)$$ |
|--------|--------|------------------|------------------|-------------------------------|-------------------|
| 1 | 2 | -1.5 | -1.5 | 2.25 | 2.25 |
| 2 | 3 | -0.5 | -0.5 | 0.25 | 0.25 |
| 3 | 5 | 0.5 | 1.5 | 0.75 | 0.25 |
| 4 | 4 | 1.5 | 0.5 | 0.75 | 2.25 |

---

### Sumas

$$\[
\sum (x_i - \bar{x})(y_i - \bar{y}) = 4
\]$$

$$\[
\sum (x_i - \bar{x})^2 = 5
\]$$

---

### Cálculo de $$\( \beta_1 \)$$

$$\[
\beta_1 = \frac{4}{5} = 0.8
\]$$

---

## 3. Cálculo de $$\( \beta_0 \)$$

### Fórmula

$$\[
\beta_0 = \bar{y} - \beta_1 \bar{x}
\]$$

**Beta cero es igual a y barra menos beta uno por x barra.**

### Sustitución

$$\[
\beta_0 = 3.5 - (0.8)(2.5)
\]$$

$$\[
\beta_0 = 3.5 - 2 = 1.5
\]$$

---

### ✅ Modelo final de regresión

$$\[
\hat{y} = 1.5 + 0.8x
\]$$

---

### Interpretación

- Cuando $$\( x = 0 \)$$, el valor estimado de $$\( y \)$$ es **1.5**
- Por cada unidad que aumenta $$\( x \)$$, $$\( y \)$$ aumenta en promedio **0.8 unidades**

<img width="486" height="600" alt="imagen1" src="/assets/grafica_regresion.png" />

---
## Ejercicio 2: Cálculo de $$\( \beta_1 \)$$ y $$\( \beta_0 \)$$

Se tienen los siguientes datos para ajustar un **modelo de regresión lineal simple**:

### Datos

| X | Y |
|---|---|
| 2 | 4 |
| 5 | 7 |
| 7 | 10 |
| 9 | 15 |

---

## 1. Cálculo de las medias

### Media de $$\( X \)$$

$$\[
\bar{x} = \frac{2 + 5 + 7 + 9}{4} = 5.75
\]$$

### Media de $$\( Y \)$$

$$\[
\bar{y} = \frac{4 + 7 + 10 + 15}{4} = 9
\]$$

---

## 2. Cálculo de $$\( \beta_1 \)$$

### Fórmula

$$\[
\beta_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}
\]$$

---

### Tabla de cálculos

| $$\(x_i\)$$ | $$\(y_i\)$$ | $$\(x_i - \bar{x}\)$$ | $$\(y_i - \bar{y}\)$$ | $$\((x_i-\bar{x})(y_i-\bar{y})\)$$ | $$\((x_i-\bar{x})^2\)$$ |
|--------|--------|------------------|------------------|-------------------------------|-------------------|
| 2 | 4 | -3.75 | -5 | 18.75 | 14.06 |
| 5 | 7 | -0.75 | -2 | 1.50 | 0.56 |
| 7 | 10 | 1.25 | 1 | 1.25 | 1.56 |
| 9 | 15 | 3.25 | 6 | 19.50 | 10.56 |

---

### Sumas

$$\[
\sum (x_i - \bar{x})(y_i - \bar{y}) = 41
\]$$

$$\[
\sum (x_i - \bar{x})^2 = 26.75
\]$$

---

### Cálculo de $$\( \beta_1 \)$$

$$\[
\beta_1 = \frac{41}{26.75} \approx 1.532
\]$$

---

## 3. Cálculo de $$\( \beta_0 \)$$

### Fórmula

$$\[
\beta_0 = \bar{y} - \beta_1 \bar{x}
\]$$

### Sustitución

$$\[
\beta_0 = 9 - (1.532)(5.75)
\]$$

$$\[
\beta_0 = 9 - 8.799 = 0.201
\]$$

---

## ✅ Modelo final de regresión

$$\[
\hat{y} = 0.201 + 1.532x
\]$$

---

### Interpretación

- El intercepto indica que cuando $$\( x = 0 \)$$, el valor estimado de $$\( y \)$$ es **0.201**
- Por cada unidad que aumenta $$\( x \)$$, el valor de $$\( y \)$$ aumenta en promedio **1.532 unidades**

<img width="486" height="600" alt="imagen1" src="/assets/grafica2.png" />

---


### 6.1.2 Regresión lineal múltiple

Se utiliza cuando existen **dos o más variables independientes**.

#### Modelo matemático

$$\[
Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \cdots + \beta_k X_k + \varepsilon
\]$$

###### **Y es igual a beta cero más beta uno por equis uno, más beta dos por equis dos, y así sucesivamente hasta beta k por equis k, más épsilon.**
---

### Ejemplo de aplicación

- $$\(Y\)$$: salario  
- $$\(X_1\)$$: años de experiencia  
- $$\(X_2\)$$: nivel educativo  

Este modelo permite analizar el **efecto individual de cada variable** sobre la respuesta.

### 📊 Ejercicio 1 — Salario según experiencia y nivel educativo

### ✏️ Modelo estimado

$$
\hat{Y} = 8500 + 1200X_1 + 2500X_2
$$

**Donde:**

- $$Y$$: Salario mensual  
- $$X_1$$: Años de experiencia  
- $$X_2$$: Nivel educativo  
  - 0 = Educación básica  
  - 1 = Educación universitaria  

---

### 📘 Interpretación de coeficientes

### ➤ Intercepto $$ \beta_0 = 8500 $$

Representa el salario de una persona **sin experiencia** ($X_1 = 0$) y con **educación básica** ($X_2 = 0$).

---

### ➤ Experiencia $$ \beta_1 = 1200 $$

Por cada año adicional de experiencia, el salario aumenta en:

$$
\$1,200
$$

Manteniendo constante el nivel educativo.

---

### ➤ Educación $$ \beta_2 = 2500 $$

Tener educación universitaria incrementa el salario en:

$$
\$2,500
$$

En comparación con una persona con educación básica, manteniendo constante la experiencia.

---

### 📐 Cálculo de un ejemplo

Calcular el salario estimado para una persona con:

- 5 años de experiencia  
- Nivel educativo universitario $$($X_2 = 1$)$$

---

### 🧮 Sustitución en el modelo

$$
\hat{Y} = 8500 + 1200(5) + 2500(1)
$$

---

### 🔎 Desglose paso a paso

**Paso 1:**

$$
1200 \times 5 = 6000
$$

**Paso 2:**

$$
2500 \times 1 = 2500
$$

**Paso 3:**

$$
8500 + 6000 + 2500 = 17000
$$

---

### ✅ Resultado final

$$
\hat{Y} = \mathbf{17,000}
$$

📌 **Interpretación:**  
Una persona con **5 años de experiencia** y **educación universitaria** tiene un salario mensual estimado de **$17,000** según el modelo de regresión.


### 🏠 Ejercicio 2 — Precio de casa según tamaño y antigüedad

### ✏️ Modelo estimado

$$
\hat{Y} = 95{,}000 + 1{,}200X_1 - 800X_2
$$

**Donde:**

- $$Y$$: Precio estimado (pesos)  
- $$X_1$$: Metros cuadrados  
- $$X_2$$: Antigüedad en años  

---

### 📘 Interpretación de coeficientes

### ➤ Intercepto $$ \beta_0 = 95{,}000 $$

Precio base teórico cuando $X_1 = 0$ y $X_2 = 0$.  
(No tiene interpretación literal práctica, ya que una casa no puede tener 0 m²).

---

### ➤ Tamaño $$ \beta_1 = 1{,}200 $$

Cada metro cuadrado adicional incrementa el precio en:

$$
\$1{,}200
$$

Manteniendo constante la antigüedad.

---

### ➤ Antigüedad $$ \beta_2 = -800 $$

Cada año adicional de antigüedad reduce el precio en:

$$
\$800
$$

Manteniendo constante el tamaño.

---

### 📐 Cálculo de un ejemplo

Casa con:

- 140 m²  
- 8 años de antigüedad  

---

### 🧮 Sustitución en el modelo

$$
\hat{Y} = 95{,}000 + 1{,}200(140) - 800(8)
$$

---

### 🔎 Desglose paso a paso

**Paso 1:**

$$
1{,}200 \times 140 = 168{,}000
$$

**Paso 2:**

$$
800 \times 8 = 6{,}400
$$

**Paso 3:**

$$
95{,}000 + 168{,}000 = 263{,}000
$$

**Paso 4:**

$$
263{,}000 - 6{,}400 = 256{,}600
$$

---

### ✅ Resultado final

$$
\hat{Y} = \mathbf{256{,}600}
$$

📌 **Interpretación:**  
Una casa de **140 m²** y **8 años de antigüedad** tiene un precio estimado de **$256,600 pesos** según el modelo de regresión.


---

## 6.2 Generalizaciones del modelo de regresión lineal y regresión no lineal

Cuando la relación entre variables no es lineal, se utilizan modelos más flexibles.

---

### 6.2.1 Regresión polinómica

Modelo:

$$\[
Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \varepsilon
\]$$

### 📊 Lectura e interpretación de la fórmula

### ✏️ Modelo

$$
Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \varepsilon
$$

---

### 📖 ¿Cómo se lee la fórmula?

Se lee:

> **“Y es igual a beta cero más beta uno por X más beta dos por X al cuadrado más épsilon.”**

---

### 📘 Interpretación estadística

- $Y$: Variable dependiente (lo que queremos explicar o predecir).
- $\beta_0$: Intercepto (valor de $Y$ cuando $X = 0$).
- $\beta_1 X$: Efecto lineal de $X$ sobre $Y$.
- $\beta_2 X^2$: Efecto cuadrático de $X$ (introduce curvatura en el modelo).
- $\varepsilon$: Término de error (parte no explicada por el modelo).

---

### 🎯 Tipo de modelo

Este es un **modelo de regresión polinómica de segundo grado** (regresión cuadrática), porque incluye el término $X^2$.

Esto implica que la relación entre $X$ y $Y$ no es una línea recta, sino una **curva (parábola)**.

---

### 📈 Interpretación del coeficiente cuadrático

- Si $\beta_2 > 0$ → La parábola abre hacia arriba (forma de "U").
- Si $\beta_2 < 0$ → La parábola abre hacia abajo (forma de "∩").


Se usa cuando los datos presentan **curvatura**.

---

### Ejercicio 2: Regresión polinómica

Suponga la relación entre velocidad y consumo de combustible:

| X | Y |
|---|---|
| 1 | 4 |
| 2 | 7 |
| 3 | 15 |
| 4 | 28 |

El comportamiento no es lineal, por lo que se propone un modelo cuadrático.

$$\[
Y = \beta_0 + \beta_1 X + \beta_2 X^2
\]$$

# 📊 Lectura e interpretación de la fórmula

## ✏️ Modelo

$$
Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \varepsilon
$$

---

## 📖 ¿Cómo se lee la fórmula?

Se lee:

> **“Y es igual a beta cero más beta uno por X más beta dos por X al cuadrado más épsilon.”**

---

## 📘 Interpretación estadística

- $Y$: Variable dependiente (lo que queremos explicar o predecir).
- $\beta_0$: Intercepto (valor de $Y$ cuando $X = 0$).
- $\beta_1 X$: Efecto lineal de $X$ sobre $Y$.
- $\beta_2 X^2$: Efecto cuadrático de $X$ (introduce curvatura en el modelo).
- $\varepsilon$: Término de error (parte no explicada por el modelo).

---

## 🎯 Tipo de modelo

Este es un **modelo de regresión polinómica de segundo grado** (regresión cuadrática), porque incluye el término $X^2$.

Esto implica que la relación entre $X$ y $Y$ no es una línea recta, sino una **curva (parábola)**.

---

## 📈 Interpretación del coeficiente cuadrático

- Si $\beta_2 > 0$ → La parábola abre hacia arriba (forma de "U").
- Si $\beta_2 < 0$ → La parábola abre hacia abajo (forma de "∩").


Este modelo se ajusta mediante mínimos cuadrados extendidos.

---

### 6.2.2 Regresión no lineal

Forma general:

$$\[
Y = f(X, \boldsymbol{\beta}) + \varepsilon
\]$$

Ejemplos:
- Modelos exponenciales
- Modelos logarítmicos
- Modelos logísticos

---

### Ejemplo de modelo exponencial

$$\[
Y = \beta_0 e^{\beta_1 X}
\]$$

Aplicaciones:
- Crecimiento poblacional
- Interés compuesto
- Difusión de tecnologías

---

## 6.3 Análisis de varianza (ANOVA) y técnicas avanzadas de modelado

El **ANOVA** permite comparar **más de dos medias poblacionales** simultáneamente.

---

### 6.3.1 Fundamento del ANOVA

Se basa en comparar:
- Variabilidad **entre grupos**
- Variabilidad **dentro de los grupos**

---

### Hipótesis

$$\[
H_0: \mu_1 = \mu_2 = \cdots = \mu_k
\]$$

$$\[
H_1: \text{Al menos una media es diferente}
\]$$

**H cero: todas las medias poblacionales son iguales**
---

### Estadístico F

$$\[
F = \frac{MS_{entre}}{MS_{dentro}}
\]$$

**F es igual a eme-ese entre, dividido entre eme-ese dentro.**
Donde:
- $$\(MS_{entre} = \frac{SS_{entre}}{k-1}\)$$
- $$\(MS_{dentro} = \frac{SS_{dentro}}{n-k}\)$$

---

### 6.3.2 ANOVA de un factor – Ejercicio

Tres métodos de enseñanza producen los siguientes resultados:

| Método | Calificaciones |
|------|----------------|
| A | 70, 72, 68 |
| B | 75, 78, 74 |
| C | 65, 67, 66 |

#### Paso 1: Calcular medias
$$\[
\bar{X}_A = 70,\quad \bar{X}_B = 75.7,\quad \bar{X}_C = 66
\]$$

#### Paso 2: Calcular suma de cuadrados
- $$\(SS_{entre}\)$$
- $$\(SS_{dentro}\)$$

#### Paso 3: Calcular F
$$\[
F = \frac{MS_{entre}}{MS_{dentro}}
\]$$

#### Decisión
Si $$\(F > F_{crítico}\)$$, se **rechaza $$\(H_0\)$$**.

---

### 6.3.3 Relación entre ANOVA y regresión

- La regresión lineal es un **caso especial del ANOVA**
- ANOVA puede verse como un modelo de regresión con variables indicadoras

---

## Conclusión

La regresión y el ANOVA permiten:
- Explicar relaciones entre variables
- Realizar predicciones
- Comparar tratamientos o grupos
- Construir modelos estadísticos robustos

Estas técnicas son fundamentales en:
- Ciencia de datos
- Economía
- Ingeniería
- Investigación científica

---

## Actividad sugerida

1. Ajusta un modelo de regresión lineal con datos reales  
2. Interpreta los coeficientes  
3. Aplica un ANOVA para comparar al menos tres grupos  
4. Presenta conclusiones estadísticas

---

