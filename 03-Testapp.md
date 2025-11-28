## Erstellen einer Testapp
# Arbeitsordner erstellen

`mkdir ~/testapp`
`cd ~/testapp`

# Minimal HTML Seite erstellen

`nano index.html`

  ------INHALT----------------------------------------------------––––––––-
  |   <html>                                                              |
  |         <body><h1> Testanwendung auf Tomcat </h1>                     |
  |                  <p> Erfolgreich deployed auf penguin.linux.test!</p> |
  |        </body>                                                        |
  |   <\html>                                                             |
  -------------------------------------------------------------------------

# WEB-INF Ordner und web.xml erstellen
  * Tomcat erwartet im Webapp Ordner ~/testapp einen WEB-INF Ordner und eine web.xml

   `mkdir -p WEB-INF`
   `nano WEB-INF/web.xml`


# Minimal-Inhalt
      <web-app xmlns="https://xmlns.jcp.org/xml/ns/javaee" version="3.1">
      </web-app>

# WAR-Datei erzeugen

`cd ..`
`jar cvf testapp.war -C testapp/ .`

# Deployment in Tomcat
`sudo cp testapp.war /var/lib/tomcat10/webapps/`

* Automatisches Entpacken der WAR Datei und starten der APP


# Test im Browser

`http://penguin.linux.test:8080/testapp`  
