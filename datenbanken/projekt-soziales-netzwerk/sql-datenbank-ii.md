# SQL-Datenbank II

### Logische Operatoren

#### AND, OR, AND NOT

{% hint style="success" %}
1. Erschließen Sie sich anhand der nachfolgenden 3 Beispiele die Funktion der Operatoren `AND` `OR, AND NOT.` Notieren Sie sich die Antworten.
   *   ```sql
     SELECT username, city FROM users where city = "Berlin" AND name LIKE "Fabian%"
     ```

   *   ```sql
     SELECT username, city FROM users where city = "Berlin" OR name LIKE "Fabian%"
     ```

   *   ```sql
     SELECT username, city FROM users where city = "Berlin" AND NOT name LIKE "Fabian%"
     ```
2. Finden Sie alle Berliner die \*Marc\* heißen.
3. Finden Sie alle Leipziger Frauen.
4. Finden Sie alle Linas und Lorenas.
5. Sortieren Sie alle Männer nach Körpergröße, welche mindestens 16 Jahre alt sind.
6. Zeige das Gebrtsdatum und den Benutzernamen aller Frauen an, die kleiner als 1,60 Meter sind.
7. Wähle alle Felix aus, die nicht aus Berlin kommen.
{% endhint %}

**Wechselwirkungen von Einschränkungen**

Gesucht werden alle Berliner:

```sql
SELECT username, name FROM users where city = "Berlin" AND gender = "male" OR gender = "female"
```

Führe den Befehl aus und prüfe das Ergebnis, indem du die Abfrage ohne explizite Ausführung des Geschlechts erneut ausführst.

Wenn du mehr als 2 Bedingungen hast ist es manchmal sinnvoll anzugeben, welche zuerst betrachtet werden müssen. Dazu kannst du Klammern verwenden:

```sql
SELECT username, name FROM users where city = "Berlin" AND (gender = "male" OR gender = "female")
```

1. Gib alle Männer aus Leipzig aus, die kleiner als 165 Zentimeter sind.
2. Die Bundeswehr sucht Rekruten gib die Namen aller Männer über 165cm und alle Frauen über 160cm aus.
3. Erna sucht eine Bekannte aus Berlin. Ihr Vorname war entweder _Bea_ oder _Naomi_.

### Verändern von Daten

#### INSERT

Füge zwei ausgedachte Datensätze nach folgendem Muster ein:

```sql
INSERT INTO users (username, email, password, name, bio, gender, birthday, city, country, centimeters, avatar, role, is_active, remember_token, created_at, updated_at) 
VALUES ('guenther37', 'guenther@instahub.app', '12345', 'Günther Müller', 'Günther mag Kartoffelsalat.', 'male', '2006-06-06 00:00:00', 'Leipzig', 'Deutschland', '173', 'avatar.png', 'user', '0', NULL, now(), now());
```

Was bedeutet `now()`?

Expertenaufgabe: Wieso wird in dem obigen SQL-Befehl die ID nicht mit übergeben?

1. Welche ID hat der neue Datensatz? Auf welche Arten können diese ermittelt werden?
2. Füge den User _Mila Bach_ aus Hamburg hinzu. Du kannst dir die fehlenden Attribute selbst ausdenken.
3. Registriere dich in deinem InstaHub \([https://_hub_.instahub.org/](https://wi-wissen.github.io/instahub-doc-de/#/exercices?id)\) als neues Mitglied.
4. Logge dich anschließend wieder als _admin_ ein und prüfe die ID des neuen Mitglieds.

#### [UPDATE](https://wi-wissen.github.io/instahub-doc-de/#/exercices?id=update) {#update}

1. Setze die Körpergröße von allen Mitgliedern auf 160.
2. Ändere in dem zuletzt hinzugefügten Eintrag die Stadt auf Dresden. \(Du kannst die ID mit einem extra SELECT-Befehl ermitteln.\)
3. Ersetze den Begriff "Germany" überall durch "Deutschland"

#### DELETE

Lösche einen Datensatz.

{% hint style="success" %}
Erstellen Sie neue Tabellen für das soziale Netzwerk:

[https://wi-wissen.github.io/instahub-doc-de/\#/exercices?id=tabelle-photo](https://wi-wissen.github.io/instahub-doc-de/#/exercices?id=tabelle-photo)
{% endhint %}

