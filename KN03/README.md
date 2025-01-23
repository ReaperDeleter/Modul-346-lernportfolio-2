Screenshot 1: Details der Instanz (Key pair assigned at launch)

In diesem Screenshot werden die Instanzdetails angezeigt, inklusive des zugewiesenen Key Pairs, das bei der Erstellung verwendet wurde. Der Abschnitt "Key pair assigned at launch" zeigt, dass der zweite Schlüssel, den ich im GUI angegeben habe, korrekt zugeordnet wurde.
Screenshot 2: SSH-Login mit Schlüssel 1 (via Cloud-init)

Dieser Screenshot zeigt den erfolgreichen SSH-Login mit dem Schlüssel, der in der Cloud-init-Datei angegeben wurde. Der Befehl lautet:

``` ssh -i <pfad-zum-ersten-schlüssel> ubuntu@<instanz-ip>

Das Resultat bestätigt, dass der Benutzer ubuntu korrekt eingerichtet wurde und der Schlüssel aus der Cloud-init-Datei funktioniert.
Screenshot 3: SSH-Login mit Schlüssel 2 (via GUI)

In diesem Screenshot wird versucht, sich mit dem zweiten Schlüssel, der bei der Instanzerstellung über das AWS GUI konfiguriert wurde, einzuloggen. Der Befehl lautet:

``` ssh -i <pfad-zum-zweiten-schlüssel> ubuntu@<instanz-ip>

Das Resultat zeigt, dass der Login nicht erfolgreich ist, da der zweite Schlüssel nicht in der Cloud-init-Konfiguration enthalten war.
Screenshot 4: Cloud-init-Log (cloud-init-output.log)

Dieser Screenshot zeigt einen Ausschnitt aus dem Cloud-init-Log (/var/log/cloud-init-output.log). Darin wird dokumentiert, wie die Konfigurationen aus der Cloud-init-Datei umgesetzt wurden, z. B. das Hinzufügen des Benutzers ubuntu und des autorisierten SSH-Schlüssels. Der Befehl zur Anzeige des Logs war:

``` cat /var/log/cloud-init-output.log | less