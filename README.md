# Reto-4
_En el siguiente repositorio se muestran las soluciones al reto 4, junto con el notebook de los mismo._

## Tabla de contenido
1. [1. Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.](#1.-dado-un-número-entero,-determinar-si-ese-número-corresponde-al-código-ascii-de-una-vocal-minúscula.)
	- [Pseudocódigo 1](#pseudocódigo-1)
	- [Diagrama de flujo 1](#diagrama-de-flujo-1)
2. [Algoritmo para sacar raiz cuadrada a un número n](#algoritmo-para-sacar-raiz-cuadrada-a-un-número-n)
	- [Pseudocódigo 2](#pseudocódigo-2)
	- [Diagrama de flujo 2](#diagrama-de-flujo-2)

### 1. Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.

```
try:
    #Se declaran variables.

    n : int
    
    n = int(input("Ingrese un numero entero: "))
    if n >= 97 and n <= 122:
        print("El numero " + str(n) + " corresponde al código ASCII de "+ chr(n) +" ")
    else:
        print("El numero " + str(n) + " no corresponde al código ASCII de una vocal minúscula")
except ValueError:
    print("Por favor ingrese un número válido")
```
    

### 2. Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.

```
try:
    n = ord(input("Ingrese un solo caracter"))

    #Si módulo de n == 0, n es par, sino, es impar.

    if n % 2 == 0:
        print("El código ASCII del primerer caracter de la cadena es par")
    else:
        print("El código ASCII del primerer caracter de la cadena no es par")
except IndexError:
    print("Por favor ingrese un caracter")
```

### 3. Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.

```
try:
    #Se declaran variables.
    
    n : int

    n = int(input("Ingrese un numero entero: "))

    #Se determina intérvalo para saber si n es un caracter.

    if 0 <= n and  n < 10:
        print("El caracter es un dígito.")
    else:
        print("El caracter no es un dígito.")
except ValueError:
    print("Por favor ingrese un caracter válido, el caracter debe ser un número menor a 10")
```

### 4. Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:
* Positivo: "El número x es positivo"
* Negativo: "El número x es negativo"
* Cero (0): "El número x es el neutro para la suma"

```
try:
    #Se declaran variables.

    n : float
    
    n = float(input("Ingrese un numero entero: "))

    #Se determinan intérvalos para saber si n es positivo, negativo o neutro para la suma.

    if n > 0:
        print("El numero " + str(n) + " es positivo")
    elif n < 0:
        print("El numero " + str(n) + " es negativo")
    else:
        print("El numero " + str(n) + " es el neutro para la suma")
except ValueError:
    print("Por favor ingrese un número válido")
```

### 5. Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.
```
try:
    #Se declaran variables.
    
    x_centro_circulo : float
    y_centro_circulo : float
    radio : float
    a_coordenada : float
    b_coordenada : float
    
    x_centro_circulo = float(input("Ingrese la coordenada x del centro del círculo"))
    y_centro_circulo = float(input("Ingrese la coordenada y del centro del círculo "))
    radio = float(input("Ingrese el radio del círculo "))
    a_coordenada = float(input("Ingrese la coordenada x del punto"))
    b_coordenada = float(input("Ingrese la coordenada y  del punto "))

    #Se determina si el punto pertenece al círculo.

    if radio >= 0.5*(((a_coordenada - x_centro_circulo)*2 + (b_coordenada - y_centro_circulo)*2)):
        print("La pareja ordenada", (a_coordenada,b_coordenada), "pertenece el círculo")
    else:
        print("La pareja ordenada", (a_coordenada,b_coordenada), "no pertenece el círculo")
except ValueError:
    print("Por favor ingrese la variable en el formato apropiado")
```

### 6.Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

```
try:
    #Se declaran variables.
    
    longitud_a : float
    longitud_b : float
    longitud_c : float

    longitud_a = float(input("Ingrese la longitud a del tiángulo: "))
    longitud_b = float(input("Ingrese la longitud b del tiángulo: "))
    longitud_c = float(input("Ingrese la longitud c del tiángulo: "))  

    #Se determina si las longitudes son aptas para hacer un triángulo.

    if longitud_a < (longitud_b + longitud_c) and longitud_b < (longitud_a + longitud_c) and longitud_c < (longitud_a + longitud_b): 
            print("Con las longitudes", longitud_a, "," , longitud_b , "y", longitud_c, "se puede hacer un triángulo ")
    else:
        print("Con las longitudes", longitud_a, "," , longitud_b ,"y", longitud_c, "no se puede hacer un triángulo ")
except ValueError:
    print("Por favor ingrese las longitudes en el formato apropiado")
```
