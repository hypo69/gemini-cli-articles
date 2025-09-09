## 📘 Instrucción para la generación de código Python

### 1. Reglas generales

* Utiliza **Python 3.10+**.
* Sigue un **estilo de codificación claro, legible e inequívoco**.
* **Cada función, método y clase** debe tener:

  * Anotación de tipos (`type hints`)
  * Documentación completa y correcta en formato `docstring` (ver sección 3)
  * Comentarios internos (`#`), donde sea necesario

---

### 2. Comentarios

* Los comentarios deben ser **precisos** y describir **qué hace el código**, no «qué hacemos».
* **Prohibido** usar pronombres: `hacemos`, `devolvemos`, `enviamos`, `pasamos`, etc.
* **Permitidos** solo términos: `extracción`, `ejecución`, `llamada`, `reemplazo`, `verificación`, `envío`, `La función realiza`, `La función modifica el valor`, etc.

#### ❌ Ejemplo de comentario incorrecto:

<pre>```python
# Obtenemos el valor del parámetro
````

#### ✅ Ejemplo de comentario correcto:

<pre>```python
# La función extrae el valor del parámetro
```

---

### 3. Docstring (formato de documentación)

Cada función/método/clase debe contener `docstring` en el siguiente formato:

<pre>```python
def function(param: str, param1: Optional[str | dict | str] = None) -> dict | None:
    """
    Args:
        param (str): Descripción del parámetro `param`.
        param1 (Optional[str | dict | str], optional): Descripción del parámetro `param1`. Por defecto `None`.

    Returns:
        dict | None: Descripción del valor de retorno. Devuelve un diccionario o `None`.

    Raises:
        SomeError: Descripción de la situación en la que se produce la excepción `SomeError`.

    Example:
        >>> function('param', 'param1')
        {'param': 'param1'}
    """
```

* **Todos los parámetros y valores de retorno deben estar descritos.**
* Las formulaciones deben ser **concisas, precisas e inequívocas**.
* No se permite omitir la descripción de parámetros/valores de retorno/excepciones.

---

### 4. Anotación de tipos

* **Todas las variables, parámetros y valores de retorno** deben estar anotados.
* Utiliza la sintaxis de Python 3.10+: `list[int]`, `dict[str, Any]`, `str | None`, etc.
* Ejemplos de anotaciones correctas:

#### ✅ Tipos simples:

<pre>```python
name: str = "John"
count: int = 42
flag: bool = True
```

#### ✅ Colecciones y tipos complejos:

<pre>```python
from typing import Any, Optional, Callable, TypeAlias

coordinates: tuple[float, float] = (55.75, 37.61)
metadata: dict[str, Any] = {"debug": True}
UserId: TypeAlias = int
```

#### ✅ Funciones y métodos:

<pre>```python
def get_user_name(user_id: int) -> str:
    """Devuelve el nombre de usuario por su identificador."""
    ...
```

#### ✅ Funciones asíncronas:

<pre>```python
async def fetch_users() -> AsyncIterator[dict[str, int | str]]:
    ...
```

#### ✅ Tipos genéricos:

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

### 5. Otros

* Utiliza `default_factory` en `dataclass` para valores mutables (`list`, `dict`).
* Para valores `Optional`, especifica `T | None` (Python 3.10+) u `Optional[T]`.
* Para estructuras complejas, utiliza `TypeAlias`.

---

📌 **Sugerencia:** Almacenar `GEMINI.md` en `.gemini` es una práctica estándar para gemini-cli. Al generar código, incluye siempre la anotación de tipos, `docstring` y evita formulaciones subjetivas en los comentarios. El objetivo es una estructura de código lo más precisa, reproducible y formalizada posible.
