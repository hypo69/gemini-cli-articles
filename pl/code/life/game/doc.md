# Projekt "Gra w życie"

## Krótki opis

Ten projekt to implementacja automatu komórkowego "Gra w życie" Conwaya w Pythonie. Gra symuluje ewolucję populacji komórek na dwuwymiarowej siatce, gdzie stan każdej komórki (żywa lub martwa) zmienia się w zależności od stanu jej sąsiadów.

## Struktura plików

-   `life.py`: Główny plik zawierający implementację klasy `Game`, która zarządza logiką symulacji "Gry w życie" i jej wizualizacją graficzną za pomocą biblioteki `pygame`.
-   `test_life.py`: Plik z testami jednostkowymi dla klasy `Game`, używający frameworka `pytest`. Zawiera test sprawdzający ewolucję oscylatora "Blinker".

## Jak uruchomić symulację

Aby uruchomić symulację "Gry w życie", upewnij się, że masz zainstalowane niezbędne biblioteki (`numpy` i `pygame`). Jeśli nie, zainstaluj je:

```bash
pip install numpy pygame
```

Następnie uruchom plik główny:

```bash
python game/life.py
```

## Jak uruchomić testy

Aby uruchomić testy, musisz zainstalować `pytest` i `numpy`:

```bash
pip install pytest numpy
```

Następnie uruchom testy, określając ścieżkę do pliku testowego:

```bash
pytest game/test_life.py
```