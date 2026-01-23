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

### Ejercicios de Tipos de números más comunes

### Números Enteros (`int`)

### Tipo de número entero (int)

```python
a = int(input("Ingresa el primer entero: "))
b = int(input("Ingresa el segundo entero: "))

print("Suma:", a + b)
print("Resta:", a - b)
print("Producto:", a * b)
```
### Tipo de número entero (float)
```python
import math

radio = float(input("Ingresa el radio: "))
area = math.pi * radio**2

print("Área del círculo:", area)
```

### Tipo de número entero (complejos)
```python
z1 = 3 + 4j
z2 = 1 + 2j

print("Suma:", z1 + z2)
print("Resta:", z1 - z2)
```
### Arreglos (listas)

```python
# Arreglo (lista) de ejemplo
arreglo = [10, 20, 30, 40]

print("Arreglo:", arreglo)
print("Primer elemento:", arreglo[0])
print("Último elemento:", arreglo[-1])

# Operaciones básicas
arreglo.append(50)          # Agregar al final
arreglo.insert(1, 15)       # Insertar en posición 1
arreglo.remove(30)          # Eliminar por valor
arreglo[2] = 200            # Modificar por índice

print("Arreglo modificado:", arreglo)
print("Longitud:", len(arreglo))

```
### Range (range(inicio, fin, paso))

- **inicio:** número inicial (incluido)
- **fin:** número final (no incluido)
- **paso:** incremento (opcional)

```python
for i in range(1, 6):
    print(i)
```

###Complejos (complex)
- Su parte real
- Su parte imaginaria
- Su módulo

  z = complex(3, 4)

```python
print("Parte real:", z.real)
print("Parte imaginaria:", z.imag)
print("Módulo:", abs(z))
```





