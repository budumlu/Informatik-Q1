# Hunde bellen

## Hunde, die bellen, beißen nicht

### Listen von Wortkarten

Um das Spiel programmieren zu können, benötigt man eine Liste, in die man an beliebiger Stelle ein Wort einfügen oder löschen kann. Glücklicherweise müssen wir entsprechende Klassen aber nicht immer selbst programmieren, sondern können einfach entsprechende Klassen benutzen, die uns die benötigte Funktionalität schon fertig bieten.

### LinkedList

Java stellt uns viele Klassen zur Verfügung, die wir einfach benutzen können. Eine dieser Klassen hatten wir schon oft benutzt:`String`. Eine andere Klasse ist`LinkedList`, die genau die Funktionalität, die wir von einer Liste erwarten, schon fertig bereit stellt. Daneben gibt es noch mehrere tausend anderer Klassen. Damit die Vielzahl dieser Klassen geordnet werden können, wurden diese in sogenannten Paketen organisiert. Um eine Klasse benutzen zu können, muss man dann das entsprechende Paket am Anfang des Quellcodes - noch vor der Definition der Klasse - importieren. Um z.B. die Klasse`LinkedList`aus dem Paket`java.util`benutzen zu können, muss man also im Quellcode schreiben:

```java
import java.util.LinkedList;
// oder um alle Klassen dieses Paketes zu importieren:
import java.util.*;

// Erst danach folgt die Definition der Klasse.
class MeineKlasse{
   ... hier kann LinkedList jetzt benutzt werden...
}
```

Wir gehen in den folgenden Beispielen von einer Klasse

`Hund`

aus:

```text
class Hund {
   void bellen() {
      System.out.println("Wuff!");
   }
}
```

Innerhalb einer Methode ließe sich dann eine entsprechende Liste z.B. folgendermaßen benutzen:

```java
// Definiere eine Variable und erzeuge eine neue LinkedList
LinkedList liste = new LinkedList();

// Erzeuge einen Hund, der an das Ende der Liste
// angehängt werden soll
Hund struppi = new Hund();
liste.add(struppi);

// oder mit anonymen Objekt
liste.add(new Hund());

// oder Einfügen an bestimmter Stelle
liste.add(1, new Hund());

// Entferne den zweiten Hund, Index ist 1 !!!
liste.remove(1);

// Gibt die Größe der Liste aus, hier: 2
System.out.println(liste.size());

// Gibt das erste Element zurück
Hund bello = liste.get(0);

// Die Liste leeren
liste.clear();
```

### Generische Klassen

Möchte man auf Methoden der Klasse`Hund`zugreifen, erhält man eine Fehlermeldung:

```java
import java.util.*;
LinkedList liste = new LinkedList();
liste.add(new Hund());
liste.get(0).bellen();
Error: cannot find symbol -   method bellen()
```

### Listen durchlaufen

Möchte man alle Elemente einer Liste durchlaufen, kann man dies z.B. mit einer for-Schleife tun:

```java
for(int i = 0; i < liste.size(); i++) {
   liste.get(i).bellen();
}
```

Für solche einfachen Anwendungsfälle kann man alternativ auch die for-each-Schleife benutzen:

```java
for(Typ name: sammlungsobjekt) {
   ...
}
```

Angewandt auf das obige Beispiel also:

```java
for(Hund h: liste) { // Lies: Für jeden Hund h aus liste
   h.bellen();
}
```

## Hund-Klasse

Einige Übungen gehen von der Verwendung der Klasse`Hund`aus. Ein Hund bekommt bei der Erzeugung einen zufälligen Namen zugewiesen. Er kann bellen und gibt dabei seinen Namen aus. Die Klasse`Hund`kannst Du Dir [hier herunterladen](http://www.inf-schule.de/content/programmierung/oopjava/experten/listen/uebungen/Hund.java).

### Aufgabe Dokumentation lesen

**Aufgabe:** Suche in einer Suchmaschine nach den Begriffen "LinkedList Java". Einer der ersten Treffer sollte zur [offizielle Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html) der Klasse`LinkedList`führen. Analog kannst Du die Dokumentation anderer Java-Klassen finden.

Auch wenn Du nicht alle Details verstehen wirst, kannst Du die wesentlichen Informationen erfassen. Finde und teste Methoden zum:

* Entfernen des ersten und letzten Elementes.
* Abfragen des ersten Elementes ohne dieses zu löschen.
* Ersetzen eines Elementes über den Index.
* Überprüfen, ob ein bestimmtes Objekt vorhanden ist.

Lass Dich nicht von der Tatsache verwirren, dass manche Methoden das gleiche bewirken. Das liegt daran, dass eine Liste z.B. auch als Warteschlange oder Stapel benutzt werden kann und dann teilweise andere Methodennamen üblich sind.

Diese Aufgabe stammt von 

[inf-schule.de](https://github.com/budumlu/Informatik-Q1/tree/54b69ff3ede27c2f3a46e62c9db6ea1d42e48439/www.inf-schule.de)

 und steht daher unter folgender Lizenz: 

![Creative Commons Lizenzvertrag](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

  
Dieses Werk ist lizenziert unter einer 

[Creative Commons Namensnennung - Nicht-kommerziell - Weitergabe unter gleichen Bedingungen 4.0 International Lizenz](http://creativecommons.org/licenses/by-nc-sa/4.0/)

.

