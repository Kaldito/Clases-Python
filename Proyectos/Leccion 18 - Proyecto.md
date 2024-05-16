# Introducción
En este proyecto haremos que nuestra tortuga pinte un cuadro como el siguiente: [Damien Hirst, Flumequine, 2007, Etching](https://www.masterworksfineart.com/artists/damien-hirst/etching/flumenquine-2007/id/W-7567)

Para lograrlo utilizaremos la libreria:
- [colorgram.py · PyPI](https://pypi.org/project/colorgram.py/)

# Primer paso
Sacar los colores como un tuple rgb de la imagen de **Hirst** para usar en el proyecto usando la librería de **colorgram**.

Al final tenemos que tener una lista compuesta de tuples con los valores rgb como el siguiente: **(249, 104, 76)**.

### SOLUCION
```
import colorgram  
  
rgb_colors = []  
colors = colorgram.extract("./hirst.jpg", 30)  
  
for color in colors:  
    c = color.rgb  
    rgb_colors.append((c.r, c.g, c.b))
```

# Segundo paso
Quitar de la lista los colores que estén demasiado cerca del blanco. Para saber si un color esta demasiado cerca del blanco tendremos que validar que los 3 parámetros de RGB no sean mayores a 240.

## SOLUCION
```
import colorgram  
  
rgb_colors = []  
colors = colorgram.extract("./hirst.jpg", 30)  
  
for color in colors:  
    c = color.rgb  
  
    if c.r < 240 or c.g < 240 or c.r < 240:  
        rgb_colors.append((c.r, c.g, c.b))
```


# PROYECTO
Hacer que el programa haga una pintura similar con una cuadricula de **puntos** de 10x10.
Cada punto tiene que tener una medida de ***20*** y estar separado por ***50***.

### SOLUCION
```
import colorgram  
import turtle as t  
import random  
  
  
# - INICIALIZACION DE LA TORTUGA - #  
def startup():  
    turtle.speed("fastest")  
    turtle.penup()  
  
    turtle.setheading(225)  
    turtle.fd(300)  
    turtle.setheading(0)  
  
  
# - Dibujar una linea de puntos - #  
def draw_row():  
    for n in range(10):  
        turtle.dot(20, random.choice(rgb_colors))  
        turtle.fd(50)  
  
    turtle.setheading(90)  
    turtle.fd(50)  
    turtle.setheading(180)  
    turtle.fd(500)  
    turtle.setheading(0)  
  
  
# ---- EXTRAER COLORES DE LA IMAGEN ---- #  
rgb_colors = []  
colors = colorgram.extract("./hirst.jpg", 30)  
  
for color in colors:  
    c = color.rgb  
  
    # - Quitar los colores cercanos al blanco - #  
    if c.r < 240 or c.g < 240 or c.r < 240:  
        rgb_colors.append((c.r, c.g, c.b))  
  
# ---- PROGRAMA ---- #  
t.colormode(255)  
turtle = t.Turtle()  
  
startup()  
   
for n in range(10):  
    draw_row()  

  
screen = t.Screen()  
screen.exitonclick()
```