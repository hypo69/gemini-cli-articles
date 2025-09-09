Nella directory `game`, crea il file life.py.
Implementa il "Gioco della Vita" di Conway in Python, utilizzando un approccio orientato agli oggetti.
Utilizza le librerie: `numpy`, `pygame` (per la grafica).


Requisiti:
1.  Crea la classe `Game`.
2.  In `__init__`, la classe dovrebbe accettare le dimensioni della griglia (larghezza, altezza) e creare un campo iniziale casuale.
3.  Crea il metodo `step()`, che aggiorna lo stato del gioco di un passo:
    - Una cellula vivente con < 2 vicini vivi muore (solitudine).
    - Una cellula vivente con 2 o 3 vicini vivi sopravvive.
    - Una cellula vivente con > 3 vicini vivi muore (sovrappopolazione).
    - Una cellula morta con esattamente 3 vicini vivi diventa viva (riproduzione).
4.  Crea il metodo `display()` o sovrascrivi `__str__`, per visualizzare il campo nella console ('■' per una cellula viva, ' ' per una cellula morta).
5.  Utilizza `numpy` per operazioni efficienti sulla griglia.
6.  Nel blocco `if __name__ == '__main__':` aggiungi un esempio che crea un gioco e avvia la simulazione con un piccolo ritardo tra i passaggi.
7. Per la visualizzazione del gioco, utilizza `pygame` o un'altra libreria grafica.
