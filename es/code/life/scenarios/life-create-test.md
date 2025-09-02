Dentro del directorio `game`, utilizando el contexto del archivo @life.py, crea un archivo de prueba test_life.py. Usa el framework pytest.

La prueba debe verificar la corrección de la evolución de un oscilador "Blinker" simple (tres celdas en fila).

Escenario de prueba:
1.  Importa la clase `Game` de `life`.
2.  Crea una función de prueba, por ejemplo `test_blinker_oscillation`.
3.  Dentro de la prueba, crea una instancia de `Game` con un tamaño fijo (por ejemplo, 5x5).
4.  Establece manualmente el estado inicial del campo para que haya una línea horizontal de tres celdas vivas (Blinker) en el centro.
5.  Llama al método `game.step()`.
6.  Usando `assert` y `numpy.array_equal`, verifica que el campo haya cambiado a una línea vertical de tres celdas.
7.  Llama al método `game.step()` de nuevo.
8.  Verifica que el campo haya vuelto a su estado horizontal original.