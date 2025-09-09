Im Verzeichnis `game` erstellen Sie die Datei life.py.
Implementieren Sie Conways "Spiel des Lebens" in Python, unter Verwendung eines objektorientierten Ansatzes.
Verwenden Sie Bibliotheken: `numpy`, `pygame` (für Grafiken).


Anforderungen:
1.  Erstellen Sie eine `Game`-Klasse.
2.  In `__init__` sollte die Klasse Gitterdimensionen (Breite, Höhe) annehmen und ein zufälliges Anfangsfeld erstellen.
3.  Erstellen Sie eine `step()`-Methode, die den Spielzustand um einen Schritt aktualisiert:
    - Eine lebende Zelle mit < 2 lebenden Nachbarn stirbt (Unterbevölkerung).
    - Eine lebende Zelle mit 2 oder 3 lebenden Nachbarn überlebt.
    - Eine lebende Zelle mit > 3 lebenden Nachbarn stirbt (Überbevölkerung).
    - Eine tote Zelle mit genau 3 lebenden Nachbarn wird lebendig (Reproduktion).
4.  Erstellen Sie eine `display()`-Methode oder überschreiben Sie `__str__`, um das Feld in der Konsole auszugeben ('■' für eine lebende Zelle, ' ' für eine tote).
5.  Verwenden Sie `numpy` für effiziente Gitteroperationen.
6.  Fügen Sie im `if __name__ == '__main__':`-Block ein Beispiel hinzu, das ein Spiel erstellt und die Simulation mit einer kleinen Verzögerung zwischen Schritten ausführt.
7. Verwenden Sie pygame oder eine andere Grafikbibliothek zur Spielvisualisierung.
