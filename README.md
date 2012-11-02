HQ WebUI 1.1.1
==============
Alternatives leichtgewichtiges und schnelles WebUI zur Bedienung der Homematic CCU.

Mit diesem WebUI k�nnen Variablen und Datenpunkte angezeigt und ge�ndert werden, Programme k�nnen gestartet werden und das Systemprotokoll kann angezeigt und gel�scht werden. Ger�te-Konfiguration u.Ä. ist nicht vorgesehen. Achtung: Wie bei XML-API Anwendungen �blich findet keine Authentifizierung statt, das HQ WebUI ist also ohne Login erreichbar.

Ben�tigt eine modifizierte Version der XML API (mindestens Version 1.2-hq4) - zu finden hier: https://github.com/hobbyquaker/hq-xmlapi

Baut auf jQuery UI auf - d.h. die Optik ist �ber jQuery UI Themes einfach anpassbar. Hier kann man sich eigene Themes "zusammenklicken": http://jqueryui.com/themeroller/

Screenshots gibt es hier: https://github.com/hobbyquaker/hq-webui/tree/master/screenshots

Siehe auch diesen Foren-Thread: http://homematic-forum.de/forum/viewtopic.php?f=31&t=10559

Installation
============
Dateien irgendwo ablegen (kann auf einem beliebigen Webserver sein, kann auf der CCU (z.B. in /www/config/hq-webui/) sein, kann aber auch einfach lokal benutzt werden).
In der Datei "hq-webui.js" (zu finden im Unterordner "js") die URL der CCU anpassen. Wird das HQ WebUI auf der CCU installiert diese Variable leer lassen (auf "" setzen), anderenfalls auf "http://IP-Adresse-der-CCU" (also z.B. "http://192.168.1.20") setzen. Nun einfach die index.html im Browser aufrufen.



Changelog
=========

1.1.1
-----
* Fixed encoding
* Added CDN for jQuery and jQuery UI

1.1
---
* Beim ersten Laden der Seite werden die einzelnen CGI f�r die "Erstbef�llung" der Grids eines nach dem anderen geladen.
* jqGrid Pager und Auswahl wieviele Eintr�ge angezeigt werden hinzugef�gt
* jqGrid Toolbar-Suche / Filter hinzugef�gt
* jqGrid sortable aktiviert - Spalten k�nnen jetzt per Drag&Drop umsortiert werden
* Tab Ger�te entfernt, Tab Status in Ger�te umbenannt


Todo
====
* Timestamp formatieren!
* Autorefresh? xmlapi update.cgi nutzen?
* Mehr Variablentypen notwendig?
* Select/Option bei Datenpunkt edit bool/value_list?
* Favoriten anzeigen, mit sch�nen Selektoren und jQuery UI Slider f�r Float Werte
* R�ume und Gewerke in Ger�teliste!
* in Ger�teliste auf Unter-Listen verzichten - nur Datenpunkte anzeigen - und stattdessen Ger�te- und Kanal-Infos als zus�tzliche Spalten?
* F�r Installation auf CCU .img File und Pack-Script erstellen (minifier einsetzen, jQuery evtl von CDN einbinden?)
* Step-by-Step Anleitung zum einbinden anderer Themes und Hinweise zu sonstigen Customizing zusammenschreiben
* Neuer Tab Servicemeldungen
* Neuer Tab Signalqualit�t (xmlapi rssilist.cgi)
* Buttons wegmachen und jqGrid Toolbar nutzen?
* automatisches Anpassen der Grids an Fenstergr�ߟe
* Auth?