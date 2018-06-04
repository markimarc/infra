# Technisch ontwerp OVDingen

## Server nummering
De servers zijn onderverdeeld in nummers. Iedere server begint met de aanduiding OV, gevolgd door een 2 cijferig getal. Het getal is altijd opvolgend.

## Server OS
Alle servers van OVDingen draaien op Debian 9.

## Server indeling
Om de belasting van de servers te verkleinen, is ervoor gekozen om verschillende diensten te versprijden over meerdere servers. De indeling van de servers is als volgt:

### OV01

* Webserver (NGINX) ovdingen.nl
* Mailserver
* Treinviewer
* NS-VT
* Spoor.app
* RDT API frontend (communiceert met backend via ZMQ) Flask op 127.0.0.1:9000
* OV-fiets API reverse proxy
* RDT-serviceinfo API reverse proxy
* NS-API cache
* spoor-app.service Flask op 127.0.0.1:4500
* Treinpositie API reverse proxy

### OV02

* Universal (BISON (doen we vooralsnog niks mee), AR-NU, DVS, binnenkort mogelijk OV-fiets)
* RDT service
* RDT-serviceinfo Flask op 0.0.0.0:8000
* OV-fiets API Flask op 0.0.0.0:8090
* Telegram bot
* Treinpositie API backend + flask op 0.0.0.0:8010

&copy; 2018 OVDingen. Op dit document kunnen geen rechten worden ontleend.
