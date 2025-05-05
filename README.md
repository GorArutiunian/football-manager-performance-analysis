# Manager Performance Analysis (2014 – 2023)

**Overview**  
An R Markdown–powered analysis of Bundesliga & EPL manager tenures and team performance.  
- Cleans Excel data with **readxl** & **lubridate**  
- Interval-joins seasons to managers via **fuzzyjoin**  
- Computes Points Per Match (PPM), fits a linear model (`Points ~ Matches`)  
- Visualizes PPM scatter plots, regression lines, and Lazio’s cumulative goal difference

**Key Features**  
- **Data ingestion & cleaning**: reads and parses four Excel tables  
- **Tenure matching**: constructs July–June season ranges and interval-joins manager tenures  
- **Modeling**: linear regression on total matches vs. total points  
- **Visualizations**:  
  - Bundesliga PPM vs. matches with league-average line  
  - EPL scatter colored by PPM and sized by clubs managed  
  - Lazio’s match-by-match cumulative goal difference shaded by manager tenure  
- **Reproducible report**: knits to both HTML and PDF with narrative interpretation

**Tech Stack**  
R | R Markdown | ggplot2 | dplyr | lubridate | fuzzyjoin | readxl | SportsAnalytics270

## Installation

```bash
git clone https://github.com/GorArutiunian/football-manager-performance-analysis.git
cd football-manager-performance-analysis
Rscript -e 'pak::pak(c("readxl","dplyr","ggplot2","lubridate","fuzzyjoin","SportsAnalytics270"))'
