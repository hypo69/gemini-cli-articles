Dentro del directorio `game`, crea el archivo life.py. 
Dentro, escribe la implementación del "Juego de la Vida" de Conway en Python, utilizando un enfoque orientado a objetos.
Utiliza las bibliotecas: `numpy`, `pygame` (para gráficos).


Requisitos:
1.  Crea la clase `Game`.
2.  En `__init__`, la clase debe aceptar las dimensiones de la cuadrícula (ancho, alto) y crear un campo inicial aleatorio.
3.  Crea el método `step()`, que actualiza el estado del juego en un paso de acuerdo con las reglas:
    - Una célula viva con < 2 vecinos vivos muere (soledad).
    - Una célula viva con 2 o 3 vecinos vivos sobrevive.
    - Una célula viva con > 3 vecinos vivos muere (superpoblación).
    - Una célula muerta con exactamente 3 vecinos vivos se vuelve viva (nacimiento).
4.  Crea el método `display()` o anula `__str__` para mostrar el campo en la consola. Utiliza símbolos, por ejemplo '■' para una célula viva y ' ' para una muerta.
5.  Utiliza la biblioteca `numpy` para operaciones eficientes con la cuadrícula.
6.  En el bloque `if __name__ == '__main__':` agrega un ejemplo que cree el juego y ejecute la simulación con un pequeño retraso entre pasos.
7. Para la visualización del juego, utiliza pygame o otra biblioteca gráfica, si es posible.
