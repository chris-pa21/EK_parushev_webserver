# Webserver mit Raspberry PI 3

  

Als EK für SYT-I habe ich mit dem Raspberry PI 3 , auf dem ein Linux läuft einen Webserver erstellt. Dazu habe ich das Tool apache2 (hauptsächlich für Linux) verwendet.

  

## Funktion Apache2

  

Apache2 ist ein Tool, das relativ simpel einen http-Webserver startet. Dazu muss man nachdem man apache2 herunterlädt alle Dateien, die man auf dem Server haben will in den Ordner in den Ordner **/var/www/html/** kopieren. Sobald den Server startet findet man mit **ipaddresse/FILENAME** das File. Hat man nur eine Datei im Ordner, braucht man nicht den noch den Dateinamen angeben. Genauso wie wenn man ein **index.html** File drinnen hat, erkennt apache das automatisch als Startseite (Sozusagen Startseite des Servers, deswegen muss man hier auch nur die IP-Adresse angeben). Apache hat automatisch ein index.html-File in dem Verzeichnis, bei dem es sich um eine Art Guide handelt. Das kann man jederzeit rausnehmen.

  

## Vorgehensweise:

Mit dem Pi verbinden:
Dazu habe ich mit dem Programm PUTTY.exe eine SSH-Sitzung mit dem Pi gestartet   	und mich dort in meinen Account eingeloggt.


Apache als root herunterladen:
```
sudo apt install apache2
```
In den Ordner **/var/www/html**:
```
cd /var/www/html
```
Neues Textfile:
```
echo "Herzlich Willkommen auf dem Webserver!" >> test.txt
```
Server starten:
```
sudo systemctl start apache2.service
```
Prüfen, ob der Server online ist:
```
sudo systemctl status apache2.service
```
Man kann den Server auch jederzeit stoppen:
```
sudo systemctl stop apache2.service
```


