# U.S. Computer Science Jobs: Bureau of Labor Statistics API Analysis

**Which U.S. industries employ the most computer-science workers, and how has that changed through COVID? This project pulls employment series from the BLS API and analyzes them.**

*Team project, Group 8: Abdullah Ibrahim, Albwin "Al" Wagner-Schmitzer, Del Vinas, Jay Howarth, Crystal White. Submitted January 11, 2023, for the OSU AI Bootcamp.*

## Question

We first set out to measure employment in artificial intelligence. The BLS doesn't track AI as its own occupation; it falls under the broader computer-science occupation codes. So we pivoted to a practical question for job seekers: **which industries have the most computer-science jobs, and which are growing?**

## Approach

- **Data sourcing:** BLS Public Data API v2. The BLS publishes no catalog of series IDs, so the team worked out how to build them by combining prefix, seasonal-adjustment code and industry code.
- **Industries analyzed:** Government, Health & Education, Financial Services, Retail, Professional & Business Services, and Manufacturing, the sectors employing the most computer scientists.
- **Analysis:** employment trends by industry, seasonality, and the impact of COVID-19, in pandas with matplotlib charts.
- **Forecasting:** Prophet time-series forecasts of the BLS series, with 90% uncertainty intervals.
- **Context:** supplemented with White House Council of Economic Advisers and agency reports on AI employment.

## What's in this repo

| File | What it is |
|---|---|
| `Project_1/Group8_BLS_API_notebook.ipynb` | **Main notebook:** API calls, cleaning, analysis and charts |
| `Project_1/Team 8 Presentation Final.pptx` | Final presentation (industry findings; seasonality and COVID charts in the appendix) |
| `Project_1/Project 1.ipynb` | Earlier working notebook |
| `Project_1/*.txt` | Raw BLS series downloads |
| `REPORT.md` | The team's full written report: approach, lessons, conclusions, references |

## Run it

1. Get a free BLS API key at [data.bls.gov/registrationEngine](https://data.bls.gov/registrationEngine/).
2. `pip install pandas numpy requests matplotlib prophet`
3. Open `Group8_BLS_API_notebook.ipynb` and replace `"Your API Key here"` with your key. Don't commit the real key.

**Tools:** Python, REST APIs (BLS v2), pandas, NumPy, matplotlib, Prophet

## Key lessons

- Government data is extensive but hard to navigate. Most of the effort went into working out the series-ID structure, not into the analysis itself.
- When the data couldn't answer the original question (AI jobs specifically), we redefined the scope instead of forcing a weak answer.
