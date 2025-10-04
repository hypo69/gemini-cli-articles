Erstellen Sie im Verzeichnis `game` die Datei life.py.
Schreiben Sie darin eine Implementierung von Conways Spiel des Lebens in Python, unter Verwendung eines objektorientierten Ansatzes.
Verwenden Sie die Bibliotheken: `numpy`, `pygame` (für Grafiken).

Anforderungen:
1.  Erstellen Sie eine Klasse `Game`.
2.  In `__init__` sollte die Klasse Gitterabmessungen (Breite, Höhe) akzeptieren und ein zufälliges Anfangsfeld erstellen.
3.  Erstellen Sie eine Methode `step()`, die den Spielzustand um einen Schritt gemäß den Regeln aktualisiert:
    - Eine lebende Zelle mit < 2 lebenden Nachbarn stirbt (Einsamkeit).
    - Eine lebende Zelle mit 2 oder 3 lebenden Nachbarn überlebt.
    - Eine lebende Zelle mit > 3 lebenden Nachbarn stirbt (Überbevölkerung).
    - Eine tote Zelle mit genau 3 lebenden Nachbarn wird lebendig (Geburt).
4.  Erstellen Sie eine Methode `display()` oder überschreiben Sie `__str__`, um das Feld in der Konsole auszugeben. Verwenden Sie Symbole, z. B. '■' für eine lebende Zelle und ' ' für eine tote.
5.  Verwenden Sie die `numpy`-Bibliothek für effiziente Gitteroperationen.
6.  Fügen Sie im Block `if __name__ == '__main__':` ein Beispiel hinzu, das ein Spiel erstellt und die Simulation in einer Schleife mit einer kleinen Verzögerung zwischen den Schritten ausführt.
7.  Verwenden Sie für die Spielvisualisierung pygame oder eine andere Grafikbibliothek, falls möglich.