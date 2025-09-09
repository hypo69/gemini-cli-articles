# Progetto "Gioco della Vita"

## Breve descrizione

Questo progetto è un'implementazione dell'automa cellulare "Gioco della Vita" di Conway in Python. Il gioco simula l'evoluzione di una popolazione di cellule su una griglia bidimensionale, dove lo stato di ogni cellula (viva o morta) cambia a seconda dello stato dei suoi vicini.

## Struttura dei file

-   `life.py`: Il file principale che contiene l'implementazione della classe `Game`, che gestisce la logica di simulazione del "Gioco della Vita" e la sua visualizzazione grafica utilizzando la libreria `pygame`.
-   `test_life.py`: Un file con test unitari per la classe `Game`, che utilizza il framework `pytest`. Include un test per verificare l'evoluzione dell'oscillatore "Blinker".

## Come avviare la simulazione

Per avviare la simulazione del "Gioco della Vita", assicurati di avere installato le librerie necessarie (`numpy` e `pygame`). In caso contrario, installale:

```bash
pip install numpy pygame
```

Quindi esegui il file principale:

```bash
python game/life.py
```

## Come eseguire i test

Per eseguire i test, devi installare `pytest` e `numpy`:

```bash
pip install pytest numpy
```

Quindi esegui i test, specificando il percorso del file di test:

```bash
pytest game/test_life.py
```
