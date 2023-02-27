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

### String

### Métodos de los String

* **capitalize()**: convierte el primer carácter del string en mayúscula.

```
>>> nombre = 'roberto'
>>> nombre.capitalize()
>>> print(nombre)
'Roberto'
```
* **casefold()**: convierte el string a minúsculas.

```
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

```
>>> nombre = 'Roberto'
>>> nombre.center(15,'_')
>>> print(nombre)
'____Roberto____'
```

* **count(substring, start=0, end=len(string))**: devuelve el número de ocurrencias de la subcadena substring en el string, dentro del rango start y end.

```
>>> nombre = 'Roberto'
>>> nombre.count('o')
>>> print(nombre)
2
```

* **encode(encoding='UTF-8', errors='strict')**: devuelve una versión codificada del string utilizando el encoding especificado.



* **endswith(sufijo, start=0, end=len(string))**: devuelve True si el string termina con la subcadena suffix dentro del rango start y end, de lo contrario devuelve False.

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| sufijo| **Requerido**: substring a evaluar si es con él que termina el string|
| start | **Opcional**: valor entero que indica la posición desde donde comenzar a buscar|
| end | **Opcional**: valor entero que indica la posición para finalizar la búsqueda |

```
>>> nombre = 'Roberto'
>>> print(nombre.endswith('to'))
True 
>>> print(nombre.endswith('pe'))
False
```

* **expandtabs(tabsize=8)**: devuelve una versión del string en la que los caracteres tabuladores se expanden a espacios en blanco. El tamaño de cada tabulador se define por el argumento tabsize.

*  **find(substring, start=0, end=len(string))**: devuelve el índice de la primera ocurrencia de la subcadena substring en el string dentro del rango start y end. Si no se encuentra la subcadena, devuelve -1.

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| substring  | **Requerido**: substring a buscar dentro del string |
|   start    | **Opcional**: Donde comenzar a buscar, por defecto 0  |
|     end    | **Opcional**: Donde termina de buscar, por defecto el final del string  |

```
>>> texto = 'Hello, World! from Python'
>>> print(texto.find('from'))
14
```
```
>>> texto = 'Hello, World! from Python'
>>> print(texto.find('java'))
-1
```

* **format(\*args, \**kwargs)**: formatea el string utilizando los argumentos proporcionados y devuelve una versión formateada del mismo.

* **format_map(mapping)**: formatea el string utilizando el diccionario mapping y devuelve una versión formateada del mismo.

* **index(substring, start=0, end=len(string))**: devuelve el índice de la primera ocurrencia de la subcadena substring en el string dentro del rango start y end. Si no se encuentra la subcadena, lanza una excepción ValueError.

* **isalnum()**: devuelve True si todos los caracteres del string son alfanuméricos, de lo contrario devuelve False.

```
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

```
>>> nombre = 'Roberto'
>>> print(nombre.isalpha())
True 

>>> nombre = 'R0berto123'
>>> print(nombre.isalpha())
False
```

* **isnumeric()**: devuelve True si todos los caracteres del string son numéricos, de lo contrario devuelve False.

```
>>> nombre = 'R0berto123'
>>> print(nombre.isnumeric())
False

>>edad = 33
>>print(edad.isnumeric())
True
```

* **isascii()**: devuelve True si **TODOS** los caracteres del string son ASCII, de lo contrario devuelve False.

```
>>> texto = 'Hello, World! from Python'
>>> print(texto.isacii())
True
 
>>> texto = 'Hello, World! from Python with ñ'
>>> print(texto.isacii())
False
```

* **isdecimal()**: devuelve True si todos los caracteres del string son dígitos decimales, de lo contrario devuelve False.

* **isdigit()**: devuelve True si todos los caracteres del string son dígitos, de lo contrario devuelve False.

* **isidentifier()**: devuelve True si el string es un identificador válido, de lo contrario devuelve False.

* **islower()**: devuelve True si **TODOS** los caracteres del string están en minúsculas, de lo contrario devuelve False.

```
>>> nombre = 'Roberto'
>>> print(nombre.islower())
False 

>>> nombre = 'roberto'
>>> print(nombre.islower())
True 
```

* **isprintable()**: devuelve True si todos los caracteres del string son imprimibles, de lo contrario devuelve False.

```
texto = 'Hello, World! From Python'
print(texto.isprintable())
True

texto = 'Hello, World!\nFrom Python'
print(texto.isprintable())
False
```

* **isspace()**: devuelve True si todos los caracteres del string son espacios en blanco, de lo contrario devuelve False.

```
texto = 'Hello, World! From Python'
print(texto.isspace())
False

texto = '                '
print(texto.isspace())
True
```

* **istitle()**: devuelve True si el string sigue el formato de título (la primera letra de cada palabra está en mayúscula

```
>>> nombre = 'Roberto'
>>> print(nombre.istitle())
True

>>> nombre = 'Roberto'
>>> print(nombre.istitle())
False
```

* **isupper()**: Returns True if all characters in the string are upper case

```
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

```
>>> nombres = ('Roberto', 'Andrés', 'Sánchez', 'Franco')
>>> nombre_completo = " ".join(nombres)
>>> print(nombre_completo)
'Roberto Andrés Sánchez Franco'
```


* **ljust()**: Returns a left justified version of the string

* **lower()**: Converts a string into lower case

* **lstrip()**: 	Returns a left trim version of the string

* **maketrans()**: Returns a translation table to be used in translations

* **partition()**:Returns a tuple where the string is parted into three parts

* **replace()**: Returns a string where a specified value is replaced with a specified value

* **rfind()**: Searches the string for a specified value and returns the last position of where it was found

* **rindex()**: Searches the string for a specified value and returns the last position of where it was found

* **rjust()**: Returns a right justified version of the string

* **partition()**: Returns a tuple where the string is parted into three parts

* **rsplit()**: Splits the string at the specified separator, and returns a list

* **rstrip()**: Returns a right trim version of the string

* **split()**: 	Splits the string at the specified separator, and returns a list

* **splitlines()**: Splits the string at line breaks and returns a list

* **startswith()**: Returns true if the string starts with the specified value

* **strip()**: Returns a trimmed version of the string

* **swapcase()**: Swaps cases, lower case becomes upper case and vice versa

* **title()**: Converts the first character of each word to upper case

* **translate()**: Returns a translated string

* **upper()**: Converts a string into upper case

* **zfill()**: Fills the string with a specified number of 0 values at the beginning


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
