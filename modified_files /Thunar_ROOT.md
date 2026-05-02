## Im Dateimanager Thunar "Als Root öffnen" hinzufügen:

- In Thunar eine "Benutzerdefinierte Aktion" hinzufügen
  - Name: Als ROOT öffnen
  - Befehl: /usr/bin/pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY thunar %f
    ```
    /usr/bin/pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY thunar %f
    ```
  - Dateizuordnung: Alle auswählen
