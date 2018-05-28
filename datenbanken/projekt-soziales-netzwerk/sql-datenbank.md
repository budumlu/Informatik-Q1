# SQL-Datenbank

## Anmeldung

1. Erstellen Sie pro Gruppe auf [https://instahub.org/](https://instahub.org/) einen Schüler-Account. 
2. Geben Sie ihre Lehrkraft mit an.
3. Lassen Sie Ihren Account von Ihrer Lehrkraft freischalten.

## Operationen auf Tabellen

Um Inhalte nicht nur über die Weboberfläche suchen zu können, können Sie als Administrator Ihrer Datenbank auf die Abfragesprache SQL \(Structered Query Language\) zugreifen.

Eine SQL-Abfrage ist von der Struktur immer gleich.

```sql
SELECT Spalte(n)
FROM Tabelle(n)
[WHERE Bedingung(en)]
```



Dabei wird der erste Zeile als **Projektion** bezeichnet. Die dritte Zeile wird **Selektion** genannt. Diese Selektion ist optional und kann auch entfallen.

### Projektion

Mit Hilfe von Projektionen kann ausgewählt werden, welche **Spalten** ausgegeben werden sollen. Recherchiere ggf. im Internet um die Aufgabe zu lösen.

{% hint style="success" %}
**Aufgaben**

1. Gib alle Benutzernamen \(username\) aus users aus.
2. Gib alle Benutzernamen \(username\) und echten Namen \(name\) aller Einträge aus users aus.
3. Gib die Wohnorte aller Mitglieder aus.
4. Wähle alle Einträge aus der Tabelle users aus.
{% endhint %}

### Selektion

Mit Hilfe der Selektion kann ausgewählt werden, welche **Zeilen** angezeigt werden sollen**.**



{% hint style="success" %}
**Aufgaben**

1. Wähle alle Einträge aus der Tabelle users aus, bei denen das Geschlecht \(gender\) weiblich \(female\) ist.
2. Wähle alle Mitglieder aus Deutschland aus.
3. Wähle alle Mitglieder aus, die in Leipzig wohnen.
4. Zeige nur _Emily Faber_ an.
5. Wähle alle Mitglieder mit der Rolle _user_ aus.
6. Ersetze in Aufgabe 5 = durch != .
7. Notiere was != bedeutet.
{% endhint %}

### Weitere SQL-Sprachbefehle

Im Anhang finden Sie weitere [SQL-Sprachelemente](../../anhang/sql-sprachelemente.md) zum Filtern der Daten mit logischen Operatoren, Vergleichoperatoren, Aggregatfunktionen, zum Gruppieren, zur Vereinigung\(UNION\) oder zum Verbund \(JOIN\) von Relationen. Finde zu jedem Sprachbefehl mindestens eine Anwendungsmöglichkeit auf der Datenbank des sozialen Netzwerks. 

{% hint style="success" %}
**Aufgabe**

Teilen Sie dabei die Befehle unter Ihnen auf, und erstellt auf [https://hackmd-ce.herokuapp.com/](https://hackmd-ce.herokuapp.com/) eine Präsentation. Als Vorlage dient Ihnen folgendes Dokument: [https://hackmd-ce.herokuapp.com/s/BksxQAIAG\#](https://hackmd-ce.herokuapp.com/s/BksxQAIAG#). Weitere Tipps zu Gestaltung der Präsentation  finden Sie hier: [https://hackmd-ce.herokuapp.com/slide-example\#](https://hackmd-ce.herokuapp.com/slide-example#) .
{% endhint %}



