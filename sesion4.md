<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

Resolver utilizando funciones en Python

-Calculadora Básica: Crea una función llamada calculadora que tome tres argumentos: dos números y un operador (+, -, *, /). La función debe realizar la operación indicada en los dos números y devolver el resultado.
Ejemplo de uso:
resultado = calculadora(5, 3, '+')  # Debe devolver 8

-Conteo de Vocales: Crea una función llamada contar_vocales que tome una cadena como argumento y devuelva el número de vocales (a, e, i, o, u) que contiene la cadena.
Ejemplo de uso:

num_vocales = contar_vocales("Hola, mundo!")  # Debe devolver 4

-Primo o No Primo: Escribe una función llamada es_primo que tome un número entero positivo como argumento y determine si es un número primo (es decir, solo es divisible por 1 y por sí mismo). La función debe devolver True si es primo y False si no lo es.
Ejemplo de uso:

resultado = es_primo(17)  # Debe devolver True

-Contador de Palabras: Escribe una función llamada contar_palabras que tome una cadena como argumento y devuelva el número de palabras en esa cadena. Supón que las palabras están separadas por espacios.
Ejemplo de uso:

num_palabras = contar_palabras("Hola, este es un ejemplo.")  # Debe devolver 5

-Cálculo de Potencia: Escribe una función llamada potencia que tome dos números enteros como argumentos, uno como base y otro como exponente, y devuelva el resultado de elevar la base al exponente.
Ejemplo de uso:

resultado = potencia(2, 3)  # Debe devolver 8 (2^3 = 2 * 2 * 2)

SOLUCIÓN

```
##ejercicio 1
def calculadora(num1, num2, operador):
    if operador == '+':
        return num1 + num2
    elif operador == '-':
        return num1 - num2
    elif operador == '*':
        return num1 * num2
    elif operador == '/':
        return num1 / num2
    else:
        return 0
    

##ejercicio 2
def contar_vocales(mensaje):
    vocales= 0
    for letra in mensaje:
        if letra in 'aeiouAEIOU':
            vocales += 1
        
    return vocales
    

##ejercicio 3
def es_primo(numero):
    for i in range(2, numero):
        if numero % i == 0:
            return False
    return True
    


##ejercicio 4
def contar_palabras(cadena):
    palabras= cadena.split()
    return len(palabras)
    
    
##ejercicio 5
def potencia(num1,num2):
    return num1 ** num2
    

def volver_al_menu():
    respuesta = input("¿Deseas volver al menú principal? (1 para sí, 2 para no): ")
    if respuesta == '1':
        menu_principal()
    elif respuesta == '2':
        print("Menu de ejercicios finalizado")
        exit()
    else:
        print("Respuesta no valida, seleccione 1 para volver al menú o 2 para salir del programa.")


def menu_principal():

    print("Menu de ejercicios")
    print("Seleccione una opcion: (1-5)")
    print("1. calculadora")
    print("2. contar_vocales")
    print("3. es_primo")
    print("4. contar_palabras")
    print("5. potencia")

    opcion= int(input("Ingrese el numero deseado: "))

    if opcion == 1:
        num1= int(input("Ingrese el numero 1: "))   
        operador= str(input("Ingrese el operador: "))
        num2= int(input("Ingrese el numero 2: "))

        resultado= calculadora(num1, num2, operador)

        print(resultado)
        volver_al_menu()
        
    elif opcion == 2:
        mensaje= str(input("Ingrese un mensaje: "))

        print(contar_vocales(mensaje))
        volver_al_menu()

    elif opcion == 3:

        numero= int(input("Ingrese un numero: "))

        if es_primo(numero):
         print("Es primo")
        else: print("no es primo")
        volver_al_menu()
        
    elif opcion == 4:
        cadena= str(input("Ingrese una cadena: "))

        palabras= contar_palabras(cadena)

        print(palabras)
        volver_al_menu()

    elif opcion == 5:
        num1= int(input("Ingrese un numero: "))
        num2= int(input("Ingrese otro numero: "))

        resultado= potencia(num1,num2)

        print(resultado)
        volver_al_menu()
    else:
        print("Opción no válida. Por favor, seleccione una opción del menú (1-5).")

    print("fin")

menu_principal() 
```






