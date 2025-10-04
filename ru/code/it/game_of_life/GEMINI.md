## 📘 Istruzioni per la generazione di codice Python

### 1. Regole generali

*   Utilizzare **Python 3.10+**.
*   Aderire a uno **stile di codifica chiaro, leggibile e inequivocabile**.
*   **Ogni funzione, metodo e classe** deve avere:

    *   Annotazioni di tipo (`type hints`)
    *   Documentazione completa e corretta in formato `docstring` (vedere sezione 3)
    *   Commenti interni (`#`) dove necessario

---

### 2. Commenti

*   I commenti devono essere **precisi** e descrivere **cosa fa il codice**, non "cosa stiamo facendo".
*   **È vietato** usare pronomi: `facciamo`, `restituiamo`, `inviamo`, `andiamo`, ecc.
*   **Sono consentiti** solo i termini: `estrazione`, `esecuzione`, `chiamata`, `sostituzione`, `verifica`, `invio`, `La funzione esegue`, `La funzione modifica il valore`, ecc.

#### ❌ Esempio di commento errato:

```python
# Ottenere il valore del parametro
```

#### ✅ Esempio di commento corretto:

```python
# La funzione estrae il valore del parametro
```

---

### 3. Docstring (formato di documentazione)

Ogni funzione/metodo/classe deve contenere un `docstring` nel seguente formato:

```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Descrizione del parametro `param`.
        param1 (Optional[str | dict | str], optional): Descrizione del parametro `param1`. Predefinito `None`.

    Returns:
        dict | None: Descrizione del valore di ritorno. Restituisce un dizionario o `None`.

    Raises:
        SomeError: Descrizione della situazione in cui si verifica l'eccezione `SomeError`.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

*   **Tutti i parametri e i valori di ritorno devono essere descritti.**
*   Le formulazioni devono essere **concise, precise e inequivocabili**.
*   Non è consentito omettere la descrizione di parametri/valori di ritorno/eccezioni.

---

### 4. Annotazioni di tipo

*   **Tutte le variabili, i parametri e i valori di ritorno** devono essere annotati.
*   Utilizzare la sintassi Python 3.10+: `list[int]`, `dict[str, Any]`, `str | None`, ecc.
*   Esempi di annotazioni corrette:

#### ✅ Tipi semplici:

```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Collezioni e tipi complessi:

```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Funzioni e metodi:

```python
def get_user_name(user_id: int) -> str:
    """Restituisce il nome utente tramite il suo ID."""
    ...
```

#### ✅ Funzioni asincrone:

```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Tipi generici:

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

### 5. Altro

*   Utilizzare `default_factory` in `dataclass` per valori mutabili (`list`, `dict`).
*   Per i valori `Optional`, specificare `T | None` (Python 3.10+) o `Optional[T]`.
*   Per strutture complesse — utilizzare `TypeAlias`.

---

📌 **Suggerimento**: Quando si genera codice, includere sempre annotazioni di tipo, `docstring` ed evitare formulazioni soggettive nei commenti. L'obiettivo è una struttura di codice il più precisa, riproducibile e formalizzata possibile.
