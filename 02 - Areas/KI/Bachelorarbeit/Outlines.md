---
cssclasses: []
---
## Outline Methode
### Auswahl der zu untersuchenden Modelle
- Welche Forschungsmethode und warum? 
- Modelle die Untersucht werden
	- Donut
	- OCR + BERT
	- LayoutLMv3 
- Donut: Es gibt zwar jüngere Nachfolger wie DUBLIN, jedoch ist Donut schon etwas etablierter, es gab mehr Forschung und es steht mehr Code zur Verfügung
- OCR + BERT: Ist noch heute ein baseline Modell und gegen dieses wird in nahezu jedem AI-Paper, welches ein Modell präsentiert verglichen. Macht nicht mehr als OCR-Ergebnisse verbessern. Kurze Begründung warum das so ist.
- LayoutLMv3: Stark und etabliert. Ungefähr so alt wie Donut aber hat zwei Vorgänger. In FUNSD schneidet er deutlich besser ab als die meisten Modelle ohne OCR. Selbst in CORD ist es besser wo OCR-freie Modelle auch gut sind. Des weiteren ist LMv3 zwar OpenSource aber hat relativ strenge Lizenzbedingungen. (CC BY-NC-SA 4.0 DEED Attribution-NonCommercial-ShareAlike 4.0 International). Geforscht werden darf dennoch, solange es nicht kommerziell verwendet wird. Hier werden auch indirekte Vergleiche gezogen. Donut (Offen) vs LMv3 (Proprietär). OCR-frei vs. OCR-abhängig.
- Auswahl der Metriken: F1-Score, Accuracy, GPUh --> daraus können Kosten abgeleitet werden
- GPUh: Beziehen sich nur auf das Finetuning und evtl. auf die Inferrenz. Für alles was nicht ein Konzern ist wird es sehr schwierig sein genug Daten anzusammeln um ein eigenes Modell zu trainieren. 
- Accuracy: Standardmetrik, die aussagt https://medium.com/analytics-vidhya/accuracy-vs-f1-score-6258237beca2
- F1: Harmonisiert Recall und und Precision. Ist eine bessere Metrik für Fälle die inkorrekt identifiziert wurden
	- ![[Pasted image 20240404090042.png]]
- Recall: Metrik für die korrekt identifizierten Positives gegenüber allen vorhergesagten positiven Fällen. -> Nützlich wenn die kosten für Falsch-Positiv hoch sind
	- ![[Pasted image 20240404090132.png]]
- Precision: Proportion von korrekt identifizierten Positives zu allen tatsächlich positiven Fällen -> Nützlich wenn die kosten für Falsch-Negativ groß sind. 
	- ![[Pasted image 20240404090147.png]]
- Accuracy: Mist alle korrekt identifizierten Fälle gegenüber allen Fällen. -> Nützlich wenn beides wichtig
	 ![[Pasted image 20240404090059.png]]

### Forschungsdesign und Beschreibung 
#### Voraussetzungen
**Untersuchungsobjekt:** KI-Modell und seine Performance
**Beobachter:** Monitoring Tools
**Versuchsaufbau:** Wird folgend beschrieben 
**Untersuchungsvorgang:** Die folgenden Kapitel
Forschungsmethode ist das Experiment. Das Paper von Donut sagt, dass es viel besser sein kann als OCR-abhängige Modelle -> Verifizierung v.a. unter Bedingungen die nicht Benchmark-Datensätze sind sondern produktiv.
**Störfaktoren**: Tokenizer, NN wekches Embeddings produziert, Unterschiedliche Daten -> Gleiche Daten, Take from top damit die Daten im Finetuning, in der Vallidierung und im Test dieselben sind.
**Unabhängige Variablen:** Daten, Hyperparameter, Modell selbst 
**Abhängige Variable**: Modellperformance, Effizienz und Genauigkeit
Kritische Betrachtung: ML-Algorithmen v. a. NNs sind nicht deterministisch. Wir haben eine Art statistisches rauschen, welches du nicht weg kriegst.

#### Durchführung
**Hypothesen:**
- Eine höhere Menge an Daten erhöht die Performance der Modelle (exklusive BERT da nur Verbesserung) mit abflachender Wirkung tendenziell sogar abfallend bei overfitting
- Bei Heterogenen Daten erzielt Donut bessere Ergebnisse als LMv3 und BERT in der Informationsextraktion
- Die Qualität der vorgelagerten OCR beeinflusst die Ergebnisse von LMv3 und BERT.
Kapitel um Hypothesen und wie diese beantwortet werden

[Operationalisierung](https://www.bachelorprint.de/methodik/operationalisierung/) (Messbarkeit der Begriffe)
Stichprobe: Bedingt möglich da wenige Daten. Daten sind im Endeffekt die Stichprobe. Diese muss gleich bleiben.

Wie werden die **Gütekriterien** gewährleistet?
**Validität** es werden die Metriken entsprechend den oben beschriebenen Formeln verwendet und daran bemessen. Die GPUh werden durch das selbe Monitoring tool gemessen
**Reliability** Zuverlässig: Es ist algorithmisch, so ist zumindest zu einem Großteil das Ergebnis reproduzierbar. Statistisches Rauschen müssen wir in kauf nehmen. 
**Objektivität** Test der Pipeline durch mehrere Personen. U.a. nicht nur auf dem Rechenknecht sondern auch auf Azure

### Testumgebung
Maschine mit genug Leistung. (Spezifikation abseits der GPU im Anhang) 
Datensätze aus dem produktiven Umfeld von ELO. Es wird darauf geachtet, dass die Daten heterogen sind, v.a. in ihren Inhalten, also nicht nur Adresse eines Unternehmens. Die Daten werden aufgrund begrenzter Daten von Azure annotiert. Wichtig ist zu beachten, dass die Qualität eingeschränkt. Diskussion in Kapitel später. Testdaten sind händisch notiert, um hohe Ground-Truth zu gewährleisten. Problem, wenn Testdaten auch OCR wären. Um Daten von Kunden zu verwenden -> Anonymisierung. Kleines Beispiel

### CRISP DM
Erwähne das Ding