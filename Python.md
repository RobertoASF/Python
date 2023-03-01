[![Python](https://img.shields.io/badge/Python-3.10+-green?style=flat&logo=python&logoColor=white&labelColor=101010)](https://python.org)
![Last commit](https://img.shields.io/github/last-commit/RobertoASF/Python?logo=git&logoColor=green)
![Progreso](https://img.shields.io/badge/estado-en%20construcci%C3%B3n-red)


# Python

---

## Índice

* [Tipos de datos](#tipos-de-datos)
* [Variables](#variables)
* [Tipos de datos](#tipos-de-datos)
  * [Enteros](#enteros)
  * [Flotantes](#flotantes)
  * [Complejos](#complejos)
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

## Tipos de datos

| Familia | Tipo |
|-------- |------| 
| Text Type |	[strings](#string) |
| Numeric Types |	[integer](#enteros), [float](#flotantes), [complex](#complejos) |
| Sequence Types |	[listas](#listas), [tuplas](#tuplas), range |
| Mapping Type | 	[diccionarios](#diccionarios) |
| Set Types |	[set](#sets), frozenset |
| Boolean Type |	[bool](#booleanos) |
| Binary Types | 	bytes, bytearray, memoryview |
| None Type | 	NoneType |

## Variables

### Formas de nombrar una variable
### Reglas para nombrar variables
### Convenciones
variables en snake case


### Enteros

Los número enteros en python son aquellos que no tienen parte decimal 

`edad = 30`

### Flotantes

`altura = 1.75 `  
`edad = 30. `

### Complejos


### Métodos de tipos numéricos

* **abs(x)**: devuelve el valor absoluto de x.

```python
x = -3
y = abs(x)
print(y) # Output: 3
```

* **int(x)**: convierte x a un entero.

```python
x = 3.7
y = int(x)
print(y) # Output: 3
```

* **float(x)** : convierte x a un número decimal.

```python
x = 4
y = float(x)
print(y) # Output: 4.0
```

* **complex(real, imag)**: crea un número complejo con la parte real real y la parte imaginaria imag.

```python
x = 2
y = complex(x)
print(y) # Output: (2+0j)
```

* **pow(x, y[, z])**: devuelve x elevado a la potencia y, si se proporciona z se aplica el operador módulo.

```python
x = 2
y = pow(x, 3)
print(y) # Output: 8
```

* **sqrt()**: Devuelve la raíz cuadrada de un número dado
```python
import math

x = 16
y = math.sqrt(x)
print(y) # Output: 4.0
```
* **sin()**: Devuelven el seno de un ángulo dado

```python
import math

x = math.pi/4 # ángulo de 45 grados
y = math.sin(x)
print(y) # Output: 0.7071067811865475
```

* **cos()**: Devuelve el coseno de un ángulo dado

```python
import math

x = math.pi/3 # ángulo de 60 grados
cos_x = math.cos(x)

print(cos_x) # Output: 0.5
```

* **tan()**: Devuelve la tangente de un ángulo dado

```python
import math

x = math.pi/3 # ángulo de 60 grados
tan_x = math.tan(x)

print(tan_x) # Output: 1.7320508075688767
```

* **log()**:

```python
import math

x = 2.71828
y = math.log(x)
print(y) # Output: 0.999999327347282
```

* **divmod(x, y)**: devuelve el cociente y el resto de la división de x entre y.

```python
x = 10
y = 3

div, mod = divmod(x, y)

print(div) # Output: 3
print(mod) # Output: 1
```

* **round(x[, n])**: devuelve el número x redondeado al número de dígitos especificado por n.

```python
x = 3.456
y = round(x, 2)
print(y) # Output: 3.46
```

* **max(iterable[, args...][key])**: devuelve el valor máximo en iterable, o el valor máximo entre los argumentos args, opcionalmente utilizando una función de key para comparar los elementos.

```python
secuencia = [1, 2, 3, 4, 5]
max_num = max(mi_lista)
print(max_num) # Output: 5
```

* **min(iterable[, args...][key])**: devuelve el valor mínimo en iterable, o el valor mínimo entre los argumentos args, opcionalmente utilizando una función de key para comparar los elementos.

```python
secuencia = [1, 2, 3, 4, 5]
min_num = min(secuencia)
print(min_num) # Output: 1
```

* **sum(iterable[, start])**: devuelve la suma de los elementos en iterable, opcionalmente comenzando por el valor start.

```python
secuencia = [1, 2, 3, 4, 5]
sum_list = sum(secuencia)
print(sum_list) # Output: 15
```

* **len(s)**: devuelve la longitud de la secuencia.

```python
secuencia = [1, 2, 3, 4, 5]

len_list = len(secuencia)
print(len_list) # Output: 5
```

* **hex(x)**: convierte x a una cadena que representa el valor en formato hexadecimal.

```python
x = 42

hex_x = hex(x)
print(hex_x) # Output: 0x2a
```

* **oct(x)**: convierte x a una cadena que representa el valor en formato octal.

```python
x = 42

oct_x = oct(x)
print(oct_x) # Output: 0o52
```

* **bin(x)**: convierte x a una cadena que representa el valor en formato binario.

```python
x = 42

bin_x = bin(x)
print(bin_x) # Output: 0b101010

```

* **isinstance(x, int/float/complex)**: devuelve True si x es una instancia de la clase int, float, o complex.

```python
x = 42
y = "42"

is_int = isinstance(x, int)
is_str = isinstance(y, str)

print(is_int) # Output: True
print(is_str) # Output: True
```

* **is_integer()**: devuelve True si el número es un entero, de lo contrario devuelve False.

```python
x = 42.0 + 3j

is_int = x.real.is_integer()
print(is_int) # Output: True
```

* **real**: devuelve la parte real del número complejo.

```python
x = 42.0 + 3j

real_x = x.real
print(real_x) # Output: 42.0
```

* **imag**: devuelve la parte imaginaria del número complejo.

```python
x = 42.0 + 3j

imag_x = x.imag
print(imag_x) # Output: 3.0
```

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

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| tabsize |

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

* **index(value, start, end)**: devuelve el índice de la primera ocurrencia de la subcadena substring en el string dentro del rango start y end. Si no se encuentra la subcadena, lanza una excepción ValueError.

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| value | **Requerido**: calor a buscar |
| start | **Opcional**: valor correspondiente a la posición donde comenzar a buscar, por defecto 0|
| end | **Opcional**: valor correspondiente a la posición donde termina de buscar, por defecto es el largo del string |


```python
>>> texto = "Hello, Wolrd! From Pyhton."
>>> print(txt.index("y"))
19
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

* **join(iterable)**: Une todos los elementos de un objeto iterable dentro de un string usando un separador (string sobre el que se aplica el método join)

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| iterable | **Requerido**: cualquier objeto iterable donde todos los valores retornados sean string|
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
Hola, chau!
```

* **partition(valor)**: devuelve una tupla en la que el string es dividido en tres partes (la parte antes del valor buscado, el valor buscado y la parte que procede al valor buscado)

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| valor | **Requerido**: string a buscar|

```python
>>> texto = 'Hello, World! From Python'
>>> print(texto.partition("World!"))
('Hello, ', 'World!', ' From Python')
```

* **replace(oldvalue, newvalue, count)**: devuelve un string donde un valor específico ha sido reemplazado por por un valor indicado

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| oldvalue | **Requerido**: string a buscar|
| newvalue | **Requerido**: string a reemplazar |
| count | **Opcional**: numero especifico de cantidad de ocurrencias del antiguo valor a reemplazar, por defecto reemplaza todas las ocurrencias |

```python
>>> texto = 'Hello World! From Python'
>>> print(texto.replace('Python','Chile'))
Hello World! From Chile
```

* **rfind(value, start, end)**: Searches the string for a specified value and returns the last position of where it was found. En caso de no encontrar el valor devuelve -1

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| value | **Requerido**: valor a buscar |
| start | **Opcional**: valor de posicion de inicio de la busqueda, por defecto 0 |
| end | **Opcional**: valor del posicion del final de la busqueda |

```python
>>> texto = 'Hello World! From Python'
>>> print(texto.rfind('m'))
16

>>> texto = 'Hello World! From Python'
>>> print(texto.rfind('m',0,15))
-1
```

* **rindex()**: Searches the string for a specified value and returns the last position of where it was found

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| value | **Requerido**: valor a buscar |
| start | **Opcional**: valor de posicion de inicio de la busqueda, por defecto 0 |
| end | **Opcional**: valor del posicion del final de la busqueda, por defecto el final del string |

```python
>>> texto = 'Hello World! From Python'
>>> print(texto.rindex('o'))
22
```

* **rjust(length, character)**: Returns a right justified version of the string

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| length | **Requerido**: largo del string a devolver |
| character | **Opcional**: caracter con el que rellenar, por defecto es espacio " "|

```python
>>> texto = 'Python'
>>> print(texto.rjust(20,'_'))
______________Python
```

* **rsplit(separator, maxsplit)**: Splits the string at the specified separator, and returns a list

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| separator | **Opcional**: especifica el separador que se va a usar |
| maxsplit | **Opcional**: especifica cuandos separaciones debe hacer, valor por defecto es -1 ("todas las ocurrencias") |

```python
>>> texto = "python, java, rust"
>>> print(texto.rsplit(", "))
['python', 'java', 'rust']

>>> texto = "python, java, rust"
>>> print(texto.rsplit(", ",1))
['python, java', 'rust']

>>> texto = "manzana confitada"
>>> print(texto.rsplit("a"))
['m', 'nz', 'n', ' confit', 'd', '']

>>> texto = "manzana confitada"
>>> print(texto.rsplit("a",3))
['manzan', ' confit', 'd', '']
```

* **rstrip(characters)**: Devuelve el recorte derecho de la cadena

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| characters | **Opcional**: una coleccion de caracteres a remover como caracteres finales |

```python
>>> texto = 'Python..--.-.-.-.-.-.-.-.-.'
>>> print(texto.rstrip('..--.-.-.-.-.-.-.-.-.'))
Python
```

* **split(separador, maxsplit)**: 	Divide el string en el separador especificado y devuelve una lista

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| separador | **Opcional**: Especifica el separador que se va a utilizar al dividir el string. De forma predeterminada, cualquier espacio en blanco es un separador |
| maxsplit | **Opcional**: Especifica cuántas divisiones se van a realizar. El valor predeterminado es -1, que es "todas las ocurrencias"|


```python
>>> texto = 'Hello World! from Python, this is the split method'
>>> print(texto.split())
['Hello', 'World!', 'from', 'Python,', 'this', 'is', 'the', 'split', 'method']

>>> texto = 'Hello World! from Python, this is the split method'
>>> print(texto.split(','))
['Hello World! from Python', ' this is the split method']
```

* **splitlines(keeplinebreaks)**: Divide el string en los saltos de línea y devuelve una lista

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| keeplinebreaks | **Opcional**: Especifica si los saltos de línea deben incluirse (**True**) o no (**False**). El valor predeterminado es False

```python
>>> texto = 'Hello World!\nfrom Python'
print(texto.splitlines())
['Hello World!', 'from Python']

>>> texto = 'Hello World!\nfrom Python'
print(texto.splitlines(True))
['Hello World!\n', 'from Python']
```

* **startswith(value, start, end)**: Devuelve True si la cadena comienza con el valor especificado

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| value |  **Requerido**: valor a comprobar si con esto comienza el string|
| start |  **Opcional**: valor entero que indica la posicion donde comienza la busqueda|
| end | **Opcional**: valor entero que indica la posicion donde finaliza la busqueda|

```python
>>> texto = 'Hello World! from Python'
>>> print(texto.startswith('H'))
True

>>> texto = 'Hello World! from Python'
>>> print(texto.startswith('H',1))
False

>>> texto = 'Hello World! from Python'
>>> print(texto.startswith('e',1))
True
```

* **strip(characters)**: Devuelve una versión recortada del string

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| characters | **Opcional**:  Un conjunto de caracteres para quitar como caracteres iniciales/finales|

```python
>>> texto = "     Python     "
>>> strip = texto.strip()
>>> print("estudiando", strip , "para IA")
estudiando Python para IA

>>> texto = "______Python______"
>>> strip = texto.strip('_')
>>> print("estudiando", strip , "para IA")
estudiando Python para IA
```

* **swapcase()**: Devuelve un string donde todas las letras mayúsculas son minúsculas y viceversa.

```python
>>> texto = 'Hello World! from Python'
>>> print(texto.swapcase())
hELLO wORLD! FROM pYTHON

>>> texto = 'hELLO wORLD! FROM pYTHON'
>>> print(texto.swapcase())
Hello World! from Python
```

* **title()**: convierte el primer caracter de cada palaba en mayusculas

```python
>>> texto = 'hello world! from python'
>>> print(texto.title())
Hello World! From Python
```

* **translate(tabla)**: devuelve un stirng traducido

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| tabla | **Requerido**: Un diccionario o una tabla de asignación que describa cómo realizar el reemplazo |

```python
>>> diccionario = {83:  80}
>>> texto = "Quiero Sandia!"
>>> print(texto.translate(diccionario))
Quiero Pandia!
```

* **upper()**: convierte todo el string a mayusculas

```python
>>> texto = 'Hello World! from Python'
>>> print(texto.upper())
HELLO WORLD! FROM PYTHON
```

* **zfill(len)**: Rellena el string con un número especificado de valores 0 al principio

| PARÁMETRO  | DESCRIPCIÓN  |
|:----------:|--------------|
| len |**Requerido**: numero deseado del largo del string 

```python
>>> numero = '99'
>>> print(numero.zfill(10))
0000000099

texto = 'Python'
print(texto.zfill(15))
000000000Python
```

### Booleanos

### Listas

### Métodos de las listas



* **append()**:	Añade un elemento al final de la lista.

```python
mi_lista = [1, 2, 3]
mi_lista.append(4)
print(mi_lista) # Output: [1, 2, 3, 4]
```

* **clear()**:	Removes all the elements from the list

```python

```

* **copy()**:	Devuelve una copia superficial de la lista.

```python
mi_lista = [1, 2, 3]
new_list = mi_lista.copy()
print(new_list) # Output: [1, 2, 3]
```

* **count()**:	Cuenta el número de veces que aparece un elemento en la lista.

```python
mi_lista = [1, 2, 3, 2]
x = mi_lista.count(2)
print(x) # Output: 2
```

* **extend()**:	Añade los elementos de otra lista al final de la lista actual.

```python
mi_lista = [1, 2, 3]
other_list = [4, 5, 6]
mi_lista.extend(other_list)
print(mi_lista) # Output: [1, 2, 3, 4, 5, 6]
```

* **index()**:	Devuelve la posición del primer elemento que tenga el valor especificado.

```python
mi_lista = [1, 2, 3, 2]
x = mi_lista.index(2)
print(x) # Output: 1
```

* **insert()**: Inserta un elemento en una posición específica de la lista.

```python
mi_lista = [1, 2, 3]
mi_lista.insert(1, 4)
print(mi_lista) # Output: [1, 4, 2, 3]
```

* **pop()**:	Elimina el elemento de la lista que se encuentra en la posición especificada, y lo devuelve.

```python
mi_lista = [1, 2, 3]
x = mi_lista.pop(1)
print(mi_lista) # Output: [1, 3]
print(x) # Output: 2
```

* **remove()**:	Elimina el primer elemento de la lista que tenga el valor especificado.

```python
mi_lista = [1, 2, 3, 2]
mi_lista.remove(2)
print(mi_lista) # Output: [1, 3, 2]
```

* **reverse()**:	Invierte el orden de los elementos de la lista.

```python
mi_lista = [1, 2, 3]
mi_lista.reverse()
print(mi_lista) # Output: [3, 2, 1]
```

* **sort()**:	Ordena los elementos de la lista en orden ascendente.

```python
mi_lista = [3, 2, 1]
mi_lista.sort()
print(mi_lista) # Output: [1, 2, 3]
```

### Listas de comprensión

### Tuplas

* **count()**:	Returns the number of times a specified value occurs in a tuple

```python

```

* **index()**:	Searches the tuple for a specified value and returns the position of where it was found

```python

```

### Sets

### Métodos de los set

* **add()**:	Adds an element to the set

```python

```

* **clear()**:	Removes all the elements from the set

```python

```

* **copy()**:	Returns a copy of the set difference() Returns a set containing the difference between two or more sets

```python

```

* **difference_update()**:	Removes the items in this set that are also included in another, specified set

```python

```

* **discard()**:	Remove the specified item

```python

```

* **intersection()**:	Returns a set, that is the intersection of two or more sets

```python

```

* **intersection_update()**:	Removes the items in this set that are not present in other, specified set(s)

```python

```

* **isdisjoint()**:	Returns whether two sets have a intersection or not

```python

```

* **issubset()**:	Returns whether another set contains this set or not

```python

```

* **issuperset()**:	Returns whether this set contains another set or not

```python

```

* **pop()**:	Removes an element from the set

```python

```

* **remove()**:	Removes the specified element

```python

```

* **symmetric_difference()**:	Returns a set with the symmetric differences of two sets

```python

```

* **symmetric_difference_update()**:	inserts the symmetric differences from this set and another
union()	Return a set containing the union of sets
update()	Update the set with another set, or any other iterable

```python

```

### Diccionarios

### Métodos de los diccionarios

* **clear()**:	Elimina todos los elementos del diccionario.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
diccionario.clear()
print(diccionario) # Output: {}
```

* **copy()**:	Devuelve una copia superficial del diccionario.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
neuevo_diccionario = diccionario.copy()
print(neuevo_diccionario) # Output: {"nombre": "Roberto", "edad": 33}
```

* **fromkeys()**:	Returns a dictionary with the specified keys and value

```python

```

* **get()**:	Devuelve el valor correspondiente a la clave especificada.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = diccionario.get("edad")
print(x) # Output: 33
```

* **items()**:	Devuelve una lista que contiene una tupla para cada par clave-valor en el diccionario.
python

```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = diccionario.items()
print(x) # Output: [("nombre", "Roberto"), ("edad", 33)]
```

* **keys()**:	Devuelve una lista que contiene todas las claves del diccionario.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = diccionario.keys()
print(x) # Output: ["nombre", "edad"]
```

* **len()**: Devuelve la cantidad de pares clave-valor en el diccionario.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = len(diccionario)
print(x) # Output: 2
```


* **pop()**:	Elimina el elemento con la clave especificada y devuelve el valor correspondiente.
```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = diccionario.pop("edad")
print(x) # Output: 33
print(diccionario) # Output: {"nombre": "Roberto"}
```

* **popitem()**:	Elimina el último par clave-valor insertado en el diccionario y lo devuelve como una tupla.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = diccionario.popitem()
print(x) # Output: ("edad", 33)
print(diccionario) # Output: {"nombre": "Roberto"}
```

* **setdefault()**:	Returns the value of the specified key. If the key does not exist: insert the key, with the specified value

```python

```

* **update()**:	Actualiza el diccionario con los pares clave-valor de otro diccionario o de una secuencia de pares clave-valor.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
diccionario.update({"edad": 34, "nacionalidad": "chilena"})
print(diccionario) # Output: {"nombre": "Roberto", "edad": 34, "nacionalidad": "New chilena"}
```

* **values()**: Devuelve una lista que contiene todos los valores del diccionario.

```python
diccionario = {"nombre": "Roberto", "edad": 33}
x = diccionario.values()
print(x) # Output: ["Roberto", 33]
```


### Operadores de desición

### Operadores de iteración

### Funciones

En Python, una función es un bloque de código reutilizable que realiza una tarea específica. Las funciones son útiles para dividir el código en tareas más pequeñas y fáciles de entender. Para definir una función en Python, se utiliza la palabra clave def, seguida del nombre de la función y los parámetros entre paréntesis. Luego, se escribe el código de la función en un bloque indentado. Aquí hay un ejemplo sencillo:  

Ejemplo:

```python
def suma(num1, num2):
    resultado = num1 + num2
    return resultado

resultado = suma(3, 5)
print(resultado)
```

En este ejemplo, se define una función llamada suma que toma dos parámetros _num1_ y _num2_. Dentro de la función, se suma los valores de _num1_ y _num2_, y se guarda el resultado en una variable llamada _resultado_. Luego, se devuelve el valor de _resultado_ con la palabra clave return. Finalmente, se llama a la función suma con los argumentos 3 y 5, y el valor devuelto se guarda en una variable llamada _resultado_, que se imprime en la pantalla.


También es posible definir funciones sin parámetros. 

Ejemplo:

```python
def imprimir_saludo():
    print("Buenas buenas, ¿cómo estás?")
imprimir_saludo()
```
En este ejemplo, se define una función llamada _imprimir_saludo_ que no toma ningún parámetro. Dentro de la función, se imprime un mensaje de saludo en la pantalla. Luego, se llama a la función _imprimir_saludo_ sin argumentos.


Las funciones también pueden tener valores predeterminados para los parámetros.

Ejemplo:

```python
def multiplicar(num1, num2=1):
    resultado = num1 * num2
    return resultado
resultado1 = multiplicar(3, 5)
resultado2 = multiplicar(3)
print(resultado1)
print(resultado2)
```

En este ejemplo, se define una función llamada _multiplicar_ que toma dos parámetros num1 y num2, donde num2 tiene un valor predeterminado de 1. Dentro de la función, se multiplica los valores de num1 y num2, y se guarda el resultado en una variable llamada resultado. Luego, se devuelve el valor de resultado con la palabra clave return. Se llama a la función multiplicar con los argumentos 3 y 5, y el valor devuelto se guarda en una variable llamada resultado1, que se imprime en la pantalla. También se llama a la función multiplicar con un solo argumento 3, lo que hace que num2 tenga el valor predeterminado de 1. El valor devuelto se guarda en una variable llamada resultado2, que también se imprime en la pantalla.


### Decoradores
 Los decoradores permiten modificar el comportamiento de una función sin modificar su código. Los decoradores son funciones que toman como argumento otra función y devuelven una nueva función. Ejemplo:  
 1. Definir un decorador:

 ```python
def mi_decorador(funcion):
    def wrapper(*args, **kwargs):
        print("Mensaje antes de llamar a la función")
        resultado = funcion(*args, **kwargs)
        print("Mensaje después de llamar a la función")
        return resultado
    return wrapper
```
Este decorador simplemente agrega un mensaje de impresión antes y después de llamar a la función que se le pasa como argumento.

2. Aplicar el decorador a una función:
 ```python
@mi_decorador
def mi_funcion():
    print("Hola desde mi_funcion")
  ```
Esto es equivalente a llamar a la función de esta manera:

 ```python
mi_funcion = mi_decorador(mi_funcion)
  ```
3. Llamar a la función:
 ```python
mi_funcion()
```

La salida de este código sería:

```python
Antes de llamar a la función
Hola desde mi_funcion
Después de llamar a la función
```
El decorador envuelve la función original en una nueva función (wrapper) que agrega el mensaje de impresión antes y después de llamar a la función original.

También se puede usar decoradores con argumentos. 

Ejemplo:

 ```python
def decorador_con_argumentos(argumento):
    def decorador(funcion):
        def wrapper(*args, **kwargs):
            print("Argumento del decorador:", argumento)
            resultado = funcion(*args, **kwargs)
            return resultado
        return wrapper
    return decorador

@decorador_con_argumentos("Hola")
def mi_funcion():
    print("Hola desde mi_funcion")

```


  
En este ejemplo, decorador_con_argumentos es un decorador de nivel superior que toma un argumento. El decorador real (decorador) toma la función y devuelve la nueva función envuelta (wrapper). Cuando _mi_funcion_ se llama, se envuelve en la nueva función creada por _decorador_con_argumentos_ y _decorador_.

### Funciones Lambda

 Las funciones lambda son una forma abreviada de definir funciones anónimas en Python. En lugar de definir una función con un nombre, puedes definir una función lambda en línea. Ejemplo:

1. Definir una función lambda:
 ```python
lambda argumentos: expresión
  ```
La sintaxis de una función lambda consiste en la palabra clave lambda, seguida de una lista de argumentos separados por comas, seguidos de dos puntos y una expresión. La expresión es lo que la función lambda devuelve cuando se llama.

Por ejemplo, aquí hay una función lambda que toma un argumento y lo duplica:  

| nombre | =| "lambda" | argumento| : | función |
|--------|:-:|---|--|:--:|:--:|
| duplicar| = | "lambda" | x | : | x  * 2 |   
```python
duplicar = lambda x: x * 2
```
2. Llamar a la función lambda:
```python
resultado = duplicar(3)
print(resultado)
```
La salida de este código sería:
```python
6
```
La función lambda '_duplicar_' toma un argumento 'x' 'y' devuelve 'x * 2'.' Cuando se llama a la función lambda con un argumento de 3, devuelve 6.  


Las funciones lambda son útiles cuando necesitas una función simple que se use solo una vez. Por ejemplo, si necesitas ordenar una lista de números de menor a mayor, se puede usar la función sorted y una función lambda para especificar el criterio de ordenamiento:
```python
numeros = [1, 3, 2, 5, 4]
numeros_ordenados = sorted(numeros, key=lambda x: x)
print(numeros_ordenados)
```
La salida de este código sería:
```python
[1, 2, 3, 4, 5]
```

### POO
