# Erstellen einer Testapp
## Arbeitsordner erstellen
<pre>bash<br>
`mkdir ~/testapp`
`cd ~/testapp`<br></pre>

## Minimal HTML Seite erstellen

`nano index.html`
<pre>bash<br>
     <html>                                                              
           <body><h1> Testanwendung auf Tomcat </h1>                     
                    <p> Erfolgreich deployed auf penguin.linux.test!</p> 
          </body>                                                        
     </html>                                                             
</br></pre>
## WEB-INF Ordner und web.xml erstellen
  * Tomcat erwartet im Webapp Ordner ~/testapp einen WEB-INF Ordner und eine web.xml
<pre>bash<br>
   `mkdir -p WEB-INF`
   `nano WEB-INF/web.xml`
</br></pre>

## Minimal-Inhalt
      
      ` <web-app xmlns="https://xmlns.jcp.org/xml/ns/javaee" version="3.1">
      </web-app>`
     

## WAR-Datei erzeugen
<pre>
`cd ..`
`jar cvf testapp.war -C testapp/ .`
</pre>

## Deployment in Tomcat
`sudo cp testapp.war /var/lib/tomcat10/webapps/`

* Automatisches Entpacken der WAR Datei und starten der APP


## Test im Browser

`http://penguin.linux.test:8080/testapp`  
