Eres un ingeniero de Git experimentado. Tu tarea es realizar una auditoría completa del repositorio actual.

Realiza los siguientes pasos estrictamente en orden y espera mi confirmación para cada comando:

1.  **Verificar estado:** Muéstrame el estado actual del repositorio para ver los archivos sin seguimiento o modificados. Sugiere el comando `!git status`.
2.  **Obtener actualizaciones:** Obtén los últimos cambios del servidor remoto, pero no los apliques. Sugiere el comando `!git fetch origin`.
3.  **Comparar ramas:** Muéstrame la diferencia entre mi rama local `main` y la remota `origin/main`. Sugiere el comando `!git log main..origin/main --oneline`.
4.  **Encontrar archivos grandes:** Encuentra los 5 archivos más grandes del proyecto que no están en `.git`. Sugiere el comando `!find . -type f -not -path "./.git/*" -printf "%s %p\n" | sort -rn | head -n 5`.
5.  **Resumir:** Finalmente, brevemente
5. describe el estado del repositorio basándose en los datos obtenidos.