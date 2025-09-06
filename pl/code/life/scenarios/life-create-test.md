Wewnątrz katalogu `game`, używając kontekstu z pliku @life.py, utwórz plik z testami test_life.py. Użyj frameworka pytest.

Test powinien sprawdzać poprawność ewolucji prostego oscylatora "Blinker" (trzy komórki w rzędzie).

Scenariusz testu:
1.  Zaimportuj klasę `Game` z `life`.
2.  Utwórz funkcję testową, na przykład `test_blinker_oscillation`.
3.  Wewnątrz testu utwórz instancję `Game` o stałym rozmiarze (na przykład 5x5).
4.  Ręcznie ustaw początkowy stan pola tak, aby w centrum znajdowała się pozioma linia trzech żywych komórek (Blinker).
5.  Wywołaj metodę `game.step()`.
6.  Za pomocą `assert` i `numpy.array_equal`, sprawdź, czy pole zmieniło się na pionową linię trzech komórek.
7.  Wywołaj metodę `game.step()` ponownie.
8.  Sprawdź, czy pole wróciło do pierwotnego stanu poziomego.