# Data Modeling

## Warum Daten modelliert werden

Beim Datenmodellieren geht es darum, Informationen so in Tabellen zu strukturieren, dass sie logisch zusammenpassen und später sinnvoll verarbeitet werden können.

Ein gutes Datenmodell hilft dabei:

- Daten übersichtlich zu speichern
- Redundanzen zu vermeiden
- Beziehungen zwischen Daten sauber darzustellen
- spätere Abfragen und Änderungen zu erleichtern

## Beziehungen zwischen Tabellen

### 1:1-Beziehung

Bei einer 1:1-Beziehung gehört genau ein Datensatz aus Tabelle A zu genau einem Datensatz aus Tabelle B.

Beispiel:
Ein Benutzerkonto hat genau ein Benutzerprofil.

### 1:n-Beziehung

Bei einer 1:n-Beziehung kann ein Datensatz aus Tabelle A mit mehreren Datensätzen aus Tabelle B verbunden sein.

Beispiel:
Ein Kunde kann mehrere Bestellungen haben.  
Eine Bestellung gehört aber immer nur zu einem Kunden.

### n:m-Beziehung

Bei einer n:m-Beziehung können mehrere Datensätze aus Tabelle A mit mehreren Datensätzen aus Tabelle B verbunden sein.

Beispiel:
Eine Bestellung kann mehrere Bücher enthalten.  
Ein Buch kann gleichzeitig in vielen verschiedenen Bestellungen vorkommen.

## Join-Tabelle / Zwischentabelle

Eine n:m-Beziehung wird in relationalen Datenbanken meist nicht direkt gespeichert, sondern über eine zusätzliche Tabelle aufgelöst.

Diese Tabelle wird oft **Join-Tabelle** oder **Zwischentabelle** genannt.

Beispiel:
Zwischen `Bestellung` und `Buch` kann eine Tabelle wie `Bestellposition` stehen.

Diese enthält zum Beispiel:

- `bestellung_id`
- `buch_id`
- `menge`

Dadurch lässt sich abbilden, welches Buch in welcher Bestellung enthalten ist und in welcher Anzahl.

## Primärschlüssel und Fremdschlüssel im Modell

Ein **Primärschlüssel** identifiziert einen Datensatz innerhalb einer Tabelle eindeutig.

Ein **Fremdschlüssel** verweist auf den Primärschlüssel einer anderen Tabelle und stellt damit die Beziehung zwischen zwei Tabellen her.

## Warum mehrere Tabellen sinnvoll sind

Würde man alles in nur eine große Tabelle schreiben, würden viele Informationen mehrfach vorkommen.

Das führt schnell zu:

- doppelten Daten
- höherem Pflegeaufwand
- Fehlern bei Änderungen
- unübersichtlichen Strukturen

Durch die Aufteilung in mehrere logisch verbundene Tabellen bleibt das Modell sauberer und wartbarer.

## Beispiel aus einer Buchhandlungsdatenbank

In einer Buchhandlungsdatenbank könnten zum Beispiel Tabellen wie diese vorkommen:

- Kunden
- Bestellungen
- Bücher
- Bestellpositionen

Ein möglicher Zusammenhang wäre:

- Ein Kunde kann viele Bestellungen haben
- Eine Bestellung kann viele Bücher enthalten
- Ein Buch kann in vielen Bestellungen vorkommen

Dadurch entsteht zwischen Bestellungen und Büchern eine n:m-Beziehung, die über eine Zwischentabelle wie `Bestellposition` aufgelöst wird.

## Aktueller Stand

In diesem Bereich habe ich bisher vor allem Grundlagen aufgebaut zu:

- 1:1-, 1:n- und n:m-Beziehungen
- Primär- und Fremdschlüsseln
- Join- bzw. Zwischentabellen
- einfachen relationalen Datenmodellen

Komplexere Datenmodelle und weiterführende Modellierungsfragen möchte ich nach und nach weiter vertiefen.
