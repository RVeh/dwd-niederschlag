# Wetterdaten mit Python – Niederschlag analysieren

Ein interaktives Notebook-Projekt zur Analyse von Niederschlagsdaten des DWD mit Python.

Der Aufbau ist bewusst **linear und dokumentiert**:  
Daten laden, prüfen, aufbereiten, auswerten und visualisieren – Schritt für Schritt in einem Notebook.  

Das Repository ergänzt den Artikel **Große Realdatensätze im Mathematikunterricht - vom Datenzugang zur Modellierung** von Reimund Vehling. Es enthält eine GeoGebra-Datei, ein Python-Notebook begleitende PDF-Dokumente, Grafiken und zusätliches Material zu den Quellen (DWD).

---

## Direktstart mit Binder – kann etwas dauern

[![launch binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/RVeh/dwd-niederschlag/HEAD)

Nach dem Start im Menü **Run → Run All Cells** ausführen.

---

## Inhalt

Das Projekt besteht aus einem zentralen Notebook mit dokumentierter Schrittfolge, unter anderem zu:

- Laden von Wetterdaten
- Entpacken und Einlesen
- Aufbereitung der Daten
- Analyse von Niederschlagswerten
- Erzeugung von Grafiken
- optionalem Export von Ergebnissen

---
# Geogebra im Mathematikunterricht 

## GeoGebra

Die GeoGebra-Simulation kann über die
[gemeinsame Auswahlseite](https://rveh.github.io/dwd-niederschlag/)
direkt im Browser geöffnet werden.

## Materialien
Im Ordner `pdf` befinden sich PDF-Dateien zu einzelnen Inhalten.


## Dateistruktur

```text
README.md
requirements.txt
.gitignore

notebooks/
    wetterdaten_niederschlag.ipynb

fig/
excel/
pdf/
daten/
