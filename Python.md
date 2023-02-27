# Python

---

## Índice

* [Variables](#variables)
* [Tipos de datos](#tipos-de-datos)
  * [Enteros](#enteros)
  * [Flotantes](#flotantes)
  * [Métodos de tipos numéricos](#métodos-de-tipos-numéricos)
  * [String](#string)
    * [Métodos de los string](#métodos-de-los-string)
  * [Booleanos](#booleanos)
  * [Listas](#listas)
    * [Métodos de las listas](#métodos-de-las-listas)
    * [Listas de comprensión](#listas-de-comprensión)
  * [Tuplas](#tuplas)
  * [Sets](#sets)
    * [Métodos de los set](#métodos-de-los-set)
  * [Diccionarios](#diccionarios)
    * [Métodos de los diccionarios](#métodos-de-los-diccionarios)
* [Operadores de desición](#operadores-de-desición)
* [Operadores de iteración](#operadores-de-iteración)
* [Funciones](#funciones)
* [Funciones Lambda](#funciones-lambda)
* [POO](#poo)

___

## Variables

## Tipos de datos

### Enteros

Los número enteros en python son aquellos que no tienen parte decimal 

`edad = 30`

### Flotantes

`altura = 1.75 `

### Métodos de tipos numéricos

## String

### Métodos de los String

* **capitalize()**: convierte el primer carácter del string en mayúscula.

```python
>>> nombre = 'roberto'
>>> nombre.capitalize()
>>> print(nombre)
'Roberto'
```
* **casefold()**: convierte el string a minúsculas.

```python
>>> nombre = 'ROBERTO'
>>> nombre.casefold()
>>> print(nombre)
'roberto'
```

* **center(width, fillchar)**: devuelve una versión centrada del string con un ancho de tamaño width y relleno con el carácter fillchar.

| PARÁMETRO | DESCRIPCIÓN |
|:---------:|-------------|
|    width  | **Requerido**: valor entero del largo del nuevo string |
| fillchar | **Requerido**: valor con el que se desea llenar el string|

```python
>>> nombre = 'Roberto'
>>> nombre.center(15,'_')
>>> print(nombre)
'____Roberto____'
```

* **count(substring, start=0, end=len(string))**: devuelve el número de ocurrencias de la subcadena substring en el string, dentro del rango start y end.

| PARÁMETRO | DESCRIPCIÓN |
|:---------:|-------------|
|substring|**Requerido**: |
|start| **Opcional**: |
|end| **Opcional**:|

```python
>>> nombre = 'Roberto'
>>> nombre.count('o')
>>> print(nombre)
2
```

* **encode(encoding='UTF-8', errors='strict')**: devuelve una versión codificada del string utilizando el encoding especificado.

| PARÁMETRO | DESCRIPCIÓN |
|:---------:|-------------|
|encoding| lorem |
|errors| ipsum |

```python
```

* **endswith(sufijo, start=0, end=len(string))**: devuelve True si el string termina con la subcadena suffix dentro del rango start y end, de lo contrario devuelve False.

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| sufijo| **Requerido**: substring a evaluar si es con él que termina el string|
| start | **Opcional**: valor entero que indica la posición desde donde comenzar a buscar|
| end | **Opcional**: valor entero que indica la posición para finalizar la búsqueda |

```python
>>> nombre = 'Roberto'
>>> print(nombre.endswith('to'))
True 
>>> print(nombre.endswith('pe'))
False
```

* **expandtabs(tabsize=8)**: devuelve una versión del string en la que los caracteres tabuladores se expanden a espacios en blanco. El tamaño de cada tabulador se define por el argumento tabsize.

```python

```

*  **find(substring, start=0, end=len(string))**: devuelve el índice de la primera ocurrencia de la subcadena substring en el string dentro del rango start y end. Si no se encuentra la subcadena, devuelve -1.

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| substring  | **Requerido**: substring a buscar dentro del string |
|   start    | **Opcional**: Donde comenzar a buscar, por defecto 0  |
|     end    | **Opcional**: Donde termina de buscar, por defecto el final del string  |

```python
>>> texto = 'Hello, World! from Python'
>>> print(texto.find('from'))
14

>>> texto = 'Hello, World! from Python'
>>> print(texto.find('java'))
-1
```

* **format(\*args, \**kwargs)**: formatea el string utilizando los argumentos proporcionados y devuelve una versión formateada del mismo.

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
|*args | lorem |
| **kwargs| ipsum |

```python
```

* **format_map(mapping)**: formatea el string utilizando el diccionario mapping y devuelve una versión formateada del mismo.

```python
```

* **index(substring, start=0, end=len(string))**: devuelve el índice de la primera ocurrencia de la subcadena substring en el string dentro del rango start y end. Si no se encuentra la subcadena, lanza una excepción ValueError.

```python
```

* **isalnum()**: devuelve True si todos los caracteres del string son alfanuméricos, de lo contrario devuelve False.

```python
>>> nombre = 'Roberto'
>>> print(nombre.isalnum())
True 

>>> nombre = 'R0berto123'
>>> print(nombre.isalnum())
True 

>>> nombre = 'R0berto123@gmail.com'
>>> print(nombre.isalnum())
False 
```

* **isalpha()**: devuelve True si todos los caracteres del string son alfabéticos, de lo contrario devuelve False.

```python
>>> nombre = 'Roberto'
>>> print(nombre.isalpha())
True 

>>> nombre = 'R0berto123'
>>> print(nombre.isalpha())
False
```

* **isnumeric()**: devuelve True si todos los caracteres del string son numéricos, de lo contrario devuelve False.

```python
>>> nombre = 'R0berto123'
>>> print(nombre.isnumeric())
False

>>edad = 33
>>print(edad.isnumeric())
True
```

* **isascii()**: devuelve True si **TODOS** los caracteres del string son ASCII, de lo contrario devuelve False.

```python
>>> texto = 'Hello, World! from Python'
>>> print(texto.isacii())
True
 
>>> texto = 'Hello, World! from Python with ñ'
>>> print(texto.isacii())
False
```

* **isdecimal()**: devuelve True si todos los caracteres del string son dígitos decimales (0-9), de lo contrario devuelve False.

```python
>>> numero = '5' # Ojo que el tipo de dato es string
>>> print(numero.isdecimal())
True

>>> uni9 = "\u0039" # Valor unicode para 9
>>> print(uni9.isdecimal())
True

>>> unik = "\u004B" # Valor unicode para K
>>> print(unik.isdecimal())
False
```

* **isdigit()**: devuelve True si todos los caracteres del string son dígitos, de lo contrario devuelve False.

```python
>>> numero = '6'
>>> print(numero.isdigit())
True

>>> uni6 = '\u0036' # valor unicode para 6
>>> print(uni6.isdigit())
True

>>> rut = '123456789-K'
>>> print(rut.isdigit())
False
```

* **isidentifier()**: devuelve True si el string es un identificador válido, de lo contrario devuelve False.  
Un string para ser considerado identificador válido debe contener solamente caracteres alfanuméricos (a-z) y (0-9) o guión bajo (_), no puede iniciar con un número o contener espacios.

```python
>>> texto = 'HelloW0rld'
>>> print(texto.isidentifier())
True

>>> texto = 'Hello W0rld'
>>> print(texto.isidentifier())
False

>>> texto = 'Hello_W0rld'
>>> print(texto.isidentifier())
True

>>> texto = '1HelloW0rld'
>>> print(texto.isidentifier())
False
```

* **islower()**: devuelve True si **TODOS** los caracteres del string están en minúsculas, de lo contrario devuelve False.

```python
>>> nombre = 'Roberto'
>>> print(nombre.islower())
False 

>>> nombre = 'roberto'
>>> print(nombre.islower())
True 
```

* **isprintable()**: devuelve True si todos los caracteres del string son imprimibles, de lo contrario devuelve False.

```python
>>> texto = 'Hello, World! From Python'
>>> print(texto.isprintable())
True

>>> texto = 'Hello, World!\nFrom Python'
>>> print(texto.isprintable())
False
```

* **isspace()**: devuelve True si todos los caracteres del string son espacios en blanco, de lo contrario devuelve False.

```python
>>> texto = 'Hello, World! From Python'
>>> print(texto.isspace())
False

>>> texto = '                '
>>> print(texto.isspace())
True
```

* **istitle()**: devuelve True si el string sigue el formato de título (la primera letra de cada palabra está en mayúscula

```python
>>> nombre = 'Roberto'
>>> print(nombre.istitle())
True

>>> nombre = 'Roberto'
>>> print(nombre.istitle())
False
```

* **isupper()**: devuelve True si **TODOS** los caracteres del string son mayúsculas

```python
>>> nombre = 'ROBERTO'
>>> print(nombre.isupper())
True

>>> nombre = 'Roberto'
>>> print(nombre.isupper())
False

>>> nombre = 'RObERTO'
>>> print(nombre.isupper())
False
```

* **join()**: Une todos los elementos de una tupla dentro de un string usando un separador (string sobre el que se aplica el método join)

```python
>>> nombres = ('Roberto', 'Andrés', 'Sánchez', 'Franco')
>>> nombre_completo = " ".join(nombres)
>>> print(nombre_completo)
Roberto Andrés Sánchez Franco
```


* **ljust(length, character)**: devuelve un strig de la longitud indicada alineado a la izquierda, el texto se rellena con espacios a la derecha a menos que se indique un valor para el llenado

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
|    length  | **Requerido**: largo del nuevo string |
|  character | **Opcional**: caracter con el que se rellena el strig, por defecto es espacio " " |

```python
>>> texto = 'Python'
>>> print(texto.ljust(20,'_'))
Python______________
```

* **lower()**: Convierte un string a minúsculas

```python
>>> nombre = 'Roberto'
>>> print(nombre.lower())
roberto
```

* **lstrip(caracter)**: Devuelve el string eliminando todos los espacios a la izquierda

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
|  caracter  | **Opcional**: caracteres que se desean eliminar, pro defecto espacio " "

```python
>>> nombre = '      Roberto      Sanchez'
>>> print(nombre.lstrip())
Roberto      Sanchez

>>> nombre = 'Roberto      Sanchez'
>>> print(nombre.lstrip('Roberto'))
      Sanchez
```

* **maketrans(x, y, z)**: devuelve una tabla mapeada que puede ser usada con el metodo traslate() para reemplazar caracteres especificos

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
|  x  | **Requerido**: If only one parameter is specified, this has to be a dictionary describing how to perform the replace. If two or more parameters are specified, this parameter has to be a string specifying the characters you want to replace.|
|  y  | **Opcional**:  A string with the same length as parameter x. Each character in the first parameter will be replaced with the corresponding character in this string.|
|  z  | **Opcional**:  A string describing which characters to remove from the original string.|

```python
>>> txt = 'Hola, chao!'
>>> table = str.maketrans("o", "u")
>>> print(txt.translate(table))
Hola chau!
```

* **partition(valor)**: devuelve una tupla en la que el string es dividido en tres partes (la parte antes del valor buscado, el valor buscado y la parte que procede al valor buscado)

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| valor | **Requerido**: string a buscar|

```python
```

* **replace()**: devuelve un string donde un valor específico ha sido reemplazado por por un valor indicado

```python
>>> texto = 'Hello World! From Python'
>>> print(texto.replace('Python','Chile'))
Hello World! From Chile
```

* **rfind()**: Searches the string for a specified value and returns the last position of where it was found

```python
```

* **rindex()**: Searches the string for a specified value and returns the last position of where it was found

```python
```

* **rjust()**: Returns a right justified version of the string

```python
```

* **partition()**: Returns a tuple where the string is parted into three parts

```python
```

* **rsplit()**: Splits the string at the specified separator, and returns a list

```python
```

* **rstrip()**: Returns a right trim version of the string

```python
```

* **split()**: 	Splits the string at the specified separator, and returns a list

```python
```

* **splitlines()**: Splits the string at line breaks and returns a list

```python
```

* **startswith()**: Returns true if the string starts with the specified value

```python
```

* **strip()**: Returns a trimmed version of the string

```python
```

* **swapcase()**: Swaps cases, lower case becomes upper case and vice versa

```python
```

* **title()**: Converts the first character of each word to upper case

```python
```

* **translate()**: Returns a translated string

```python
```

* **upper()**: Converts a string into upper case

```python
```

* **zfill()**: Fills the string with a specified number of 0 values at the beginning

```python
```

### Booleanos

### Listas

### Métodos de las listas

### Listas de comprensión

### Tuplas

### Sets

### Métodos de los set

### Diccionarios

### Métodos de los diccionarios

### Operadores de desición

### Operadores de iteración

### Funciones

### Funciones Lambda

### POO
