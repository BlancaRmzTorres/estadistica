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

## ¿Para qué se utilizan?

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

#### Intervalo de confianza para la media (σ conocida)
La fórmula general del intervalo de confianza (IC) para la media poblacional $$(\(\mu \))$$ con desviación estándar conocida $$(\(\sigma \))$$ es:

$$\[
IC = \bar{x} \pm Z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)
\]$$

---

## ¿Cómo se lee la fórmula del intervalo de confianza?

> **"El intervalo de confianza es la media muestral más–menos el valor Z crítico multiplicado por la desviación estándar poblacional dividida entre la raíz cuadrada del tamaño de la muestra."**

---

## Donde:

### **IC**
**Significa:** “Intervalo de confianza”.

---

### **x̄**
**Significa:** “Media muestral”.

---

### **±**
**Significa:** “Más o menos”.

---

### **$$Z_{α/2}$$**
**Significa:**  
“Valor crítico de Z para un nivel de confianza de alfa entre dos”.

Este valor depende del nivel de confianza:  
- 90% → 1.645  
- 95% → 1.96  
- 99% → 2.575  

---

### **$$σ / √n$$**
**Significa:**  
“Desviación estándar poblacional dividida entre la raíz cuadrada del tamaño de la muestra”.

Este término es conocido como **error estándar de la media**.

---

### Lectura completa de la fórmula

> **$$IC = x̄ ± Z_{α/2} (σ / √n)$$**  
>  
> Se lee como:  
> **“El intervalo de confianza es la media muestral más o menos Z sub alfa sobre dos por sigma sobre raíz de n”.**

### Ejemplos de Intervalos de Confianza

### Ejemplo 1: Intervalo de confianza para la media poblacional (σ conocida)

### Planteamiento
Se desea estimar la media poblacional del tiempo de atención en una clínica.  
Se toma una muestra de **64 pacientes** y se obtiene:

- Media muestral: $$\(\bar{x} = 50\)$$
- Desviación estándar poblacional: $$\(\sigma = 8\)$$
- Nivel de confianza: **95%**

---

### Fórmula

$$\[
IC = \bar{x} \pm Z_{\alpha/2}\left(\frac{\sigma}{\sqrt{n}}\right)
\]$$

---

### Paso 1: Valor crítico

Para un nivel de confianza del 95%:

$$\[
Z_{0.025} = 1.96
\]$$

---

### Paso 2: Error estándar

$$\[
\frac{\sigma}{\sqrt{n}} = \frac{8}{\sqrt{64}} = 1
\]$$

---

### Paso 3: Margen de error

$$\[
E = 1.96 \times 1 = 1.96
\]$$

---

### Paso 4: Intervalo de confianza

$$\[
(50 - 1.96,\; 50 + 1.96) = (48.04,\; 51.96)
\]$$

---

### Interpretación
Con un **95% de confianza**, la media poblacional del tiempo de atención se encuentra entre **48.04 y 51.96** minutos.

---

### Ejemplo 2: Intervalo de confianza para la media poblacional (σ desconocida)

### Planteamiento
Se desea estimar el peso promedio de un grupo de estudiantes. Se obtiene:

- Tamaño de muestra: $$\(n = 25\)$$
- Media muestral: $$\(\bar{x} = 68\)$$
- Desviación estándar muestral: $$\(s = 6\)$$
- Nivel de confianza: **95%**

---

### Fórmula (distribución t de Student)

$$\[
IC = \bar{x} \pm t_{\alpha/2,\,n-1}\left(\frac{s}{\sqrt{n}}\right)
\]$$

---

### Paso 1: Grados de libertad

$$\[
gl = n - 1 = 24
\]$$

De la tabla t:

$$\[
t_{0.025,24} = 2.064
\]$$

---

### Paso 2: Error estándar

$$\[
\frac{s}{\sqrt{n}} = \frac{6}{\sqrt{25}} = 1.2
\]$$

---

### Paso 3: Margen de error

$$\[
E = 2.064 \times 1.2 = 2.48
\]$$

---

### Paso 4: Intervalo de confianza

$$\[
(68 - 2.48,\; 68 + 2.48) = (65.52,\; 70.48)
\]$$

---

### Interpretación
Con un **95% de confianza**, el peso promedio de los estudiantes se encuentra entre **65.52 y 70.48 kg**.

---

### Intervalo de Confianza para una Proporción Poblacional

### 1. ¿Qué es una proporción poblacional?

Una **proporción poblacional** $$\( p \)$$ representa la fracción de individuos en una población que poseen cierta característica.

Ejemplos:
- Proporción de personas que apoyan una propuesta.
- Porcentaje de defectos en una línea de producción.
- Proporción de estudiantes que aprueban un examen.

Como $$\( p \)$$ es desconocida, se estima mediante una muestra.

---

## 2. Proporción muestral

Si en una muestra de tamaño $$\( n \)$$ se observan $$\( x \)$$ "éxitos", la **proporción muestral** es:

$$\[
\hat{p} = \frac{x}{n}
\]$$

Esta es la mejor estimación puntual del parámetro real $$\( p \)$$.

---

## 3. Distribución de la proporción muestral

Bajo ciertas condiciones (criterio $$\( n\hat{p} \ge 5 \)$$ y $$\( n(1-\hat{p}) \ge 5 \))$$, la proporción muestral sigue una distribución:

$$\[
\hat{p} \sim N\left(p,\ \frac{p(1-p)}{n}\right)
\]$$

Como $$\( p \)$$ es desconocido, en el cálculo del intervalo se usa:

$$\[
SE = \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]$$

Este valor es el **error estándar de la proporción**.

---

## 4. Fórmula del intervalo de confianza

El intervalo de confianza para una proporción poblacional, con nivel $$\((1 - \alpha) \cdot 100\%\)$$, es:

$$\[
IC = \hat{p} \pm Z_{\alpha/2} \cdot \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]$$

Donde:

- $$\( \hat{p} \)$$: proporción muestral  
- $$\( n \)$$: tamaño de la muestra  
- $$\( Z_{\alpha/2} \)$$: valor crítico de la distribución normal estándar  
- $$\( SE \)$$: error estándar de la proporción  

---

## 5. Valores Z más comunes

| Nivel de confianza | \( Z_{\alpha/2} \) |
|-------------------|--------------------|
| 90%               | 1.645              |
| 95%               | 1.96               |
| 99%               | 2.57               |

Estos valores provienen de la distribución normal estándar y son constantes para cada nivel de confianza.

---

## 6. Interpretación del intervalo de confianza

Si el intervalo calculado es, por ejemplo:

$$\[
IC = (0.39,\ 0.45)
\]$$

La interpretación correcta es:

> Si tomáramos muchas muestras del mismo tamaño y construyéramos intervalos de confianza de la misma forma, aproximadamente el **(1 - α)·100%** de ellos contendrían la proporción verdadera $$\( p \)$$.

**Nota importante:**  
No se debe interpretar como “hay un 95% de probabilidad de que $$\( p \)$$ esté dentro del intervalo”, porque el parámetro no es aleatorio; lo aleatorio es el intervalo.

---
## 7. Resumen final

El intervalo de confianza para una proporción poblacional se construye como:

$$\[
IC = \hat{p} \pm Z_{\alpha/2} \cdot \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]$$

Este intervalo permite estimar el rango en el cual probablemente se encuentra la verdadera proporción poblacional $$\( p \)$$, considerando la variabilidad natural del muestreo.

---

## Ejemplo 3: Intervalo de confianza para una proporción poblacional

### Planteamiento
En una encuesta aplicada a **400 personas**, **160** indicaron que usan transporte público.

- Tamaño de muestra: $$\(n = 400\)$$
- Proporción muestral:
$$\[
\hat{p} = \frac{160}{400} = 0.4
\]$$
- Nivel de confianza: **95%**

---

### Fórmula

$$\[
IC = \hat{p} \pm Z_{\alpha/2}
\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]$$

---

### Paso 1: Error estándar

$$\[
\sqrt{\frac{0.4(0.6)}{400}} = \sqrt{0.0006} = 0.0245
\]$$

---

### Paso 2: Margen de error

$$\[
E = 1.96 \times 0.0245 = 0.048
\]$$

---

### Paso 3: Intervalo de confianza

$$\[
(0.4 - 0.048,\; 0.4 + 0.048) = (0.352,\; 0.448)
\]$$

---

### Interpretación
Con un **95% de confianza**, la proporción poblacional de personas que usan transporte público se encuentra entre **35.2% y 44.8%**.

---

**Nota:** A mayor tamaño de muestra, menor será el margen de error del intervalo de confianza.

---

### Ejemplo 4. Intervalo de Confianza para una Proporción Poblacional

### Planteamiento del problema

Un investigador quiere estimar la proporción de empleados que están satisfechos con su trabajo.  
En una muestra aleatoria de **250 empleados**, **170** respondieron que están satisfechos.

Construye un **intervalo de confianza del 95%** para la proporción poblacional $$\( p \)$$.

---

### Calcular la proporción muestral

$$\[
\hat{p} = \frac{x}{n} = \frac{170}{250}
\]$$

$$\[
\hat{p} = 0.68
\]$$

---

### Verificar condiciones para usar la aproximación normal

Se deben cumplir:

$$\[
n\hat{p} \ge 5, \qquad n(1 - \hat{p}) \ge 5
\]$$

Cálculo:

$$\[
n\hat{p} = 250 \cdot 0.68 = 170 \ge 5
\]$$

$$\[
n(1 - \hat{p}) = 250 \cdot 0.32 = 80 \ge 5
\]$$

Ambas condiciones se cumplen.

---

### Calcular el error estándar (SE)

$$\[
SE = \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]$$

$$\[
SE = \sqrt{\frac{0.68(1 - 0.68)}{250}}
\]$$

$$\[
SE = \sqrt{\frac{0.2176}{250}}
\]$$

$$\[
SE = \sqrt{0.0008704} = 0.0295
\]$$

---

### Valor crítico $$\( Z_{\alpha/2} \)$$

Para un **95% de confianza**:

$$\[
Z_{\alpha/2} = 1.96
\]$$

---

### Construcción del intervalo de confianza

Fórmula:

$$\[
IC = \hat{p} \pm Z_{\alpha/2} \cdot SE
\]$$

Sustitución:

$$\[
IC = 0.68 \pm 1.96(0.0295)
\]$$

$$\[
ME = 1.96 \cdot 0.0295 = 0.0578
\]$$

---

### Cálculo de los límites

### Límite inferior:

$$\[
0.68 - 0.0578 = 0.6222
\]$$

### Límite superior:

$$\[
0.68 + 0.0578 = 0.7378
\]$$

---

### Resultado final

El intervalo de confianza del **95%** para la proporción poblacional es:

$$\[
\boxed{(0.6222,\ 0.7378)}
\]$$

---

### Interpretación

Con un **95% de confianza**, la proporción verdadera de empleados satisfechos se encuentra entre:

$$\[
62.22\% \text{ y } 73.78\%
\]$$

Si repitiéramos este proceso muchas veces, el **95% de los intervalos** calculados de esta misma forma contendrían el valor real de $$\( p \)$$.

---

### 5.2 Estimaciones para una y dos poblaciones

### 5.2.1 Intervalo de confianza para una media (σ desconocida)

### Intervalo de Confianza para una Media (σ desconocida)
### Teoría completa en Markdown

Cuando queremos estimar la **media poblacional μ** pero **no conocemos la desviación estándar de la población (σ)**, debemos utilizar la **distribución t de Student** en lugar de la distribución normal estándar.

---

### 1. Contexto del problema

En la práctica, rara vez se conoce la desviación estándar poblacional σ.  
Por ello, cuando trabajamos con:

- una **muestra aleatoria**,  
- tamaño de muestra **n**,  
- desviación estándar muestral **s**,  
- y distribución aproximadamente normal,

la estimación de μ se basa en la distribución **t**.

---

## 2. Proporción muestral y estimación de σ

### Media muestral
$$\[
\bar{X} = \frac{1}{n}\sum_{i=1}^{n} X_i
\]$$

### Desviación estándar muestral
$$\[
s = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(X_i - \bar{X})^2}
\]$$

Esta s sustituye a σ, introduciendo más variabilidad, lo cual justifica el uso de t-Student.

---

## 3. Distribución t de Student

Cuando σ es desconocida, el estadístico:

$$\[
t = \frac{\bar{X} - \mu}{\frac{s}{\sqrt{n}}}
\]$$

sigue una distribución **t con $$\( n-1 \)$$ grados de libertad**.

La distribución t:

- Es similar a la normal, pero con **colas más pesadas**.  
- Se vuelve más parecida a la normal conforme $$\( n \)$$ aumenta.  
- Ajusta la incertidumbre por usar **s en lugar de σ**.

---

## 4. Error estándar de la media

$$\[
SE = \frac{s}{\sqrt{n}}
\]$$

---

## 5. Fórmula del intervalo de confianza

Para un nivel de confianza $$\((1 - \alpha) \cdot 100\%\)$$, el intervalo de confianza es:

$$\[
IC = \bar{X} \pm t_{\alpha/2, \, n-1} \cdot \frac{s}{\sqrt{n}}
\]$$

Donde:

- $$\( \bar{X} \)$$ = media muestral  
- $$\( s \)$$ = desviación estándar muestral  
- $$\( n \)$$ = tamaño de la muestra  
- $$\( t_{\alpha/2, \, n-1} \)$$ = valor crítico t con $$\(n-1\)$$ grados de libertad  
- $$\( SE = \frac{s}{\sqrt{n}} \)$$ = error estándar  

---

## 6. Valores t más comunes (colección)

| Nivel de confianza | gl (df) | t crítico |
|-------------------|---------|-----------|
| 90% | grande | 1.645 (aprox. normal) |
| 95% | grande | 1.96 (aprox. normal) |
| 95% | n=10 | 2.262 |
| 95% | n=20 | 2.093 |
| 95% | n=30 | 2.042 |
| 99% | n=10 | 3.169 |
| 99% | n=20 | 2.845 |

**Nota:** A medida que n crece, t se acerca al valor Z correspondiente.

---

## 7. Interpretación del intervalo

Si el intervalo obtenido es, por ejemplo:

$$\[
(23.1,\; 27.8)
\]$$

la interpretación correcta es:

> Con un nivel de confianza del (1 − α)·100%, si repitiéramos el proceso muchas veces, **aproximadamente ese porcentaje de intervalos contaría con el valor real de la media poblacional μ**.

No se interpreta como probabilidad de que μ esté dentro del intervalo, porque μ es fija.

---

## 8. Resumen final

Cuando **σ es desconocida**, usamos:

- El valor t crítico (no Z).  
- La desviación estándar muestral s.  
- La fórmula:

$$\[
IC = \bar{X} \pm t_{\alpha/2, n-1}\left(\frac{s}{\sqrt{n}}\right)
\]$$

Este intervalo ajusta correctamente la incertidumbre adicional introducida por desconocer σ.

---


Cuando la desviación poblacional no es conocida y la muestra es pequeña, se usa la **distribución t de Student**.

$$\[
IC = \bar{x} \pm t_{\alpha/2, n-1} \left( \frac{s}{\sqrt{n}} \right)
\]$$

> **" La fórmula se lee: El intervalo de confianza es la media muestral más o menos el valor t crítico con alfa entre dos y n menos uno grados de libertad, multiplicado por la desviación estándar muestral dividida entre la raíz cuadrada del tamaño de la muestra"

#### Ejemplo 1

Datos:
- $$\(\bar{x} = 68\)$$
- $$\(s = 8\)$$
- $$\(n = 25\)$$
- Nivel de confianza = 95%
- $$\(t_{0.025,24} = 2.064\)$$

**Cálculo:**
$$\[
E = 2.064 \times \frac{8}{\sqrt{25}} = 2.064 \times 1.6 = 3.30
\]$$

$$\[
IC = (64.7,\; 71.3)
\]$$

---

### 5.2.2 Intervalo de confianza para la diferencia de medias (dos poblaciones)

$$\[
IC = (\bar{x}_1 - \bar{x}_2) \pm Z_{\alpha/2}
\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}
\]$$

#### Ejemplo 2

Datos:
- $$\(\bar{x}_1 = 80\), \(s_1 = 6\), \(n_1 = 40\)$$
- $$\(\bar{x}_2 = 75\), \(s_2 = 5\), \(n_2 = 50\)$$
- Nivel de confianza = 95%

**Paso 1. Diferencia de medias**
$$\[
80 - 75 = 5
\]$$

**Paso 2. Error estándar**
$$\[
\sqrt{\frac{36}{40} + \frac{25}{50}} = \sqrt{0.9 + 0.5} = \sqrt{1.4} = 1.18
\]$$

**Paso 3. Margen de error**
$$\[
1.96 \times 1.18 = 2.31
\]$$

**Intervalo**
$$\[
(2.69,\; 7.31)
\]$$

---

## 5.3 Intervalos de confianza para proporciones y grandes muestras

### 5.3.1 Intervalo de confianza para una proporción

Se utiliza cuando:
- $$\(np \geq 5\)$$
- $$\(n(1-p) \geq 5\)$$

$$\[
IC = \hat{p} \pm Z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]$$

---

#### Ejemplo 1 (paso a paso)

Datos:
- $$\(n = 400\)$$
- Éxitos = 160
- $$\(\hat{p} = 160/400 = 0.4\)$$
- Nivel de confianza = 95%

**Paso 1. Error estándar**
$$\[
\sqrt{\frac{0.4(0.6)}{400}} = \sqrt{0.0006} = 0.0245
\]$$

**Paso 2. Margen de error**
$$\[
1.96 \times 0.0245 = 0.048
\]$$

**Intervalo**
$$\[
(0.352,\; 0.448)
\]$$

---

### 5.3.2 Interpretación del intervalo de confianza

Un intervalo de confianza del 95% significa que, si se tomaran muchas muestras y se construyeran intervalos de la misma forma, aproximadamente el 95% de ellos contendrían el verdadero parámetro poblacional.

---

## Conclusiones

- La estimación puntual proporciona un solo valor aproximado.
- Los intervalos de confianza reflejan la incertidumbre del estimador.
- A mayor tamaño de muestra, menor margen de error.
- El nivel de confianza influye directamente en la amplitud del intervalo.

---

📌 **Nota:** Estos métodos son fundamentales en estadística inferencial y en el análisis de datos en ciencia, ingeniería y ciencias sociales.

