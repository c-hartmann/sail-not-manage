# sail!manage

"sail! not manage" (vorläufiger Projektname)

## Abstract

Eine "webbasierte" Sportart unabhängige Open Source Software zur Vorbereitung, Begleitung und Auswertung von Sportwettkämpfen im Amateursportbereich.

## Das Projekt

Zielvorgabe des Projektes ist ein direkt einsatzfähiger Prototyp der oben genannten Software und insbesondere dabei der belastbare Entwurf einer erweiterbaren Architektur, sowie deren vollständige "Use Case" (Nutzung, Entwicklung) orientierte Dokumentation.

## Umfeld

Allein im deutschen Amateursport sind 27.000.000 Amateursportler organisiert. Hier gehen wir von einer Wettkampfquote von 10% aus. Alle diese Wettkämpfe bedürfen einer Auswertung der Leistungen, also i.d.R. die Ermittlung einer Rangfolge. Dies gilt für alle Sportarten, seien es Einzel- oder Teamteilnehmer.

## Umfeldanalyse

Ein überdurchschnittlich weit verbreitetes Modell von Software zu diesem Zweck lässt sich wie folgt beschreiben:

* Proprietär (kein Open Source)
* Sportart spezifisch
* überwiegend Platform gebunden (90% MS Windows)
* Fat Clients, webbasiert selten
* "in die Jahre gekommen"
* kaum oder gar nicht vorhandene Erweiterbarkeit (Module)

s!m soll sich hingegen auszeichnen durch:

* Open Source (unwiderruflich)
* basiert auf gängigen Programmiersprachen
* Erweiterbarkeit

## Beispiele im Umfeld (am Beispiel Segelsport)

manage2sail, raceoffice.org, Velum

## warum sportart übergreifend

Die Kriterien für die Auswertung lassen sich in wenige "Modelle"differenzieren: Ligen, zusammen legen von Gruppenwertungen, Turnier orientierte wie Tennis und Fussball und - vor Allem - Mischformen. Zeitliche Strukturierung / Organisation dürfte für alle zutreffen.

## Technische Umsetzung

Mit Blick auf zukünftige Beteiligung Dritter ist die Verwendung von einfachen, gut gepflegten und leicht verfügbaren Werkzeugen elementar.

Die Einstiegshürden für die Mitarbeit Dritter muss so niedrig wie möglichs sein.

s!m ist ein webbasiertes Werkzeug und wird aus den oben genannten Gründen mit PHP (CakePHP als Framework) und JavaScript (oder Derivate wie TypeScript) entwickelt.

Um eine nahtlose Integration in vorhandenen Vereins-Webseiten zu ermöglichen, soll schon zum Ende des ersten Projektzeitraums ein WordPress Plugin mit einem Auszug der Funktionalitäten (insbesondere Meldung und Dokumente) zur Verfügung stehen. Dieses lässt sich sowohl eine SaaS Lösung der Cloud, als auch an eine selbst-gehostete Implementierung anbinden.

## Ausblick

Nach einer initialen Projektphase soll dauerhaft der Cloud gestützte Betrieb für alle im DOSB organisierten (Amateur) Sportvereine möglich sein. Mögliche Finanzierungsmodelle dafür sind:

* Spenden
* Zuwendungen durch Sport-Verbände
* Fees
* Anteile an Meldegeldern / Startgebühren (~1%)

Neben der SaaS Variante ist es jedem Sportverein möglich, s!m selbst zu betreiben. Ein nahtloser einfachster Übergang von SaaS zur selbst-gehosteten Variante ist durch Synchronisation der Datenbestände möglich. Auch ein zeitlich begrenzter gleichzeitiger Betrieb ist dadurch möglich.

