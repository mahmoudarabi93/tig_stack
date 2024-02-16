Westsächsische Hochschule Zwickau | Smart City Zwönitz
Softwareprojekt im Master: IoT-Stack zur Hochwassererkennung

## ÜBERSICHT

Das Projekt ist im Umfeld von Smart City Zwönitz (https://smartcity-zwoenitz.de/, https://smartcity-zwoenitz.de/smarte-buerger/, https://smartcity-zwoenitz.de/smarte-umwelt/) angesiedelt.

Ziel ist die Erstellung eines Internet of Things(IoT)-Stacks (Software und Hardware) für kleine und mittelgroße Kommunen auf Basis von Open-Source-Software und offenen Standards.

Die Entwicklung des Projektes und das Erreichen des oben genannten Ziels erfolgt anhand eines konkreten Anwendungsfalls: Der Hochwassererkennung im Zwönitzer Ortsteil Dorfchemnitz (https://goo.gl/maps/Mj6zW56pD3JKs9N39), durch den der Fluss Zwönitz fließt. Dabei soll nicht zur der Fluss Zwönitz analysiert werden, sondern auch kleine Fließgewässer, die in den Fluss münden. Denkbar ist auch die Nutzung von Regensensoren in verschiedenen Teilbereichen des Stadtgebiets, um eine Zuordnung von Regenmengen zu Pegelständen zu ermöglichen.

## ZIELE

1.  Plattform (Hard- und Software), die auch Nicht-Informatiker (bzw. Systemadministratoren in einer kleinen Stadtverwaltung) installieren, konfigurieren, betreiben und erweitern können
2. Aufwandsarme, möglichst automatisierte Einbindung von LoRa-Sensorik zum Hochwassermanagement
3. Erweiterbare, offene (nicht proprietäre) Architektur, die dennoch einfach bedienbar ist; 
   1. Hinweis: Möglichst ohne Verwendung von AWS oder ähnlichen (Cloud-)Plattformen (Grund: hohe Kosten, Vendor Lock-In)
   2. Hosting/Betrieb sollte “on premise” oder auf “einfacher” Miet-Server-Hardware erfolgen können

## ERGEBNISSE

1. Tutorial zum Deployment & Git-Repository mit Konfigurationsartefakten für Set-Up
2. Architekturbeschreibung (inkl. ADRs)
   1. Plug&Play-Ansatz für Sensorik
3. optional: Wie kann aus diesem Ansatz ein “Citizen Science”-Szenario entstehen?

## AKTIVITÄTEN

### Projekteinstieg (insbesondere für die 1–3 Semesterwoche)
Auseinandersetzen mit folgenden Technologien/Themen:
* IoT in der Smart City
* LoRaWAN kennenlernen
   * Auseinandersetzung mit Funktechnologien
   * physische Grundlagen verschiedener Technologien
   * Welche Bedeutung hat LoRaWAN für den Einsatz in Kommunen?
   * Welche Vor- und Nachteile bietet LoRaWAN im Vergleich zu anderen Technologien? (z. B. 5G)
   * anhand des Beispiels Dorfchemnitz:
      * Abdeckung & Positionierung[a][b] von LoRaWAN-Gateways
         * Einbeziehen der Positionen kommunaler Gebäude, da wir dort unproblematischer Gateways platzieren werden können. Möglicherweiser Gegenüberstellung idealer Platzierung versus Platzierung auf dem am besten geeigneten komm. Gebäude.
      * Sichtanalyse, Ausleuchtungsplanung
      * Welche geografischen Gegebenheiten sind zu beachten?
   * Welche Sensoren wären für Messung geeignet
      * Hinweis: Die Projektpartner von Smart City Zwönitz besitzen bereits Ultraschallsensoren, die zur Verfügung gestellt werden können
* Open-Source-Stacks für LoRaWAN
   * Vor- und Nachteile des Betriebs über TheThingsNetwork
   * Self-hosted LoRa-Backend mit Fokus auf https://www.chirpstack.io/[c][d][e][f] 

### Kickoff

* Was:
   * Kennenlernen der Projektbeteiligten (Projektpartner von Smart City Zwönitz um Dr. Martin Benedict und sein Team)
   * Diskussion der Ziele und Anforderungen
* Wann und Wo: 19.10., 15:20 in Raum PKB370

## MEILENSTEINE

### Meilenstein 1
* Vorstellung für Betriebskonzept (Aufbau Softwarestack) und Konzept für Positionierung von Gateways und Sensoren

### Meilenstein 2
* Gateway(s) plus Sensorik in Dorfchemnitz in Betrieb nehmen

### Meilenstein 3
* Ergebnispräsentation
[a]Eventuell sollten wir hier noch die Positionen kommunaler Gebäude mit einbeziehen, da wir dort unproblematischer die Gateways platzieren können. Möglicherweiser Gegenüberstellung idealer Platzierung versus Platzierung auf dem am besten geeigneten komm. Gebäude?
- Martin W.
[b]Danke für den Vorschlag. Habe ich mit aufgenommen.
[c]Wollen wir perspektivisch vom TheThingsNetwork weg? Hat Vor- und Nachteile. Vorteil: Man kann eigene Infrastruktur aufbauen und ist unabhängiger von dritten. Nachteil: Man hat nicht so ein global angeschlossenes Netzwerk wie bei TTN, welches auch dritten einen einfachen Zugang über die kommunalen Gateways ermöglicht.
- Martin W.
[d]Chirp Stack hatte Martin B. in den Ring geworfen — und ich folglich hier mit aufgeführt.
Ich möchte euren TTN-Ansatz natürlich nicht infrage stellen. Durch TTN erziehlt man ja auch eine gewisse Sichtbarkeit.
[e]Ich habe mal dazugefügt, dass die Studis sich auch mal die Vor- und Nachteile von TTN anschauen. Mein Gedanke beim Thema Chirpstack war, dass man als Kommune damit unabhängig von einem zentralen Player ist, mit dem man kein definiertes SLA hat. Man könnte auch über TheThingsIndustries nachdenken, aber ich finde damit die Studenten schnell zu einem eigenen Stack kommen, würde ich nicht zu viele Abhängigkeiten zur Drittanbietern etc. schaffen.
[f]Wunderbar, danke.
