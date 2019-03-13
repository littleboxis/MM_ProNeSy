# MM_ProNeSy
Nützliche Befehle und Problemlösungsansätze im Umgang mit dem Magic Mirror

## Bekannte Probleme

1. **Wunderlist:** Neue Listeneinträge erscheinen erst nach der zweiten Modulaktualisierung. Diese erfolgt automatisch anhand des definierten Aktualisierungsintervalls (z.B. 60 Sekunden). Nach zwei Minuten (120 Sekunden) erscheint also erst der neue Listeneintrag

## Nützliches

1. **Aktualisierung der MagicMirror-Seite**: Mit Hilfe der Tastenkombination `STRG + R` kann eine manuelle Aktualisierung der MagicMirror-Ansicht erzwungen werden. Damit werden auch alle Module etc. aktualisiert. Dieser Schritt empfiehlt sich zu Beginn.

2. **Verlassen der MagicMirror-Ansicht**: Sollte die manuelle Aktualisierung das Problem nicht lösen, kann die Ansicht des MagicMirrors mittels `STRG + Q` verlassen werden. Man gelangt somit zum Desktop des Raspberry Pi, um weitere Aktionen ausführen zu können. BEACHTE: Dieser Befehl schließt lediglich das Fenster, indem die MagicMirror-Anwendung dargestellt wird. Die Anwendung selbst wird damit nicht beendet!

3. **Beenden der MagicMirror-Anwendung**: Im Gegensatz zu Punkt 2 kann die MagicMirror-Anwendung komplett beendet werden. Dies empfiehlt sich vor allem bei Änderungen der config-Datei oder um Problemlösungen zu testen. Hierfür benötigt man die Kommandozeile (CLI). Hierfür wird zunächst wieder mittels `STRG + Q` das Anwendungsfenster geschlossen. Auf dem Desktop wird nun das Terminal geöffnet (dies geht auch über die Tastenkombination `STRG + ALt + BACKSPACE`). Im Terminal kann nun mithilfe des Befehls `pm2 stop mm` die MagicMirror-Anwendung beendet werden.

4. **Starten der MagicMirror-Anwendung**: Um die Anwendung des MagicMirrors erneut zu starten wird, wie in Punkt 3 beschrieben, die Kommandozeile geöffnet. Der Befehl `pm2 start mm.sh` startet nun die Anwendung. 

5. **Neustarten des MagicMirrors**: Alternativ kann über den Befehl `pm2 restart mm` der MagicMirror neugestartet werden. 
