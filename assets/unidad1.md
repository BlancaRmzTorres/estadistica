# INTRODUCCIÓN A LA ESTADÍSTICA DESCRIPTIVA Y VISUALIZACIÓN DE DATOS

La estadística es una herramienta fundamental en el análisis de datos, ya que permite **recopilar, organizar, resumir, analizar e interpretar información** para apoyar la toma de decisiones en contextos donde existe variabilidad e incertidumbre.  
Dentro de esta disciplina, la **estadística descriptiva** constituye el primer nivel de análisis, enfocándose en **describir y sintetizar los datos observados**, mientras que la **visualización de datos** facilita la comprensión y comunicación de patrones, tendencias y relaciones.

---

## 1.1 Conceptos fundamentales

### Dato
Un **dato** es el valor observado de una variable para un individuo, objeto o evento específico.

**Ejemplos:**
- Edad de una persona: 25  
- Ingreso mensual: 12,500  
- Nivel educativo: Licenciatura  

Los datos pueden provenir de:
- Encuestas  
- Experimentos  
- Registros administrativos  
- Sistemas de información  
- Sensores o dispositivos digitales  

---

### Información
La **información** surge cuando los datos son **organizados, procesados y analizados**, permitiendo extraer significado.

Por ejemplo, una lista de edades es un conjunto de datos; calcular el promedio y la distribución por rangos genera información útil.

---

### Variable
Una **variable** es una característica que puede tomar distintos valores entre los elementos de estudio.

**Ejemplos:**
- Edad  
- Sexo  
- Ingreso  
- Número de hijos  
- Calificación  

Las variables son la base del análisis estadístico y pueden clasificarse según su naturaleza.

---

### Población
La **población estadística** es el conjunto total de elementos de interés en un estudio.

**Ejemplos:**
- Todos los estudiantes de una universidad  
- Todos los hogares de un país  
- Todas las personas encuestadas en un censo  

---

### Muestra
Una **muestra** es un subconjunto de la población, seleccionada con el objetivo de representar adecuadamente a la población total.

La estadística descriptiva puede aplicarse tanto a:
- **Poblaciones completas**
- **Muestras**, cuando no es posible observar a todos los elementos

---

### Parámetro
Un **parámetro** es una medida numérica que describe una característica de la población.

**Ejemplos:**
- Media poblacional (μ)  
- Varianza poblacional (σ²)  
- Proporción poblacional (p)  

Los parámetros suelen ser **desconocidos**.

---

### Estadístico
Un **estadístico** es una medida calculada a partir de una muestra y se utiliza para estimar un parámetro.

**Ejemplos:**
- Media muestral (x̄)  
- Varianza muestral (s²)  
- Proporción muestral (p̂)  

---

### Variabilidad
La **variabilidad** refleja el grado de dispersión o heterogeneidad de los datos.  
Dos conjuntos de datos pueden tener la misma media pero comportamientos muy distintos.

---

### Distribución de datos
Describe la forma en que los valores de una variable se reparten o concentran.

Se analiza mediante:
- Tablas  
- Medidas numéricas  
- Gráficos  

---

### Estadística descriptiva
La **estadística descriptiva** comprende el conjunto de métodos utilizados para:
- Organizar datos  
- Resumir información  
- Presentar resultados de forma clara  

No realiza inferencias ni generalizaciones más allá de los datos observados.

---

### Visualización de datos
La **visualización de datos** utiliza representaciones gráficas para:
- Explorar patrones  
- Identificar valores atípicos  
- Comunicar resultados de manera efectiva  

Es una herramienta clave tanto en estadística tradicional como en ciencia de datos.

---

## 1.2 Definición y aplicación de la estadística

### Definición de estadística
La **estadística** es la rama de las matemáticas que se encarga del diseño de experimentos, recolección, organización, análisis, interpretación y presentación de datos.

Su objetivo principal es **apoyar la toma de decisiones bajo incertidumbre**.

---

### Ramas de la estadística

#### Estadística descriptiva
Se enfoca en describir y resumir los datos disponibles mediante:
- Tablas  
- Medidas numéricas  
- Gráficos  

**Ejemplos:**
- Promedio de calificaciones  
- Distribución de edades  
- Gráfica de ingresos mensuales  

---

#### Estadística inferencial
Utiliza información de una muestra para:
- Estimar parámetros poblacionales  
- Probar hipótesis  
- Realizar predicciones  

**Ejemplo:**  
Inferir el ingreso promedio de una población a partir de una encuesta.

---

### Proceso estadístico
El análisis estadístico sigue un proceso estructurado:

1. Planteamiento del problema  
2. Recolección de datos  
3. Organización de la información  
4. Análisis descriptivo  
5. Interpretación de resultados  
6. Comunicación de conclusiones  

---

### Aplicaciones de la estadística

#### Ciencias sociales
- Análisis de encuestas  
- Estudios demográficos  
- Evaluación de políticas públicas  

#### Economía y finanzas
- Análisis de mercados  
- Medición de inflación  
- Evaluación de riesgos  

#### Salud
- Estudios epidemiológicos  
- Ensayos clínicos  
- Análisis de factores de riesgo  

#### Educación
- Evaluación del rendimiento académico  
- Análisis de resultados de exámenes  
- Estudios de deserción escolar  

#### Ingeniería y tecnología
- Control de calidad  
- Optimización de procesos  
- Análisis de confiabilidad  

---

### Estadística en la era del análisis de datos
Actualmente, la estadística es el **fundamento del análisis de datos**, la **ciencia de datos** y la **inteligencia artificial**, integrándose con herramientas computacionales como Python y R.

**Ejemplo en Python:**

```python
import numpy as np

datos = [70, 75, 80, 85, 90]

media = np.mean(datos)
mediana = np.median(datos)
desviacion = np.std(datos)

media, mediana, desviacion
