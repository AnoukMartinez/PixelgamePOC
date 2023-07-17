# PixelgamePOC
Schnelles Konzept in dem ich statt freiem Spieler Movement die Bewegung auf eine HTML Tabelle beschränke.

Wir haben jetzt statt freien Koordinaten eine HTML Tabelle. Wenn ihr das Repo klont und dann das Projekt mit node app.js startet, solltet ihr ein 9x9 Spielbrett sehen
auf dem ihr euch mit WASD frei bewegen könnt. Ihr könnt nicht über die Ränder, und nicht in die Beet rein, aber wenn ihr vor einem Beet steht und E drückt wird dieses Beet gelb.

So wie funktioniert das Ganze?

### html body
In der HTML File wird die Tabelle zunächst definiert, jede Zelle hat eine ID so wie in einem Array. Hier habe ich die in der Form [Zeile][Spalte] gemacht,
aber ich hätte das auch hello-test-(Zeile)-(Spalte) machen können.
Manche Zellen haben bestimmte class Attribute, die sie von anderen Zellen unterscheiden. 
Beispielsweise haben wie eine beet class. Diese Zellen sollen die Beete darstellen, auf Kollisionen reagieren (Indem der Spieler nicht in die hereinrennen kann), 
und interagierbar sein (Sprich, wenn der Spieler sich vor einem Beet befindet und 'E' drückt, kann er den Status des Beets verändern). In der CSS File
werden alle Zellen mit der Klasse beet braun gemacht.

### Script
Im Script Teil wird wie in unserem tatsächlichem Projekt bisher gecheckt, welcher Key gedrückt wird (Ich habe die Steuerung hierbei zu WASD geändert weil's mehr
Sinn mit Interagieren auf E gemacht hat). Je nachdem wird dann die momentane Zelle wieder Grün, und die Zelle in die wir uns bewegen wird rot.
Später könnte man vielleicht statt einer roten Zelle ein kleines Bild der Spielers oder so etwas einfügen.

Notizen:

In der Tabelle haben die Beete neben dem beet class Attribut zusätzlich noch ein Nummer Attribut. Das sind Überbleibsel von etwas, das ich ausprobiert hatte.
Ich überlege noch, wie man den Beeten jeweils eine Nummerierung geben kann, und dann seperat trackt welches Beet vor wie langer Zeit bepflanzt wurde. Hmm.
