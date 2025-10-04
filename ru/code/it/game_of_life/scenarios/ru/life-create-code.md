Nella directory `game`, crea il file life.py.
All'interno, scrivi un'implementazione del Gioco della Vita di Conway in Python, utilizzando un approccio orientato agli oggetti.
Usa le librerie: `numpy`, `pygame` (per la grafica).

Requisiti:
1.  Crea una classe `Game`.
2.  In `__init__`, la classe dovrebbe accettare le dimensioni della griglia (larghezza, altezza) e creare un campo iniziale casuale.
3.  Crea un metodo `step()` che aggiorna lo stato del gioco di un passo secondo le regole:
    - Una cellula viva con < 2 vicini vivi muore (solitudine).
    - Una cellula viva con 2 o 3 vicini vivi sopravvive.
    - Una cellula viva con > 3 vicini vivi muore (sovrappopolazione).
    - Una cellula morta con esattamente 3 vicini vivi diventa viva (nascita).
4.  Crea un metodo `display()` o sovrascrivi `__str__` per visualizzare il campo nella console. Usa simboli, ad esempio '■' per una cellula viva e ' ' per una morta.
5.  Usa la libreria `numpy` per operazioni efficienti sulla griglia.
6.  Nel blocco `if __name__ == '__main__':`, aggiungi un esempio che crea un gioco ed esegue la simulazione in un ciclo con un piccolo ritardo tra i passi.
7.  Per la visualizzazione del gioco, usa pygame o un'altra libreria grafica, se possibile.