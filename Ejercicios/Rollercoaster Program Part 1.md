Hacer un programa que simule la entrada de una montaña rusa, en este programa se preguntara si quiere o no quiere entrar a la montaña rusa, y solo podrán entrar personas con una altura mayor a 1.20m.
# Código
```
print("Bienvenido a la montaña rusa!")

entrar = input("Te gustaria entrar? s/n ")

if entrar == "s":
    altura = float(input("Antes de entrar tenemos que verificar tu altura(m): "))

    if altura > 1.20:
        print("Si puedes pasar. ¡Disfruta tu estancia!")
    else:
        print("No tienes la altura minima para poder pasar.")

print("\nGracias por su vista!")
```