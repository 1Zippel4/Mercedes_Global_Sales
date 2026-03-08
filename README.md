## Datenquelle
Der Datensatz stammt von Kaggle:

Dhrubang Talukdar (2025).
**Mercedes Global Car Sales (2020–2025)**

https://www.kaggle.com/datasets/dhrubangtalukdar/mercedes-global-car-sales-2020-2025

Die Daten wurden lokal heruntergeladen und im Ordner `input/raw` gespeichert.
Für die Analyse wurde eine aufbereitete Version im Ordner `input/processed` erzeugt.



─Mercedes_Global_Sales
│   │   01_EDA_Mercedes_Global_Sales.ipynb
│   │   02_Regressionsbaum.ipynb
│   │   03_Multiple_Regression.ipynb
│   │   README.md
│   │
│   ├───docs
│   │       01_EDA_Mercedes_Global_Sales.pdf
│   │       02_Regressionsbaum.pdf
│   │       03_Multiple_Regression.pdf
│   │       Mercedes_Sales_Profiling.html
│   │
│   ├───input
│   │   ├───processed
│   │   │       mercedes_sales_processed.csv
│   │   │
│   │   └───raw
│   │           mercedes_benz_sales_2020_2025.csv
│   │
│   └───output
│       └───figures
│           ├───eda
│           │       01 Verteilung mit Quantilbereichen.png
│           │       02 Base Price vs Horsepower PS.png
│           │       03 Durchschnittspreis je Horsepower PS.png
│           │       04 Verteilung Horsepower PS.png
│           │       05 Base Price nach Modell Top 10.png
│           │       06 Preis je Fuel Type Median.png
│           │
│           └───modeling
│               ├───multiple_regression
│               │       01 Durchschnittliche Vorhersage pro Preisgruppe.png
│               │       02 Residual Plot.png
│               │       03 Histogramm der Residuen.png
│               │
│               └───regressionsbaum
│                       01 Relative Merkmale - Top 10.png
│                       02 Regressionsbaum Ausschnitt bis Tiefe 3.png
│                       03 Prognose vs Realität Stichprobe 10000.png


## Ziel der Analyse
Ziel dieser Analyse ist die Untersuchung der Preisstruktur von Mercedes-Benz Fahrzeugen im Zeitraum von **2020 bis 2025**.  
Im Mittelpunkt steht die Frage, **Welche Fahrzeugmerkmale den Basispreis beeinflussen**.

Die Analyse kombiniert explorative Datenanalyse mit statistischen und maschinellen Lernverfahren.


## Datensatz
Der Datensatz enthält Informationen zu Mercedes-Benz Fahrzeugen mit folgenden Variablen:

- Modellreihe
- Baujahr
- Region
- Farbe
- Kraftstofftyp
- Motorleistung (Horsepower)
- Turboaufladung
- Basispreis in USD

Datensatzgröße: **ca. 12 Millionen Beobachtungen**


## Analyseablauf
Die Analyse ist in drei Notebooks gegliedert.


### 1 Explorative Datenanalyse
Notebook:  
`01_EDA_Mercedes_Global_Sales.ipynb`

Inhalte:

- Struktur und Größe des Datensatzes  
- Datentypen der Variablen  
- Preisverteilungen  
- Zusammenhang zwischen Preis und Motorleistung  
- Analyse der Preisstruktur nach Modell und Kraftstofftyp  

Ziel:  
Grundlegendes Verständnis der Daten und möglicher Einflussfaktoren.

---

### 2 Regressionsbaum

Notebook:  
`02_Regressionsbaum.ipynb`

Inhalte:

- Feature Engineering  
- Train-Test-Split  
- Decision Tree Regressor  
- Cross-Validation  
- Feature Importance  
- Modellinterpretation  

Ziel:  
Identifikation der wichtigsten Merkmale für die Preisbildung.


### 3 Multiple lineare Regression

Notebook:  
`03_Multiple_Regression.ipynb`

Inhalte:

- One-Hot-Encoding kategorialer Variablen  
- Multiple lineare Regression  
- Modellbewertung mit  

  - R²  
  - MAE  
  - RMSE  

- Analyse der Regressionskoeffizienten  
- Residuenanalyse  
- Multikollinearitätsprüfung (VIF)

Ziel:  
Quantitative Bewertung des Einflusses einzelner Fahrzeugmerkmale auf den Basispreis.


## Reproduzierbarkeit
Die Analyse kann vollständig reproduziert werden, indem die Notebooks in folgender Reihenfolge ausgeführt werden:

1. `01_EDA_Mercedes_Global_Sales.ipynb`  
2. `02_Regressionsbaum.ipynb`  
3. `03_Multiple_Regression.ipynb`