### Natürliche Neuronen
**Axon:** Leitet Signale weiter

**Dendriten:** Erhalten Signale von Vorgängern
Schwellspannung bei Axon. Wenn diese übertroffen wird feuert das Axon.

**Synapsen:** Dienen zur Übertragung von Impulsen zwischen Neuronen und arbeiten **unidirektional**
Sie können Zielzellen aktivieren oder hemmen
Können Übertragungsstärke verändern **(=synaptische Plastizität)**. Beeinflussbar durch die Anzahl der Neurotransmitter oder das Herabsetzen der Aufnahmefähigkeit der Rezeptoren. **Plastizität** entscheidender Faktor bei der Lernfähigkeit
Erhöhung: Potenzierung
Verringerung: Depression

**Aktivierungsfunktion Perceptron**

Sigmoid:
![[Pasted image 20240204215706.png]]
$$
y = \frac{1}{1+e^{-x}}
$$
Nicht um 0 zentriert.
Bei 1. Ableitung für große Werte nur noch sehr kleine Steigung aus.

TanH, ReLU und Leaky-ReLU beheben diese Probleme
![[Pasted image 20240204215921.png]]

### Aufbau Künstliches Neuron
![[Pasted image 20240204215951.png]]![[Pasted image 20240204220031.png]]

## Fehlerminimierung
Soll - Ist
|Soll -Ist| --> Immer positiv
$(Soll-Ist)^2$ --> Für kleiner Schritte nur noch kleinere Werte

Um Fehler zu minimieren --> Ableiten. Erste Ableitung um Extrempunkt zu bestimmen. Zweite Ableitung um Art zu bestimmen (Min, Max)

In einem Netz kennen wir nur den Output, also müssen wir die Fehlerkorrektur vom Output zum Input durchreichen und dabei Gewichte anpassen --> **Backpropagation**
Wie führe ich diese für mehrdimensionale Berechnungen durch?

### Gradientenabstiegsverfahren

**Gradientenabstiegsverfahren (Verfahren des steilsten Abstiegs** --> Iterative Methode um Fehler zu minimieren
**Gradient:** Veränderung (Ableitung) einer mehrdimensionalen Funktion

Verfahren. Steigungen um einen Startpunkt werden berechnet. Heuristik: Steilster Abstieg führt vermutlich in ein Minimum -> Punkt in diese Richtung bewegen und wiederholen.

Ein Vektor der die Ableitungen aller Dimensionen darstellt

![[Pasted image 20240204232855.png]]

Gradientenvektor zeigt stärkste Steigung daher mit -1 multiplizieren

Gesucht ist die Änderung des Fehlers E wenn sich die Gewichte $w_{i,j}$ verändern:
![[Pasted image 20240204233012.png]] ^a4dc76

Die gesuchte Gewichtkorrektur lautet damit:
![[Pasted image 20240204233049.png]]

Um [[#^a4dc76|das Ding]] zu Differenzieren wird benötigt:
- Die partiellen Ableitungen der Fehlerfunktion für jedes Gewicht
- Kettenregel weil E im Zähler von Output Oj abängt, die wiederum von den Gewichten wij
![[Pasted image 20240204233351.png]]![[Pasted image 20240204233403.png]]
![[Pasted image 20240204234013.png]]
#### Nachteile
- Es wird nicht zwingend das globale Minimum gefunden
- Es können lange Umwege in Kauf genommen werden
- Lösungsansätze: Ändern der Lernrate oder setzten verschiedener Startpunkte