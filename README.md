# Mercedes Global Sales Analysis


## Datenquelle
Der Datensatz stammt von Kaggle:

Dhrubang Talukdar (2025).
**Mercedes Global Car Sales (2020–2025)**

https://www.kaggle.com/datasets/dhrubangtalukdar/mercedes-global-car-sales-2020-2025

Die Daten wurden lokal heruntergeladen und im Ordner `input/raw` gespeichert.
Für die Analyse wurde eine aufbereitete Version im Ordner `input/processed` erzeugt.


## Projektstruktur

```text
Mercedes_Global_Sales
│   .gitignore
│   01_EDA_Mercedes_Global_Sales.ipynb
│   02_Regressionsbaum.ipynb
│   03_Multiple_Regression.ipynb
│   README.md
│   requirements.txt
│
├── docs
│   ├── 01_EDA_Mercedes_Global_Sales.pdf
│   ├── 02_Regressionsbaum.pdf
│   ├── 03_Multiple_Regression.pdf
│   └── Mercedes_Sales_Profiling.html
│
├── input
│   ├── processed
│   │   └── mercedes_sales_processed.csv
│   └── raw
│       └── mercedes_benz_sales_2020_2025.csv
│
└── output
    └── figures
        ├── eda
        └── modeling
```


## Zentrale Fragestellung
Welche Fahrzeugmerkmale beeinflussen den Basispreis von Mercedes-Benz Fahrzeugen
und welche Muster lassen sich in der Preisstruktur erkennen?


## Ziel der Analyse
Ziel der Analyse ist es, die Preisstruktur von Mercedes-Benz Fahrzeugen im Zeitraum
2020–2025 zu untersuchen und zentrale Einflussfaktoren auf den Basispreis zu identifizieren.


## Verwendete Methoden
- Explorative Datenanalyse
- Regressionsbaum
- Multiple lineare Regression


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