# Natural-Language-Processing
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/beckceline/Natural-Language-Processing/HEAD)

In diesem NLP Projekt werden wir versuchen Yelp Reviews in 1 Stern oder 5 Sterne Kategorien zu klassifizieren. Dazu nutzen wir den Text ihrer Bewertung. 

### Schritte

Zu Beginn des Projekts laden wir einen Yelp-Datensatz von Kaggle, der Bewertungen von Geschäften und Restaurants enthält. Jede Zeile des Datensatzes repräsentiert eine Bewertung, die von einem Nutzer für ein bestimmtes Geschäft abgegeben wurde. Die Spalte "stars" enthält die Anzahl der Sterne (von 1 bis 5), die der Bewerter dem Geschäft gegeben hat. Wir verwenden diese Sterne als Grundlage für unsere Klassifikation. Darüber hinaus gibt es weitere Spalten wie "cool", "useful" und "funny", die Informationen über das Feedback der anderen Nutzer zu dieser Bewertung enthalten. Alle Bewertungen bspw. starten mit 0 "Cool"-Votes und es gibt nach oben kein Limit. Je mehr Leute die Bewertung "Cool" finden und sie so voten, desto höhere die Anzahl.

1. Explorative Datenanalyse: Unsere erste Aufgabe besteht darin, den Datensatz zu erkunden und ein besseres Verständnis für die Daten zu gewinnen. Dazu führen wir verschiedene Schritte durch, darunter das Erstellen von Histogrammen der Textlängen, Boxplots für die Verteilung der Textlängen in den verschiedenen Sterne-Kategorien und die Berechnung von Durchschnittswerten für numerische Spalten in Bezug auf die Sterne.

2. NLP Klassifizierungsaufgabe: Nun konzentrieren wir uns auf die eigentliche Aufgabe: die Klassifizierung der Bewertungen. Zuerst erstellen wir einen neuen DataFrame, der nur Bewertungen mit 1 oder 5 Sternen enthält, da wir uns auf besonders negative und positive Bewertungen konzentrieren möchten.
Danach verwenden wir die Textinhalte der Bewertungen (Spalte "text") als unsere unabhängige Variable X und die Sterne (Spalte "stars") als unsere abhängige Variable y. Diese Daten werden für das Training und die Evaluierung unseres Modells verwendet.
Unser erstes Modell verwenden wir auf Basis des Naive Bayes Algorithmus. Wir transformieren den Text mithilfe des Count Vectorizers und teilen die Daten in Trainings- und Testsets auf. Nach dem Training und der Vorhersage des Modells evaluieren wir die Leistung mit Hilfe einer Confusion Matrix und eines Classification Reports.

3. Integration von TF-IDF: Um zu sehen, wie sich die Integration von TF-IDF (Term Frequency-Inverse Document Frequency) auf die Modellleistung auswirkt, verwenden wir eine Pipeline, die eine Kombination aus Count Vectorizer, TF-IDF Transformer und Naive Bayes enthält. Wir trainieren und evaluieren dieses Modell erneut, um festzustellen, ob TF-IDF eine Verbesserung bringt.

### Ergebnis

Am Ende des Projekts haben wir erfolgreich ein Modell entwickelt, das anhand von Yelp-Bewertungen zwischen "1 Stern" und "5 Sterne" unterscheiden kann.
