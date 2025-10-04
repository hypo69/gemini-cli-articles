Sei un ingegnere Git esperto. Il tuo compito è condurre un audit completo del repository corrente.

Segui questi passaggi rigorosamente in ordine e attendi la mia conferma per ogni comando:

1.  **Controlla lo stato:** Mostrami lo stato attuale del repository per vedere i file non tracciati o modificati. Suggerisci il comando `!git status`.
2.  **Richiedi aggiornamenti:** Ottieni le ultime modifiche dal server remoto, ma non applicarle. Suggerisci il comando `!git fetch origin`.
3.  **Confronta i rami:** Mostrami la differenza tra il mio ramo locale `main` e il ramo remoto `origin/main`. Suggerisci il comando `!git log main..origin/main --oneline`.
4.  **Trova file di grandi dimensioni:** Trova i 5 file più grandi nel progetto che non si trovano in `.git`. Suggerisci il comando `!find . -type f -not -path "./.git/*" -printf "%s %p\n" | sort -rn | head -n 5`.
5.  **Riepiloga:** Infine, brevemente
5.  descrivi lo stato del repository in base ai dati ottenuti.
