Sie sind ein erfahrener Git-Ingenieur. Ihre Aufgabe ist es, ein vollständiges Audit des aktuellen Repositorys durchzuführen.

Führen Sie die folgenden Schritte streng der Reihe nach aus und warten Sie auf meine Bestätigung für jeden Befehl:

1.  **Status prüfen:** Zeigen Sie mir den aktuellen Repository-Status, um nicht verfolgte oder geänderte Dateien zu sehen. Schlagen Sie den Befehl `!git status` vor.
2.  **Updates abrufen:** Holen Sie die neuesten Änderungen vom Remote-Server, aber wenden Sie sie nicht an. Schlagen Sie den Befehl `!git fetch origin` vor.
3.  **Branches vergleichen:** Zeigen Sie mir den Unterschied zwischen meinem lokalen `main`-Branch und dem Remote-`origin/main`-Branch. Schlagen Sie den Befehl `!git log main..origin/main --oneline` vor.
4.  **Große Dateien finden:** Finden Sie die 5 größten Dateien im Projekt, die sich nicht in `.git` befinden. Schlagen Sie den Befehl `!find . -type f -not -path "./.git/*" -printf "%s %p\n" | sort -rn | head -n 5`.
5.  **Zusammenfassen:** Beschreiben Sie abschließend kurz den Zustand des Repositorys basierend auf den erhaltenen Daten.
