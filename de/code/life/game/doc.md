# Projekt "Spiel des Lebens"

## Kurzbeschreibung

Dieses Projekt ist eine Implementierung von Conways zellulärem Automaten "Spiel des Lebens" in Python. Das Spiel simuliert die Evolution einer Population von Zellen auf einem zweidimensionalen Gitter, wobei der Zustand jeder Zelle (lebend oder tot) in Abhängigkeit von den Zuständen ihrer Nachbarn wechselt.

## Dateistruktur

-   `life.py`: Die Hauptdatei, die die Implementierung der `Game`-Klasse enthält, welche die Simulationslogik des "Spiel des Lebens" und dessen grafische Visualisierung mit der `pygame`-Bibliothek verwaltet.
-   `test_life.py`: Eine Datei mit Unit-Tests für die `Game`-Klasse, die das `pytest`-Framework verwendet. Enthält einen Test zur Überprüfung der Evolution des "Blinker"-Oszillators.

## So starten Sie die Simulation

Um die Simulation des "Spiel des Lebens" zu starten, stellen Sie sicher, dass Sie die erforderlichen Bibliotheken (`numpy` und `pygame`) installiert haben. Falls nicht, installieren Sie diese:

```bash
pip install numpy pygame
```

Führen Sie dann die Hauptdatei aus:

```bash
python game/life.py
```

## So führen Sie Tests aus

Um Tests auszuführen, müssen Sie `pytest` und `numpy` installieren:

```bash
pip install pytest numpy
```

Führen Sie dann die Tests aus, indem Sie den Pfad zur Testdatei angeben:

```bash
pytest game/test_life.py
```
