# Listen in Java

Um mehrere Objekte in Java zu verwalten, wurden bisher Arrays verwendet, auf die häufig in `for`-Schleifen über den Laufindex `i` zugegriffen wurde. Dieses Beispiel wurde aus dem Landeplatz-Projekt entnommen:

```java
 lampe = new GLKugel[20];
          for (int i=0; i<20; i++){
              lampe[i] = new GLKugel(290,20,0,10);
              lampe[i].drehe(0,i*360/20,0, 0,0,0);
          }
```

In bestimmten Modelierungsfragen erweist sich die **statische Datenstruktur** des Arrays als ungünstig. So muss bereits am Anfang festgelegt werden, welche Größe das Array haben soll.

Während beim Landeplatz es kein Problem darstellt, am Anfang festzulegen, wie viele Lampen dieser besitzen soll, ist es bei einer ToDo-Liste ungünstig. Nun könnte man hier einfach das Array groß genug \(&gt;1000?\) wählen - was jedoch bedeuten würde, dass man immer Speicherplatz für die maximal mögliche Anzahl an wartenden vorhalten muss.

Eine Lösung stellt die Datenstruktur der `Liste`dar. Die wichtigsten Eigenschaften der generischen Listetyps für das Zentralabitur \(siehe [/Generische Klasse List&lt;ContentType&gt;](/Generische Klasse List<ContentType>)\) sollen hier kurz vorgestellt werden:

## Konstruktor

```Java
public class BeispielListe {
  private List<Aufgabe> beispielListe;

  public BeispielListe() {
    beispielListe = new List<Aufgabe>();
  }
```

## Aufträge

Aktuellen Listeneintrag entfernen: `beispielListe.remove();`  
Einen neuen Eintrag vor dem aktuellen Listeneintrag einfügen: `beispielListe.insert();`

Einen neuen Eintrag hinter den letzten Listeneintrag anhängen: `beispielListe.append();`

Gehe zum ersten Listeneintrag: `beispielListe.toFirst()`

Gehe zum letzten Listeneintrag: `beispielListe.toLast()`

Gehe zum nächsten Listeneintrag: `beispielListe.next()`

Prüfe Zugriff auf einen Listeneintrag: `beispielListe.hasAccess()`

Frage nach Inhalt/Objekt aus der Liste: `beispielListe.getContent()`

