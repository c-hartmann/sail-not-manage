# sail!manage

"sail! not manage" (vorläufiger Projektname)

nachfolgend 's!m'

## Projektbeschreibung

Version: 0.1.1, 2022-03-31

this document living: https://github.com/c-hartmann/sail-manage

## Abstract

Eine browserbasierte Sportart unabhängige Open Source Software zur Vorbereitung (Meldung), Begleitung (Kommunikation und Veröffentlichungen) und insbesondere Ergebnisermittlung (Auswertung) von Sportwettkämpfen im Amateursportbereich.


## Das Projekt

Zielvorgabe des Projektes ist ein direkt einsatzfähiger Prototyp der oben genannten Software und insbesondere dabei der belastbare Entwurf einer erweiterbaren Architektur, sowie deren vollständige "Use Case" (Nutzung, Entwicklung) orientierte Dokumentation. Der Sportart spezifische Teil wird durch eine Referenzimplementierung "Segeln" realisiert. Dieser umfasst wenigstens alle in Deutschland relevanten Auswertesysteme.


## Umfeld

Allein im deutschen Amateursport sind 27.000.000 Amateursportler organisiert. Hier gehen wir von einer Wettkampfquote von 10% aus. Alle diese Wettkämpfe bedürfen einer Auswertung der Leistungen, also i.d.R. die Ermittlung einer Rangfolge. Dies gilt für alle Sportarten, seien es Einzel- oder Mannschaftsteilnehmer.


## Umfeldanalyse

Ein überdurchschnittlich weit verbreitetes Modell von Software zu diesem Zweck lässt sich wie folgt beschreiben:

* Proprietär (kein Open Source)
* Sportartspezifisch
* überwiegend Plattform gebunden (90% MS Windows)
* Fat Clients (webbasiert selten)
* "in die Jahre gekommen"
* kaum oder gar nicht vorhandene Erweiterbarkeit (Module)
* Monolytische Architektur
* Einzelentwickler (oft mit direktem Bezug zur Sportart)
* Keine Internationalisierung
* Nutzung nur durch Veranstalter

s!m soll sich hingegen auszeichnen durch:

* Open Source (unwiderruflich)
* basiert auf verbreiteten Programmiersprachen
* Erweiterbarkeit
* API
* i10n
* Primär browserbasiert
* Nutzung durch Veranstalter und Teilnehmer


## Umfeldanalyse (exemplarisch)

Als Beispiele im Umfeld (am Beispiel Segelsport) seien genannt:

Kennzahlen, Technologie, Klasse, Kosten

### Manage2Sail

* Zielgruppe: nur Segeln, Veranstalter und Teilnehmer
* Software Klasse: Web
* Technologie:
* Hersteller: DSV (u.A.)
* Kosten: anfänglich Jahresgebühr, mittlerweile kostenfrei
* Open Source: nein
* Erste Version: vor 2019
* Letzte Version: leidlich aktuell, Entwicklung schleppend
* Link: https://www.manage2sail.com

### raceoffice.org

* Zielgruppe: nur Segeln, Veranstalter und Teilnehmer
* Software Klasse: Web
* Technologie:
* Hersteller: Guido
* Kosten: keine
* Open Source: nein
* Erste Version: 2007
* Letzte Version: kontinuierliche Pflege, seit Jahren keine neuen Features
* Link: https://raceoffice.org

### Velum Regatta

* Zielgruppe: nur Segeln, nur Veranstalter
* Software Klasse: Fat Client, Windows 95 (inkl. Win 10) (sic)
* Technologie: ?
* Hersteller: Markus Wegmann
* Kosten: 36 bzw. 54 Euro (max. für vier Jahre)
* Open Source: nein
* Erste Version: vor 2000
* Letzte Version: 2022
* Link: https://www.velumng.com

### JavaScore

* Zielgruppe: nur Segeln, nur Veranstalter
* Software Klasse: Fat Client
* Technologie: Java
* Plattform: Windows, MacOS, Linux
* Hersteller:
* Kosten: keine (Open Source)
* Weiteres: US-lastig
* Open Source: ja
* Erste Version: vo 2000
* Letzte Version: September 2017
* Link: http://www.gromurph.org/javascore

### WinRegatta

* Zielgruppe: nur Segeln, nur Veranstalter
* Software Klasse: Fat Client
* Technologie:
* Plattform: Windows
* Hersteller: Günter Meissner
* Kosten: 95 Euro einmalig (Updates kostenfrei)
* Weiteres:
* Open Source: nein
* Erste Version: April 2001
* Letzte Version: Juli 2021
* Link: https://www.winregatta.de


## Umfeldanalyse (Allgemein)

### PLAYINGA

Es gibt eine offenkundig kommerzielle Plattform "PLAYINGA", deren Urspung in Indien zu liegen scheint. Nach Eigenaussage eine "Software zum Online Sportmanagement zum Erstellen und Verwalten von Turnieren". Eine Auswertung, wie sie für s!m angedacht ist, scheint hiermit nicht möglich zu sein. Die grafischen Darstellungen von Turnieren sind ansprechend und können durchaus als Vorbild dienen. Die Aufbereitung für den deutschen Markt ist ebenso offenkundig nicht ausgereift ("Streichhölzer" anstatt "Matches", "Fahrkarte" anstatt (Help Desk) "Ticket").

* Zielgruppe: Turniersportarten, Veranstalter und Teilnehmer
* Software Klasse: SaaS
* Technologie: ?
* Hersteller: SKYBIS
* Kosten: keine
* Open Source: nein
* Erste Version:
* Letzte Version: 2022
* Link: https://playinga.com

### WMTurnier

WMTurnier ist eine seit 1999 entwickelte aus Deutschland stammende Software zur Verwaltung von Turnieren.

* Zielgruppe: Turniersportarten, Veranstalter und Teilnehmer (?)
* Software Klasse: Fat Client, Windows (only)
* Technologie: ?
* Hersteller: Peter Wode
* Kosten: 99 Euro (lifetime)
* Open Source: nein
* Erste Version: 1999
* Letzte Version: 2017
* Link: https://www.turniermanager.de

### SPORT Software - Turnier Manager

* Zielgruppe: Turniersportarten, Veranstalter und Teilnehmer (eingeschränkt)
* Software Klasse: Fat Client, Windows (only), Android
* Technologie: ?
* Hersteller: Ottmar Krämer-Fuhrmann
* Kosten: 80 Euro (Updates 40)
* Open Source: nein
* Erste Version:
* Letzte Version: 2021
* Link:


## Abgrenzung

s!m (Core) soll nicht:

* Alle möglichen denkbaren organisatorischen Aufgaben eines Wettkampfs unterstützen.
* Keine Vereins- oder Mitgliederverwaltug sein


## Sportart übergreifend / Module

Die Kriterien für die Auswertung lassen sich in wenige und überschaubare "Modelle" differenzieren: Ligen, zusammenlegen von Gruppenwertungen, Turnier orientierte wie Tennis und Fussball und - vor Allem - Mischformen. Zeitliche Strukturierung und Organisation dürften für alle zutreffen.

Spezifische Algorythmen zur Auswertung können sehr anspruchsvoll sein und werden deshalb in "Modulen" realisiert. Neben der Basisaufgabe Auswertung steuern diese Module auch Ablauf eines Wettkampfs, z.B. durch Zwischenergebnisse

### Sub-Module

Sportartspezifische aber z.B. ländespezifische Aspekte (insbesondere) bei der Auswertung werden in Sub-Modulen realisiert. Auch hier gilt das Prinzip für die Nutzbarkeit: "Nicht mehr als nötig".


## Erweiterbarkeit / Extensions

s!m (Core) soll aber erweiterbar sein. Als Beispiele seien hier genannt:

* Benachrichtigungen von Teilnehmern (SMS; Messenger Dienste)
* Druck von Urkunden
* Statistik
* Fair Play Wertungen
* Zahlungen von Startgeldern (PayPal u.A.)
* Einreichen von Dokumenten durch Teilnehmer (z.B. Proteste, Anträge jeder Art)
  (im Upload oder direkte Formulare)
* Booking (Unterkünfte, Park- und Stellplätze)


Gemeinsames Merkmal der Erweiterungen ist, dass sie im Gegensatz zu Modulen prinzipiell unabhängig von einer Sportart sind.

(nicht Teil der Zielvorgabe im Rahmen des Projektantrages)


## Technische Umsetzung

Mit Blick auf zukünftige Beteiligung Dritter ist die Verwendung von einfachen, gut gepflegten und leicht verfügbaren Werkzeugen elementar.

Die Einstiegshürden für die Mitarbeit Dritter muss so niedrig wie möglich sein.

s!m ist ein browserbasiertes Werkzeug und wird aus den oben genannten Gründen mit PHP (CakePHP als Framework) und JavaScript (oder Derivate wie TypeScript) entwickelt.

Um eine nahtlose Integration in vorhandenen Vereins-Webseiten zu ermöglichen, soll schon zum Ende des ersten Projektzeitraums ein WordPress Plugin mit einem Auszug der Funktionalitäten (insbesondere Meldung und Dokumente) zur Verfügung stehen. Dieses lässt sich sowohl eine SaaS Lösung der Cloud, als auch an eine selbst-gehostete Implementierung anbinden.

Auf Basis der verwendeten Werkzeuge wird von Anfang an eine (REST) API entstehen.

Der Antragsteller verfügt über professionelle praktische Erfahrung in der Realisierung und dem Design sowie Umsetzung verschiedener REST basierter APIs.

Desweiteren hat er ein mittelgroßes Projekt auf Basis von CakePHP in ca. drei Monaten realisiert. (Vorstellung nur vertraulich)


### User Interface

Die Gestaltung der Benutzeroberfläche orientiert sich am Gedanken:

* Einfach und nur notwendige Elemente zu Beginn
* weitere speziellere Elemente erst auf Anforderung
* Expert Modus wenn erforderlich


### i10n

s!m wird von Anfang an internationalisiert entwickelt. Zunächst in Englisch (intern) und Deutsch. Realisierung: gettext.


## Zielpersonen, Nutzer (Use Cases)

### "Niklas"

Hat keinen Plan von gar nichts und will nur zu einer Veranstaltung melden

### "Uwe"

Organisiert die Veranstaltung, hat keinerlei IT Background und leitet am Wochenende den Wettkampt. Das Alles in seiner eh schon begrenzten Freizeit.

### "Michael"

Ist der IT Beauftragte seines Vereins, hat vielleicht sogar Informatik studiert und kann auch programmieren.

### "Maria"

Sitzt im "Büro" des Vereins und gleicht Meldungen mit Zahlungen ab und erteilt eine Startberechtigung.


## Meilensteine

1. Quick Vertical Demonstrator (functional limited)
2. Ausarbeitung der Architektur und der Datenmodelle auf Basis der Erfahrungen mit 1.
3. Ausarbeitung / Entwurf API
4. Trennung von Frontend und API
5. Isolation des sportartspezifischen Teils (Sailing)
6. Modulasierung des Kerns (mit besonderem Blick auf Frontend, Micro GUI)
7. Ausarbeitung Modul-Schnittstelle, Implementierung als Module: Entries, Auswertung
8. Implementierung erster Extensions: Payment
9. Schnittstelle Datenexport (insbesondere Ergebnisse)
10. Stylesheets Ergebnisse (HTML / PDF)
11. Stylesheets / Design Frontend / Fokus Usability
12. Öffentliche Beta

Dokumentation über den gesamten Zeitraum

## Ausblick

Nach einer initialen Projektphase soll dauerhaft der Cloud gestützte Betrieb für alle im DOSB organisierten (Amateur) Sportvereine möglich sein.

Implementierung weiterer Sportarten, evtl. in Zusammenarbeit mit Sporthochschule Köln.

### Finanzierung (langfristig)

Mögliche Finanzierungsmodelle dafür sind:

* Spenden
* Zuwendungen durch Sport-Verbände
* Fees
* Anteile an Meldegeldern / Startgebühren (~1%)

Neben der SaaS Variante ist es jedem Sportverein möglich, s!m selbst zu betreiben. Ein nahtloser einfachster Übergang von SaaS zur selbst-gehosteten Variante ist durch Synchronisation der Datenbestände möglich. Auch ein zeitlich begrenzter gleichzeitiger Betrieb ist dadurch möglich.

### Mobile Plattformen

Entwicklung einer Anwendung für Smartphones insbesondere für Meldung und Zahlungen.


### Der Antragsteller

* Christian Hartmann
* geb. 1963-07-27 (Berlin)
* Studium Maschinenbau und Informatik an der TU Berlin
* Selbstständig tätig seit 1990
* Seit vielen Jahren ehrenamtlich im (Segel)-Sport engagiert



Anlagen (online):

Screenshots verschiedenster Software Pakete
Auswertesysteme im Segelsport (WR Anhang A, Yardstick, ORC)
Dokumentation CoMaTo, Screenshots, Beschreibung
Verschiedene Auswertungen / Ergebnislisten
