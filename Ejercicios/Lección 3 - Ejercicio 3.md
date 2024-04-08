# Año Bisiesto (ESTA CABRON)
Escribe un programa que averigüe si un año determinado es bisiesto. Un año normal tiene 365 días, los años bisiestos tienen 366, con un día extra en febrero.

Así es como se determina si un año en particular es bisiesto.
- Cada año que es divisible por 4
- **Excepto** cada año que es divisible por 100
- **A menos que** el año también sea divisible por 400.
## Por ejemplo, el año 2000:
- 2000 ÷ 4 = 500 (Bisiesto)
- 2000 ÷ 100 = 20 (No bisiesto)
- 2000 ÷ 400 = 5 (Bisiesto)

Así pues, el año 2000 es bisiesto.
## Pero el año 2100 no es bisiesto porque:
- 2100 ÷ 4 = 525 (Bisiesto)
- 2100 ÷ 100 = 21 (No bisiesto)
- 2100 ÷ 400 = 5,25 (No bisiesto)
## Código Inicial
```
# --- No cambiar el codigo de abajo --- #
year = int(input("Que año quieres checar? "))
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #

```
## Solución
```
# --- No cambiar el codigo de abajo --- #
year = int(input("Que año quieres checar? "))
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print("Es un año bisiesto.")
        else:
            print("No es un año bisiesto.")	
    else:
        print("Es un año bisiesto.")
else:
    print("No es un año bisiesto.")
```