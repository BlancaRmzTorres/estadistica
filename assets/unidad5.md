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

#### Intervalo de confianza para la media (σ conocida)

$$\[
IC = \bar{x} \pm Z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)
\]$$

---

# ¿Cómo se lee la fórmula del intervalo de confianza?

**"El intervalo de confianza es la media muestral más–menos el valor Z crítico multiplicado por la desviación estándar poblacional dividida entre la raíz cuadrada del tamaño de la muestra."**

---

## 📌 Desglose de cada elemento

### **IC**
**Significa:** “Intervalo de confianza”.

---

### **x̄**
**Significa:** “Media muestral”.

---

### **±**
**Significa:** “Más o menos”.

---

### **Z_{α/2}**
**Significa:**  
“Valor crítico de Z para un nivel de confianza de alfa entre dos”.

Este valor depende del nivel de confianza:  
- 90% → 1.645  
- 95% → 1.96  
- 99% → 2.575  

---

### **σ / √n**
**Significa:**  
“Desviación estándar poblacional dividida entre la raíz cuadrada del tamaño de la muestra”.

Este término es conocido como **error estándar de la media**.

---

## 📘 Lectura completa de la fórmula

> **IC = x̄ ± Z_{α/2} (σ / √n)**  
>  
> Se lee como:  
> **“El intervalo de confianza es la media muestral más o menos Z sub alfa sobre dos por sigma sobre raíz de n”.**

#### Ejemplo 2 (paso a paso)

Datos:
- $$\(\bar{x} = 75\)$$
- $$\(\sigma = 10\)$$
- $$\(n = 100\)$$
- Nivel de confianza = 95% → $$\(Z = 1.96\)$$

**Paso 1. Error estándar**
$$\[
\frac{\sigma}{\sqrt{n}} = \frac{10}{\sqrt{100}} = 1
\]$$

**Paso 2. Margen de error**
$$\[
E = 1.96 \times 1 = 1.96
\]$$

**Paso 3. Intervalo de confianza**
$$\[
(75 - 1.96,\; 75 + 1.96) = (73.04,\; 76.96)
\]$$

---

## 5.2 Estimaciones para una y dos poblaciones

### 5.2.1 Intervalo de confianza para una media (σ desconocida)

Cuando la desviación poblacional no es conocida y la muestra es pequeña, se usa la **distribución t de Student**.

$$\[
IC = \bar{x} \pm t_{\alpha/2, n-1} \left( \frac{s}{\sqrt{n}} \right)
\]$$

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

