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

## 5.2 Estimaciones para una y dos poblaciones

### 5.2.1 Intervalo de confianza para una media (σ desconocida)

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

