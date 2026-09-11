# Niederschlagsdaten im Mathematikunterricht

Begleitmaterial zum Artikel **„Große Realdatensätze im Mathematikunterricht – vom Datenzugang zur Modellierung“** von Reimund Vehling.

Wie lässt sich untersuchen, ob ein Sommer besonders verregnet war? Das Repository verbindet die Erschließung realer Niederschlagsdaten des Deutschen Wetterdienstes (DWD) mit ihrer Beschreibung, stochastischen Modellierung und begründeten Beurteilung. Als Beispiel dient die Station **Hannover-Herrenhausen (Stationskennung 02011)**.

Enthalten sind vorbereitete Excel-Dateien, eine GeoGebra-Simulation, ein erläutertes Python-Notebook mit Arbeitsaufträgen sowie PDF-Dokumente, Grafiken und Quellennachweise. Die Materialien lassen sich je nach Lerngruppe, Fragestellung und verfügbarer Zeit unterschiedlich einsetzen.

## Schnell zu den Materialien

| Einstieg | Material |
| --- | --- |
| Niederschlagsdaten unmittelbar untersuchen | [Vorbereitete Excel-Auswertung](excel/niederschlag_auswertung_Hannover-Herrenhausen_02011.xlsx) |
| Rekorde und Anstiege durch zufällige Neuanordnung erkunden | [GeoGebra-Simulation im Browser](https://rveh.github.io/dwd-niederschlag/) |
| Datenzugang, Aufbereitung und Auswertung nachvollziehen oder eine andere Station wählen | [Python-Notebook mit Binder starten](https://mybinder.org/v2/gh/RVeh/dwd-niederschlag/main?labpath=notebooks%2FDWD_Niederschlag_Ebene1.ipynb) |
| Das Notebook ohne Ausführung lesen | [Notebook auf GitHub](notebooks/DWD_Niederschlag_Ebene1.ipynb) · [PDF-Fassung](pdf/DWD_Niederschlag_Ebene1.pdf) |
| Den begleitenden Beitrag lesen | [Artikel als PDF](pdf/dwd-niederschlag.pdf) |

## Mit Excel beginnen

Die [Excel-Dateien](excel/) ermöglichen einen Einstieg ohne Python-Programmierung:

- [Niederschlagsauswertung Hannover-Herrenhausen](excel/niederschlag_auswertung_Hannover-Herrenhausen_02011.xlsx): aufbereitete Daten für die Untersuchung der Niederschläge.
- [Modellierung der Jahressummen](excel/modellierung_jahressummen_Hannover-Herrenhausen_02011.xlsx): Ergebnisse des stochastischen Modellvergleichs.
- [DWD-Stationsübersicht](excel/stationsuebersicht_DWD.xlsx): Orientierung bei der Auswahl einer Messstation.

Zum Öffnen eine Datei auf GitHub auswählen und über die Download-Schaltfläche herunterladen. Die bereitgestellten Dateien dokumentieren einen bestimmten Datenstand; eine neue Notebook-Ausführung kann inzwischen hinzugekommene DWD-Daten einbeziehen.

## GeoGebra: Anstiege und Rekorde

Die [GeoGebra-Simulation](https://rveh.github.io/dwd-niederschlag/) lässt sich direkt im Browser öffnen. Sie veranschaulicht die zufällige Neuanordnung von Niederschlagswerten und die Untersuchung von Anstiegen und Rekorden.

Alternativ kann die [GeoGebra-Datei heruntergeladen](https://rveh.github.io/dwd-niederschlag/geogebra/RekordeAnstiegeSimulation.ggb) und in GeoGebra Classic geöffnet werden. Für die eingebettete Browseransicht werden eine Internetverbindung und aktiviertes JavaScript benötigt.

## Python-Notebook mit Binder ausführen

[![Mit Binder öffnen](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/RVeh/dwd-niederschlag/main?labpath=notebooks%2FDWD_Niederschlag_Ebene1.ipynb)

Binder öffnet eine ausführbare Arbeitsumgebung im Browser; eine lokale Python-Installation ist nicht erforderlich. Der Start kann mehrere Minuten dauern.

1. Binder über die Schaltfläche öffnen. Das zentrale Notebook `DWD_Niederschlag_Ebene1.ipynb` wird direkt aufgerufen.
2. Die einleitenden Erläuterungen und Einstellungen lesen. Für eine andere Messstation die Stationskennung an der vorgesehenen Stelle ändern.
3. Die Zellen der Reihe nach ausführen. Für einen vollständigen Durchlauf im Menü **Run → Run All Cells** wählen.
4. Neu erzeugte Excel-Dateien, Grafiken und Quellennachweise im Ordner `ausgabe/` der Arbeitsumgebung öffnen und bei Bedarf herunterladen.

**Binder-Sitzungen sind vorübergehend:** Änderungen am Notebook und neu erzeugte Dateien vor dem Beenden herunterladen. Sie werden nicht automatisch in diesem Repository gespeichert.

Das Notebook erläutert den Weg vom Datenzugang bis zum Urteil: Station auswählen, historische und aktuelle Daten laden, Daten prüfen und aufbereiten, Ergebnisse nach Excel exportieren, Niederschläge beschreiben und beobachtete Rekord- und Anstiegszahlen mit simulierten Vergleichsverteilungen untersuchen. Die Lernenden müssen die Verarbeitung nicht selbst programmieren; sie können die zugrunde liegenden Entscheidungen anhand der Erläuterungen und Ausgaben nachvollziehen.

### Optional: lokal ausführen

Wer mit einer eigenen Jupyter-Umgebung arbeitet, kann das Repository herunterladen und die benötigten Python-Pakete installieren:

```bash
python -m pip install -r requirements.txt
```

Anschließend `notebooks/DWD_Niederschlag_Ebene1.ipynb` in Jupyter öffnen und die Zellen der Reihe nach ausführen. Eine Jupyter-Umgebung wird hierbei vorausgesetzt; `requirements.txt` enthält die zusätzlichen Pakete für die Datenverarbeitung und Auswertung.

## Datenherkunft und Aussagekraft

Die Niederschlagsdaten stammen aus dem [Climate Data Center des DWD – tägliche Niederschläge](https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/daily/more_precip/). Die Messreihe für Hannover-Herrenhausen beginnt am **1. Januar 1931**; der verfügbare Endzeitpunkt hängt vom Datenstand beim Abruf ab.

Der Ordner [quellen/](quellen/) enthält die für den bereitgestellten Datenstand verwendeten Archive, die eingelesene Stationsübersicht und Nachweise zum Abruf. Die dokumentierten Zeiträume, Messlücken und Aufbereitungsentscheidungen sind bei der Interpretation zu berücksichtigen. Stationsdaten beschreiben zunächst den jeweiligen Messort; sie stehen nicht ohne Weiteres für ein ganzes Stadtgebiet.

Beim Modellvergleich werden vorhandene Jahreswerte zufällig neu angeordnet. Die simulierten Verteilungen dienen der Einordnung der beobachteten Rekord- und Anstiegszahlen. Sie erklären keine physikalischen Ursachen und liefern für sich genommen keinen Nachweis für oder gegen eine klimatische Veränderung.

## Aufbau des Repositorys

```text
README.md          Orientierung und Zugänge zu den Materialien
index.html         Browseransicht der GeoGebra-Simulation
requirements.txt   Python-Pakete für das Notebook
notebooks/         Zentrales Python-Notebook
excel/             Vorbereitete Excel-Dateien
geogebra/          GeoGebra-Datei zu Rekorden und Anstiegen
fig/               Erzeugte Grafiken als PDF
pdf/               Artikel und PDF-Fassung des Notebooks
quellen/           DWD-Archive, Stationsübersicht und Quellennachweise
```

Neue Notebook-Durchläufe legen ihre Ergebnisse separat unter `ausgabe/` an.
