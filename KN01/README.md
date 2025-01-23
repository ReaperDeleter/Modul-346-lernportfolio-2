## 1. Screenshot 1: CPUs bei weniger CPU-Zuteilung als das Host-System hat

Screenshot 1 zeigt die Konsolenausgabe des Befehls lscpu | grep "CPU(s)", nachdem der VM weniger logische Prozessoren zugewiesen wurden, als das Host-System besitzt. Dies demonstriert, wie die Ressourcen der VM gezielt reduziert werden können.

## 2. Screenshot 2: CPUs bei mehr CPU-Zuteilung als das Host-System hat
Screenshot 2 zeigt die Konsolenausgabe des Befehls lscpu | grep "CPU(s)", nachdem der VM mehr logische Prozessoren zugewiesen wurden, als das Host-System tatsächlich hat. Dies veranschaulicht, wie eine Überzuteilung von CPU-Ressourcen entweder funktioniert oder zu einer Fehlermeldung führt.

## 3. Screenshot 3: RAM bei weniger RAM-Zuteilung als das Host-System hat
Screenshot 3 zeigt die Ausgabe des Befehls free -g, nachdem der VM weniger RAM zugewiesen wurde, als im Host-System verfügbar ist. Dies verdeutlicht die Möglichkeit, den Arbeitsspeicher der VM flexibel zu begrenzen.

## 4. Screenshot 4: RAM bei mehr RAM-Zuteilung als das Host-System hat
Screenshot 4 zeigt die Ausgabe des Befehls free -g, nachdem der VM mehr RAM zugewiesen wurde, als das Host-System tatsächlich besitzt. Der Screenshot zeigt, ob eine Überzuteilung erfolgreich ist oder eine Fehlermeldung auftritt.

## 5. Erklärung zu Fehlermeldungen oder Überzuteilung
Die Überzuteilung von Ressourcen wie CPU oder RAM kann in Virtualisierungsumgebungen durch sogenanntes Overcommitment möglich sein. Dies bedeutet, dass die Virtualisierungssoftware mehr Ressourcen zuweist, als physisch vorhanden sind, da davon ausgegangen wird, dass nicht alle VMs ihre zugewiesenen Ressourcen gleichzeitig voll ausnutzen. Sollte die VM allerdings mehr Ressourcen beanspruchen, als tatsächlich verfügbar sind, kann dies zu Leistungseinbußen oder Fehlermeldungen führen.