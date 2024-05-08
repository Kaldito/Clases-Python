Documentación del modulo: [turtle — Turtle graphics — Python 3.12.3 documentation](https://docs.python.org/3/library/turtle.html)

# Inicialización del Proyecto
Primero hay que importar las clases Turtle y Screen para asi poder crear nuestros objetos de dichas clases y poder empezar a trabajar.

```
from turtle import Turtle, Screen  
  
# Creamos nuestro objeto de la clase tortuga  
cesar_the_turtle = Turtle()  
  
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = Screen()  
screen.exitonclick()
```

# Reto
Investigar sobre el parámetro shape en la documentación del modulo, y cambiar la forma de nuestro objeto `cesar_the_turtle`.
### Solucion
```
cesar_the_turtle = Turtle()
cesar_the_turtle.shape("turtle")
```

# Reto
Investigar como cambiar el color de la tortuga.
### Solucion
```
cesar_the_turtle = Turtle()  
cesar_the_turtle.shape("turtle")  
cesar_the_turtle.color("red")
```





# Mover a la tortuga
En la seccion de *Turtle Motion* podemos encontrar la mayoria de comandos para realizar la traccion de la tortuga.

![[Pasted image 20240508135053.png]]

# Primer Ejercicio - Dibujar un cuadrado
Hacer un programa que mueva a nuestro objeto de la clase tortuga para que dibuje un cuadrado.

### Solucion
```
from turtle import Turtle, Screen  
  
# Creamos nuestro objeto de la clase tortuga  
cesar_the_turtle = Turtle()  
cesar_the_turtle.shape("turtle")  
cesar_the_turtle.color("red")  
  
# --- HACER UN CUADRADO --- #  
for n in range(4):  
    cesar_the_turtle.forward(100)  
    cesar_the_turtle.left(90)  
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = Screen()  
screen.exitonclick()
```

# Refactor Pycharm
Se puede usar la funcion de Refactor que viene incluida por defecto en Pycharm para cambiar el nombre de variables. Usar la funcion de Refactor para cambiar el nombre de nuestro objeto tortuga.

# Formas de importar
- `import turtle`
- `from turtle import Turtle`
- `from turtle import *`
- `import turtle as t`
# Segundo Ejercicio - Dibujar una linea de puntos
Hacer que nuestra tortuga dibuje una linea de puntos como la siguiente:
![[Pasted image 20240508140253.png]]
### Solucion
```
from turtle import Turtle, Screen  
  
# Creamos nuestro objeto de la clase tortuga  
cesar_the_turtle = Turtle()  
cesar_the_turtle.shape("turtle")  
cesar_the_turtle.color("red")  

# --- HACER UNA LINEA DE PUNTOS --- #
for n in range(10):  
    cesar.forward(10)  
    cesar.penup()  
    cesar.forward(10)  
    cesar.pendown()
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = Screen()  
screen.exitonclick()
```

# Tercer Ejercicio - Dibujar diferentes figuras
Hacer que nuestra tortuga dibuje un patrón como el siguiente:
![[Pasted image 20240508141356.png]]

Si se quieren usar varios colores para cada figura diferente usar la siguiente pagina para sacar los colores: [Colors](https://trinket.io/docs/colors)
### Solucion
```
from turtle import Turtle, Screen  
  
# Creamos nuestro objeto de la clase tortuga  
cesar_the_turtle = Turtle()  
cesar_the_turtle.shape("turtle")  
cesar_the_turtle.color("red")  

# --- VARIAS FIGURAS --- #  
def draw_shape(num_sides):  
    angle = 360 / num_sides  
    for n in range(num_sides):  
        cesar.forward(100)  
        cesar.right(angle)  
  
  
for shape in range(3, 11):  
    draw_shape(shape)
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = Screen()  
screen.exitonclick()
```
