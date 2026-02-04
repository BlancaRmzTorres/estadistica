
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>


# UNIDAD 5. INTERVALOS DE CONFIANZA Y ESTIMACIÓN PUNTUAL

## Objetivo de la unidad
Comprender y aplicar los conceptos de estimación puntual e intervalos de confianza para uno y dos parámetros poblacionales, utilizando métodos estadísticos adecuados en el análisis de datos.

---

## 5.1 Estimación puntual y por intervalos de confianza

### 5.1.1 Estimación puntual

La **estimación puntual** consiste en utilizar un solo valor calculado a partir de una muestra para estimar un parámetro poblacional desconocido.

| Parámetro poblacional | Estimador puntual |
|----------------------|------------------|
| Media poblacional (μ) | Media muestral (x̄) |
| Proporción poblacional (p) | Proporción muestral (p̂) |
| Varianza poblacional (σ²) | Varianza muestral (s²) |

#### Ejemplo 1
Una muestra de 50 estudiantes tiene un promedio de calificaciones de 82.

**Estimación puntual de μ:**  
$$\[
\hat{\mu} = \bar{x} = 82
\]$$

---

### 5.1.2 Estimación por intervalos de confianza

Un **intervalo de confianza (IC)** proporciona un rango de valores dentro del cual se espera que se encuentre el parámetro poblacional con un cierto nivel de confianza (95%, 99%, etc.).

### ¿Para qué se utilizan los intervalos de confianza?

Los **intervalos de confianza** se utilizan en estadística para **estimar un valor desconocido de una población** (como una media o proporción) a partir de una muestra, indicando además **qué tan segura es esa estimación**.

---

### Ejemplo:  
> “La media está entre 45 y 52 con un 95% de confianza”.

---

### Utilidades de los intervalos de confianza

### 1. Expresar la incertidumbre de una estimación  
Una sola medida (como la media muestral) es solo un punto.  
El intervalo muestra **qué tan confiable** es esa estimación.

### 2. Tomar decisiones basadas en datos  
Se usan en investigaciones científicas, encuestas, medicina, ingeniería, economía, etc., para evaluar **fiabilidad**.

### 3. Comparar grupos  
Si los intervalos de dos grupos no se traslapan mucho, podría indicar una **diferencia significativa**.

### 4. Evitar conclusiones engañosas  
El intervalo evita depender solo de un valor puntual.

### 5. Evaluar precisión  
- Intervalo **estrecho** → mayor precisión  
- Intervalo **amplio** → menor precisión

---

El intervalo de confianza se calcula a partir de las estadísticas de la muestra y el nivel de confianza deseado (normalmente, el 95% o el 99%). Es importante señalar que un intervalo de confianza no indica si la hipótesis nula es verdadera o falsa, sino que proporciona un intervalo de valores que probablemente incluya el parámetro poblacional verdadero con un cierto nivel de confianza.

<img width="486" height="600" alt="imagen1" src="/assets/intervalos.png" />

Los valores de 1.96 y 2.57 representan percentiles específicos de la curva normal estándar, estos son fijos

> - Z=1.96Z = 1.96Z=1.96 deja 2.5% en cada cola (95% al centro).
> - Z=2.57Z = 2.57Z=2.57 deja 0.5% en cada cola (99% al centro).


### ¿Qué significa “2.5% en cada cola” o “0.5% en cada cola”?

Cuando trabajamos con **niveles de confianza** y la **distribución normal estándar (Z)**, imaginamos la famosa **curva en forma de campana**.

- El **nivel de confianza** es el porcentaje del **área central** de la curva.
- Lo que queda fuera de ese nivel se divide en **dos colas**:
  - cola izquierda  
  - cola derecha  

---

### Nivel de confianza del 95%

La frase:

> **Z = 1.96 deja 2.5% en cada cola (95% al centro)**

significa que:

- El **95% del área total** está entre:
  
 $$ \[
  -1.96 \le Z \le 1.96
  \]$$

- El **5% restante** queda fuera del intervalo.
- Ese 5% se reparte en dos partes iguales:
  - **2.5% en la cola izquierda**
  - **2.5% en la cola derecha**

**Por eso**, $$\( Z = 1.96 \)$$ es el **valor crítico** para un **intervalo de confianza del 95%**.

---

### Nivel de confianza del 99%

La frase:

> **Z = 2.57 deja 0.5% en cada cola (99% al centro)**

significa que:

- El **99% del área total** está entre:
  
  $$\[
  -2.57 \le Z \le 2.57
  \]$$

- El **1% queda fuera** del intervalo.
- Ese 1% se divide en:
  - **0.5% en la cola izquierda**
  - **0.5% en la cola derecha**

**Por eso**, $$\( Z = 2.57 \)$$ es el **valor crítico** para un **intervalo de confianza del 99%**.

---

### ¿Por qué se divide en dos colas?

Porque los **intervalos de confianza suelen ser bilaterales**:  
queremos capturar el valor verdadero **por arriba y por abajo** del estimador.

La regla general es:

$$\[
\frac{1 - \text{nivel de confianza}}{2}=\ text{proporción de cada cola}\]]$$

---

### Ejemplo con 95%

$$\[\frac{1 - 0.95}{2}=\frac{0.05}{2}=0.025=2.5\%\]$$

---

### Ejemplo con 99%

$$\[\frac{1 - 0.99}{2}=\frac{0.01}{2}=0.005=0.5\%\]$$

---

### ¿Qué es un valor crítico en estadística?

El **valor crítico** es un número que marca el **límite entre el área central y las colas** de una distribución estadística  
(normal, *t* de Student, chi-cuadrada, etc.).

En otras palabras:

Es el **valor Z** que determina **hasta dónde debes ir desde la media** para cubrir un cierto **nivel de confianza**.

---

### Interpretación visual

Un valor crítico divide la distribución de la siguiente forma:

[ - valor crítico ] ---- área central ---- [ + valor crítico ]


- El **área central** corresponde al nivel de confianza.
- Las **colas** representan la probabilidad que queda fuera del intervalo.

---

### ¿Por qué Z = 1.96 es el valor crítico del 95%?

Porque al moverte **1.96 desviaciones estándar** hacia la izquierda y hacia la derecha desde la media en una **distribución normal estándar**, cubres exactamente el **95% del área total**.

Esto significa que:

- Entre **-1.96 y +1.96** está el **95% de los valores**.
- Fuera de ese rango queda el **5% restante**, repartido en:
  - **2.5% en la cola izquierda**
  - **2.5% en la cola derecha**

---

### Conclusión clave

Por eso decimos que:

> **1.96 es el valor crítico del 95%**

Es el número que **corta la curva normal** de tal forma que deja **dentro exactamente el 95% del área**, lo que permite construir **intervalos de confianza** y realizar **pruebas de hipótesis** correctamente.

---

### Resumen

- El área que **no** pertenece al nivel de confianza se reparte **en dos colas**.
- Cada cola tiene la misma proporción.
- De aquí surgen los valores críticos **Z** usados en los **intervalos de confianza**.



### Tabla de valores Z para intervalos de confianza

| Nivel de confianza | Área central | α (cola total) | α/2 | Valor Z (±) |
|-------------------|--------------|----------------|------|-------------|
| 80%               | 0.80         | 0.20           | 0.10 | 1.28        |
| 85%               | 0.85         | 0.15           | 0.075| 1.44        |
| 90%               | 0.90         | 0.10           | 0.05 | 1.645       |
| 92%               | 0.92         | 0.08           | 0.04 | 1.75        |
| 95%               | 0.95         | 0.05           | 0.025| 1.96        |
| 96%               | 0.96         | 0.04           | 0.02 | 2.05        |
| 97%               | 0.97         | 0.03           | 0.015| 2.17        |
| 98%               | 0.98         | 0.02           | 0.01 | 2.33        |
| 99%               | 0.99         | 0.01           | 0.005| 2.57        |
| 99.5%             | 0.995        | 0.005          | 0.0025| 2.81       |
| 99.9%             | 0.999        | 0.001          | 0.0005| 3.29       |

## Ejemplo

En una encuesta, 60% de personas apoyan una propuesta, con un intervalo de confianza del 95% entre 56% y 64%.

**Interpretación:**  
> Con un 95% de confianza, el apoyo real en la población está entre 56% y 64%.

---

## 5.2 Estimaciones para una y dos poblaciones.

En estadística inferencial, la **estimación para una y dos poblaciones** permite comparar o describir características de una o más poblaciones a partir de muestras.  
En este tema se construyen **intervalos de confianza para medias poblacionales**, considerando distintos escenarios.

---

### Estimación para una población (media poblacional)

Cuando se desea estimar la **media poblacional μ** a partir de una muestra, el tipo de intervalo de confianza depende de si la **desviación estándar poblacional σ** es conocida o desconocida.

#### Caso 1: σ conocida

Se utiliza la **distribución normal estándar (Z)**.

**Fórmula:**

$$\[
IC = \bar{x} \pm Z_{\alpha/2}\left(\frac{\sigma}{\sqrt{n}}\right)
\]$$

**Intervalo de confianza igual a equis barra más o menos Z sub alfa entre dos, multiplicado por sigma entre raíz cuadrada de n.**

Dondee:

- IC → “intervalo de confianza”
- x̄ → “equis barra” (la media muestral)
- ± → “más o menos”
- Zα/2 → “Z sub alfa sobre dos” (valor crítico de la distribución normal)
- σ → “sigma” (desviación estándar poblacional)
- √n → “raíz cuadrada de n” (n es el tamaño de la muestra)

**Supuestos:**
- σ conocida
- Población normal o muestra grande $$(\(n \ge 30\))$$
- Muestra aleatoria

---

### Ejemplo 1: Intervalo de confianza para una media (σ conocida)

**Problema:**  
Una población tiene desviación estándar σ = 8. Se toma una muestra de tamaño n = 64 y se obtiene una media muestral de $$\(\bar{x} = 70\)$$.  
Construya un intervalo de confianza del 95% para la media poblacional.

**Solución paso a paso:**

1. Nivel de confianza: 95%  
   $$\[
   Z_{\alpha/2} = 1.96
   \]$$

2. Fórmula:
   $$\[
   IC = \bar{x} \pm Z_{\alpha/2}\left(\frac{\sigma}{\sqrt{n}}\right)
   \]$$

3. Sustitución:
   $$\[
   IC = 70 \pm 1.96\left(\frac{8}{\sqrt{64}}\right)
   \]$$

4. Cálculo:
   $$\[
   IC = 70 \pm 1.96(1)
   \]$$

   $$\[
   IC = 70 \pm 1.96
   \]$$

5. Intervalo de confianza:
   $$\[
   (68.04,\;71.96)
   \]$$

**Interpretación:**  
Con un 95% de confianza, la media poblacional se encuentra entre 68.04 y 71.96.

---

### Estimación para dos poblaciones (diferencia de medias)

Cuando se desea comparar **dos poblaciones independientes**, se estima la **diferencia de medias poblacionales**:

$$\[
\mu_1 - \mu_2
\]$$

Si ambas desviaciones estándar poblacionales son conocidas, se utiliza la **distribución Z**.

**Fórmula:**

$$\[(\bar{x}_1 - \bar{x}_2) \pm Z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} \]$$

**Supuestos:**
- Poblaciones independientes
- σ₁ y σ₂ conocidas
- Muestras aleatorias

---

### Ejemplo 2: Intervalo de confianza para la diferencia de medias

**Problema:**  
Dos grupos de estudiantes presentan los siguientes datos:

- Grupo 1: $$\(\bar{x}_1 = 85\)$$, σ₁ = 4, n₁ = 40  
- Grupo 2: $$\(\bar{x}_2 = 80\)$$, σ₂ = 5, n₂ = 50  

Construya un intervalo de confianza del 95% para la diferencia de medias poblacionales.

**Solución paso a paso:**

1. Nivel de confianza:
   $$\[
   Z_{\alpha/2} = 1.96
   \]$$

2. Fórmula:
$$(\bar{x}_1 - \bar{x}_2) \pm Z_{\alpha/2}
\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}$$


3. Sustitución:
   $$\[
   (85 - 80) \pm 1.96
   \sqrt{\frac{16}{40} + \frac{25}{50}}
   \]$$

4. Cálculo:
   $$\[
   5 \pm 1.96\sqrt{0.4 + 0.5}
   \]$$

   $$\[
   5 \pm 1.96\sqrt{0.9}
   \]$$

   $$\[
   5 \pm 1.86
   \]$$

5. Intervalo de confianza:
   $$\[
   (3.14,\;6.86)
   \]$$

**Interpretación:**  
Con un 95% de confianza, la diferencia entre las medias poblacionales se encuentra entre 3.14 y 6.86 unidades.

---

### Conclusión del tema 5.2

- Para **una población**, el intervalo depende de si σ es conocida o desconocida.
- Para **dos poblaciones**, se estima la **diferencia de medias**.
- Estos intervalos permiten **comparar grupos y tomar decisiones estadísticas fundamentadas**.

## 5.3 Intervalos de confianza para proporciones y grandes muestras

En muchos estudios estadísticos, el interés se centra en **estimar una proporción poblacional (p)**, como el porcentaje de personas que apoyan una propuesta o la proporción de productos defectuosos.

Cuando el tamaño de la muestra es suficientemente grande, la distribución muestral de la proporción puede aproximarse por una **distribución normal**, lo que permite construir **intervalos de confianza**.

---

### Proporción poblacional y proporción muestral

- **Proporción poblacional (p):** parámetro desconocido.
- **Proporción muestral (p̂):** estimador puntual de p.

$$\[
\hat{p} = \frac{x}{n}
\]$$

donde:
- $$\(x\)$$ = número de éxitos
- $$\(n\)$$ = tamaño de la muestra

---

### Condición de gran muestra

Para usar la aproximación normal se deben cumplir:

- $$\(n\hat{p} \ge 5\)$$
- $$\(n(1 - \hat{p}) \ge 5\)$$

Si estas condiciones se cumplen, se puede utilizar la distribución **Z**.

---

### Intervalo de confianza para una proporción

El intervalo de confianza para una proporción poblacional es:

$$\[
\hat{p} \pm Z_{\alpha/2}
\sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}
\]$$

donde:
- $$\(\hat{p}\)$$ = proporción muestral  
- $$\(Z_{\alpha/2}\)$$ = valor crítico de la normal estándar  
- $$\(n\)$$ = tamaño de la muestra  

---

### Ejemplo 1: Intervalo de confianza para una proporción

**Problema:**  
En una encuesta a 300 personas, 180 respondieron que están a favor de una política pública.  
Construya un intervalo de confianza del 95% para la proporción poblacional.

**Solución paso a paso:**

1. Calcular la proporción muestral:

$$\[
\hat{p} = \frac{180}{300} = 0.60
\]$$

2. Verificar condición de gran muestra:


$$
n\hat{p} = 300(0.60) = 180 \ge 5
$$

$$
n(1 - \hat{p}) = 300(0.40) = 120 \ge 5
$$


Se cumple la condición.

3. Nivel de confianza del 95%:

$$\[
Z_{\alpha/2} = 1.96
\]$$

4. Sustituir en la fórmula:

$$\[
IC = 0.60 \pm 1.96
\sqrt{\frac{0.60(0.40)}{300}}
\]$$

5. Cálculo:

$$\[
IC = 0.60 \pm 1.96(0.0283)
\]$$

$$\[
IC = 0.60 \pm 0.055
\]$$

6. Intervalo de confianza:

$$\[
(0.545,\;0.655)
\]$$

**Interpretación:**  
Con 95% de confianza, la proporción poblacional se encuentra entre 0.545 y 0.655.

---

### Intervalo de confianza para la diferencia de proporciones

Cuando se comparan **dos poblaciones independientes**, se construye un intervalo de confianza para la diferencia:

$$\[
p_1 - p_2
\]$$

La fórmula es:


$$
(\hat{p}_1 - \hat{p}_2) \pm Z_{\alpha/2}
\sqrt{\frac{\hat{p}_1(1 - \hat{p}_1)}{n_1} + \frac{\hat{p}_2(1 - \hat{p}_2)}{n_2}}
$$

---

### Ejemplo 2: Intervalo de confianza para la diferencia de proporciones

**Problema:**  
En dos ciudades se estudia el uso de transporte público:

- Ciudad A: 120 de 200 personas lo usan.
- Ciudad B: 90 de 180 personas lo usan.

Construya un intervalo de confianza del 95% para la diferencia de proporciones.

**Solución paso a paso:**

1. Proporciones muestrales:

$$\[
\hat{p}_1 = \frac{120}{200} = 0.60
\]$$

$$\[
\hat{p}_2 = \frac{90}{180} = 0.50
\]$$

2. Valor crítico:

$$\[
Z_{\alpha/2} = 1.96
\]$$

3. Sustituir en la fórmula:

$$\[
IC = (0.60 - 0.50) \pm 1.96
\sqrt{\frac{0.60(0.40)}{200} + \frac{0.50(0.50)}{180}}
\]$$

4. Cálculo:

$$\[
IC = 0.10 \pm 1.96(0.048)
\]$$

$$\[
IC = 0.10 \pm 0.094
\]$$

5. Intervalo de confianza:

$$\[
(0.006,\;0.194)
\]$$

**Interpretación:**  
Con 95% de confianza, la diferencia entre las proporciones poblacionales se encuentra entre 0.006 y 0.194.

---

### Conclusión del tema 5.3

- Las proporciones se estiman usando la **distribución normal** en muestras grandes.
- Es fundamental verificar las **condiciones de gran muestra**.
- Los intervalos permiten comparar poblaciones y apoyar la toma de decisiones estadísticas.

---
