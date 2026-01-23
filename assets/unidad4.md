# TIPOS DE DATOS Y ALGORITMOS APLICADOS I  
---

## 4.1 Números y secuencias

### Teoría

Los **números** son uno de los tipos de datos fundamentales en programación y algoritmia. Se utilizan para representar cantidades, realizar cálculos y modelar fenómenos reales.

**Tipos de números más comunes:**
- **Enteros (int):** números sin parte decimal.
- **Reales (float):** números con decimales.
- **Complejos (complex):** números con parte real e imaginaria. (numero_complejo = 3 + 4j)

Una **secuencia** es una colección ordenada de elementos numéricos, donde cada elemento ocupa una posición específica.

Ejemplos de secuencias:
- Arreglos (listas) | [10, 20, 30, 40]
- Rangos | range(inicio, fin, paso)
- Series numéricas | \[a_n = a_1 + (n - 1)d\]

### Ejemplo en Python

```python
numeros = [2, 4, 6, 8, 10]
suma = sum(numeros)
promedio = suma / len(numeros)
print(promedio)

