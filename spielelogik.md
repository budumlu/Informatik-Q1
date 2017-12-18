# Spielelogik
Um das Spiel zu spielen benötigen wir eine Klasse, welche die Spielelogik enthält und den Benutzer führt. Lässt man die hier nicht mehr relavanten Teile der Klassen Warteschlange und Person weg, ergibt sich insgesamt folgendes Klassendiagramm: 
![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/spielelogik/KlassendiagrammGesamt.png)

Beim Erzeugen des Spiels soll die Zahl der Kinder, die gleichzeitig auf einen Baumstamm passen, angegeben werden. Diese Zahl wird im Attribut `breite` gespeichert. Außerdem wird eine Warteschlange erzeugt und diese als `stamm` referenziert. 

Die Methode `leseString` liest eine Benutzereingabe ein. Dies wird zur Eingabe der Namen der Personen auf dem Stamm benötigt. Du kannst die Methode einfach übernehmen. Verstehen musst Du sie nicht.


```
String leseString() {
    return new java.util.Scanner(System.in).nextLine();
}
```
**Aufgabe:**
Erstelle eine neue Klasse Spiel in Deinem Projekt. Implementiere die notwendigen Attribute, den Konstruktor und die Methode `leseString`.
*Startbelegung: Zu Beginn des Spiels sollen die Spieler reihum die Namen der Personen eingeben, die auf dem Stamm stehen, bis dieser voll belegt ist. Die Methode `startBelegungEingeben` soll also in einer Schleife so oft einen neuen Namen abfragen und die Personen auf dem Stamm platzieren bis dieser voll belegt ist.
* Tipp überprüfen: Um zu überprüfen, ob ein Tipp mit dem Namen der vordersten Person auf dem Stamm übereinstimmt, kann man einige lokale Variablen benutzen oder einen etwas komplexeren Ausdruck formulieren.




```
boolean tippIstRichtig(String tipp) {
    if(stamm.gibErstePerson().name.equals(tipp))
        return true;
    else
        return false;
}
```



