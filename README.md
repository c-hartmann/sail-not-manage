# sail!manage

"sail! not manage" (vorläufiger Projektname)

nachfolgend 's!m'


## Abstract

Eine "webbasierte" Sportart unabhängige Open Source Software zur Vorbereitung, Begleitung und Auswertung von Sportwettkämpfen im Amateursportbereich.


## Das Projekt

Zielvorgabe des Projektes ist ein direkt einsatzfähiger Prototyp der oben genannten Software und insbesondere dabei der belastbare Entwurf einer erweiterbaren Architektur, sowie deren vollständige "Use Case" (Nutzung, Entwicklung) orientierte Dokumentation. Der Sportart spezifische Teil wird durch eine Referenzimplementierung "Segeln" realisiert. Dieser umfasst alle in Deutschland relevanten Auswertesysteme. (siehe Anhang)


## Umfeld

Allein im deutschen Amateursport sind 27.000.000 Amateursportler organisiert. Hier gehen wir von einer Wettkampfquote von 10% aus. Alle diese Wettkämpfe bedürfen einer Auswertung der Leistungen, also i.d.R. die Ermittlung einer Rangfolge. Dies gilt für alle Sportarten, seien es Einzel- oder Mannschaftsteilnehmer.


## Umfeldanalyse

Ein überdurchschnittlich weit verbreitetes Modell von Software zu diesem Zweck lässt sich wie folgt beschreiben:

* Proprietär (kein Open Source)
* Sportart spezifisch
* überwiegend Plattform gebunden (90% MS Windows)
* Fat Clients (webbasiert selten)
* "in die Jahre gekommen"
* kaum oder gar nicht vorhandene Erweiterbarkeit (Module)
* Monolytische Architektur

s!m soll sich hingegen auszeichnen durch:

* Open Source (unwiderruflich)
* basiert auf gängigen Programmiersprachen
* Erweiterbarkeit


## Umfeldanalyse (Segeln)

Als Beispiele im Umfeld (am Beispiel Segelsport) seien genannt:

Kennzahlen, Technologie, Klasse, Kosten

### manage2sail

* Nutzer:
* Software Klasse:
* Technologie:
* Hersteller: DSV (u.A.)
* Kosten: anfänglich Jahresgebühr, mittlerweile kostenfrei

### raceoffice.org

* Nutzer:
* Software Klasse:
* Technologie:
* Hersteller:
* Kosten:

### Velum

* Nutzer:
* Software Klasse:
* Technologie:
* Hersteller:
* Kosten:

### JavaScore

* Nutzer:
* Software Klasse:
* Technologie:
* Hersteller:
* Kosten:


## Sportart übergreifend

Die Kriterien für die Auswertung lassen sich in wenige und überschaubare "Modelle" differenzieren: Ligen, zusammenlegen von Gruppenwertungen, Turnier orientierte wie Tennis und Fussball und - vor Allem - Mischformen. Zeitliche Strukturierung und Organisation dürften für alle zutreffen.

Spezifische Algorythmen zur Auswertung können sehr anspruchsvoll sein und werden deshalb in "Modulen" realisiert. Neben der Basisaufgabe Auswertung steuern diese Module auch Ablauf eines Wettkampfs, z.B. durch Zwischenergebnisse

## Abgrenzung

s!m (Core) soll nicht:

* Alle möglichen denkbaren organisatorischen Aufgaben eines Wettkampfs unterstützen.
* Keine Vereins- oder Mitgliederverwaltug sein

## Erweiterbarkeit

s!m (Core) soll aber erweiterbar sein. Als Beispiele seien hier genannt:

* Benachrichtigungen von Teilnehmern (SMS; Messenger Dienste)
* Druck von Urkunden
* Statistik
* Fair Play Wertungen
* Zahlungen von Startgeldern (PayPal u.A.)


## Technische Umsetzung

Mit Blick auf zukünftige Beteiligung Dritter ist die Verwendung von einfachen, gut gepflegten und leicht verfügbaren Werkzeugen elementar.

Die Einstiegshürden für die Mitarbeit Dritter muss so niedrig wie möglichs sein.

s!m ist ein webbasiertes Werkzeug und wird aus den oben genannten Gründen mit PHP (CakePHP als Framework) und JavaScript (oder Derivate wie TypeScript) entwickelt.

Um eine nahtlose Integration in vorhandenen Vereins-Webseiten zu ermöglichen, soll schon zum Ende des ersten Projektzeitraums ein WordPress Plugin mit einem Auszug der Funktionalitäten (insbesondere Meldung und Dokumente) zur Verfügung stehen. Dieses lässt sich sowohl eine SaaS Lösung der Cloud, als auch an eine selbst-gehostete Implementierung anbinden.


### User Interface

Die Gestaltung der Benutzeroberfläche orientiert sich am Gedanken:

* Einfach und nur notwendige Elemente zu Beginn
* weitere speziellere Elemente erst auf Anforderung
* Expert Modus if required


### i10n

s!m wird von Anfang an internationalisiert entwickelt. Zunächst in Englisch und Deutsch.


## User (siehe KDE) Zielpersonen, Nutzer

### Uwe

Organisiert die Veranstaltung, hat keinerlei IT Background und leitet am Ende den Wettkampt. Das Alles in seiner eh schon begernzten Freizeit.

### Michael

Ist der IT Beauftragte seines Vereins, hat vielleicht sogar Informatik studiert und kann auch programmieren.

### Niklas

Hat keinen Plan von gar nichts und will nur zu einer Veranstaltung melden

### Maria

Sitzt im "Büro" des Vereins und gleicht Meldungen mit Zahlungen ab und erteilt eine Startberechtigung.

## Ausblick

Nach einer initialen Projektphase soll dauerhaft der Cloud gestützte Betrieb für alle im DOSB organisierten (Amateur) Sportvereine möglich sein. Mögliche Finanzierungsmodelle dafür sind:

* Spenden
* Zuwendungen durch Sport-Verbände
* Fees
* Anteile an Meldegeldern / Startgebühren (~1%)

Neben der SaaS Variante ist es jedem Sportverein möglich, s!m selbst zu betreiben. Ein nahtloser einfachster Übergang von SaaS zur selbst-gehosteten Variante ist durch Synchronisation der Datenbestände möglich. Auch ein zeitlich begrenzter gleichzeitiger Betrieb ist dadurch möglich.

Entwicklung einer Anwendung für Smartphones.
