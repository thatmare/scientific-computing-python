# 💹 Aprende funciones Lambda construyendo un registrador de gastos
1. [Listas en Python](#1-listas-en-python)
2. [Diccionarios](#2-diccionarios)
3. [Bucle `for` para una lista](#3-bucle-for-para-una-lista)
4. [Funciones Lambda en Python](#4-funciones-lambda-en-python)
5. [Bucle `while`](#5-bucle-while)
6. [Otros métodos](#6-otros-metodos)

## 1. Listas en Python
`list` Las listas (`lists`) son un tipo de valor que almacena o contiene otros valores. 
```
[ 1, 2, 3, 4 ]
[ 'a', 'b', 'c' ]
```
Pueden ser valores del mismo tipo o de distinto tipo. 
- `[1, 'a', 2, 'b']`

Pueden tener listas embedidas dentro de las mismas. 
- `[1, 'a', 2, 'b', [ 1, 2, 3, 4 ]]`

### Métodos para listas

#### `append()`
El método `append()` permite insertar elementos en una lista. Por default, lo agrega al final de la lista.

```python
my_list = [1, 2]
my_list.append(3)

print(my_list) # [1, 2, 3]
```

#### `insert()`
El método `insert()` inserta elementos en una lista dado un índice. 

```python
my_list = [1, 2]
my_list.insert(1, "ab")

print(my_list) # [1, "ab"]
```

#### `filter()`
La función `filter()` permite seleccionar items de un objeto iterable, como las listas, basado en el resultado de una función.

**Sintaxis**
```python
filter(función, lista)

# función - función que da el criterio del filtro
# lista - iterables que va a filtrar
```

#### `map()`
La función `map()` ejecuta una función para cada item en un elemento iterable. 

**Sintaxis**
```python
map(function, iterable)

# function - requerido, función a ejecutar en cada item
# iterable - requerido, una secuecia, colección u objeto iterable
```

#### `pop()`
El mé`todo `pop()` remueve elementos de una lista. Por default, remueve el último elemento, aunque también se puede dar un índice del elemento a borrar.

```python
my_list = [1, 2, 3]
my_list.pop()

print(my_list) # [1, 2]

my_list_2 = [1, 2, 3]
my_list_2.pop(0)

print(my_list_2) # [2, 3]
```

#### `sum()`
El método `sum()` retorna un número, que es la suma de todos los elementos dentro del objeto iterable. 

**Sintaxis**
```python
sum(iterable, inicio)

# iterable - requerido, secuencia que va a sumar
# inicio - opcional, valor que se agrega a la suma

# Ejemplos
a = ([1, 2, 3])
x = sum(a) # 6

a = (1, 2, 3, 4, 5)
x = sum(a, 7) # 22
```

### Índices en las listas
Las listas tienen índices base 0. Esto quiere decir que el primer elemento empieza con 0, el siguiente con 1 y así consecutivamente. 

Para accesar al elemento se utiliza la notación de corchetes: `list[index]`.

```python
my_list = [1, 2]

print(my_list[0]) # 1
print(my_list[1]) # 2
```

### Mutabilidad
Las listas son mutables. Esto quiere decir que se pueden modificar los elementos de las listas; se puede realizar a través de la notación de corchetes.

```python
my_list = [1, 2]
my_list[0] = 0

print(my_list) # [0, 2]
```
## 2. Diccionarios
Los diccionaros se utilizan para guardar información en pares claves-valor.
- Los valores tienen un orden y este no puede cambiar.
- Son mutables.
- No permiten duplicados.
- Se definen con llaves ({}) y doble punto (:)

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
```

### Acceder a valores en diccionarios a través de su clave
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

print(thisdict['brand']) # 'Ford'
```

## 3. Bucle `for` para una lista
Método para recorrer o iterar en una lista (aunque también sirve para otros valores como string, diccionario, set...)

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)

# "apple
# "banana"
# "cherry"
```

## 4. Funciones Lambda en Python
En Python, las funciones *lambda* son funciones breves y anónmas cuyo propósito es ejecutar tareas sencillas que solo se utilicen una vez. Se definen con la palabra *lambda*. Siguen la siguiente sintaxis:

```python
lambda arguments : expression
```
**Ejemplos**
```python
x = lambda a : a + 10
print(x(5)) # 15

exampleFunction = lambda param1, param2 : param1 * param2
print(exampleFunction(2,6)) # 12
```

## 5. Bucle `while`
El bucle `while` es un bucle que recorre una parte del código siempre y cuando la condición sea verdadera; el bucle termina cuando la condición se vuelve falsa. 

```python
while condition:
  <code>
```

## 6. Otros metodos
### `input()`
El método `input()` permite que los usuarios ingresen información.

```python
# Sintaxis
input(prompt) # prompt - una cadena de texto

# Ejemplo

x = input("Ingresa tu nombre") # <- Marissa
print("Hola, " + x) # Hola, Marissa
```
