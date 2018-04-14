# Wort-Scrabble II

Nun geht es an die Umsetzung des Wort-Scrabble-Spiels.

Die Attribute speichern die zu einem Satz gelegten Karten, die gerade gezogene, aktuelle Karte und je einen Zähler für die insgesamt gezogenen und aus dem Satz wieder entfernten Karten.

Die Attribute speichern die zu einem Satz gelegten Karten, die gerade gezogene, aktuelle Karte und je einen Zähler für die insgesamt gezogenen und aus dem Satz wieder entfernten Karten.

Im Konstruktor muss dann die `List` von Karten erzeugt werden.

`karteZiehen`überprüft, ob schon 10 Karten gezogen wurden. Falls nicht, wird eine neue Karte als `aktuelleKarte` erzeugt und gespeichert.

`zeigeAktuelleKarte` zeigt die gerade gezogene Karte an. Falls noch keine Karte gezogen wurde, wird ein entsprechender Hinweis ausgegeben.

`karteAnlegen` bzw. `entferneKarte`legt die aktuelle Karte an der angegebenen Position im Satz an bzw. löscht diese. Beachte, dass die Nummerierung einer Liste bei 0 beginnt.

`infoAusgeben` druckt eine Gesamtübersicht über den momentanen Spielstand aus.

`getGesamtPunktzahl` berechnet den Punktewert des Satzes und gibt diesen zurück.

## Aufgabe - Implementierung

Implementiere die vorgestellte Spielidee. Du kannst Dich an den oben dargestellten Rahmen halten oder Deine eigenen Ideen umsetzen. Achte jedenfalls darauf das Spiel möglichst benutzerfreundlich zu gestalten. Du kannst die Ausgabe auf der Konsole auch durch ein animiertes Kartenspiel in GLOOP ersetzen.

Die Klasse `Karte`kannst Du bereits fertig programmiert kopieren:

```java
import java.util.Random;

public class Karte
{
    private int wert;
    private String wort;

    /**
     * Erzeugt eine Karte mit zufälligem Wort
     * und zufälligem Wert zwischen 1 und 10.
     */
    public Karte()
    {
        String[] worte = {
            "ich", "ich", "ich", "ich", "ich",
            "du", "du", "du", "du", "du", 
            "mich", "dich","mich", "dich","mich", "dich",
            "wieder", "heute", "gestern", "wald",
            "Haus", "Blume", "PC", "Schule", "Tapete",
            "haben", "haben", "möchten", "möchten",
            "gehen", "gehen", "laufen", "laufen",
            "sprechen", "sprechen", "singen", "singen",
            "voll", "daneben", "wieder", "mal",
            "echt", "blau", "leer", "Cola", "Sofa",
            "und", "und", "und", "und", "und",
            "oder", "oder", "oder", "oder", "oder",
            "Fußball", "Bild", "hallo"
        };
        Random random = new Random();
        int index = random.nextInt(worte.length);
        wort = worte[index].toUpperCase();
        wert = random.nextInt(10) + 1;
    }

    /**
     * Konstruktor, der v.a. zum Testen benutzt werden kann.
     */
    public Karte(String wort, int wert)
    {
        this.wort = wort;
        this.wert = wert;
    }

    public String getWort()
    {
        return wort;
    }

    public int getWert()
    {
        return wert;
    }
}
```

Diese Aufgabe stammt von 

[inf-schule.de](https://github.com/budumlu/Informatik-Q1/tree/54b69ff3ede27c2f3a46e62c9db6ea1d42e48439/www.inf-schule.de)

 und steht daher unter folgender Lizenz: 

![Creative Commons Lizenzvertrag](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

  
Dieses Werk ist lizenziert unter einer 

[Creative Commons Namensnennung - Nicht-kommerziell - Weitergabe unter gleichen Bedingungen 4.0 International Lizenz](http://creativecommons.org/licenses/by-nc-sa/4.0/)

.

