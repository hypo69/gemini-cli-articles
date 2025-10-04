## 📘 Instrukcje dotyczące generowania kodu Python

### 1. Zasady ogólne

*   Używaj **Python 3.10+**.
*   Przestrzegaj **jasnego, czytelnego i jednoznacznego stylu kodowania**.
*   **Każda funkcja, metoda i klasa** musi posiadać:

    *   Adnotacje typów (`type hints`)
    *   Pełną i poprawną dokumentację w formacie `docstring` (patrz sekcja 3)
    *   Wewnętrzne komentarze (`#`) tam, gdzie jest to konieczne

---

### 2. Komentarze

*   Komentarze powinny być **precyzyjne** i opisywać **co robi kod**, a nie „co robimy”.
*   **Zabronione** jest używanie zaimków: `robimy`, `zwracamy`, `wysyłamy`, `przechodzimy` itp.
*   **Dozwolone** są tylko terminy: `ekstrakcja`, `wykonanie`, `wywołanie`, `zamiana`, `sprawdzenie`, `wysyłanie`, `Funkcja wykonuje`, `Funkcja zmienia wartość` itp.

#### ❌ Przykład nieprawidłowego komentarza:

```python
# Pobieramy wartość parametru
```

#### ✅ Przykład prawidłowego komentarza:

```python
# Funkcja ekstrahuje wartość parametru
```

---

### 3. Docstring (format dokumentacji)

Każda funkcja/metoda/klasa musi zawierać `docstring` w następującym formacie:

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

*   **Wszystkie parametry i wartości zwracane muszą być opisane.**
*   Formuły muszą być **zwięzłe, precyzyjne i jednoznaczne**.
*   Niedopuszczalne jest pomijanie opisu parametrów/wartości zwracanych/wyjątków.

---

### 4. Adnotacje typów

*   **Wszystkie zmienne, parametry i wartości zwracane** muszą być adnotowane.
*   Używaj składni Python 3.10+: `list[int]`, `dict[str, Any]`, `str | None` itp.
*   Przykłady prawidłowych adnotacji:

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

*   Używaj `default_factory` w `dataclass` dla zmiennych wartości (`list`, `dict`).
*   Dla wartości `Optional` określ `T | None` (Python 3.10+) lub `Optional[T]`.n*   Dla złożonych struktur — używaj `TypeAlias`.

---

📌 **Wskazówka**: Podczas generowania kodu zawsze dołączaj adnotacje typów, `docstring` i unikaj subiektywnych sformułowań w komentarzach. Celem jest maksymalnie precyzyjna, odtwarzalna i sformalizowana struktura kodu.
