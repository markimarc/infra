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
* Trein.app
* RDT API frontend (communiceert met backend via ZMQ)
* OV-fiets API reverse proxy
* RDT-serviceinfo API reverse proxy
* NS-API cache

### OV02

* Universal (BISON (doen we vooralsnog niks mee), AR-NU, DVS, binnenkort mogelijk OV-fiets)
* RDT service
* RDT-serviceinfo
* OV-fiets API
* Telegram bot

&copy; 2018 OVDingen. Op dit document kunnen geen rechten worden ontleend.
