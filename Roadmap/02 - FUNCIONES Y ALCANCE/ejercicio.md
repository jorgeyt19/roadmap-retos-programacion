# #02 FUNCIONES Y ALCANCE
> #### Dificultad: Fácil | Publicación: 08/01/24 | Corrección: 15/01/24

## Ejercicio

```
/*
 * EJERCICIO:
 * - Crea ejemplos de funciones básicas que representen las diferentes
 *   posibilidades del lenguaje:
 *   Sin parámetros ni retorno, con uno o varios parámetros, con retorno...
 * - Comprueba si puedes crear funciones dentro de funciones.
 * - Utiliza algún ejemplo de funciones ya creadas en el lenguaje.
 * - Pon a prueba el concepto de variable LOCAL y GLOBAL.
 * - Debes hacer print por consola del resultado de todos los ejemplos.
 *   (y tener en cuenta que cada lenguaje puede poseer más o menos posibilidades)
 *
 * DIFICULTAD EXTRA (opcional):
 * Crea una función que reciba dos parámetros de tipo cadena de texto y retorne un número.
 * - La función imprime todos los números del 1 al 100. Teniendo en cuenta que:
 *   - Si el número es múltiplo de 3, muestra la cadena de texto del primer parámetro.
 *   - Si el número es múltiplo de 5, muestra la cadena de texto del segundo parámetro.
 *   - Si el número es múltiplo de 3 y de 5, muestra las dos cadenas de texto concatenadas.
 *   - La función retorna el número de veces que se ha impreso el número en lugar de los textos.
 *
 * Presta especial atención a la sintaxis que debes utilizar en cada uno de los casos.
 * Cada lenguaje sigue una convenciones que debes de respetar para que el código se entienda.
 */
---------------------------
 Definición de funciones
---------------------------

# Función sin parámetros ni retorno
def saludar():
    print("¡Hola, bienvenido!")

saludar()  # Llamada a la función

# Función con un parámetro
def saludar_nombre(nombre):
    print(f"¡Hola, {nombre}!")

saludar_nombre("Carlos")

# Función con varios parámetros
def suma(a, b):
    return a + b

resultado = suma(5, 3)
print("Resultado de la suma:", resultado)

# Función con valores por defecto
def presentar(nombre="Desconocido", edad=0):
    print(f"Nombre: {nombre}, Edad: {edad}")

presentar("Ana", 25)
presentar()

# Función con retorno múltiple
def operaciones(a, b):
    suma = a + b
    resta = a - b
    return suma, resta

res_suma, res_resta = operaciones(10, 5)
print("Suma:", res_suma, "Resta:", res_resta)

---------------------------
 Funciones dentro de funciones
---------------------------
def funcion_externa():
    print("Dentro de la función externa")

    def funcion_interna():
        print("Dentro de la función interna")

    funcion_interna()  # Llamada a la función interna

funcion_externa()

---------------------------
 Uso de funciones incorporadas en Python
---------------------------
print("Número absoluto de -10:", abs(-10))
print("Máximo entre 4, 8 y 2:", max(4, 8, 2))
print("Longitud de 'Python':", len("Python"))

---------------------------
 Variables Locales y Globales
---------------------------

variable_global = "Soy global"

def prueba_variables():
    variable_local = "Soy local"
    global variable_global  # Se indica que se va a modificar la variable global
    variable_global = "Ahora cambié desde la función"
    print("Dentro de la función:", variable_local)

prueba_variables()
print("Fuera de la función:", variable_global)

---------------------------
 DIFICULTAD EXTRA
---------------------------

def fizzbuzz_custom(palabra1, palabra2):
    contador_numeros = 0  # Contador de números impresos
    
    for num in range(1, 101):
        if num % 3 == 0 and num % 5 == 0:
            print(palabra1 + palabra2)
        elif num % 3 == 0:
            print(palabra1)
        elif num % 5 == 0:
            print(palabra2)
        else:
            print(num)
            contador_numeros += 1  # Sumar cuando se imprime un número
    
    return contador_numeros

# Llamada a la función con dos palabras personalizadas
conteo = fizzbuzz_custom("Fizz", "Buzz")
print("Números impresos en lugar de palabras:", conteo)

```
#### Tienes toda la información extendida sobre el roadmap de retos de programación en **[retosdeprogramacion.com/roadmap](https://retosdeprogramacion.com/roadmap)**.

Sigue las **[instrucciones](../../README.md)**, consulta las correcciones y aporta la tuya propia utilizando el lenguaje de programación que quieras.

> Recuerda que cada semana se publica un nuevo ejercicio y se corrige el de la semana anterior en directo desde **[Twitch](https://twitch.tv/mouredev)**. Tienes el horario en la sección "eventos" del servidor de **[Discord](https://discord.gg/mouredev)**.
