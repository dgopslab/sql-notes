# Basics

## Was ist eine relationale Datenbank?

Eine relationale Datenbank dient dazu, Daten strukturiert zu speichern, zu verwalten und gezielt wieder abzurufen.

Die Daten werden dabei in **Tabellen** organisiert. Beziehungen zwischen diesen Tabellen werden über **Schlüssel** hergestellt. Dadurch lassen sich Informationen geordnet speichern, Redundanzen verringern und Daten einfacher pflegen.

## Grundbegriffe

### Tabelle
Eine Tabelle ist eine strukturierte Sammlung von Daten zu einem bestimmten Thema, zum Beispiel `Kunden`, `Bestellungen` oder `Bücher`.

### Datensatz
Ein Datensatz ist eine einzelne Zeile in einer Tabelle. Er beschreibt einen konkreten Eintrag, zum Beispiel einen bestimmten Kunden.

### Attribut
Ein Attribut ist eine Eigenschaft eines Datensatzes, also eine Spalte in der Tabelle, zum Beispiel `Vorname`, `Nachname` oder `E-Mail`.

### Datenwert
Ein Datenwert ist der konkrete Inhalt eines Attributs, zum Beispiel `Daniel` im Attribut `Vorname`.

## Warum mehrere Tabellen statt nur einer?

Daten werden oft auf mehrere Tabellen verteilt, um:

- doppelte Daten zu vermeiden
- die Daten besser wartbar zu machen
- Beziehungen zwischen Daten sauber abzubilden
- Änderungen leichter durchführen zu können

Ein Beispiel:
Statt Kundendaten bei jeder Bestellung neu zu speichern, kann man Kunden und Bestellungen in getrennten Tabellen speichern und über eine Beziehung verbinden.

## Primärschlüssel

Ein Primärschlüssel dient dazu, einen Datensatz innerhalb einer Tabelle eindeutig zu identifizieren.

Beispiel:
Jeder Kunde hat eine eindeutige `kunden_id`.

## Fremdschlüssel

Ein Fremdschlüssel stellt eine Verbindung zu einer anderen Tabelle her.

Beispiel:
In einer Bestelltabelle kann `kunden_id` als Fremdschlüssel gespeichert werden. Dadurch ist erkennbar, zu welchem Kunden eine Bestellung gehört.

## Wichtige SQL-Befehle im Überblick

### SELECT
Mit `SELECT` werden Daten aus einer Tabelle abgefragt.

### INSERT
Mit `INSERT` werden neue Datensätze eingefügt.

### UPDATE
Mit `UPDATE` werden bestehende Datensätze geändert.

### DELETE
Mit `DELETE` werden Datensätze gelöscht.

### CREATE TABLE
Mit `CREATE TABLE` wird eine neue Tabelle erstellt.

### ALTER TABLE
Mit `ALTER TABLE` wird eine bestehende Tabelle verändert.

### DROP TABLE
Mit `DROP TABLE` wird eine Tabelle gelöscht.

## Mein aktueller Lernstand

Ich habe bereits ein gutes Grundverständnis bei:

- einfachen SELECT-Abfragen
- relationalen Datenbankstrukturen
- Primär- und Fremdschlüsseln
- grundlegenden SQL-Befehlen

Aktuell vertiefe ich mein Wissen Schritt für Schritt weiter.
