# Cara o Cruz
Vas a escribir un programa virtual para lanzar una moneda. Le dirá aleatoriamente al usuario "Cara" o "Cruz".

Debes generar un número aleatorio, ya sea 0 ó 1. A continuación, utiliza ese número para imprimir "Cara" o "Cruz". Luego usa ese número para imprimir Cara o Cruz.

**Ejemplo:** 1 significa Cara 0 significa Cruz

## Solución
```
import random

random_number = random.randint(0, 1)

if random_number == 0:
    print("Cara")
else:
    print("Cruz")
```
