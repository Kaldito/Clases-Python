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
# Ejercicio 4 - Generar un camino aleatorio

Hacer que nuestra tortuga genere un camino aleatorio al pudiendo elegir entre moverse hacia arriba, abajo, derecha e izquierda. Cada que elija un camino, el color con el que pinte también cambiara.

**EXTRA:** Investigar y aplicar como cambiar el grosor de la linea que traza la tortuga.
**EXTRA:** Investigar y aplicar como acelerar el movimiento de la tortuga.

**DOCUMENTACION:** [Camino aleatorio - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Camino_aleatorio)

![[Pasted image 20240510112042.png]]

### AYUDA: Métodos utilizados
- `.setheading()`
- `.pensize()`
- `.speed()`
- `.choice()` del modulo random.
### SOLUCION
```
from turtle import Turtle, Screen  
import random  
  
# Creamos nuestro objeto de la clase tortuga  
cesar = Turtle()  
cesar.shape("turtle")  
cesar.color("red")  
  
# --------- CAMINO ALEATORIO --------- #  
colors = ["red", "green", "blue", "yellow", "purple", "orange"]  
directions = [0, 90, 180, 270]  
cesar.pensize(10) # Grosor de la línea  
cesar.speed("fastest") # Velocidad de la tortuga  
  
for _ in range(100):  
    cesar.color(random.choice(colors))  
    cesar.forward(30)  
    cesar.setheading(random.choice(directions))  
    # setheading() es un método que nos permite cambiar la dirección de la    tortuga  
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = Screen()  
screen.exitonclick()
```
# Tuples
Un tuple se escribe de la siguiente manera: 
```
tuple = (1, 2, 3)
```

Y para acceder a cualquier item de nuestro tuple se hace igual que si quisieramos acceder al item de una lista:

```
print(tuple[0]) # Imprime: 1
```

## Diferencia entre tuple y list:
- A los tuple no se les pueden cambiar sus items.

# RETO - Pintar con un color aleatorio usando .colormode()
Hacer que la tortuga pinte con un color aleatorio en lugar de uno seleccionado de una lista predefinida, para esto es necesario investigar la función `.colormode()` y cambiar los colores de la tortuga asignándole un color **RGB** mediante un tuple.

### SOLUCION
```
import turtle as t  
import random  
  
  
# --------- FUNCION PARA GENERAR UN COLOR RGB --------- #  
def random_color():  
    r = random.randint(0, 255)  
    g = random.randint(0, 255)  
    b = random.randint(0, 255)  
  
    rgb_tuple = (r, g, b)  
  
    return rgb_tuple  
  
  
# Creamos nuestro objeto de la clase tortuga  
cesar = t.Turtle()  
t.colormode(255) # Modo de color RGB  
cesar.shape("turtle")  
  
# --------- CAMINO ALEATORIO --------- #  
directions = [0, 90, 180, 270]  
cesar.pensize(10) # Grosor de la línea  
cesar.speed("fastest") # Velocidad de la tortuga  
  
for _ in range(100):  
    cesar.color(random_color())  
    cesar.forward(30)  
    cesar.setheading(random.choice(directions))  
    # setheading() es un método que nos permite cambiar la dirección de la tortuga  
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = t.Screen()  
screen.exitonclick()
```

# Ejercicio 5 - Dibujar un espirógrafo
Hacer que la tortuga simule el comportamiento de un espirografo creando patrones como el siguiente:
![[Pasted image 20240510114511.png]]
### AYUDA
- `.circle()`
- `.heading()`

### SOLUCION
```
import turtle as t  
import random  
  
  
# --------- FUNCION PARA GENERAR UN COLOR RGB --------- #  
def random_color():  
    r = random.randint(0, 255)  
    g = random.randint(0, 255)  
    b = random.randint(0, 255)  
  
    rgb_tuple = (r, g, b)  
  
    return rgb_tuple  
  
  
def draw_spirograph(circle_size, size_of_gap):  
    for _ in range(int(round(360 / size_of_gap))):  
        cesar.color(random_color()) # Color aleatorio  
        cesar.circle(circle_size) # Dibujamos un circulo  
        cesar.setheading(cesar.heading() + size_of_gap) # Cambiamos la dirección de la tortuga  
  
  
# Creamos nuestro objeto de la clase tortuga  
cesar = t.Turtle()  
t.colormode(255) # Modo de color RGB  
cesar.shape("turtle")  
  
# --------- ESPIROGRAFO --------- #  
cesar.speed("fastest") # Velocidad de la tortuga  
  
draw_spirograph(100, 10)  
draw_spirograph(150, 5)  
  
  
# --------- SCREEN SETUP --------- #  
# Los ajustes de la pantalla deben estar hasta abajo para que funcione  
screen = t.Screen()  
screen.exitonclick()
```