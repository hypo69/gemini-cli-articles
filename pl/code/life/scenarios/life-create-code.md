Wewnątrz katalogu `game` utwórz plik life.py. 
Zaimplementuj "Grę w życie" Conwaya w Pythonie, używając podejścia obiektowego.
Użyj bibliotek: `numpy`, `pygame` (do grafiki).


Wymagania:
1.  Utwórz klasę `Game`.
2.  W `__init__` klasa powinna przyjmować wymiary siatki (szerokość, wysokość) i tworzyć losowe pole początkowe.
3.  Utwórz metodę `step()`, która aktualizuje stan gry o jeden krok:
    - Żywa komórka z < 2 żywymi sąsiadami umiera (samotność).
    - Żywa komórka z 2 lub 3 żywymi sąsiadami przeżywa.
    - Żywa komórka z > 3 żywymi sąsiadami umiera (przeludnienie).
    - Martwa komórka z dokładnie 3 żywymi sąsiadami staje się żywa (narodziny).
4.  Utwórz metodę `display()` lub nadpisz `__str__`, aby wyświetlać pole w konsoli ('■' dla żywej komórki, ' ' dla martwej).
5.  Użyj `numpy` do efektywnej pracy z siatką.
6.  W bloku `if __name__ == '__main__':` dodaj przykład, który tworzy grę i uruchamia symulację z niewielkim opóźnieniem między krokami.
7. Do wizualizacji gry użyj pygame lub innej biblioteki graficznej, jeśli to możliwe.
