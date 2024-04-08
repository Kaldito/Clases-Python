# BMI CALCULATOR
Crear una calculadora BMI que se basa en dividir tu peso entre tu altura al cuadrado.

**Formula:** 
![[bmi-calculator-en-scaled.jpg]]

## Código Inicial
```
# --- No cambiar el codigo de abajo --- #
altura = input("ingresa tu altura en metros m: ")
peso = input("ingresa tu peso en kg: ")
# --- No cambiar el codigo de arriba --- #

# --- Escribe tu codigo debajo --- #

```

## Solución
```
# --- No cambiar el codigo de abajo --- #
altura = input("ingresa tu altura en metros m: ")
peso = input("ingresa tu peso en kg: ")
# --- No cambiar el codigo de arriba --- #

# --- Escribe tu codigo debajo --- #
bmi = float(peso) / (float(altura)**2)
print(f"Tu BMI es de: {bmi}")
```