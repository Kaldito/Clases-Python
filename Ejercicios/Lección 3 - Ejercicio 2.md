# BMI CALCULATOR PLUS

Escribe un programa que interprete el Índice de Masa Corporal (IMC) basándose en el peso y la altura de un usuario.

Debe indicarles la interpretación de su IMC basándose en el valor del IMC.
- Por debajo de 18,5 tienen **bajo peso**.
- Por encima de 18,5 pero por debajo de 25 tienen un **peso normal**.
- Por encima de 25 pero por debajo de 30 tienen un **ligero sobrepeso**.
- Por encima de 30 pero por debajo de 35 son **obesos**.
- Por encima de 35 son **clínicamente obesos**.
## NOTAS
- Redondea el resultado al número entero más próximo. 
- El mensaje de interpretación debe incluir las palabras en negrita de las interpretaciones anteriores, por ejemplo: **bajo peso, peso normal, sobrepeso, obesidad, obesidad clínica**.
## Código inicial
```
# --- No cambiar el codigo de abajo --- #
altura = float(input("Escribe tu altura en metros: "))
peso = float(input("Escribe tu peso en kg: "))
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
```
## Solución
```
# --- No cambiar el codigo de abajo --- #
altura = float(input("Escribe tu altura en metros: "))
peso = float(input("Escribe tu peso en kg: "))
# --- No cambiar el codigo de arriba --- #

####################################
# --- Escribe tu codigo abajo --- #
BMI = altura / (peso ** 2)

if BMI < 18.5:
    print(f"Tu BMI es de {round(BMI)}, tienes bajo peso.")
elif BMI < 25:
    print(f"Tu BMI es de {round(BMI)}, tienes un peso normal.")
elif BMI < 30:
    print(f"Tu BMI es de {round(BMI)}, estas un poco arriba de tu peso ideal.")
elif BMI < 35:
    print(f"Tu BMI es de {round(BMI)}, tienes obesidad.")
else:
    print(f"Tu BMI es de {round(BMI)}, tienes obesidad clinica.")
```