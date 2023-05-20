# HUK - Coding Challenge

## Einleitung
Dieses Projekt umfasst die Entwicklung und den Einsatz eines Random Forest Classifiers zur Vorhersage der Kundenaffinität zum Kauf einer KFZ-Versicherung. Der Random Forest Classifier ist ein leistungsstarker Machine Learning-Algorithmus, der in der Lage ist, komplexe Muster in den Daten zu erkennen und präzise Vorhersagen zu treffen.

## Modellbeschreibung
Der Random Forest Classifier ist ein Ensemble-Lernalgorithmus, der aus einer Kombination von Entscheidungsbäumen besteht. Jeder Entscheidungsbaum wird auf einem zufälligen Unterdatensatz der Gesamtdaten trainiert und liefert eine individuelle Vorhersage. Die Vorhersagen der einzelnen Bäume werden kombiniert, indem eine Mehrheitsentscheidung getroffen wird (im Fall der Klassifikation) oder durch eine Durchschnittsbildung (im Fall der Regression). Dieser Ansatz ermöglicht es dem Modell, eine hohe Flexibilität und Robustheit zu erlangen, da die Vorhersagen auf einer Vielzahl von unterschiedlichen Entscheidungsbäumen basieren.

## Datenbeschreibung
Das Projekt verwendet drei separate Datenquellen für die Vorhersage der Kundenaffinität zum Kauf einer KFZ-Versicherung:

1. 'alter_geschlecht.csv':
- ID: ID des Kunden
- Geschlecht: Geschlecht des Kunden
- Alter: Alter des Kunden in Jahren

2. 'rest.csv':
- ID: ID des Kunden
- Fahrerlaubnis: Gibt an, ob der Kunde eine Fahrerlaubnis hat (Ja=1)
- Regional_Code: Eindeutiger Code für die Region des Wohnorts des Kunden
- Vorversicherung: Gibt an, ob der Kunde bereits eine Kfz-Versicherung hat (Ja=1)
- Alter_Fzg: Alter des Fahrzeugs
- Vorschaden: Gibt an, ob der Kunde bereits einen Schaden am Fahrzeug hatte (Ja=1)
- Jahresbeitrag: Erwarteter Versicherungsbeitrag bei Abschluss in Euro
- Vertriebskanal: Code für den Vertriebskanal
- Kundentreue: Anzahl der Tage seit dem Zeitpunkt, ab dem eine Kundenbeziehung mit dem Kunden besteht

3. 'interesse.csv':
- ID: ID des Kunden
- Interesse: Gibt an, ob der Kunde an einem Angebot interessiert ist (Ja=1) [Zielvariable]

## Projektstruktur
- data/input_data: Enthält die bereitgestellten Daten für die Coding Challenge
- data/raw_data: Enthält die bereitgestellten Daten als einzlene CSV
- data/clean_data: Enthält die bereitgestellten Daten mit grundlegenden Datenbereinigungen
- data/encoded_data: Enthält die bereitgestellten Daten mit Encodings für die kategorischen Spalten.
- models/: Enthält das trainnierte Random Forrest Classifier Modell mit Timestamp.
- src/: Enthält das Jupyter Notebook mit dem Code für das Projekt.
- .gitignore: Enthält alle Strukturen, die Git ignorieren soll.
- eda_output.html: Enthält die Ergebnisse der  explorativen Datenanalyse (EDA).
- environment.yml: Enthält die Konfiguration für die Conda-Umgebung.
- README.md: Enthält die Projektbeschreibung und Anleitung.

## Vorraussetzungen
Um das Projekt auszuführen, müssen Sie zunächst sicherstellen, dass die folgenden Abhängigkeiten installiert sind:
- Anaconda: (Download und Installationsanleitung)[https://www.anaconda.com/download]

## Installation
1. Klonen Sie das Projekt-Repository auf Ihrem lokalen Computer.
`git clone https://github.com/pmherp/huk_proj.git`

2. Navigieren Sie in das Projektverzeichnis.
`cd huk_proj`

3. Erstellen Sie die conda-Umgebung aus der bereitgestellten environment.yml-Datei.
`conda env create -f environment.yml`

4. Aktivieren Sie die erstellte conda-Umgebung.
`conda activate huk_coding_challenge`

## Verwendung
Öffnen Sie das Jupyter-Notebook "coding_challenge.ipynb", um den Code auszuführen.
