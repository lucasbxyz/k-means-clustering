# K-Means Clustering – US Universities

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/lucasbxyz/k-means-clustering/HEAD)

Anwendung von K-Means Clustering, um US-Universitäten anhand von Features wie Studiengebühren, Einschreibungszahlen und Abschlussquote in zwei Cluster (privat vs. öffentlich) zu gruppieren — ohne die tatsächlichen Labels beim Training zu verwenden.

## Ausführung

1. Auf den **Binder Badge** oben klicken — die Umgebung startet automatisch.
2. Im Jupyter-Interface das Notebook `3-K_Means_Clustering_Projekt.ipynb` öffnen.
3. **Cell → Run All** ausführen (oder Zellen einzeln mit Shift+Enter durchlaufen).
4. Die Ausführung dauert ca. 1–2 Minuten.

## Erwartete Ergebnisse

- **Explorative Analyse:** Scatterplots und Verteilungen der University-Features (Graduation Rate, Room.Board, Outstate-Tuition etc.).
- **K-Means mit K=2:** Clustering der Universitäten in zwei Gruppen.
- **Vergleich mit echten Labels:** Classification Report, der die Cluster-Zuordnung mit den tatsächlichen Private/Public-Labels abgleicht (ca.):

| Metrik    | Klasse 0 (Public) | Klasse 1 (Private) |
|-----------|-------------------|-------------------|
| Precision | 0.21              | 0.31              |
| Recall    | 0.65              | 0.06              |
| F1-Score  | 0.31              | 0.10              |

- **Gesamtgenauigkeit:** ca. **22 %** — das zeigt, dass ein unsupervised K-Means nicht direkt die Private/Public-Unterscheidung lernt, da die Cluster-Struktur nicht den Labels entspricht. Das ist erwartetes Verhalten für unüberwachtes Lernen.

## Dateien

| Datei | Beschreibung |
|-------|-------------|
| `3-K_Means_Clustering_Projekt.ipynb` | Jupyter Notebook mit der Analyse |
| `College_Data` | Datensatz mit US-Universitätsdaten |
| `requirements.txt` | Python-Abhängigkeiten für Binder |
