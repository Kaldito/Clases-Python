
# Ruleta de Comida
Vas a escribir un programa que seleccionará un nombre al azar de una lista de nombres. La persona seleccionada tendrá que pagar la cuenta de la comida de todos.

**Importante:** No puedes utilizar la función `choice()`.
## Ejemplo de input
Dante, Christian, Yanira, Diana, Cesar
**Nota:** observa que hay un espacio entre la coma y el siguiente nombre.
## Ejemplo de output
¡Yanira va a comprar la comida hoy!
## Ayudas
- Puede que necesites la ayuda de la función len(). https://stackoverflow.com/questions/1712227/how-do-i-get-the-number-of-elements-in-a-list
- Recuerda que las listas empiezan en el índice 0.

## Código Inicial
```
import random
names = input("Quienes participaran en el juego? ").split(", ")
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
```

## Solución
```
import random
names = input("Quienes participaran en el juego? ").split(", ")
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
numero_random = random.randint(0, len(names) - 1)
print(f"\n¡{names[numero_random]} va a comprar la comida hoy!")
```