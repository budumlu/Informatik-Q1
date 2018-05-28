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

