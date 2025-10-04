## 📘 Instrucciones para la generación de código Python

### 1. Reglas generales

*   Utilice **Python 3.10+**.
*   Adhiérase a un **estilo de codificación claro, legible e inequívoco**.
*   **Cada función, método y clase** debe tener:

    *   Anotaciones de tipo (`type hints`)
    *   Documentación completa y correcta en formato `docstring` (ver sección 3)
    *   Comentarios internos (`#`) donde sea necesario

---

### 2. Comentarios

*   Los comentarios deben ser **precisos** y describir **qué hace el código**, no "qué estamos haciendo".
*   **Prohibidos** están los pronombres: `hacemos`, `devolvemos`, `enviamos`, `vamos`, etc.
*   **Permitidos** están solo los términos: `extracción`, `ejecución`, `llamada`, `reemplazo`, `verificación`, `envío`, `La función realiza`, `La función cambia el valor`, etc.

#### ❌ Ejemplo de comentario incorrecto:

```python
# Obteniendo valor de parámetro
```

#### ✅ Ejemplo de comentario correcto:

```python
# La función extrae el valor del parámetro
```

---

### 3. Docstring (formato de documentación)

Cada función/método/clase debe contener un `docstring` en el siguiente formato:

```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Descripción del parámetro `param`.
        param1 (Optional[str | dict | str], optional): Descripción del parámetro `param1`. Por defecto `None`.

    Returns:
        dict | None: Descripción del valor de retorno. Devuelve un diccionario o `None`.

    Raises:
        SomeError: Descripción de la situación en la que ocurre la excepción `SomeError`.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

*   **Todos los parámetros y valores de retorno deben estar descritos.**
*   Las formulaciones deben ser **concisas, precisas e inequívocas**.
*   No se permite omitir la descripción de parámetros/valores de retorno/excepciones.

---

### 4. Anotaciones de tipo

*   **Todas las variables, parámetros y valores de retorno** deben estar anotados.
*   Utilice la sintaxis de Python 3.10+: `list[int]`, `dict[str, Any]`, `str | None`, etc.
*   Ejemplos de anotaciones correctas:

#### ✅ Tipos simples:

```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Colecciones y tipos complejos:

```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Funciones y métodos:

```python
def get_user_name(user_id: int) -> str:
    """Devuelve el nombre de usuario por su ID."""
    ...
```

#### ✅ Funciones asíncronas:

```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Tipos genéricos:

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

### 5. Otros

*   Utilice `default_factory` en `dataclass` para valores mutables (`list`, `dict`).
*   Para valores `Optional`, especifique `T | None` (Python 3.10+) o `Optional[T]`.
*   Para estructuras complejas, utilice `TypeAlias`.

---

📌 **Sugerencia**: Al generar código, incluya siempre anotaciones de tipo, `docstring` y evite el lenguaje subjetivo en los comentarios. El objetivo es una estructura de código lo más precisa, reproducible y formalizada posible.
