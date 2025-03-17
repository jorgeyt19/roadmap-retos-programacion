# #01 OPERADORES Y ESTRUCTURAS DE CONTROL
> #### Dificultad: Fácil | Publicación: 02/01/24 | Corrección: 08/01/24

## Ejercicio

```
/*
 * EJERCICIO:
 * - Crea ejemplos utilizando todos los tipos de operadores de tu lenguaje:
 *   Aritméticos, lógicos, de comparación, asignación, identidad, pertenencia, bits...
 *   (Ten en cuenta que cada lenguaje puede poseer unos diferentes)
 * - Utilizando las operaciones con operadores que tú quieras, crea ejemplos
 *   que representen todos los tipos de estructuras de control que existan
 *   en tu lenguaje:
 *   Condicionales, iterativas, excepciones...
 * - Debes hacer print por consola del resultado de todos los ejemplos.
 *
 * DIFICULTAD EXTRA (opcional):
 * Crea un programa que imprima por consola todos los números comprendidos
 * entre 10 y 55 (incluidos), pares, y que no son ni el 16 ni múltiplos de 3.
 *
 * Seguro que al revisar detenidamente las posibilidades has descubierto algo nuevo.
 */
---------------------------
 Operadores en Python
---------------------------

# Operadores aritméticos
a = 10
b = 3

print("Suma:", a + b)  # 13
print("Resta:", a - b)  # 7
print("Multiplicación:", a * b)  # 30
print("División:", a / b)  # 3.333...
print("División entera:", a // b)  # 3
print("Módulo:", a % b)  # 1
print("Exponente:", a ** b)  # 1000

# Operadores de comparación
print("¿a es mayor que b?", a > b)  # True
print("¿a es igual a b?", a == b)  # False

# Operadores lógicos
x = True
y = False

print("AND lógico:", x and y)  # False
print("OR lógico:", x or y)  # True
print("NOT lógico:", not x)  # False

# Operadores de asignación
c = 5
c += 2  # Equivalente a c = c + 2
print("Operador de asignación (+=):", c)  # 7

# Operadores de identidad
d = [1, 2, 3]
e = [1, 2, 3]
f = d

print("¿d y e son el mismo objeto?", d is e)  # False (listas diferentes)
print("¿d y f son el mismo objeto?", d is f)  # True (referencian lo mismo)

# Operadores de pertenencia
print("¿2 está en d?", 2 in d)  # True
print("¿5 no está en d?", 5 not in d)  # True

# Operadores a nivel de bits
num1 = 5  # 0b101
num2 = 3  # 0b011

print("AND bit a bit:", num1 & num2)  # 1 (0b001)
print("OR bit a bit:", num1 | num2)  # 7 (0b111)
print("XOR bit a bit:", num1 ^ num2)  # 6 (0b110)
print("Desplazamiento a la izquierda:", num1 << 1)  # 10 (0b1010)
print("Desplazamiento a la derecha:", num1 >> 1)  # 2 (0b10)

---------------------------
 Estructuras de control
---------------------------

# Condicionales
edad = 18

if edad >= 18:
    print("Eres mayor de edad")
elif edad > 12:
    print("Eres un adolescente")
else:
    print("Eres un niño")

# Bucle for (iterando sobre una lista)
frutas = ["manzana", "banana", "cereza"]
for fruta in frutas:
    print("Me gusta la", fruta)

# Bucle while
contador = 3
while contador > 0:
    print("Contando:", contador)
    contador -= 1

# Manejo de excepciones
try:
    resultado = 10 / 0  # Esto genera un error
except ZeroDivisionError:
    print("Error: División por cero no permitida")
finally:
    print("Fin del manejo de excepciones")

---------------------------
 DIFICULTAD EXTRA
---------------------------
print("\nNúmeros entre 10 y 55 que cumplen la condición:")

for num in range(10, 56):
    if num % 2 == 0 and num != 16 and num % 3 != 0:
        print(num, end=" ")

```
#### Tienes toda la información extendida sobre el roadmap de retos de programación en **[retosdeprogramacion.com/roadmap](https://retosdeprogramacion.com/roadmap)**.

Sigue las **[instrucciones](../../README.md)**, consulta las correcciones y aporta la tuya propia utilizando el lenguaje de programación que quieras.

> Recuerda que cada semana se publica un nuevo ejercicio y se corrige el de la semana anterior en directo desde **[Twitch](https://twitch.tv/mouredev)**. Tienes el horario en la sección "eventos" del servidor de **[Discord](https://discord.gg/mouredev)**.
