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

   ```text
   2. Finde alle Berliner die *Marc* heißen.
   3. Finde alle Leipziger Frauen.
   4. Finde alle Linas und Lorenas. 
   5. Sortiere alle Männer nach ihrer Körpergröße, welche mindestens 16 Jahre alt sind.
   6. Zeige das Geburtsdatum und den Benutzernamen aller Frauen an, die kleiner als 1,60 Meter sind.
   7. Wähle alle Felix aus, die nicht aus Berlin kommen. 
   ```
{% endhint %}

{% hint style="success" %}
```sql
SELECT username, city FROM users where city = "Berlin" AND name LIKE "Fabian%"
```



```sql
SELECT username, city FROM users where city = "Berlin" OR name LIKE "Fabian%"
```



```sql
SELECT username, city FROM users where city = "Berlin" AND NOT name LIKE "Fabian%"
```
{% endhint %}



```text
Logische Operatoren

#### AND, OR, AND NOT

1. 

2. Finde alle Berliner die *Marc* heißen.
3. Finde alle Leipziger Frauen.
4. Finde alle Linas und Lorenas. 
5. Sortiere alle Männer nach ihrer Körpergröße, welche mindestens 16 Jahre alt sind.
6. Zeige das Geburtsdatum und den Benutzernamen aller Frauen an, die kleiner als 1,60 Meter sind.
7. Wähle alle Felix aus, die nicht aus Berlin kommen.
```

