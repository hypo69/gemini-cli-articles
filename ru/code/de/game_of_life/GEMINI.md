## 📘 Anweisungen zur Python-Code-Generierung

### 1. Allgemeine Regeln

*   Verwenden Sie **Python 3.10+**.
*   Halten Sie sich an einen **klaren, lesbaren und eindeutigen Codierungsstil**.
*   **Jede Funktion, Methode und Klasse** muss Folgendes enthalten:

    *   Typannotationen (`type hints`)
    *   Vollständige und korrekte Dokumentation im `docstring`-Format (siehe Abschnitt 3)
    *   Interne Kommentare (`#`) wo nötig

---

### 2. Kommentare

*   Kommentare sollten **präzise** sein und beschreiben, **was der Code tut**, nicht "was wir tun".
*   **Verboten** sind Pronomen: `wir machen`, `wir geben zurück`, `wir senden`, `wir gehen` usw.
*   **Erlaubt** sind nur Begriffe: `Extraktion`, `Ausführung`, `Aufruf`, `Ersetzung`, `Überprüfung`, `Senden`, `Funktion führt aus`, `Funktion ändert Wert` usw.

#### ❌ Beispiel für einen falschen Kommentar:

```python
# Parameterwert abrufen
```

#### ✅ Beispiel für einen korrekten Kommentar:

```python
# Funktion extrahiert Parameterwert
```

---

### 3. Docstring (Dokumentationsformat)

Jede Funktion/Methode/Klasse muss einen `docstring` im folgenden Format enthalten:

```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Beschreibung des Parameters `param`.
        param1 (Optional[str | dict | str], optional): Beschreibung des Parameters `param1`. Standardmäßig `None`.

    Returns:
        dict | None: Beschreibung des Rückgabewerts. Gibt ein Wörterbuch oder `None` zurück.

    Raises:
        SomeError: Beschreibung der Situation, in der die Ausnahme `SomeError` auftritt.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

*   **Alle Parameter und Rückgabewerte müssen beschrieben werden.**
*   Formulierungen müssen **prägnant, präzise und eindeutig** sein.
*   Das Weglassen der Beschreibung von Parametern/Rückgabewerten/Ausnahmen ist nicht zulässig.

---

### 4. Typannotationen

*   **Alle Variablen, Parameter und Rückgabewerte** müssen annotiert werden.
*   Verwenden Sie die Python 3.10+-Syntax: `list[int]`, `dict[str, Any]`, `str | None` usw.
*   Beispiele für korrekte Annotationen:

#### ✅ Einfache Typen:

```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Sammlungen und komplexe Typen:

```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Funktionen und Methoden:

```python
def get_user_name(user_id: int) -> str:
    """Gibt den Benutzernamen anhand seiner ID zurück."""
    ...
```

#### ✅ Asynchrone Funktionen:

```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Generische Typen:

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

### 5. Sonstiges

*   Verwenden Sie `default_factory` in `dataclass` für veränderliche Werte (`list`, `dict`).
*   Für `Optional`-Werte geben Sie `T | None` (Python 3.10+) oder `Optional[T]` an.
*   Für komplexe Strukturen — verwenden Sie `TypeAlias`.

---

📌 **Tipp**: Fügen Sie beim Generieren von Code immer Typannotationen und `docstring` hinzu und vermeiden Sie subjektive Formulierungen in Kommentaren. Ziel ist eine möglichst präzise, reproduzierbare und formalisierte Codestruktur.
