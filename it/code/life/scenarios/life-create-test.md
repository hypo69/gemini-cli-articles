Nella directory `game`, crea il file test_life.py, utilizzando il contesto del file @life.py. Utilizza il framework pytest.

Il test dovrebbe verificare l'evoluzione di un semplice oscillatore "Blinker":

1. Importa la classe `Game` da `life`.
2. Crea una funzione di test, ad esempio `test_blinker_oscillation`.
3. Crea un'istanza di `Game` con una dimensione fissa (ad esempio, 5x5).
4. Imposta manualmente lo stato iniziale del campo: una linea orizzontale di tre cellule vive al centro.
5. Chiama `game.step()`.
6. Usando `assert` e `numpy.array_equal`, verifica che il campo sia cambiato in una linea verticale di tre cellule.
7. Chiama `game.step()` di nuovo.
8. Verifica che il campo sia tornato al suo stato orizzontale originale.
