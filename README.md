# Ford GoBike Trip Data — Exploratory Data Analysis

EDA on 12 months (2018) of Ford GoBike trip data from the San Francisco Bay Area bike-share program. Cleans and merges ~1.86M monthly trip records, then analyzes usage patterns across rider segments, time, and stations to surface insights for fleet operations and business strategy.

## Dataset
~1.86M trips (2018), 12 monthly CSVs → ~1.74M after cleaning. Fields include trip duration, start/end station, timestamps, user type, rider age, and gender.

## Approach
1. **Data Wrangling** — Merged monthly files, fixed data types, handled missing values, removed birth-year outliers.
2. **Feature Engineering** — Derived hour, day-of-week, month, duration (min), and rider age.
3. **EDA** — Univariate, bivariate, and multivariate analysis using groupby/pivot tables, correlation analysis, and heatmaps.
4. **Station Analysis** — Identified top start/end stations by trip volume.

## Key Findings
- Median trip duration ~9 min — short, functional trips dominate.
- Subscribers = 88.6% of trips (short commute rides); Customers = 11.4% (longer, weekend/summer leisure rides).
- Demand peaks on weekday mornings (~8 AM) and evenings (~5 PM).
- A small set of stations drive most trip starts/ends — key network hubs.

## Tech Stack
Python · Pandas · NumPy · Matplotlib · Seaborn · missingno · Jupyter Notebook

## Repository Contents
```
├── Ford_Go_Bike_EDA.ipynb
├── Ford_GoBike_2018_EDA_Report.pdf
└── README.md
```

## How to Run
```bash
pip install pandas numpy matplotlib seaborn missingno
```
Open `Ford_Go_Bike_EDA.ipynb`, update the data file paths, and run all cells.

## Author
*SAHIL VERMA (www.linkedin.com/in/sahil-verma-b839b7212)*
