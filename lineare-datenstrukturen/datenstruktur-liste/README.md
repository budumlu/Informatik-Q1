# Datenstruktur Liste

Um mehrere Objekte in Java zu verwalten, wurden bisher Arrays verwendet, auf die häufig in `for`-Schleifen über den Laufindex `i` zugegriffen wurde. Dieses Beispiel wurde aus dem Landeplatz-Projekt entnommen:

```java
 lampe = new GLKugel[20];
          for (int i=0; i<20; i++){
              lampe[i] = new GLKugel(290,20,0,10);
              lampe[i].drehe(0,i*360/20,0, 0,0,0);
          }
```

In bestimmten Modelierungsfragen erweist sich die **statische Datenstruktur** des Arrays als ungünstig. So muss bereits am Anfang festgelegt werden, welche Größe das Array haben soll.

Während beim Landeplatz es kein Problem darstellt, am Anfang festzulegen, wie viele Lampen dieser besitzen soll, ist es bei einer ToDo-Liste ungünstig. Nun könnte man hier einfach das Array groß genug \(&gt;1000?\) wählen - was jedoch bedeuten würde, dass man immer Speicherplatz für die maximal mögliche Anzahl an ToDo-Einträgen vorhalten muss.

Eine Lösung stellt die Datenstruktur der `Liste`dar. Die wichtigsten Eigenschaften der generischen Listetyps für das Zentralabitur \(siehe [/Generische Klasse List&lt;ContentType&gt;](https://github.com/budumlu/Informatik-Q1/tree/54b69ff3ede27c2f3a46e62c9db6ea1d42e48439/Generische%20Klasse%20List%3CContentType%3E/README.md)\) sollen hier kurz vorgestellt werden:

## Konstruktor

```java
public class BeispielListe {
  private List<Aufgabe> beispielListe;

  public BeispielListe() {
    beispielListe = new List<Aufgabe>();
  }
```

## Aufträge

### Prüfe Zugriff auf einen Listeneintrag

Die Anfrage liefert den Wert true, wenn es ein aktuelles Objekt gibt, sonst liefert sie den Wert false.

```text
beispielListe.hasAccess()
```

### Aktuellen Listeneintrag entfernen

Wenn die Liste leer ist oder es kein aktuelles Objekt gibt \(hasAccess\(\)== false\), geschieht nichts.  
 Falls es ein aktuelles Objekt gibt \(hasAccess\(\) == true\), wird das aktuelle Objekt geloescht und das Objekt hinter dem geloeschten Objekt wird zum aktuellen Objekt.   
 Wird das Objekt, das am Ende der Liste steht, geloescht, gibt es kein aktuelles Objekt mehr.

```text
beispielListe.remove();
```

### Einen neuen Eintrag vor dem aktuellen Listeneintrag einfügen

Falls es ein aktuelles Objekt gibt \(hasAccess\(\) == true\), wird ein neues Objekt vor dem aktuellen Objekt in die Liste eingefuegt. Das aktuelle Objekt bleibt unveraendert.

Wenn die Liste leer ist, wird pContent in die Liste eingefuegt und es gibt weiterhin kein aktuelles Objekt \(hasAccess\(\) == false\).

Falls es kein aktuelles Objekt gibt \(hasAccess\(\) == false\) und die Liste nicht leer ist oder pContent gleich null ist, geschieht nichts.

```text
beispielListe.insert();
```

### Einen neuen Eintrag hinter den letzten Listeneintrag anhängen

Falls pContent gleich null ist, geschieht nichts.

Ansonsten wird ein neues Objekt pContent am Ende der Liste eingefuegt. Das aktuelle Objekt bleibt unveraendert.

Wenn die Liste leer ist, wird das Objekt pContent in die Liste eingefuegt und es gibt weiterhin kein aktuelles Objekt \(hasAccess\(\) == false\).

```text
beispielListe.append(ContentType pContent);
```

### Gehe zum ersten Listeneintrag

Falls die Liste nicht leer ist, wird das erste Objekt der Liste aktuelles Objekt. Ist die Liste leer, geschieht nichts.

```text
beispielListe.toFirst()
```

### Gehe zum letzten Listeneintrag

Falls die Liste nicht leer ist, wird das letzte Objekt der Liste aktuelles Objekt. Ist die Liste leer, geschieht nichts.

```text
beispielListe.toLast()
```

### Gehe zum nächsten Listeneintrag

Falls die Liste nicht leer ist, es ein aktuelles Objekt gibt und dieses nicht das letzte Objekt der Liste ist, wird das dem aktuellen Objekt in der Liste folgende Objekt zum aktuellen Objekt, andernfalls gibt es nach Ausfuehrung des Auftrags kein aktuelles Objekt, d.h. hasAccess\(\) liefert den Wert false.

```text
beispielListe.next()
```

### Frage nach Inhalt/Objekt aus der Liste:

Falls es ein aktuelles Objekt gibt \(hasAccess\(\) == true\), wird das aktuelle Objekt zurueckgegeben, andernfalls \(hasAccess\(\) == false\) gibt die Anfrage den Wert null zurueck.

@return das aktuelle Objekt \(vom Typ ContentType\) oder null, wenn es kein aktuelles Objekt gibt

```text
beispielListe.getContent()
```

### Verändere den Inhalt aus der Liste

Falls es ein aktuelles Objekt gibt \(hasAccess\(\) == true\) und pContent ungleich null ist, wird das aktuelle Objekt durch pContent ersetzt. Sonst geschieht nichts.

@param pContent das zu schreibende Objekt vom Typ ContentType

```text
beispielListe.setContent()
```

### Hänge eine Zweite Liste an die erste Liste

Falls pList null oder eine leere Liste ist, geschieht nichts.

Ansonsten wird die Liste pList an die aktuelle Liste angehaengt. Anschliessend wird pList eine leere Liste. Das aktuelle Objekt bleibt unveraendert. Insbesondere bleibt hasAccess identisch.

@param pList die am Ende anzuhaengende Liste vom Typ List

```text
beispielListe.concat(List<ContentType> pList)
```

