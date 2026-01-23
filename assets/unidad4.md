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

###Complejos (complex)###
- Su parte real
- Su parte imaginaria
- Su módulo

  z = complex(3, 4)

```python
print("Parte real:", z.real)
print("Parte imaginaria:", z.imag)
print("Módulo:", abs(z))
```

### 4.2 Conjuntos y cadenas de caracteres###
Un **conjunto (set)** es una colección no ordenada de elementos únicos, es decir, no permite duplicados.
Una **cadena de caracteres (string)** es una secuencia de símbolos que representa texto.

###Características principales:###

Los conjuntos permiten operaciones matemáticas como unión e intersección.
Las cadenas permiten manipulación de texto (concatenar, dividir, buscar).

### Operaciones con Conjuntos en Python ###

A continuación se muestran ejemplos básicos de las operaciones más comunes entre conjuntos: unión, intersección y diferencia, usando sintaxis de Python.

### Unión (A ∪ B) ###
Combina todos los elementos de ambos conjuntos sin duplicados.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

union_1 = A | B
union_2 = A.union(B)

print("Unión (|):", union_1)
print("Unión (.union):", union_2)
```

### Intersección (A ∩ B) ###
Devuelve los elementos que están en ambos conjuntos.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

inter_1 = A & B
inter_2 = A.intersection(B)

print("Intersección (&):", inter_1)
print("Intersección (.intersection):", inter_2)
```

### Diferencia (A − B) ###
Elementos que están en A pero no en B.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

dif_1 = A - B
dif_2 = A.difference(B)

print("Diferencia A - B:", dif_1)
print("Diferencia (.difference):", dif_2)
```

### Manipulación de Cadenas en Python ###
Las cadenas (str) en Python permiten operaciones como concatenar, dividir, buscar, entre muchas otras.
Aquí tienes ejemplos básicos y muy usados.

### 1. Concatenar cadenas ###

```python
texto1 = "Hola"
texto2 = "Mundo"

# Concatenación con +
resultado = texto1 + " " + texto2
print(resultado)

# Concatenación con f-strings (más moderno)
resultado2 = f"{texto1} {texto2}"
print(resultado2)
```
### 2. Dividir cadenas (split) ###
```python
frase = "manzana,pera,uva,mango"

# Divide usando coma como separador
lista_frutas = frase.split(",")

print(lista_frutas)   # ['manzana', 'pera', 'uva', 'mango']
```
### 3. Buscar dentro de una cadena ###
```python
texto = "Programar en Python es divertido."

# Buscar posición de una palabra
pos = texto.find("Python")
print("Posición de 'Python':", pos)

# Verificar si una palabra está en la cadena
existe = "Python" in texto
print("¿Está 'Python'? :",
```

### 4. Reemplazar texto (replace) ###
```python
mensaje = "Hola mundo"
nuevo = mensaje.replace("mundo", "Python")

print(nuevo)  # Hola Python
```

### 5. Cambiar mayúsculas/minúsculas ###
```python
cadena = "Python es Genial"

print(cadena.upper())     # MAYÚSCULAS
print(cadena.lower())     # minúsculas
print(cadena.title())     # Estilo Título
print(cadena.capitalize()) # Solo primera letra en mayúscula
```

### 6. Eliminar espacios (strip) ###
```python

texto = "   hola python   "

print(texto.strip())   # elimina espacios al inicio y fin
print(texto.lstrip())  # elimina espacios a la izquierda
print(texto.rstrip())  # elimina espacios a la derecha
```

### 7. Cortar subcadenas (slicing) ###
```python

texto = "ABCDEFGHIJK"

print(texto[0:4])   # ABCD
print(texto[5:])    # FGHIJK
print(texto[:3])    # ABC
print(texto[-3:])   # IJK
```

### 8. Contar ocurrencias ###
```python

frase = "banana"

print(frase.count("a"))  # 3

```

### 9. Unir cadenas (join) ###
```python

palabras = ["Hola", "mundo", "Python"]

resultado = " ".join(palabras)
print(resultado)   # Hola mundo Python

```




