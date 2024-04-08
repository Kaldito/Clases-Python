# Mapa del Tesoro (CABRON)
Vas a escribir un programa que marque con una X un punto en un mapa.

En el código inicial, encontrarás una variable llamada `map`.

Este mapa contiene una lista anidada. Cuando se imprime `map` esto es lo que parece, observa el anidamiento:

`[['⬜️', '⬜️', '⬜️'],['⬜️', '⬜️', '⬜️'],['⬜️', '⬜️', '⬜️']]`

Tu trabajo consiste en escribir un programa que te permita marcar un cuadrado en el mapa utilizando un sistema de letras y números.

![[Pasted image 20240330193154.png]]

Así que un input de A3 debe colocar una X en la posición que se muestra a continuación:

![[Pasted image 20240330193219.png]]

En primer lugar, tu programa debe tomar el input del usuario y convertirla a un formato utilizable.

A continuación, debes utilizar ese input para actualizar tu lista anidada con una "X".

## Código Inicial
```
line1 = ["⬜️","️⬜️","️⬜️"]
line2 = ["⬜️","⬜️","️⬜️"]
line3 = ["⬜️️","⬜️️","⬜️️"]
map = [line1, line2, line3]
position = input("Donde quieres esconder tu tesoro? ")
# --- No cambiar el codigo de arriba --- #


# --- No cambiar el codigo de abajo --- #
print(f"{line1}\n{line2}\n{line3}")
```
## Solución
```
line1 = ["⬜️","️⬜️","️⬜️"]
line2 = ["⬜️","⬜️","️⬜️"]
line3 = ["⬜️️","⬜️️","⬜️️"]
map = [line1, line2, line3]
position = input("Donde quieres esconder tu tesoro? ")
# --- No cambiar el codigo de arriba --- #
letter = position[0].lower()
number = int(position[1]) - 1
letter_number = 0

if letter == "b":
	letter_number = 1
elif letter == "c":
	letter_number = 2

map[number][letter_number] = "X"
# --- No cambiar el codigo de abajo --- #
print(f"{line1}\n{line2}\n{line3}")
```
