## Phasenmodell überwachtes lernen
1. Datengenerierung --> Trainings- & Testdatengenerierung, Features, Labels, Normierung
2. Netzdesign --> Topologie, Anzahl Knoten und Schichten, Aktivierungsfunktion, Initialgewichte
3. Training --> Überwachtes Training mit Backpropagation & Performance-Messung, ggf. Feintuning
4. Test --> Performance-Messung mit Testdaten
5. Anwendung --> Anwendung des Modells auf unbekannte Daten

### 1. Datengenerierung
Feature (Merkmale) sind Inputdaten, Labels (Markierer) sind due gewünschten Outputs
Für Self-supervised Learning können Labels entfallen.

Durch Wrapper-Methoden können Feature entfernt oder hinzugefügt werden und es wird geprüft, wie sich dadurch die Netz-Performance verändert. Auch Filtermethoden sinnvoll z.B. fliegen Feature mit vielen Leerwerten oder hoher Korrelation zu anderem Feature raus

Qualität der Daten mit wenig Leerwerten
Genügend Daten

### 2. Netzdesign
Für jedes Element im Eingabetupel genau ein Knoten: Für 28x28px Bild braucht man 784 Knoten Input.

Unterschiedliche Probleme, unterschiedliche Topologien.
Bsp. Transformer, Rekurrente Netze (Für Sequenz), konvolutionale Netze (Bild und Audio)

Zu viele Hidden-Layers --> Overfitting aka. das Ding lernt Zusammenhänge, die keine Relevanz haben
Zu wenigen HL --> Nicht genug Kapazität zum lernen von komplexen Zusammenhängen

In ersten Schichten werden Basics des Problems gelernt, in tieferen schichten die komplexen Zusammenhänge. In tieferen Schichten höhere Abstraktion also verdichtete Information

Zu kleine Gewichte --> Lange Trainingszeiten
Zu groß --> explodierende Gradienten, Gradientenabstiegsverfahren oszilliert um Minimum, Netz liefert keine guten Outputs
**Als Gewichte positive und negative Anfangsgewichte die für jede Schicht mit Mittelwert Null folgen**

Aktivierungsfunktion wählen

### 3. Training
▪ Überwachtes Lernen (supervised learning)
▪ Unüberwachtes Lernen (unsupervised learning)
▪ Bestärkendes Lernen (reinforced learning)

**Pass:** Vollständiger durchlauf eines Samples bestehend aus Propagation, Fehlerberechnung, Backpropagation und Gewichtsanpassung
**Batch:** Reihe von Instanzen werden zu einem Batch zusammengefasst und gemeinsam durch das Netz propagiert bevor die Gewichtsanpassung vorgenommen wird.
**Iteration:** Vollständiger Durchlauf eine Batches durch das Netz
**Epoche** Vollständiger durchlauf des gesamten Trainingsdatensatzes

### 4.Test
Testen mit Daten die noch nicht gesehen wurden --> Eigener Datensatz
Es kann sein, dass Netz auf neue Eingabe schlechter reagiert --> Noch nicht ausreichend generalisiert.

### 5. Anwendung (Inferenzphase)
Netz lernt nicht mehr (Ausnahme: Transformer)
Feintuning (möglich)

## Unsupervised learning
▪ keine Zielvariable
▪ Training auf Mustererkennung, nicht auf Ergebnisvorhersage
▪ Datensatz hat nur Features, keine Labels
▪ Suche nach Ähnlichkeiten in den Features
▪ kein eigenes Erkennen, was gelernt wurde, keine Interpretation der Zusammenhänge
▪ Interpretation anschließend in getrennter Analysephase (Beispiel: Tier-Clustering)

**Clustering:** Szenario-Management
**Anomalieerkennung:** Nebeneffekt des Clustering: Anomalien können erkannt werden
**Assoziationsanalyse:** Finden von Abhängigkeiten und Korrelationen in einem Datensatz
**Dimensionsreduktion:** Komplexität von Datensätzen zu reduzieren, indem korrelierte Features entfernt werden 

In NN unsupervised learning in seiner reinen Form nicht möglich
Alternative Verfahren zur Gewichtsanpassung

Hebb'sche Lernregel: $\Delta w_{ij}=n * a_{i}*a_{j}$  --> Zwei Neuronen stärken Verbindung, je mehr sie Feuern

## Self-supervised Learning
Self-supervised learning steht zwischen überwachtem und unüberwachtem Lernen.

▪ Einsatz vor allem bei Bild-, Sprach- und Videoverarbeitung und bei generativer KI.
▪ Kernidee: Labels werden selbst erzeugt.
▪ Hintergrund: Labeling aufwändig und teuer (Beispiel: Medizin)
▪ Label-Erzeugung i.d.R. durch Maskieren. (Beispiel: maskierte Worte in Eingabe-Satz)
▪ Kein vorab gelableter Datensatz notwendig => Analogie zum „unsupervised“ Modus.
▪ Abgleich Vorhersagewert mit maskiertem Sollwert und Fehlerermittlung => Analogie zum 
„supervised“ Modus.

## Reinforcement Learning
Agent lernt alleine durch Interaktion mit seiner Umwelt.

- Es gibt einen bestimmten Endzustand
- Der Agent wird auf dem Weg zum Endzustand belohnt für jede Aktion die er durchführt --> Agent will Belohnung maximieren
- Keine Fehlerfunktion sondern Gewinnfunktion zu maximieren
- Lernt durch ausprobieren

**Komponenten:**
- Umwelt
- Agent der mit Umwelt interagiert
- Endliche Anzahl von Aktionen die Agent ausführen kann um mit Umwelt zu interagieren --> Policy: Verfahren nachdem der Agent nächste Aktion auswählt
- Fest definierte Zustände -> Jede Aktion versetzt Agent in Zustand
- Belohnungen

**Gut geeignet für:**
Steuerungsprobleme, Optimierungsaufgabe (Ameisenkolonie), Monitoring
Alles wo Trial-and-Error angewandt werden kann
Klares Regelwerk vorhanden (Schach)
Problem in simulierte Umgebung übertragbar

Beschrieben durch **Markov Decision Process** $(Z,A,p,P_{o})$ 
Z: Menge an Zuständen
A: Menge an Aktionen
p: Policy
$P_{o}$: Startverteilung

Zwei Probleme:
- Wie hoch Belohnung
- Wie muss Policy aussehen
--> Q-Learning mit Q-Tabellen

Q: Qualität und **Q-Wert** sagt aus, wie sinnvoll eine bestimmte Aktion in einem bestimmten Zustand ist

Nach jeder Aktion müssen Q-Werte angepasst werden
**Formel die uns für jeden Zustand und jede in diesem Zustand mögliche Aktion eine Aktualisierung des Q-Wertes für diese Aktion erlaubt:**
$$
Q_{neu}(Z_{t},a_{t})=Q_{alt}+\Gamma*Q_{max}(Z_{t+1}) 
$$
Zt  = aktueller Zustand (Zeitpunkt t) 
Zt₊₁ = Folgezustand (Zeitpunkt t+1) 
at   = aktuelle Aktion
Qact = aktuelle Belohnung für Aktion at im aktuellen Zustand Zt lt. Policy
ϒ    = Verzögerungsrate Gamma. Steuert, wie weit spätere Belohnungen mit in die Berechnung 
einfließen.
- Bei ϒ = 0 schaut der Agent nur auf die unmittelbare Belohnung im aktuellen Schritt, die Lernrate ist sehr niedrig. Bei ϒ = 1 schaut der Agent auf alle Belohnungen aller Folgeschritte. Die  Belohnungen werden dann irrelevant, da jeder gewählte Weg irgendwann zum Ziel führt; alle  Belohnungen stünden auf dem max-Wert. In der Praxis haben sich ϒ-Werte zwischen 0,9 und 0,99 bewährt.
Qmₐₓ = höchster Q-Wert des Folgezustands lt. Policy = max (Q(Zt₊₁ , a₁), Q(Zt₊₁ , a₂), … , Q(Zt₊₁ , 
an))
- mit n = Anzahl der maximal verfügbaren Aktionen
