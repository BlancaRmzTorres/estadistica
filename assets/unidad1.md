# UNIDAD 1  
# INTRODUCCIÓN A LA ESTADÍSTICA DESCRIPTIVA Y VISUALIZACIÓN DE DATOS

La estadística es una herramienta fundamental en el análisis de datos, ya que permite recopilar, organizar, resumir, analizar e interpretar información para apoyar la toma de decisiones en contextos donde existe variabilidad e incertidumbre.  
Dentro de esta disciplina, la **estadística descriptiva** constituye el primer nivel de análisis, enfocándose en describir y sintetizar los datos observados, mientras que la **visualización de datos** facilita la comprensión y comunicación de patrones, tendencias y relaciones.

---

## 1.1 Conceptos fundamentales

### Dato
Un **dato** es el valor observado de una variable para un individuo, objeto o evento específico.

**Ejemplos:**
- Edad: 25  
- Ingreso mensual: 12,500  
- Nivel educativo: Licenciatura  

---

### Variable
Una **variable** es una característica que puede tomar distintos valores entre los elementos de estudio.

Ejemplos comunes:
- Edad
- Sexo
- Ingreso
- Número de hijos
- Calificación

---

### Población
La **población estadística** es el conjunto total de elementos de interés en un estudio.

Ejemplos:
- Todos los estudiantes de una universidad
- Todos los hogares de un país

---

### Muestra
Una **muestra** es un subconjunto representativo de la población, utilizado cuando el estudio de toda la población no es posible.

---

### Parámetro y estadístico
- **Parámetro:** medida numérica que describe a la población (μ, σ², p).
- **Estadístico:** medida calculada a partir de una muestra (x̄, s², p̂).

---

### Variabilidad
La **variabilidad** mide la dispersión de los datos y es un concepto central en estadística.

---

## Ejemplo estadístico (conceptos fundamentales)

Datos de calificaciones:

\[
X = \{70, 75, 80, 85, 90, 90, 95, 100\}
\]

### Media aritmética

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i
$$

$$
\bar{x} = \frac{685}{8} = 85.625
$$

#### En Python

```python
import numpy as np

calificaciones = [70, 75, 80, 85, 90, 90, 95, 100]
np.mean(calificaciones)
```

## 1.2 Definición y aplicación de la estadística

### Definición de estadística
La **estadística** es la rama de las matemáticas que se encarga del diseño de experimentos, la recolección, organización, análisis, interpretación y presentación de datos.

Su objetivo principal es apoyar la **toma de decisiones bajo incertidumbre**.

---

### Ramas de la estadística

#### Estadística descriptiva
Se enfoca en describir y resumir los datos observados mediante:
- Tablas
- Medidas numéricas
- Gráficos

#### Estadística inferencial
Utiliza información obtenida de una muestra para:
- Estimar parámetros poblacionales
- Probar hipótesis
- Realizar predicciones

---

### Ejemplo de aplicación estadística

Si de 40 estudiantes, 28 aprobaron una asignatura, la proporción muestral es:

$$
\hat{p} = \frac{28}{40} = 0.70
$$

#### Implementación en Python

```python
28 / 40
```


## 1.3 Población y muestra de datos

### Población
La **población estadística** es el conjunto total de elementos que comparten una o más características de interés y sobre los cuales se desea realizar un estudio.

**Ejemplos de población:**
- Todos los estudiantes de una universidad
- Todos los hogares de un país
- Todos los registros de una base de datos administrativa

Las poblaciones se describen mediante **parámetros**, los cuales generalmente son desconocidos:
- Media poblacional: \( \mu \)
- Varianza poblacional: \( \sigma^2 \)
- Proporción poblacional: \( p \)

---

### Muestra
Una **muestra** es un subconjunto representativo de la población, utilizado cuando no es posible estudiar a todos los elementos.

Las muestras se describen mediante **estadísticos**, tales como:
- **Media muestral:** $\bar{x}$
- **Varianza muestral:** $s^2$
- **Proporción muestral:** $\hat{p}$

---

### Ejemplo estadístico

Edades registradas en una muestra de cinco personas:

$$
X = \{22,\; 25,\; 30,\; 28,\; 35\}
$$

#### Media muestral

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i
$$

$$
\bar{x} = \frac{22 + 25 + 30 + 28 + 35}{5} = 28
$$

---

### Implementación en Python

```python
import numpy as np

edades = [22, 25, 30, 28, 35]
np.mean(edades)
```

## 1.4 Tipos de variables y atributos

En estadística, una **variable** es una característica observable que puede tomar distintos valores en los elementos de una población o muestra.

---

### Clasificación de las variables

#### Variables cualitativas
Representan **atributos o cualidades** y no tienen significado numérico.

- **Nominales:** no tienen orden
  - Ejemplos: sexo, color de ojos, estado civil
- **Ordinales:** tienen un orden
  - Ejemplos: nivel educativo, grado de satisfacción

---

#### Variables cuantitativas
Representan **valores numéricos medibles**.

- **Discretas:** toman valores enteros
  - Ejemplos: número de hijos, número de llamadas
- **Continuas:** pueden tomar cualquier valor real
  - Ejemplos: estatura, peso, ingreso mensual

---

### Ejemplo estadístico con fórmulas

Número de hijos en una muestra de familias:

$$
X = \{0, 1, 2, 3, 2, 1, 4\}
$$

Media aritmética:

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i = \frac{13}{7} \approx 1.86
$$

---

### Implementación en Python

```python
import numpy as np

hijos = [0, 1, 2, 3, 2, 1, 4]
np.mean(hijos)
```

## 1.5 Medidas numéricas para la descripción de datos

Las **medidas numéricas descriptivas** permiten resumir, analizar y describir un conjunto de datos mediante valores representativos que facilitan su interpretación.

---

### 1.5.1 Medidas de tendencia central

#### Media aritmética
Es el promedio de los valores observados.

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i
$$

#### Mediana
Es el valor central cuando los datos están ordenados de menor a mayor.

#### Moda
Es el valor que se repite con mayor frecuencia.

---

### 1.5.2 Medidas de dispersión

#### Rango
Mide la amplitud total de los datos.

$$
R = x_{\max} - x_{\min}
$$

#### Varianza muestral
Mide la dispersión de los datos respecto a la media.

$$
s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2
$$

#### Desviación estándar
Es la raíz cuadrada de la varianza.

$$
s = \sqrt{s^2}
$$

---

### Ejemplo estadístico con fórmulas

Ingresos mensuales (en pesos) de una muestra:

$$
X = \{8000,\; 9000,\; 10000,\; 10000,\; 12000\}
$$

**Media:**

$$
\bar{x} = \frac{49000}{5} = 9800
$$

**Mediana:**

$$
\text{Mediana} = 10000
$$

**Moda:**

$$
\text{Moda} = 10000
$$

**Rango:**

$$
R = 12000 - 8000 = 4000
$$

---

### Implementación en Python

```python
import numpy as np

ingresos = [8000, 9000, 10000, 10000, 12000]

media = np.mean(ingresos)
mediana = np.median(ingresos)
desv_std = np.std(ingresos, ddof=1)

media, mediana, desv_std
```

## 1.6 Fundamentos de la visualización de datos en estadística descriptiva

La **visualización de datos** es una herramienta fundamental en la estadística descriptiva que permite representar información mediante gráficos, facilitando la exploración, el análisis y la comunicación de los resultados.

---

### Importancia de la visualización de datos

La correcta visualización de los datos permite:

- Identificar patrones y tendencias
- Detectar valores atípicos
- Comparar grupos o categorías
- Comunicar resultados de forma clara y efectiva

Una visualización adecuada complementa las medidas numéricas descriptivas y mejora la comprensión de los datos.

---

### Principios básicos de la visualización

- Claridad: los gráficos deben ser fáciles de interpretar
- Precisión: los datos deben representarse correctamente
- Simplicidad: evitar información innecesaria
- Coherencia: usar escalas y formatos consistentes

---

### Tipos de gráficos utilizados en estadística descriptiva

#### Gráfica de barras
Se utiliza para comparar variables cualitativas o datos discretos.

#### Histograma
Representa la distribución de una variable cuantitativa continua mediante intervalos.

#### Diagrama de caja (boxplot)
Muestra la dispersión de los datos, la mediana y los valores atípicos.

#### Gráfica de líneas
Permite observar la evolución de una variable a lo largo del tiempo.

---

### Ejemplo estadístico

Calificaciones obtenidas por un grupo de estudiantes:

$$
X = \{70,\; 75,\; 80,\; 85,\; 90,\; 95,\; 100\}
$$

---

### Implementación en Python

#### Histograma

```python
import matplotlib.pyplot as plt

calificaciones = [70, 75, 80, 85, 90, 95, 100]

plt.hist(calificaciones, bins=5)
plt.xlabel("Calificación")
plt.ylabel("Frecuencia")
plt.title("Histograma de calificaciones")
plt.show()
```

