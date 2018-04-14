# Konzept der Warteschlange

Um das Spiel zu implementieren, benötigen wir eine Möglichkeit die einzelnen Personen auf dem Baumstamm wie in einer Warteschlange zu organisieren. Warteschlangen begegnet man innerhalb und außerhalb der Informatik immer wieder. Eine Warteschlange bietet dabei immer die prinzipiell gleiche Funktionalität:

* Wenn man ein Element einer Warteschlange hinzufügt, dann wird dieses hinten an die Schlange angehängt.
* Wenn man ein Element von einer Warteschlange entfernt, dann wird dieses vorne von der Schlange entfernt.

Man spricht in der Informatik auch vom FIFO-Prinzip \(first-in - first-out\). Das Element das zuerst in der Warteschlange ist, wird auch zuerst wieder entfernt.

Eine Warteschlange lässt sich z.B. dadurch realisieren, dass die Warteschlange das erste Element kennt, und jedes Element wiederum seinen Nachfolger kennt:

![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/warteschlange/WarteschlangeObjektdiagramm.png)

Besonders beachtenswert ist hier, dass eine Person eine andere Person kennt. Man spricht hier von einer rekursiven Beziehung oder reflexiven Beziehung, was im Klassendiagramm besonders deutlich wird:

![](http://inf-schule.de/content/programmierung/oopjava/beziehungen/platzda/warteschlange/RekursiveDatenstruktur.png)

**Aufgabe:** Entwerfe nachdem du Dir die generische Klasse `Queue` im Anhang angeschaut hast, ein Klassendiagramm für dein Projekt nach dem oben dargestellten Schema.

