## PROBABILIDAD Y TEOREMA DE BAYES

## 2.1 Concepto y propiedades fundamentales de la probabilidad

### ¿Qué es la probabilidad?
La **probabilidad** es una medida numérica que indica la posibilidad de que ocurra un evento aleatorio.  
Su valor está comprendido entre **0 y 1**, donde:
- 0 significa que el evento es imposible
- 1 significa que el evento es seguro

Formalmente, si un experimento tiene un espacio muestral $$\( S \)$$ y un evento $$\( A \subseteq S \)$$, la probabilidad se define como:

$$ \[
P(A) = \frac{\text{Número de resultados favorables}}{\text{Número total de resultados posibles}}
\] $$

---

### Propiedades fundamentales de la probabilidad

- **No negatividad**  
  La probabilidad de cualquier evento es siempre mayor o igual que cero:
  
 $$ \[
  P(A) \geq 0
  \]$$

- **Normalización**  
  La probabilidad del espacio muestral es igual a uno:
  
  $$\[
  P(S) = 1
  \]$$

- **Aditividad**  
  Si $$\( A \)$$ y $$\( B \)$$ son eventos mutuamente excluyentes, entonces:
  
  $$\[
  P(A \cup B) = P(A) + P(B)
  \]$$


---

### Ejemplo 1: Lanzamiento de un dado
Un dado justo tiene 6 resultados posibles.

- Evento A: obtener un número par → {2, 4, 6}

$$ \[
P(A) = \frac{3}{6} = 0.5
\] $$

** Interpretación **

Sabiendo que un dado tiene 6 caras y que dentro de estas caras son 3 pares la probabilidad de que caiga un par sería $$ \[P(A) = \frac{3}{6}\] $$

---

### Ejemplo 2: Cartas
De una baraja estándar de 52 cartas:
- Evento B: sacar un as

$$ \[
P(B) = \frac{4}{52} = \frac{1}{13}
\] $$

** Interpretación: **
Sabiendo que la carta es roja, la probabilidad de que sea un as es de ( \frac{1}{13} ).

### Ejemplo 4: Lanzamientos de moneda
Se lanza una moneda dos veces:
- Evento A: cara en el primer lanzamiento
- Evento B: cara en el segundo lanzamiento

$$ \[
P(A) = \frac{1}{2}, \quad P(B) = \frac{1}{2}
\] $$

$$ \[
P(A \cap B) = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}
\] $$

Los eventos son independientes.

---

## 2.2 Probabilidad condicionada e independencia de sucesos

---

### Probabilidad condicionada

La **probabilidad condicionada** mide la probabilidad de que ocurra un evento \( A \), **sabiendo que** ya ocurrió otro evento \( B \).  
Es decir, el espacio muestral se **reduce** únicamente a los casos donde \( B \) sucede.

Se define como:

\[
P(A \mid B) = \frac{P(A \cap B)}{P(B)}, \quad P(B) > 0
\]

**Interpretación importante**  
Cuando condicionamos, **ya no consideramos todos los resultados posibles**, solo aquellos donde ocurre \( B \).

---

### 🔹 Ejemplo 1: Cartas condicionadas (revisado)

En una baraja estándar de 52 cartas:

- Evento \( A \): sacar un as  
- Evento \( B \): sacar una carta roja  

Datos:
- Hay 26 cartas rojas
- De ellas, 2 son ases

Entonces:

\[
P(A \mid B) = \frac{2}{26} = \frac{1}{13}
\]

**Interpretación:**  
Sabiendo que la carta es roja, la probabilidad de que sea un as es de \( \frac{1}{13} \).

---

### Ejemplo 2: Probabilidad condicionada con dados

Se lanza un dado justo.

- Evento \( A \): obtener un número par  
- Evento \( B \): obtener un número mayor que 3  

\[
A = \{2,4,6\}, \quad B = \{4,5,6\}
\]

Intersección:
\[
A \cap B = \{4,6\}
\]

Cálculos:
\[
P(A \cap B) = \frac{2}{6}, \quad P(B) = \frac{3}{6}
\]

\[
P(A \mid B) = \frac{2/6}{3/6} = \frac{2}{3}
\]

**Interpretación:**  
Si sabemos que el número fue mayor que 3, la probabilidad de que sea par es \( \frac{2}{3} \).

---

### Ejemplo 3: Probabilidad condicionada en contexto real

En una universidad:
- El 60% de los alumnos cursa matemáticas
- El 30% cursa matemáticas y estadística

Sea:
- \( M \): cursar matemáticas
- \( E \): cursar estadística

\[
P(M) = 0.6, \quad P(M \cap E) = 0.3
\]

\[
P(E \mid M) = \frac{0.3}{0.6} = 0.5
\]

**Interpretación:**  
Dado que un alumno cursa matemáticas, hay un 50% de probabilidad de que también curse estadística.

---

## 🔹 Independencia de sucesos

Dos eventos \( A \) y \( B \) son **independientes** si la ocurrencia de uno **no modifica** la probabilidad del otro.

Formalmente:

\[
P(A \mid B) = P(A)
\]

De forma equivalente:

\[
P(A \cap B) = P(A)\cdot P(B)
\]

---

### Ejemplo 4: Lanzamientos de moneda

Se lanza una moneda dos veces:

- Evento \( A \): obtener cara en el primer lanzamiento
- Evento \( B \): obtener cara en el segundo lanzamiento

\[
P(A) = \frac{1}{2}, \quad P(B) = \frac{1}{2}
\]

\[
P(A \cap B) = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}
\]

**Conclusión:**  
Los eventos son independientes porque el resultado del primer lanzamiento no afecta al segundo.

---

###  Ejemplo 5: Independencia vs dependencia

Se extraen dos cartas **con reemplazo**:

- Evento \( A \): la primera carta es roja
- Evento \( B \): la segunda carta es roja

\[
P(A) = P(B) = \frac{26}{52} = \frac{1}{2}
\]

\[
P(A \cap B) = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}
\]

**Conclusión:**  
Los eventos son independientes porque la carta se regresa al mazo.

---

### 🔹 Ejemplo 6: Eventos dependientes (contraste)

Ahora sin reemplazo:

\[
P(B \mid A) = \frac{25}{51} \neq \frac{26}{52}
\]

 **Conclusión:**  
Los eventos **no son independientes**, ya que el primer resultado afecta al segundo.

---

## 🧠 Resumen conceptual

| Concepto | Idea clave |
|--------|-----------|
| Probabilidad condicionada | El espacio muestral se reduce |
| Eventos independientes | No se afectan entre sí |
| Eventos dependientes | La probabilidad cambia |
| Fórmula clave | \( P(A \mid B) = \frac{P(A \cap B)}{P(B)} \) |

---

---


## 2.3 Teorema de Bayes y su aplicación en probabilidad

### Teorema de Bayes
El **Teorema de Bayes** permite calcular probabilidades condicionadas cuando se tiene información previa.

$$ \[
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}
\] $$

Donde:
- $$\( P(A) \)$$ es la probabilidad a priori
- $$\( P(B \mid A) \)$$ es la probabilidad condicional
- $$\( P(A \mid B) \)$$ es la probabilidad a posteriori

---

### Ejemplo 5: Prueba médica
Una enfermedad afecta al 1% de la población:
$$\[
P(E) = 0.01
\]$$

La prueba:
- Da positivo si la persona está enferma:  
$$\[
P(+ \mid E) = 0.95
\]$$
- Da positivo si no está enferma:  
$$\[
P(+ \mid E^c) = 0.05
\]$$

Queremos calcular:
$$\[
P(E \mid +)
\]$$

---

### Solución paso a paso

$$\[
P(+) = P(+ \mid E)P(E) + P(+ \mid E^c)P(E^c)
\]$$

$$\[
P(+) = (0.95)(0.01) + (0.05)(0.99) = 0.059
\]$$

Aplicando Bayes:

$$\[
P(E \mid +) = \frac{(0.95)(0.01)}{0.059} \approx 0.161
\]$$

**Interpretación**:  
Aunque la prueba dio positivo, la probabilidad real de estar enfermo es solo del **16.1%**.

---

### Ejemplo 6: Urnas
Una urna A contiene bolas rojas con probabilidad 0.7  
Una urna B contiene bolas rojas con probabilidad 0.4  

Se elige una urna al azar y se extrae una bola roja.  
¿Cuál es la probabilidad de que la bola provenga de la urna A?

$$\[
P(A) = P(B) = 0.5
\]$$

$$\[
P(R \mid A) = 0.7, \quad P(R \mid B) = 0.4
\]$$

$$\[
P(R) = (0.7)(0.5) + (0.4)(0.5) = 0.55
\]$$

$$\[
P(A \mid R) = \frac{(0.7)(0.5)}{0.55} \approx 0.636
\]$$

---

## Conclusión
La probabilidad y el Teorema de Bayes son herramientas fundamentales en estadística, con aplicaciones en:
- Medicina
- Inteligencia artificial
- Ciencia de datos
- Toma de decisiones bajo incertidumbre

---

