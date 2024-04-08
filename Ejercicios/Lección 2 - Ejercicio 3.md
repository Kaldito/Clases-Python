# Life in Weeks
Suponiendo que vives 90 años calcula cuantas semanas de tu vida te quedan.

Nota: Calcula solo en base a los años, no en base a la fecha actual.

##  Código Inicial
```
# --- No cambiar el codigo de abajo --- #
user_age = input("Cuantos años tienes? ")
# --- No cambiar el codigo de arriba --- #

# --- Escribe tu codigo debajo --- #

```

## Solución
```
# --- No cambiar el codigo de abajo --- #
years = input("Cuantos años tienes? ")
# --- No cambiar el codigo de arriba --- #

# --- Escribe tu codigo debajo --- #
years_left = 90 - int(user_age)
months_left = years_left * 12
weeks_left = months_left * 4
print(f"Te quedan {weeks_left} semanas de vida.")
```