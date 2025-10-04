## 📘 Instructions pour la génération de code Python

### 1. Règles générales

*   Utilisez **Python 3.10+**.
*   Adhérez à un **style de codage clair, lisible et univoque**.
*   **Chaque fonction, méthode et classe** doit avoir:

    *   Annotations de type (`type hints`)
    *   Documentation complète et correcte au format `docstring` (voir section 3)
    *   Commentaires internes (`#`) si nécessaire

---

### 2. Commentaires

*   Les commentaires doivent être **précis** et décrire **ce que fait le code**, et non "ce que nous faisons".
*   **Il est interdit** d'utiliser des pronoms: `nous faisons`, `nous retournons`, `nous envoyons`, `nous allons`, etc.
*   **Sont autorisés** uniquement les termes: `extraction`, `exécution`, `appel`, `remplacement`, `vérification`, `envoi`, `La fonction exécute`, `La fonction modifie la valeur`, etc.

#### ❌ Exemple de commentaire incorrect:

```python
# Obtention de la valeur du paramètre
```

#### ✅ Exemple de commentaire correct:

```python
# La fonction extrait la valeur du paramètre
```

---

### 3. Docstring (format de documentation)

Chaque fonction/méthode/classe doit contenir un `docstring` au format suivant:

```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Description du paramètre `param`.
        param1 (Optional[str | dict | str], optional): Description du paramètre `param1`. Par défaut `None`.

    Returns:
        dict | None: Description de la valeur de retour. Retourne un dictionnaire ou `None`.

    Raises:
        SomeError: Description de la situation dans laquelle l'exception `SomeError` se produit.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

*   **Tous les paramètres et valeurs de retour doivent être décrits.**
*   Les formulations doivent être **concises, précises et univoques**.
*   Il n'est pas permis d'omettre la description des paramètres/valeurs de retour/exceptions.

---

### 4. Annotations de type

*   **Toutes les variables, paramètres et valeurs de retour** doivent être annotés.
*   Utilisez la syntaxe Python 3.10+: `list[int]`, `dict[str, Any]`, `str | None`, etc.
*   Exemples d'annotations correctes:

#### ✅ Types simples:

```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Collections et types complexes:

```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Fonctions et méthodes:

```python
def get_user_name(user_id: int) -> str:
    """Retourne le nom d'utilisateur par son ID."""
    ...
```

#### ✅ Fonctions asynchrones:

```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Types génériques:

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

### 5. Autres

*   Utilisez `default_factory` dans `dataclass` pour les valeurs mutables (`list`, `dict`).
*   Pour les valeurs `Optional`, spécifiez `T | None` (Python 3.10+) ou `Optional[T]`.
*   Pour les structures complexes, utilisez `TypeAlias`.

---

📌 **Conseil**: Lors de la génération de code, incluez toujours les annotations de type, le `docstring` et évitez les formulations subjectives dans les commentaires. L'objectif est une structure de code aussi précise, reproductible et formalisée que possible.
