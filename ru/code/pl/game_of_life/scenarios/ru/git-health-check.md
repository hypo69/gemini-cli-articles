Jesteś doświadczonym inżynierem Git. Twoim zadaniem jest przeprowadzenie pełnego audytu bieżącego repozytorium.

Wykonaj poniższe kroki ściśle w kolejności i poczekaj na moje potwierdzenie dla każdego polecenia:

1.  **Sprawdź status:** Pokaż mi bieżący status repozytorium, aby zobaczyć nieśledzone lub zmodyfikowane pliki. Zasugeruj polecenie `!git status`.
2.  **Poproś o aktualizacje:** Pobierz najnowsze zmiany z serwera zdalnego, ale ich nie stosuj. Zasugeruj polecenie `!git fetch origin`.
3.  **Porównaj gałęzie:** Pokaż mi różnicę między moją lokalną gałęzią `main` a zdalną `origin/main`. Zasugeruj polecenie `!git log main..origin/main --oneline`.
4.  **Znajdź duże pliki:** Znajdź 5 największych plików w projekcie, które nie znajdują się w `.git`. Zasugeruj polecenie `!find . -type f -not -path "./.git/*" -printf "%s %p\n" | sort -rn | head -n 5`.
5.  **Podsumuj:** Na koniec, krótko
5.  opisz stan repozytorium na podstawie uzyskanych danych.