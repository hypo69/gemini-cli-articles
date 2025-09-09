## 📘 Anweisung zur Generierung von Python-Code

### 1. Allgemeine Regeln

* Verwenden Sie **Python 3.10+**.
* Halten Sie sich an einen **klaren, lesbaren und eindeutigen Codierungsstil**.
* **Jede Funktion, Methode und Klasse** muss Folgendes haben:

  * Typannotationen (`type hints`)
  * Vollständige und korrekte Dokumentation im `docstring`-Format (siehe Abschnitt 3)
  * Interne Kommentare (`#`), wo nötig

---

### 2. Kommentare

* Kommentare müssen **genau** sein und beschreiben, **was der Code tut**, nicht „was wir tun“.
* **Verboten** ist die Verwendung von Pronomen: `wir tun`, `wir geben zurück`, `wir senden`, `wir gehen` usw.
* **Erlaubt** sind nur Begriffe: `Extraktion`, `Ausführung`, `Aufruf`, `Ersetzung`, `Prüfung`, `Senden`, `Funktion führt aus`, `Funktion ändert Wert` usw.

#### ❌ Beispiel für einen falschen Kommentar:

<pre>```python
# Parameterwert abrufen
````

#### ✅ Beispiel für einen korrekten Kommentar:

<pre>```python
# Funktion extrahiert Parameterwert
```

---

### 3. Docstring (Dokumentationsformat)

Jede Funktion/Methode/Klasse muss einen `docstring` im folgenden Format enthalten:

<pre>```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Beschreibung des Parameters `param`.
        param1 (Optional[str | dict | str], optional): Beschreibung des Parameters `param1`. Standardwert `None`.

    Returns:
        dict | None: Beschreibung des Rückgabewerts. Gibt ein Wörterbuch oder `None` zurück.

    Raises:
        SomeError: Beschreibung der Situation, in der die `SomeError`-Ausnahme auftritt.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

* **Alle Parameter und Rückgabewerte müssen beschrieben werden.**
* Formulierungen müssen **prägnant, genau und eindeutig** sein.
* Das Überspringen von Beschreibungen von Parametern/Rückgabewerten/Ausnahmen ist nicht zulässig.

---

### 4. Typannotationen

* **Alle Variablen, Parameter und Rückgabewerte** müssen annotiert werden.
* Verwenden Sie die Python 3.10+-Syntax: `list[int]`, `dict[str, Any]`, `str | None` usw.
* Beispiele für korrekte Annotationen:

#### ✅ Einfache Typen:

<pre>```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Sammlungen und komplexe Typen:

<pre>```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Funktionen und Methoden:

<pre>```python
def get_user_name(user_id: int) -> str:
    """Gibt den Benutzernamen anhand seiner ID zurück."""
    ...
```

#### ✅ Asynchrone Funktionen:

<pre>```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Generische Typen:

<pre>```python
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

* Verwenden Sie `default_factory` in `dataclass` für veränderliche Werte (`list`, `dict`).
* Für `Optional`-Werte geben Sie `T | None` (Python 3.10+) oder `Optional[T]` an.
* Für komplexe Strukturen — verwenden Sie `TypeAlias`.

---

📌 **Tipp:** Das Speichern von `GEMINI.md` in `.gemini` ist eine Standardpraxis für gemini-cli. Beim Generieren von Code sollten Sie immer Typannotationen und `docstring` einschließen und subjektive Formulierungen in Kommentaren vermeiden. Ziel ist eine möglichst präzise, reproduzierbare und formalisierte Code-Struktur.
