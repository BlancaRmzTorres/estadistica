## PROBABILIDAD Y TEOREMA DE BAYES

## 2.1 Concepto y propiedades fundamentales de la probabilidad

### ¿Qué es la probabilidad?
La **probabilidad** es una medida numérica que indica la posibilidad de que ocurra un evento aleatorio.  
Su valor está comprendido entre **0 y 1**, donde:
- 0 significa que el evento es imposible
- 1 significa que el evento es seguro

Formalmente, si un experimento tiene un espacio muestral \( S \) y un evento \( A \subseteq S \), la probabilidad se define como:

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

---

### Ejemplo 2: Cartas
De una baraja estándar de 52 cartas:
- Evento B: sacar un as

$$ \[
P(B) = \frac{4}{52} = \frac{1}{13}
\] $$

---

## 2.2 Probabilidad condicionada e independencia de sucesos

### Probabilidad condicionada
La **probabilidad condicionada** es la probabilidad de que ocurra un evento \( A \), dado que ya ocurrió otro evento \( B \).

Se define como:

$$ \[
P(A \mid B) = \frac{P(A \cap B)}{P(B)}, \quad P(B) > 0
\] $$

---

### Ejemplo 3: Cartas condicionadas
- Evento A: sacar un as  
- Evento B: sacar una carta roja  

Hay 26 cartas rojas y 2 de ellas son ases.

$$ \[
P(A \mid B) = \frac{2}{26} = \frac{1}{13}
\] $$

---

### Independencia de sucesos
Dos eventos \( A \) y \( B \) son **independientes** si la ocurrencia de uno no afecta la probabilidad del otro.

$$ \[
P(A \mid B) = P(A)
\] $$

Equivalente a:

$$ \[
P(A \cap B) = P(A) \cdot P(B)
\] $$

---

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

