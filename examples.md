# Examples

## Einfache SELECT-Abfrage

Mit einer einfachen `SELECT`-Abfrage lassen sich bestimmte Spalten aus einer Tabelle auslesen.

```sql
SELECT vorname, nachname
FROM kunde;
```
Dieses Beispiel gibt den Vor- und Nachnamen aller Kunden aus.

## SELECT mit WHERE

```sql
SELECT titel, preis
FROM buch
WHERE preis > 20;
```
Dieses Beispiel zeigt alle Bücher mit einem Preis größer als 20.

## SELECT mit ORDER BY

```sql
SELECT titel, preis
FROM buch
ORDER BY preis ASC;
```
Dieses Beispiel sortiert die Bücher aufsteigend nach Preis.

## INNER JOIN

```sql
SELECT kunde.vorname, bestellung.bestellung_id
FROM kunde
INNER JOIN bestellung
ON kunde.kunden_id = bestellung.kunden_id;
```
Dieses Beispiel zeigt, welcher Kunde welche Bestellung aufgegeben hat.

## Beispiel für eine n:m-Beziehung

```sql
SELECT bestellung.bestellung_id, buch.titel, bestellposition.menge
FROM bestellposition
INNER JOIN bestellung
ON bestellposition.bestellung_id = bestellung.bestellung_id
INNER JOIN buch
ON bestellposition.buch_id = buch.buch_id;
```
Dieses Beispiel zeigt, welche Bücher in einer Bestellung enthalten sind und in welcher Menge.

# Aktueller Stand
Ich nutze dieses Repository, um einfache SQL-Abfragen und typische Grundlagenbeispiele nachvollziehbar festzuhalten.

Mit der Zeit möchte ich die Beispiele um weitere JOINs, Views und komplexere Abfragen ergänzen.
