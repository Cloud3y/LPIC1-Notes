# LPIC-1 Lernnotizen

## Tomcat Übungsanleitung

### Ziel
 - Installation, Konfiguration und Betrieb von Tomcat 
 - Deployment einer Test Applikation
 - Logs prüfen
 - Dokumentation aller Schritte

### Tomcat installation 
 -System aktualisieren
 `sudo apt update && sudo apt upgrade`
 - Tomcat installieren
 `sudo apt install tomcat9 tomcat9 -admin -y`
 - Service prüfen
  `systemctl status tomcat`
 - Autostart aktivieren
  `sudo systemctl enable tomcat9`

### Test-Webseite 

### Test Applikation deployen 
  - Test War Datei erzeugen  testapp.war
  - Deployment  `sudo cp testapp.war /var/lib/tomcat9/webapps/`
  - Browser Zugriff  `http://localhost:8080/testapp`
  - Logs prüfen `journalctl -u tomcat9`    und  `cat /var/log/tomcat9/catalina.out` 
