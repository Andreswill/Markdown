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
print(name)      #  Andres
print(Pais)     #  Colombia 
print(year)     #  2022

```


