# Keep or throw II

## Schwächen der Modellierung

Die Stapel-Klasse und das Spiel sind soweit funktionsfähig. Soll die Stapelklasse außerhalb des Spiels nicht wieder benutzt werden, ist die Modellierung auf die obige Art auch in Ordnung. Prinzipiell besitzt sie aber zwei Nachteile:

1. Man hat Funktionalität in eine Klasse verlagert, die rein logisch dort nicht hin gehört: Eine Karte besitzt von der eigentlichen Logik keinen Nachfolger. Um auch andere Objekttypen analog auf einen Stapel zu legen, müsste man immer ein `next`-Attribut einführen.
2. Die Stapel-Klasse muss für andere Anwendungen immer angepasst werden. Die Funktionalität bleibt gleich, aber die Datentypen müssen geändert werden. Falls das `next`-Attribut der zu stapelnden Objekte einen anderen Namen hat, muss auch dieser geändert werden.

Insgesamt ist der Entwurf also richtig, lässt sich aber nicht direkt für andere Projekte wiederverwenden.

## Generische Klassen

Um die oben genannten Schwächen zu umgehen und die Stapel-Klasse auch für andere Projekte nutzen zu können ohne die _Typsicherheit_ in Java aufzugeben, verwendet man sogenannte **generische Klassen** oder **parametrisierte Klassen**. Der Begriff _generische Klasse_ ist etwas geläufiger, der Begriff _parametrisierte Klasse_ beschreibt das Konzept aber deutlicher. Eine generische oder parametrisierte Klasse erhält einen Typ-Parameter, der innerhalb der Klasse benutzt werden kann. Der Typ-Parameter wird in spitzen Klammern hinter den Klassennamen geschrieben und kann dann innerhalb der Klasse wie ein konkreter Datentyp benutzt werden.

## Aufgabe

Nimm die erste Version des _Keep or throw_-Spiels als Grundlage und vollziehe die Erklärungen nach, indem Du dieses selbst so anpasst, dass es die generische Klasse Stack für NRW \(siehe Anhang\) verwendet.

