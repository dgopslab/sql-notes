# Joins

## Warum JOINs wichtig sind?

In relationalen Datenbanken liegen zusammengehörige Informationen oft nicht in nur einer Tabelle, sondern verteilt auf mehrere Tabellen.

Mit einem `JOIN` lassen sich diese Tabellen in einer Abfrage logisch miteinander verbinden.

Dadurch kann man Informationen gemeinsam auswerten, zum Beispiel:

- welcher Kunde welche Bestellung aufgegeben hat
- welche Bücher in einer Bestellung enthalten sind
- welche Daten über Fremdschlüssel zusammengehören

## INNER JOIN

Ein `INNER JOIN` liefert nur Datensätze, bei denen auf beiden Seiten der Verknüpfung passende Werte vorhanden sind.

Beispiel:  
Wenn Kunden und Bestellungen miteinander verbunden werden, zeigt ein `INNER JOIN` nur die Kunden an, zu denen auch tatsächlich passende Bestellungen existieren.

### Beispiel

```sql
SELECT kunde.vorname, bestellung.bestellung_id
FROM kunde
INNER JOIN bestellung
ON kunde.kunden_id = bestellung.kunden_id;
```
## Was bei einem JOIN verbunden wird?

Die Verbindung erfolgt meistens über einen **Primärschlüssel** und einen dazugehörigen **Fremdschlüssel**.

Beispiel:

- `kunde.kunden_id` = Primärschlüssel in der Kundentabelle
- `bestellung.kunden_id` = Fremdschlüssel in der Bestelltabelle

So kann erkannt werden, welche Bestellung zu welchem Kunden gehört.

## Unterschied zwischen Tabellenbeziehung und JOIN

Eine **Tabellenbeziehung** beschreibt, wie Tabellen im Datenmodell miteinander verbunden sind.

Ein **JOIN** ist die SQL-Abfrage, mit der diese Verbindung genutzt wird, um Daten gemeinsam abzurufen.

Das bedeutet:
- die Beziehung besteht im Modell
- der JOIN nutzt diese Beziehung in der Abfrage

## JOINs in der Praxis

JOINs sind besonders wichtig, wenn Informationen aus mehreren Tabellen zusammen angezeigt oder ausgewertet werden sollen.

Gerade bei relationalen Datenbanken gehören JOINs deshalb zu den wichtigsten Grundlagen.

## LEFT JOIN

Ein `LEFT JOIN` liefert alle Datensätze der linken Tabelle und ergänzt passende Werte aus der rechten Tabelle.

Wenn es auf der rechten Seite keine passende Verbindung gibt, werden dort `NULL`-Werte angezeigt.

### Beispiel

Ein `LEFT JOIN` kann genutzt werden, wenn alle Kunden angezeigt werden sollen, auch wenn noch nicht jeder Kunde eine Bestellung hat.

## Aktueller Stand

Ich habe bereits erste praktische Erfahrungen mit JOIN-Abfragen gesammelt und ein grundlegendes Verständnis dafür aufgebaut, wie zusammengehörige Daten aus mehreren Tabellen abgefragt werden.

Mein Fokus liegt aktuell vor allem auf dem Verständnis von `INNER JOIN` und ersten Grundlagen zu `LEFT JOIN`. Weitere JOIN-Arten möchte ich nach und nach ergänzen und sicherer anwenden lernen.
