Im Verzeichnis `game` erstellen Sie die Datei test_life.py, unter Verwendung des Kontexts aus der Datei @life.py. Verwenden Sie das pytest-Framework.

Der Test sollte die Evolution eines einfachen "Blinker"-Oszillators überprüfen:

1. Importieren Sie die `Game`-Klasse aus `life`.
2. Erstellen Sie eine Testfunktion, zum Beispiel `test_blinker_oscillation`.
3. Erstellen Sie eine `Game`-Instanz mit einer festen Größe (z. B. 5x5).
4. Legen Sie den Anfangszustand des Feldes manuell fest: eine horizontale Linie aus drei lebenden Zellen in der Mitte.
5. Rufen Sie `game.step()` auf.
6. Überprüfen Sie mit `assert` und `numpy.array_equal`, ob sich das Feld in eine vertikale Linie aus drei Zellen geändert hat.
7. Rufen Sie `game.step()` erneut auf.
8. Überprüfen Sie, ob das Feld in seinen ursprünglichen horizontalen Zustand zurückgekehrt ist.
