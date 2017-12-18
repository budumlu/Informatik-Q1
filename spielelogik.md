# Spielelogik
Um das Spiel zu spielen benötigen wir eine Klasse, welche die Spielelogik enthält und den Benutzer führt. Lässt man die hier nicht mehr relavanten Teile der Klassen Warteschlange und Person weg, ergibt sich insgesamt folgendes Klassendiagramm: 
![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/spielelogik/KlassendiagrammGesamt.png)

Beim Erzeugen des Spiels soll die Zahl der Kinder, die gleichzeitig auf einen Baumstamm passen, angegeben werden. Diese Zahl wird im Attribut breite gespeichert. Außerdem wird eine Warteschlange erzeugt und diese als `stamm`` referenziert. 

Die Methode `leseString` liest eine Benutzereingabe ein. Dies wird zur Eingabe der Namen der Personen auf dem Stamm benötigt. Du kannst die Methode einfach übernehmen. Verstehen musst Du sie nicht.