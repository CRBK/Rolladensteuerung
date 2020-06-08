# Rollladensteuerung – M. Arldt, H. Wittkopp
## Projektbeschreibung
Über die Rollladensteuerung soll ein elektrischer Rollladen von Hand (3 Taster: AUF, AB und STOPP) oder per Automatik (Zufahren bei Wind oder Dämmerung, Auffahren bei Windstille und Tageslicht) gesteuert werden. 
Die Hand/Automatik - Umschaltung erfolgt über einen Betriebsartenwahlschalter.  
Der aktuelle Status wird durch LEDs visualisiert.(„Fährt auf“ grüne LED P3, „fährt zu“ grüne LED P4, „Windwarnung“ rote LED P1, „Dämmerung“ gelbe LED P2) 
Über 2 Potentiometer lassen sich die Schaltschwellen für den Windsensor sowie den Dämmerungsschalter einstellen.
Wie lange die Windwarnung sowie der Dämmerungsschalter aktiv/inaktiv sein muss bis eine Reaktion (Rollladen auf oder ab) erfolgt, lässt sich über in Variablen hinterlegten Sollwerten vorgeben.
Alle Analogwerte sowie die Betriebsart werden bei Werteänderung über den seriellen Monitor ausgegeben. 
Ebenso erfolgt eine Klartextausgabe über den seriellen Monitor, wenn er Taster betätigt wurde, in welche Richtung der Rollladen gerade fährt und ob er oben oder unten ist.
## Funktionen/2do
* Motor auf/ab (Software unproblematisch, Hardware: Sicherheit 230V Antrieb einschl. Störsicherheit)
* Windsensor auswerten (Analogwertverarbeitung)
* Dämmerungsschalter auswerten (Analogwertverarbeitung)
* Rückmeldungen per LEDs geben (Programmlogik)
* Taster AUF/STOPP/AB auswerten (Programmlogik)
* Schalter Hand/Automatik auswerten (Programmlogik)
* Schaltschwelle für Windsensor per Potentiometer vorgeben (Analogwertverarbeitung)
* Schaltschwelle für Dämmerungsschalter per Potentiometer vorgeben (Analogwertverarbeitung)
* Rückmeldung der Analogwerte Windgeschwindigkeit (DW und m/s), Helligkeit (DW und %), Sollwertvorgaben (DW und %), Tasterbetätigungen,   Betriebsart und Endlage des Rollladens über den seriellen Monitor (Programmlogik)

## Aufbau

![Aufbau](https://github.com/CRBK/Rolladensteuerung/blob/master/Bilder%20TinkerCad/mit_bez.PNG?raw=true)

## Beispielausgabe des seriellen Monitors

![Ausgabe](https://github.com/CRBK/Rolladensteuerung/blob/master/Bilder%20TinkerCad/Ausgabe.PNG?raw=true)

## Schaltplan
Der Schaltplan zu dem Projekt ist [hier](https://github.com/CRBK/Rolladensteuerung/blob/master/Schaltplan.pdf) zu finden.

## Komponentenliste
* Arduino
* Taster
   * Auf 
   * Zu
   * Stop
* Wahlschalter Hand/ Automatik
* LED´s 
   * Rot  P1 (Windwarnung)
   * Gelb P2 (Dämmerung)
   * Grün P3 (Auffahrt)
   * Grün P4 (Zufahrt)
* Poti´s
   * Sollwertvorgabe Wind
   * Sollwertvorgabe Dämmerung
* Windsensor - https://www.amazon.de/Eltako-Windsensor-WS/dp/B0018LBFG8 (simuliert mit Poti)
* LDR
* 2 stk. Relais zur Motoransteuerung 
(https://eckstein-shop.de/5V-220V-2-Channel-Optocouplers-Relay-Shield-for-Arduino-Optokoppler-Relais-Modul?gclid=CjwKCAjwhOD0BRAQEiwAK7JHmDFOuYZx6fTf-5ashzG0MYxnc3YtHgYE7g4iQayORHhfT-ZqGMiXcxoCtKoQAvD_BwE)
Alternative:
https://www.conrad.de/de/p/weidmueller-optokopplerrelais-tos-5vdc-48vdc-0-5a-last-strom-max-0-5-a-schaltspannung-max-48-v-dc-1-st-506843.html


## Programm

[Aktueller Programmstand](https://github.com/CRBK/Rollladensteuerung/blob/master/Programm/Rollladensteuerung)

## Videbeschreibung

Eine kurzes Video zur Simulation des Projektes in Tinkercad befindet sich [hier](https://github.com/CRBK/Rolladensteuerung/blob/master/Video%20TinkerCad/Rollladensteuerung.mp4).
