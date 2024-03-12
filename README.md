# Estruc-Pilas
class Pila:
    def __init__(self, capacidad_maxima):
        self.capacidad_maxima = capacidad_maxima
        self.pila = []
        self.tope = 0

    def insertar(self, elemento):
        if self.tope < self.capacidad_maxima:
            self.pila.append(elemento)
            self.tope += 1
            self.mostrar_estado()
        else:
            print("Error: Desbordamiento. La pila está llena.")

    def eliminar(self):
        if self.tope > 0:
            elemento_eliminado = self.pila.pop()
            self.tope -= 1
            self.mostrar_estado()
            return elemento_eliminado
        else:
            print("Error: Subdesbordamiento. La pila está vacía.")
            return None

    def mostrar_estado(self):
        print(f"TOPE = {self.tope}, PILA = {self.pila}")

# Crear la pila con capacidad máxima de 8 elementos
pila = Pila(8)

# a. Insertar (PILA, X)
pila.insertar("X")

# b. Insertar (PILA, Y)
pila.insertar("Y")

# c. Eliminar (PILA, Z)
pila.eliminar()

# d. Eliminar (PILA, T)
pila.eliminar()

# e. Eliminar (PILA, U)
pila.eliminar()

# f. Insertar (PILA, V)
pila.insertar("V")

# g. Insertar (PILA, W)
pila.insertar("W")

# h. Eliminar (PILA, p)
pila.eliminar()

# i. Insertar (PILA, R)
pila.insertar("R")
print(f"La pila tiene {pila.tope} elementos.")
