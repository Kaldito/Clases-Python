# PapasPizzeria
Felicidades, has conseguido un trabajo en PapasPizzeria. Tu primer trabajo es construir un programa automático de pedidos de pizza.

Basándote en el pedido de un usuario, calcula su factura final.
## Tamaños de Pizza:
- Pizza pequeña: $300.
- Pizza mediana: $400.
- Pizza grande: $500.
## Adiciones:
- Pepperoni para **pizza pequeña**: +$40
- Pepperoni para **pizza mediana** o **grande**: +$60.
- Queso extra para **cualquier tamaño** de pizza: + $20.
## Código Inicial
```
# --- No cambiar el codigo de abajo --- #
print("¡Bienvenido a PapasPizzeria!")
size = input("¿Qué tamaño de pizza quieres? P, M o G ")
add_pepperoni = input("¿Quieres pepperoni? S o N ")
extra_cheese = input("¿Quieres extra queso? S o N ")
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
```
## Solución
```
# --- No cambiar el codigo de abajo --- #
print("¡Bienvenido a PapasPizzeria!")
size = input("¿Qué tamaño de pizza quieres? P, M o G ")
add_pepperoni = input("¿Quieres pepperoni? S o N ")
extra_cheese = input("¿Quieres extra queso? S o N ")
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
bill = 0

# Eleccion de tamaño
if size == "P":
    bill += 300
elif size == "M":
    bill += 400
else:
    bill += 500

# peperoni
if add_pepperoni == "S":
	if size == "P":
	    bill += 40
	else:
		bill += 60    
	
# extra queso 
if extra_cheese == "S":
    bill += 20

print(f"Su factura final es: ${bill}")
```