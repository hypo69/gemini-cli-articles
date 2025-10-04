# Projekt "Spiel des Lebens"

## Kurzbeschreibung

Dieses Projekt ist eine Implementierung des zellulären Automaten "Spiel des Lebens" von Conway in Python. Das Spiel simuliert die Evolution einer Population von Zellen auf einem zweidimensionalen Gitter, wobei sich der Zustand jeder Zelle (lebendig oder tot) in Abhängigkeit vom Zustand ihrer Nachbarn ändert.

## Dateistruktur

-   `life.py`: Die Hauptdatei, die die Implementierung der Klasse `Game` enthält, welche die Logik der Simulation des "Spiel des Lebens" und deren grafische Visualisierung mithilfe der `pygame`-Bibliothek verwaltet.
-   `test_life.py`: Eine Datei mit Unit-Tests für die Klasse `Game`, die das `pytest`-Framework verwendet. Enthält einen Test zur Überprüfung der Evolution des "Blinker"-Oszillators.

## So starten Sie die Simulation

Um die Simulation des "Spiel des Lebens" auszuführen, stellen Sie sicher, dass Sie die erforderlichen Bibliotheken (`numpy` und `pygame`) installiert haben. Falls nicht, installieren Sie diese:

```bash
pip install numpy pygame
```

Führen Sie dann die Hauptdatei aus:

```bash
python game/life.py
```

## So führen Sie die Tests aus

Um die Tests auszuführen, müssen Sie `pytest` und `numpy` installieren:

```bash
pip install pytest numpy
```

Führen Sie dann die Tests aus, indem Sie den Pfad zur Testdatei angeben:

```bash
pytest game/test_life.py
```