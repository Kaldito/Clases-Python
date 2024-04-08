# Calculadora del amor
Vas a escribir un programa que compruebe la compatibilidad entre dos personas.

Para calcular la puntuación de amor entre dos personas:
1. Toma los nombres de ambas personas y comprueba el número de veces que aparecen las letras de la palabra TRUE.
2. A continuación, comprueba el número de veces que aparecen las letras de la palabra LOVE.
3. Combina estas cifras para obtener un número de 2 dígitos.
## Puntuaciones
- Para puntuaciones de amor inferiores a 10 o superiores a 90, el mensaje debe ser:
	- "Lo siento, no son el uno para el otro."
- Para puntuaciones de amor entre 40 y 50, el mensaje debe ser:
	- "Deberían casarse ya."
- De lo contrario, el mensaje será:
	- "Meh"
## Ejemplo
nombre1 = "Dante Kaled"
nombre2 = "Kaladin"
### Conteo de True
- T ocurre 1 veces
- R aparece 0 vez
- U aparece 0 veces
- E ocurre 2 veces

**Total = 3**
### Conteo de Love
- L ocurre 2 vez
- O ocurre 0 veces
- V ocurre 0 veces
- E ocurre 2 veces

**Total = 4**
### TOTALES
Puntuación de amor = 34
Imprime: "Meh".

## Código Inicial
```
# --- No cambiar el codigo de abajo --- #
print("¡Bienvenido a la Calculadora del Amor!")
name1 = input("¿Cómo te llamas? \n")
name2 = input("¿Cómo se llama tu amor? \n")
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
```
## Solución
```
# --- No cambiar el codigo de abajo --- #
print("¡Bienvenido a la Calculadora del Amor!")
name1 = input("¿Cómo te llamas? \n")
name2 = input("¿Cómo se llama tu amor? \n")
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
name1_lower = name1.lower()
name2_lower = name2.lower()

T = name1_lower.count("t") + name2_lower.count("t")
R = name1_lower.count("r") + name2_lower.count("r")
U = name1_lower.count("u") + name2_lower.count("u")
E = name1_lower.count("e") + name2_lower.count("e")

L = name1_lower.count("l") + name2_lower.count("l")
O = name1_lower.count("o") + name2_lower.count("o")
V = name1_lower.count("v") + name2_lower.count("v")

true_count = str(T + R + U + E)
love_count = str(L + O + V + E)

percentage_string = true_count + love_count
percentage_int = int(percentage_string)

if percentage_int < 10 or percentage_int > 90:
	print("Lo siento, no son el uno para el otro.")
elif percentage_int > 40 and percentage_int < 50:
	print("Deberían casarse ya.")
else:
	print("Meh.")
```