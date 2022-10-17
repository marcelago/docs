# Netzwerke
# Nromung und Modelle
## Gremien
### Institute of Electrical and Electronics Engineers (IEEE)
Die IEEE ist zuständig für Standardisierung im raum Elektrotechnik. Dies beinhaltet Networking, Data Transfer und Wireless Data Networks.

|Nummer|Beschreibung|Status|
|:-----|:-----------|:----:|
|802.1|Internetworking|aktiv|
|802.2|Logical Link Control (LLC) -Teilschicht|inaktiv|
|802.3|CSMA/CD, Ethernet|aktiv|
|802.10|Netzwerksicherheit|aufgeöst|
|802.11|Drahtlose Netzwerke|aktiv|
|802.12|Demand Priority Access, 100VG AnyLAN|inaktiv|
|802.15|Wireless Personal Area Network (WPAN)|aktiv|
|802.16|Broadband Wireless Access Working Group|aktiv|
|802.17|Resilient Packet Ring Working Group|aktiv|
|802.18|Radio Regulatory TAG|aktiv|
|802.19|Coexistance TAG|aktiv|
|802.20|Mobile Broadband Wireless Access (MBWA), drahtlose Breitbandnetz|aktiv|
|802.21|Media Independent Handoff Working Group|aktiv|
|802.22|Wireless Regional Area Networks, drahtlose Regionalnetze|aktiv|

### International Organization for Standardization (ISO)
ISO ist eine Dachorganisation von 163 nationalen Normungsausschüssen, darunter die ANSI (American National Standards Institute) und DIN (Deutsches Institut für Normung). Die ISO ist selber aber auch teile der ITU-T.

Die Aufgaben der ISO ist Nationale Standards zu globalisieren und mit andern zu vereinen. Zum Beispiel ASCII (American Standard Code for Information Interchange) welche von der ANSI entwickelt und der ISO unterm Namen ISO-9000 Globalisierte wurde.

### Internet Corporation for Assigned Names and Numbers (ICANN)
Sie ist primär zuständig für die vergabe von Top-Level Domains wie z.B. de, com, org und IP-Adressen im Internet. Sie deferieren auch die Strukturen für dienst DNS. Die aufgaben von Verteilung von IP-Adressen haben einer Unterorganisierung weiter gegeben Namens IANA.

## OSI-Modell

### Wichtige theoretische Grundlage
Das Open-System-Interconnection-Modell, ermöglicht den komplexen Ablauf bei der Übermittlung von Daten zwischen zwei Systemen logisch aufzuteilen. Der Blick auf das Netzwerk wird vereinfacht. Zudem bezieht sich jede Definition eines Netzwerkdienstes auf das OSI-Schichten-Modell bzw. auf das TCP/IP-Referenzmodell, welches ein noch weiter vereinfachtes Modell darstellt.

### Herleitung und Übersicht
Um die Datenkommunikation in offenen System zu beschreiben, entwickelte die ISO 1977 ein abstraktes, logisch-funktionelles Architekturmodell, mit der Zielsetzung einen einheitlichen Standard zu schaffen. Erstmalig veröffentlicht wurde das Modell ISO 7498 1978. Später, 1978, wurde die heutige und somit überarbeitete Version unter dem Namen OSI-Modell veröffentlicht.

### Überblick über das OSI-Referenz-Modell
Die gesamte Netzwerkkomunikation wird in ein Modell aus sieben Schichten eingeteilt. Die folgende Tabelle gibt, von oben nach unten, einen Überblick über die englischen und deutschen Bezeichnungen der einzelnen Schichten sowie eine kurze Beschreibeng der jeweiligen Aufgabe.

**Image Space**

Wie funktioniert das OSI-Modell? à Wenn man beispielsweise eine E-Mail versendet, durchläuft diese alle sieben OSI-Schichten, bis zum Empfänger.
****
**Eine gute Erklärung des OSI-Modells findet ihr unter folgendem Link:** 
https://www.youtube.com/watch?v=_kDogzR0-4Q
****
**Gehen wir einmal weiter auf die einzelnen Protokolle ein:**
Im TCP/IP Schichten-Modell wird zwischen Application-, Transport-, Internet- und Netzwork Access Layer unterschieden. Im Application Layer gibt es Protokolle wie SMTP was z.B Emails empfängt.
****
**Unterschiede zwischen TCP und UDP:**<br>
​​​​​​*Wichtig zu Wissen:*<br>
Im OSI-Modell entspricht jede Schicht einer genau definierten Funktion. Zudem soll zwischen den Schichten der Informationsfluss so gering wie möglich sein. Außerdem kann eine Schicht nur mit der darüber oder darunterliegenden Schicht kommunizieren. Die Anzahl der Schichten soll dennoch so gering wie möglich sein, da neue Schichten einen neuen und höheren Abstraktionsgrad darstellen.
****
**Vorteile des OSI-Modells:**<br>
Der wichtigste Vorteil ist, dass das Verfahren innerhalb einer Schicht durch ein anderes ausgetauscht oder ergänzt werden kann, ohne dass Änderungen auf anderen Schichten vorgenommen werden müssen.

*Header*<br>
Beim Weitergeben stellt jede involvierte Schicht des Senders (mit Ausnahme von Schicht 1) den erhaltenen Daten einen Header voran, der von der entsprechenden Schicht auf der Seite des Empfängers interpretiert und wieder entfernt wird. Der Header die vom Kommunikationspartner in der jeweiligen Schicht wichtigen Steuerinformationen und stellt den wichtigen Teil der virtuellen Kommunikation zwischen den Instanzen gleicher Schichten her.

### 1. Physical Layer (Bitübertragende-Schicht)
Der Physical Layer meint alles, was für die Übertragung (Senden-Empfangen) einzelner Datenbits über ein Medium notwendig ist.

Dazu werden im mechanischen Teil die physikalischen Eigenschaften des Interface zu einem Übertragungsmedium (z. B. Steckergeometrie, Pinbelegung) bestimmt.

Der elektrische bzw. optische Bereich wiedergibt, wie die Datenbits auf dem Medium dargestellt werden. Daraus ergibt sich eine maximal erreichbare Datenübertragungsrate.

Die funktionalen Bestimmungen befassen sich mit dem Aufbau von Verbindungen, wie z. B. der Unterscheidung zwischen Datenleitung – Steuerungsleitung oder Taktgebung.

Die verfahrenstechnischen Bestimmungen definieren u. a. den Übertragungsmodus (Halb-, Vollduplex).

### 2. Data Link Layer (Sicherungs-/Datenverbindungs-Schicht)
Der Data Link Layer wandelt die Daten des Network Layers in Frames (Daten[1]rahmen unterschiedlicher Größe) oder Zellen (Datenrahmen fester Größe) um und reicht sie an die Bitübertragungs-Schicht weiter und auch umgekehrt.

Zu den Aufgaben gehört ebenfalls das Zerlegen von Frames in Bits für die Übertragungs-Schicht und das Zusammensetzen der Bits. Der Data Link Layer verbindet somit zwei an ein gemeinsames Medium angeschlossene Teilschichten (Network Layer/Physical Layer).

Ein Frame besteht bei Ethernet aus einem Header (den Adressen von Empfänger und Sender sowie Steuerinformationen), den Daten sowie einem angehängten Trailer. Ebenfalls darin ent[1]halten ist die Frame Check Sequence (FCS), um zu erkennen, ob die Daten fehlerfrei übertragen wurden. Für die Berechnung der Frame Checksum wird in der Regel ein Cyclic Redundancy Check (CRC) Algorithmus verwendet.

### 3. Network Layer (Vermittlungs-/Netzwerk-Schicht)
Die als besagte Schicht ist für die Wegfindung (Routing) der Pakete über verschiedene Netzwerkknoten. Andere Aufgaben sind die Kontrolle der Pakete und schließlich der Transport der Pakete zu den Zielknoten (Messages Forwarding). Auf Layer 3 finden sich auch wichtige Protokolle für die Wegefindung (Internet Protocol Version 4 und 6 (IPv4/IPv6)) und Statusmitteilungen (Internet Control Message Protocol (ICMP/ICMPv6)).

### 4. Transport Layer (Transport-Schicht)
Der Transport Layer realisiert eine verbindung von Endsystemen über eine transparente Verbindung (Ende-zu-Ende-Kommunikation). Weitere Aufgaben sind die Teilung des Datenstroms, die Anregung des erneuten Sendens von fehlenden Datensegmenten, falls keine Empfangsbestätigung vom Empfänger eintrifft (bei Verwendung des Transmission Control Protocols (TCP)) und die Überwachung der Netzlast (Congestion Control) zwischen den benachbarten Netzknoten. Die Transport-Schicht vermittelt den darüber liegenden, Anwendung-Schichten und den darunterliegenden, transportorientierten Schichten.

### 5. Session Layer (Kommunikationssteuerungs-/Sitzungs-Schicht)
Im OSI-Kommunikationsmodell verwaltet die Sitzungsschicht (Session oder manchmal auch Port Layer genannt) den Auf- und Abbau der Verbindung zwischen kommunizierenden Endgeräten. Eine Verbindung wird aufrechterhalten, während sich die beiden Endpunkte miteinander unterhalten. 

### 6. Präsentation Layer (Darstellungs-/Präsentations-Schicht)
Der Präsentation Layer wandelt die Daten in ein allgemeines, vereinbartes und für die beteiligten Computer verständliches Standardformat (Abstract Syntax Notation One (ASN.1)) um. Dies ist notwendig, da sich die innere Darstellung von Daten (z. B. in den Zeichencodes ASCII, ANSI, EBCDIC) je nach eingesetztem System unterscheidet. Sie komprimieren Daten und kodieren.

### 7. Application Layer (Anwendungs-Schicht)
Der Application Layer erstellt die Schnittstelle zwischen den Anwendungen (Programmen) und dem darunterliegenden Netzwerk. Zu diesem Zweck stehen den Anwendungen diverse Protokolle zur Verfügung. Zwei der bekanntesten sind das Hypertext Transfer Protocol (HTTP) und das Simple Mail Transfer Protocol (SMTP).

## Frames Der Aufbau eines Ethernet-V2-Rahmens (nach IEEE 802.3)
Grundsätzlich werden größere Datenmengen nicht in einem Stück verschickt, da es zeitweise den Netzwerk-Zugriff für alle anderen Teilnehmer sperren kann. Um dieses Problem zu vermeiden, werden größere Datenmengen in kleinere Einheiten, sogenannte Frames, Rahmen oder Datagramme, zerlegt. Mehrere Benutzer können abwechselnd Rahmen verschicken, wodurch ein nahezu zeitgleicher Netzwerkzugriff möglich wird.

Bei der Konfiguration eines Netzinterfaces kann eine sogenannte Maximum Transmission Unit (MTU) angegeben werden. Sie definiert die maximale Größe eines Datagramms. Daten, die diese Länge überschreiten, werden immer in mehrere Frames aufgeteilt und danach über das Netzwerk versendet.

Um sicheren Datenverkehr zu gewährleisten, müssen die Daten mit entsprechenden Informationen versehen werden. Der Aufbau eines Rahmens nach IEEE 802.3 ist dabei immer:
<br><br><br>
Ein Ethernet-V2-Rahmen hat, ohne VLAN-Tag, eine Rahmengröße zwischen 64 und 1518 Bytes und folgenden Aufbau:
- Die Präambel enthält ein Bitmuster, das es den Netzwerkkarten ermöglicht, ihre Empfangs- Elektronik zu synchronisieren. Sie endet mit dem sogenannten Start Frame Delimiter (SFD), der den Beginn des eigentlichen Frames anzeigt.
- Als Ziel- und Ursprungs-Adresse werden die MAC-Adressen der beteiligten Netzwerk- Schnittstellen eingetragen.
- Im Typ-Feld wird die Art des darüber liegenden Protokolls angegeben, zum Beispiel ob es für IPv4 oder IPv6 bestimmt ist.
- Der Daten-Teil hat eine Größe zwischen 46 und 1500 Bytes.
- Als Frame-Kontroll-Sequenz (FCS) wird ein CRC-Algorithmus eingesetzt. Anhand der FCS kann erkannt werden, ob der Rahmen korrekt übertragen wurde.
- Wenn ein Netzwerk über einen oder mehrere Switche in virtuelle Netzwerke aufgeteilt ist, erhält jeder Frame im Datenteil, zur Identifizierung der VLANs, zusätzlich ein 4 Byte großes Feld, das VLAN-Tag
- ein Frame zu groß, erhält der Absender eine Fehlermeldung per ICMPv6, damit er die MTU reduziert

Es existieren neben dem Ethernet-V2 noch andere Frame Definitionen, die veraltet sind. Ethernet-V2 besitzt kein Längenfeld, dafür ein Typfeld mit Informationen über das Protokoll der Nutzdaten im Datenteil.

# Netzwerkkomponenten
## Übersicht
Die Verschiedenen Komponenten können nach dem OSI-Modell verschiedenen Schichten zugeordnet werden. Mit den Schichten steigt auch die Komplexität dieser Geräte.

## Repeater und Hub (Schicht 1)
*Repeater:* Verstärkt ein Signal (drahtlos oder kabelgebunden), sodass eine Längenbeschränkung eines Mediums erweitert werden kann. Bei Umwandlung eines Signals von drahtlos zu kabelgebunden oder umgekehrt nennt man diesen auch Medienkonverter.

*Hub:* Stellt mehr Ports zur Verfügung, allerdings handelt es sich um eine Bus-Topologie, und somit ein Shared Medium. Zu Lastspitzen wird die Bandbreite also stark ausgebremst, was ein Grund für die Ablösung von Hubs durch Switches ist.

*OSI-Einordnung:* Beide Komponenten arbeiten auf Schicht 1, d.h. sie regenerieren ausschließlich Bits, sie haben keinerlei Einblick in den Inhalt.

## Bridge (Schicht 2)
Verbindet lokale Netzwerksegmente über zwei Ports miteinander und nutzt dabei MAC-Adressen, die bei "Learning Bridges" für effizienteren Datenverkehr gespeichert werden

## Switch (Schicht 2)
### Definition
Ein Switch bringt alle Vorteile eines Multiport-Bridge auf mehrere Ports. Des weiteren läuft es auch auf Schicht 2 des OSI-Modells. Durch das Schalten von Verbindungen ist es für miteinander kommunizieren von Geräten wie eine direkt Verbindung.
Per Kaskadierung lässt sich mit Switch eine Vergrößerung der Gesamtportanzahl ermöglichen. Das verursacht einen Flaschenhals für Datenverkehr und die Latenzzeit erhöhen sich. Dieses Problem wird mit Stacking gelöst. Vor allem bei einer Kaskadierung können sehr viele Geräte miteinander verbunden sein, daher verfügen bereits Desktop-Switches über internen Speicherplatz für 1000 und mehr MAC-Adressen

Es gibt zwei Sorten an Switches.<br>
**Managed Switches**<br>
Die meist per Webinterface Konfiguriert werden können.<br>
**Desktop Switches**<br>
Sie sind meistens ungemanaged und daher nicht Konfigurierbar, aber dafür sofort einsetzbar. 
### Arbeitsweise