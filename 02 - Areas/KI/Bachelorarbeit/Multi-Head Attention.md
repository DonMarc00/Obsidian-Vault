Head: Eigenständige Einheit innerhalb des Attention-Mechanismus, die unabhängig Queries, Keys und Values verarbeitet, um eine eigene Version der Attention-Gewichtung zu berechnen.

Multi-Head: Prozess wird häufiger parallel durchgeführt, wobei jeder "Head" möglicherweise unterschiedliche Aspekte der Daten erfasst, indem er auf verschiedenen Repräsentation der Eingabe arbeitet.

**Diversifizierung:** Jeder Head kann potenziell unterschiedliche Beziehungen zwischen den Eingabedaten erfassen. 

**Reichhaltige Repräsentation:** Durch die Kombination der Ergebnisse aus mehreren Heads kann das Modell eine reichhaltigere, multidimensionale Repräsentation von Daten erzeugen, was zu besseren Leistungen bei einer Vielzahl von Aufgaben führt

## Scaled Dot-Product Attention:
- Um die Attention Gewichte zu erhalten Scaled dot-product
- Dot-product schneller wegen Matrix-multiplication code
- Scale weil bei großer Dimensionalität $d_{k}$ wird die Softmax Funktion in Regionen von extrem kleinen Gradienten. Um dies zu vermeiden Skalierung: $\sqrt{d­_{k}}$ 

**Query:** Die Query (Q) repräsentiert das Element (z.B. ein Wort in einem Satz), für das das Modell den Kontext verstehen möchte. Es ist wie eine Anfrage, die das Modell an alle anderen Wörter im Satz richtet, um herauszufinden, wie relevant sie für das aktuelle Wort sind.

**Key:** Der Key (K) repräsentiert jedes Element in der Eingabesequenz, gegenüber der die Queries abgeglichen werden. Der Key hilft dem Modell zu entscheiden, wie relevant jedes andere Wort (oder Element) im Kontext des aktuellen Wortes (oder Elements) ist.

**Value:** Der Value (V) ist der Inhalt (oder die Repräsentation) jedes Elements in der Eingabesequenz. Nachdem das Modell mithilfe der Queries und Keys festgestellt hat, wie relevant jedes Element für das betrachtete Element ist, werden die Values gewichtet und aggregiert, um einen neuen Repräsentationsvektor für das betrachtete Element zu erzeugen. Dieser Vektor ist eine Kombination der Informationen, die basierend auf ihrer Relevanz ausgewählt wurden.