## Im Dateimanager Thunar (xfce) "Als Root öffnen" hinzufügen:

- In Thunar eine "Benutzerdefinierte Aktion" hinzufügen
  - Name: Als ROOT öffnen
  - Befehl: /usr/bin/pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY thunar %f
    ```
    /usr/bin/pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY thunar %f
    ```
  - Dateizuordnung: Alle auswählen

&nbsp;
&nbsp;
&nbsp;
&nbsp;

----------------------

&nbsp;
&nbsp;
&nbsp;
&nbsp;

## Im Dateimanager Dolphin (KDE) "Als Root öffnen" hinzufügen:

- Im Terminal folgenden Befehl ausführen:
  ```
  pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY KDE_SESSION_VERSION=5 KDE_FULL_SESSION=true dolphin
  ```
