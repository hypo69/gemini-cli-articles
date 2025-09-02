Dentro del directorio `game`, crea el archivo life.py.
Dentro, escribe la implementación del "Juego de la Vida" de Conway en Python, utilizando un enfoque orientado a objetos.
Usa las bibliotecas: `numpy`, `pygame` (para gráficos).


Requisitos:
1.  Crea una clase `Game`.
2.  En `__init__`, la clase debe tomar las dimensiones de la cuadrícula (ancho, alto) y crear un campo inicial aleatorio.
3.  Crea un método `step()` que actualice el estado del juego un paso de acuerdo con las reglas:
    - Una célula viva con < 2 vecinos vivos muere (subpoblación).
    - Una célula viva con 2 o 3 vecinos vivos sobrevive.
    - Una célula viva con > 3 vecinos vivos muere (superpoblación).
    - Una célula muerta con exactamente 3 vecinos vivos cobra vida (reproducción).
4.  Crea un método `display()` o anula `__str__` para mostrar el campo en la consola. Usa símbolos, por ejemplo '■' para una célula viva y ' ' para una muerta.
5.  Usa la biblioteca `numpy` para operaciones eficientes de la cuadrícula.
6.  En el bloque `if __name__ == '__main__':`, agrega un ejemplo que cree un juego y ejecute la simulación en un bucle con un pequeño retraso entre pasos.
7. Usa pygame o otra biblioteca de gráficos para la visualización del juego, si es posible.