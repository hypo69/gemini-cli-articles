## 📘 Instrukcja do generowania kodu Python

### 1. Ogólne zasady

* Używaj **Python 3.10+**.
* Przestrzegaj **jasnego, czytelnego i jednoznacznego stylu** kodowania.
* **Każda funkcja, metoda i klasa** powinna mieć:

  * Adnotację typów (`type hints`)
  * Pełną i poprawną dokumentację w formacie `docstring` (patrz sekcja 3)
  * Wewnętrzne komentarze (`#`), gdzie to konieczne

---

### 2. Komentarze

* Komentarze powinny być **precyzyjne** i opisywać **co kod robi**, a nie «co robimy».
* **Zabronione** jest używanie zaimków: `robimy`, `zwracamy`, `wysyłamy`, `przechodzimy` itp.
* **Dozwolone** są tylko terminy: `ekstrakcja`, `wykonanie`, `wywołanie`, `zamiana`, `sprawdzenie`, `wysyłanie`, `Funkcja wykonuje`, `Funkcja zmienia wartość` itp.

#### ❌ Przykład niepoprawnego komentarza:

```python
# Pobieramy wartość parametru
```

#### ✅ Przykład poprawnego komentarza:

```python
# Funkcja ekstrahuje wartość parametru
```

---

### 3. Docstring (format dokumentacji)

Każda funkcja/metoda/klasa powinna zawierać `docstring` w następującym formacie:

```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Opis parametru `param`.
        param1 (Optional[str | dict | str], optional): Opis parametru `param1`. Domyślnie `None`.

    Returns:
        dict | None: Opis zwracanej wartości. Zwraca słownik lub `None`.

    Raises:
        SomeError: Opis sytuacji, w której występuje wyjątek `SomeError`.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

* **Wszystkie parametry i zwracane wartości muszą być opisane.**
* Sformułowania powinny być **zwięzłe, precyzyjne i jednoznaczne**.
* Nie wolno pomijać opisu parametrów/zwracanych wartości/wyjątków.

---

### 4. Adnotacja typów

* **Wszystkie zmienne, parametry i zwracane wartości** muszą być adnotowane.
* Używaj składni Python 3.10+: `list[int]`, `dict[str, Any]`, `str | None` itp.
* Przykłady poprawnych adnotacji:

#### ✅ Proste typy:

```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Kolekcje i typy złożone:

```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Funkcje i metody:

```python
def get_user_name(user_id: int) -> str:
    """Zwraca nazwę użytkownika na podstawie jego identyfikatora."""
    ...
```

#### ✅ Funkcje asynchroniczne:

```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Typy generyczne:

```python
from typing import TypeVar, Generic

T = TypeVar("T")

class Container(Generic[T]):
    def __init__(self, value: T) -> None:
        self.value = value

    def get(self) -> T:
        return self.value
```

---

### 5. Inne

* Używaj `default_factory` w `dataclass` dla wartości zmiennych (`list`, `dict`).
* Dla wartości `Optional` określ `T | None` (Python 3.10+) lub `Optional[T]`.
* Dla złożonych struktur — używaj `TypeAlias`.

---

📌 **Wskazówka:** Przechowywanie `GEMINI.md` w `.gemini` jest standardową praktyką dla gemini-cli. Podczas generowania kodu zawsze dołączaj adnotację typów, `docstring` i unikaj subiektywnych sformułowań w komentarzach. Celem jest jak najdokładniejsza, odtwarzalna i sformalizowana struktura kodu.