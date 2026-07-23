# Ford GoBike Trip Data — Exploratory Data Analysis

Exploratory data analysis of 12 months (2018) of Ford GoBike trip data from the San Francisco Bay Area bike-share program. The project cleans and merges monthly trip files, engineers time-based features, and analyzes usage patterns across rider segments, time, and stations to surface actionable insights for fleet operations and business strategy.

## Dataset

- **Source**: Ford GoBike (now Bay Wheels) public trip data, 2018
- **Size**: ~1.86M raw trip records across 12 monthly CSV files, ~1.74M after cleaning
- **Fields**: trip duration, start/end station (id, name, lat/long), start/end timestamps, bike ID, user type (Subscriber/Customer), member birth year, member gender, bike-share-for-all program flag

## Objective

Help Ford GoBike make data-driven decisions to:
- Optimize fleet rebalancing by identifying peak demand windows and high-traffic stations
- Support revenue growth by understanding the Subscriber vs. Customer mix
- Improve rider experience by understanding usage patterns across time, segment, and geography

## Approach

1. **Data Wrangling** — Merged 12 monthly CSVs into a single DataFrame; fixed data types (datetime, string, category); handled missing values in station and demographic fields; removed birth-year outliers (e.g., implausible ages) via threshold filtering.
2. **Feature Engineering** — Derived hour, day-of-week, month, trip duration (minutes), and rider age from raw timestamp and birth-year fields.
3. **Exploratory Data Analysis** — Univariate, bivariate, and multivariate analysis using Pandas, Matplotlib, and Seaborn, including distribution plots, groupby/pivot-table aggregations, correlation analysis, and heatmaps.
4. **Station Analysis** — Identified top start/end stations by trip volume to flag key operational hubs.

## Key Findings

- Median trip duration is ~9 minutes; the distribution is heavily right-skewed, confirming GoBike is used mainly for short, functional trips.
- Subscribers account for ~88.6% of trips vs. ~11.4% for Customers, with Subscribers riding shorter, more consistent commute trips and Customers riding longer, more leisure-oriented trips concentrated on weekends and in summer.
- Demand peaks sharply on weekday mornings (~8 AM) and evenings (~5 PM), consistent with commute-driven usage.
- A small number of stations account for a disproportionate share of trip starts and ends, indicating key network hubs.

## Tech Stack

- **Language**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, missingno
- **Environment**: Jupyter Notebook (Google Colab)

## Repository Contents

```
├── Ford_Go_Bike_EDA.ipynb     # Main analysis notebook
├── Ford_GoBike_2018_EDA_Report.pdf   # Formatted PDF report with visualizations & insights
└── README.md
```

## How to Run

1. Clone the repo and open `Ford_Go_Bike_EDA.ipynb` in Jupyter Notebook or Google Colab.
2. Download the Ford GoBike 2018 monthly trip data CSVs and update file paths in the notebook.
3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn missingno
   ```
4. Run all cells to reproduce the cleaning, analysis, and visualizations.

## Recommendations

- Prioritize bike rebalancing at top stations ahead of weekday rush hours.
- Target Customers with conversion campaigns during high-usage weekend/summer periods.
- Optimize fleet capacity for high-turnover, short trips rather than long single-rider holds.
- Expand awareness of the Bike Share for All subsidized access program to grow ridership.

## Author

*SAHIL VERMA and links (www.linkedin.com/in/sahil-verma-b839b7212)*
