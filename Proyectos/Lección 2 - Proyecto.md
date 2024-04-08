# Single Total Calculator
Hacer un programa que calcule el total que debe pagar cada persona en una cuenta de una comida. 

Si la cuenta fue de $150 pesos, y la queremos dividir entre 5 personas, con 12% de propina

Cada persona debería pagar *(150.00 / 5) * 1.12 = 33.6*
Redondear el numero a dos decimales = *33.60*
## Solución
```
total_cuenta = int(input("Cual fue el total de la cuenta? "))
personas = int(input("Cuantas personas van a pagar? "))
porcentaje_propina = int(input("Que porcentaje de propina desea agregar? "))

total_individual = (total_cuenta / personas) * (1 + (porcentaje_propina / 100))

print(f"El total a pagar para cada persona es de ${total_individual:.2f}".format())
```