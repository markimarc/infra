#Technisch ontwerp OVDingen

##Server nummering
De servers zijn onderverdeeld in nummers. Iedere server begint met de aanduiding OV, gevolgd door een 2 cijferig getal. Het getal is altijd opvolgend.

##Server OS
Alle servers van OVDingen draaien op Debian 9.

##Server indeling
Om de belasting van de servers te verkleinen, is ervoor gekozen om verschillende diensten te versprijden over meerdere servers. De indeling van de servers is als volgt:

###OV01

* Webserver (NGINX) ovdingen.nl
* Mailserver
* Treinviewer
* RDT API frontent

###OV02

* Universal
* RDT service

Op dit document kunnen geen rechten worden ontleend.
&copy; 2018 OVDingen.