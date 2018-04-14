# Platz da!

Auf einem Spielplatz liegt ein Baumstamm, der zum Spielen und Balancieren einlädt. Alle Kinder möchten darauf spielen, aber leider ist der Stamm nicht groß genug. Die ersten drei Kinder steigen auf den Stamm und spielen dort. Sobald das nächste Kind von links auf den Stamm steigen möchte, schiebt es alle Kinder etwas weiter. Das Kind, das sich ganz rechts auf dem Stamm befindet, fällt hinunter. Du sollst Dir merken welches Kind als nächstes vom Baumstamm fällt.

## Ablauf

Das Spiel kann mit beliebig vielen Spielern gespielt werden. Zu Beginn des Spiels wird festgelegt für wie viele Kinder der Baumstamm Platz bieten soll. Je länger der Stamm, desto schwieriger wird das Spiel. Für die weiteren Erklärungen wird von einem Baumstamm ausgegangen, der Platz für drei Kinder bietet.

Ein beliebiger Spieler beginnt. Dieser nennt den Namen des Kindes, das zuerst auf den Baum steigt, z.B. "Johanna". Der nächste Spieler nennt einen weiteren Namen, z.B. "Sandra". Nachdem der darauf folgende Spieler einen Namen, z.B. Philipp, genannt hat, ist der Baum voll.

![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/spielregeln/baumvoll.png)

voll belegter Baum mit drei Kindern

Ab jetzt muss der Spieler, der an der Reihe ist, sagen welches Kind als nächstes vom Baumstamm fällt. Gelingt ihm dies, bestimmt er den Namen des nächsten Kindes. Tippt er auf einen falschen Namen, hat er das Spiel verloren.

![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/spielregeln/fallen.png)

Da im oben dargestellten Fall "Johanna" als nächstes vom Stamm fällt, muss der Spieler diesen Namen nennen. Gelingt ihm dies, bestimmt er den Namen des nächsten Kindes, z.B. "Tom": 

![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/spielregeln/neuesKind.png)

Dies wird so lange fortgeführt bis ein Spieler den falschen Namen nennt. Wird das Spiel mit mehr als zwei Spielern gespielt, können diese so lange weiterspielen, bis nur noch ein Spieler übrig bleibt. Dieser hat dann gewonnen.

Am Computer gespielt kann das Spiel dann bspw. so aussehen:

