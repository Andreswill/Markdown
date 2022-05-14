# ***Aprendiendo Python*** :computer:

Este documento lo realizo con el objetivo de guardar mis apuntes
relacionadas a Python. Como; Funciones, Tuplas, Diccionarios, Condicionales. etc

___
## **Operadores y Variables** 
*Operadores Aritméticos:*
+ El operador de suma (+)
+ El operador de resta (-)
+ Multiplicación (*)
+ División (/)
+ Módulo (%)
+ Exponente (**)
+ División entera (//)

*Operadores de comparación:*
+ Igual que (==)
+ Mayor que (>)
+ Menor que (<)
+ Mayor o igual que (>=)
+ Menor o igual que (<=)
+ Diferente que (!=)

*Operadores Lógicos:*
+ AND 
+ OR
+ NOT

*Operadores de Asignación:*
+ Igual (=)
+ Incremento (+=)
+ Decremento (-=)

## **Variables**
Espacio en la memoria del ordenador donde se almacenará un valor que podrá cambiar durante la ejecución del programa.
___
Para asignar un valor a una variable se utiliza el operador de igualdad (=).
Los nombres de las variables pueden contener mayúsculas, pero tenga en cuenta que Python distingue entre mayúsculas y minúsculas (en inglés se dice que Python es case-sensitive).
 ___

 ```python
 >>> # Definimos dos variables llamadas numero1 y
>>> # numero2, y asociaremos un número a cada una
>>> numero1=int(5)
>>> numero2=float(6.5)
>>> print (numero1)
5
>>> print (numero2)
6.5 
```

```py
nombre = input("Introduce tu nombre: ")

print("Hola " + nombre + ", vamos a realizar una multiplicación.")

num1 = int(input("Introduce el primer numero: "))
num2 = int(input("Introduce el segundo numero: "))

resultado = num1*num2

print(nombre + " El resultado de la multiplicación es: ", resultado)
```


# **Funciones** 
Una función te permite definir un bloque de código reutilizable que se puede ejecutar muchas veces dentro de tu programa. Una función tiene las siguientes características:

* La palabra clave **(def)**
* Un nombre de función
* Paréntesis **()**, y dentro de los paréntesis los parámetros de entrada, aunque los parámetros de entrada sean opcionales.
* Dos puntos ’**:**’
* Algún bloque de código para ejecutar
* Una sentencia de retorno (opcional)  
___
Aquí en este ejemplo ya definimos la función

```python
def suma(a, b):
   resul = a + b
   return resul

```
El programa funciona, pero la consola aún no mostrara el resultado, debemos llamar a esa función y agregarle los datos o numeros a sumar.

```python
def suma(a, b):
   resul = a + b
   return resul # retornamos los valores cuantas veces queramos
   
# Creamos dos variables para almacenar los datos ingresados por teclado
num1 = int(input("Ingresa el primer numero: ")) # num1 = a
num2 = int(input("Ingresa el segundo numero: ")) # num2 = b
suma = suma(num1,num2) # suma = a+b     
print("El resultado de la suma es: ", suma)   # resultado

```
___
# Tuplas o Listas
*Una lista no es lo mismo que una tupla. Ambas son un conjunto ordenado de valores, en donde este último puede ser cualquier objeto: un número, una cadena, una función, una clase, una instancia, etc. La diferencia es que las listas presentan una serie de funciones adicionales que permiten un amplio manejo de los valores que contienen. Basándonos en esta definición, puede decirse que las listas son dinámicas, mientras que las tuplas son estáticas.*
* ## **Listas** 
*Existen dos formas de hacerlo:*

````python
a = []     # Forma 1
b = list()  # Forma 2
````
*Al utilizar los corchetes [] se crea una lista vacía, sin valores. Estos pueden especificarse durante la creación ingresándolos dentro de los corchetes y separados por comas.*

```python
milista = ["Andres", "Colombia", 27, 2002]
```
```py
lista = ["Andres", "Pacheco", "Colombia"]
print(lista)

print(lista[0:2])
print(lista[-1])
print(len(lista))



lista.append(2022) # Append se utiliza para agregar mas elementos a la lista 
print(lista)

lista.insert(3, "Mayo") # Insertar un elemento donde queramos en este caso posición 3
print(lista)

```

```py
numeros = [1, 2, 3, 4, 5]

numeros.extend([6, 7, 8])  # Extend se utiliza para concatenar listas 
print(numeros)
```

```py
lista = ["Andres", "Colombia", 2022]
print("Andres" in lista)     # se utiliza para saber si un elemento esta en la lista (True o False)



print(lista.index(2022)) # posición del elemento 2022 en este caso seria index 2

print(lista.count("Andres")) # Cuantas veces esta "Andres"

lista.remove(2022) # Elimina un elemento descrito
print(lista)  

lista.clear() # Elimina todos los elementos
print(lista)
```


* ## **Tuplas**
*Al igual que en las listas hay dos formas de hacerlo:* 

````python
a = ()
b = tuple()
````
*Como las tuplas son estáticas, debes especificar sus elementos durante la creación:*

```python
mitupla=("Andres", "Colombia", 2002)
```
*Puedo hacer un llamado de datos* :open_mouth:
```python
mitupla=("Andres", "Colombia", 2022)

name, Pais, year=mitupla # Aquí estoy dandole un nombre a cada elemento de la tupla

# al llamarlos me apareceran los datos de la tupla en consola
print(name)     #  Andres
print(Pais)     #  Colombia 
print(year)     #  2022

```
# **Condicionales if - else**

```py
print("Este es un sistema que te dice si pasaste el semestre.")

nombre = input("Para comenzar digita tu nombre: ")
print("Hola " + nombre + ", presiona la tecla 'Enter' para ingresar tus calificaciones.")

matematicas = int(input("Introduce la calificación de Matemáticas: "))
fisica = int(input("Introduce la calificación de Fisíca: "))
quimica = int(input("Introduce la calificación de Química: "))

promedio = (matematicas + fisica + quimica) / 3

promedio = int(promedio)

if promedio >= 3:
	print("Felicidades " + nombre + ", has pasado el semestre en: ", promedio)


else:
	print("Lo sentimos mucho " + nombre + ", has reprobado el semestre.")


print("El programa ha finalizado.")	 


```
```py
print(":::Calculadora:::")

print("\n")
print("Menú de opciones...")
print("\n")
print("Suma: 1")
print("Resta: 2")
print("Multiplicación: 3")
print("División: 4")
print("División Entera: 5")
print("Exponente: 6")
print("Resto o Modulo: 7")
print("\n")

opcion = int(input("Ingresa el numero de la operación que deseas ejecutar: "))
print("\n")

if opcion == 1:
	numero = int(input("Ingresa el primer numero: "))
	numero += int(input("Ingresa el segundo numero: "))
	print("El resultado de la suma es: ", numero)
	print("FIN DEL PROGRAMA...")
elif opcion == 2:
	numero = int(input("Ingresa el primer numero: "))
	numero -= int(input("Ingresa el segundo numero: "))
	print("El resultado de la resta es: ", numero)
	print("FIN DEL PROGRAMA...")
elif opcion == 3:
	numero = int(input("Ingresa el primer numero: "))
	numero *= int(input("Ingresa el segundo numero: "))	
	print("El resultado de la Multiplicación es: ", numero)
	print("FIN DEL PROGRAMA...")
elif opcion == 4:
	numero = float(input("Ingresa el primer numero: "))
	numero /= float(input("Ingresa el segundo numero: "))
	print("El resultado de la División es: ", round(numero, 2))
	print("FIN DEL PROGRAMA...")
elif opcion == 5:
	numero = int(input("Ingresa el primer numero: "))
	numero //= int(input("Ingresa el segundo numero: "))
	print("El resultado de la División Entera es: ", numero)
	print("FIN DEL PROGRAMA...")
elif opcion == 6:
	numero = int(input("Ingresa el primer numero: "))
	numero **= int(input("Ingresa el segundo numero: "))
	print("El resultado de Exponente es: ", numero)
	print("FIN DEL PROGRAMA...")
elif opcion == 7:
	numero = int(input("Ingresa el primer numero: "))
	numero %= int(input("Ingresa el segundo numero: "))
	print("El resultado de Resto o Modulo es: ", numero)
	print("FIN DEL PROGRAMA...")
else:
	print("Opción no valida...")


```

# **Bucles**
*Los bucles son otra herramienta para alterar el flujo normal de un programa. Nos permiten repetir una porción de código tantas veces como queramos. Python incluye únicamente dos tipos de bucle: while y for.* 
___
## **For**
En general, un bucle es una estructura de control que repite un bloque de instrucciones. Un bucle for es un bucle que repite el bloque de instrucciones un número prederminado de veces. El bloque de instrucciones que se repite se suele llamar cuerpo del bucle y cada repetición se suele llamar iteración.

La sintaxis de un bucle for es la siguiente:

```python
for variable in elemento iterable (lista, cadena, range, etc.):
    cuerpo del bucle
```

```py
for i in [1,2,3]:
	print("Hello") 

# Hello
# Hello 
# Hello


```
```py
# con (end)

for i in [1,2,3]:
	print("Hello", end=" ") # Hello Hello Hello
```
```PY

mail=False

Email = input("Ingresa tu correo electronico: ")

for i in Email:
	if (i=="@"):
		mail=True
if mail:
	print("El email es correcto") 
else:
	print("El email es incorrecto")

```
> **range()** *es el argumento que controla el número de veces que se ejecuta el bucle.*

````py
for i in range(5): # 0, 1, 2, 3, 4
	print("Hello Word") # Ejecuta "Hello Word" 4 veces
````

## **While**
*Un bucle **while** permite repetir la ejecución de un grupo de instrucciones mientras se cumpla una condición (es decir, mientras la condición tenga el valor True).*

*La sintaxis del bucle **while** es la siguiente:*
```py
while condicion:
    cuerpo del bucle
```
```py
numero = int(input("Ingresa un numero positivo menor que 100: "))


while numero<0 or numero>100:
	print("Has introducido un numero incorrecto")
	numero = int(input("Ingresa el numero de nuevo: "))

print("Ya puedes pasar")
print("verificación exitosa, porque el numero: ", str(numero) + " es positivo") 
```

```py
for name in "Andres":
	print("Estas viendo la letra: " + name)
```

# **Continue**

La instrucción **continue** da la opción de omitir la parte de un bucle en la que se activa una condición externa, pero continuar para completar el resto del bucle. Es decir, la iteración actual del bucle se interrumpirá, pero el programa volverá a la parte superior del bucle.

```py
for name in "Andres Pacheco":
	if name==" ": # Quitara el espacio entre Andres y Pacheco
		continue
	print("Estas viendo la letra: " + name)

# Estas viendo la letra: A
# Estas viendo la letra: n
# Estas viendo la letra: d
# Estas viendo la letra: r
# Estas viendo la letra: e
# Estas viendo la letra: s
# Estas viendo la letra: P
# Estas viendo la letra: a
# Estas viendo la letra: c
# Estas viendo la letra: h
# Estas viendo la letra: e
# Estas viendo la letra: c
# Estas viendo la letra: o


```

```py
print(len("Hola Andres"))
print("\n")

print("Hola Andres", len("Hola Andres"))
print("\n")

longitud = len("Hola Andres")
print(longitud)
```