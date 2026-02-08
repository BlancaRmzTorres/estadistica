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

$$\[
\beta_0 = \bar{y} - \beta_1 \bar{x}
\]$$

---

### Ejercicio 1: Regresión lineal simple

Se desea analizar la relación entre **horas de estudio (X)** y **calificación (Y)**.

| X | Y |
|---|---|
| 1 | 60 |
| 2 | 65 |
| 3 | 70 |
| 4 | 75 |
| 5 | 80 |

#### Paso 1: Calcular medias
$$\[
\bar{x} = 3,\quad \bar{y} = 70
\]$$

#### Paso 2: Calcular $$\(\beta_1\)$$

$$\[
\beta_1 = \frac{(1-3)(60-70)+\cdots+(5-3)(80-70)}{(1-3)^2+\cdots+(5-3)^2} = 5
\]$$

#### Paso 3: Calcular $$\(\beta_0\)$$

$$\[
\beta_0 = 70 - 5(3) = 55
\]$$

#### Modelo final

$$\[
\hat{Y} = 55 + 5X
\]$$

**Interpretación:**  
Cada hora adicional de estudio incrementa la calificación en **5 puntos**.

---

### 6.1.2 Regresión lineal múltiple

Se utiliza cuando existen **dos o más variables independientes**.

#### Modelo matemático

$$\[
Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \cdots + \beta_k X_k + \varepsilon
\]$$

---

### Ejemplo de aplicación

- $$\(Y\)$$: salario  
- $$\(X_1\)$$: años de experiencia  
- $$\(X_2\)$$: nivel educativo  

Este modelo permite analizar el **efecto individual de cada variable** sobre la respuesta.

---

## 6.2 Generalizaciones del modelo de regresión lineal y regresión no lineal

Cuando la relación entre variables no es lineal, se utilizan modelos más flexibles.

---

### 6.2.1 Regresión polinómica

Modelo:

$$\[
Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \varepsilon
\]$$

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

---

### Estadístico F

$$\[
F = \frac{MS_{entre}}{MS_{dentro}}
\]$$

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

