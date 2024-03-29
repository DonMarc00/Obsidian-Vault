Grundidee: Zweidimensionale Matrizen werden eingespeist
Aus jeder Matrix werden nur die relevantesten Features extrahiert

Informationsverdichtung: Feature Learning
Erfolgt mit Filter-Matrix --> Sucht nach relevantesten Pixeln, die das Filter-Fenster am ehesten definieren
**Schrittgröße s und Filtergröße k**
in dem Fall s=1 und k=3
Ergebnisse des Feature-Leranings werden in eine Feature Map eingetragen:
![[Pasted image 20240205195000.png]]

Mit dem Filter **verstärken und verkleinern** wir Muster --> Convolution bzw. Faltung
Damit dabei nicht zu schnell zu viele Informationen verloren gehen verwenden wir Padding, um eine Feature-Map so groß wie die Input-Matrix zu erhalten. 
![[Pasted image 20240205201531.png]]
Filter und Padding wird für verschiedene Feature-Filter wiederholt

![[Pasted image 20240205201805.png]]

Nächster Schritt: Pooling
Für effiziente Verarbeitung ist es wichtig, das Datenvolumen vor der Vorhersagephase zu verdichten

**Max Pooling** statt Skalarprodukt wie im Filter
**Beim pooling gilt meist s=k**
Resultat ist die **Down-Sampling-Matrix**
Padding bietet sich an, damit die Randwerte auch mitgenommen werden. Hier Identitätsfunktion
In der Praxis häufig mehrere Down-Sampling Schritte und Feature-Filtering
![[Pasted image 20240205202613.png]]

**Flattening um aus Matrizen Vektoren zu machen**
![[Pasted image 20240205202759.png]]

**Vorteile:**
- Verdichtung (Faltung) und Verkleinerung (Pooling)
- Abstraktion von der Position eines Objektes innerhalb eines Bildes (Wo-Information wird entfernt, Konzentration auf was)