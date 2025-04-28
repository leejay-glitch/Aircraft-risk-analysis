# Aircraft-risk-analysis
Analyzing aviation accident data from 1962 to 2023 to recommend low-risk aircraft models and operational strategies for safer business investments.

## Overview
This project explores historical aviation accident data to identify aircraft makes and models with the lowest risk profiles, assess conditions under which accidents occur, and provide actionable recommendations for fleet composition and operational policies.

## 📊 Business Understanding
### Stakeholders
- Aircraft investors and asset managers
- Airline and private charter companies
- Aviation safety regulators

### Business Goals
- Identify **low-risk aircraft models** based on incident counts and injury severity.
- Determine **environmental and operational conditions** (weather, flight phase, location) that correlate with higher accident risk.
- Provide **data-driven recommendations** for selecting, deploying, and operating aircraft safely.

## Data Understanding and Analysis
- **Source:** Kaggle – NTSB Aviation Accident Database & Synopses (1962–2023)
- **Key Fields:**
  - `Event.Date`, `Location`, `Country`
  - `Make` / `Model` (combined as `Aircraft.Name`)
  - Injury metrics: `Total.Fatal.Injuries`, `Total.Serious.Injuries`, `Total.Minor.Injuries`, `Total.Uninjured`
  - `Aircraft.damage`, `Weather.Condition`, `Purpose.of.flight`, `Broad.phase.of.flight`

### Data Preparation
- Dropped columns with excessive missing data: Latitude, Longitude, Aircraft.Category, Broad.phase.of.flight
- Imputed or filled missing values:
  - Categorical fields → “Unknown”
  - Injury counts → 0
- Converted and validated data types for date and numeric fields.

## 📈 Visualizations
1. **Injury Distribution Across All Accidents**  
   ![Injury Distribution](notebooks/images/injury_distribution.png)
2. **Top 10 Aircraft Models by Total Injuries**  
   ![Model vs Injuries](notebooks/images/model_vs_injuries.png)
3. **Accident and Injury Trends Over Time**  
   ![Yearly Trends](notebooks/images/yearly_trends.png)

> Visuals correspond to the figures in the Jupyter Notebook and presentation slides.

## Conclusion
**Key Findings:**
1. **Safest Models:** Multi-engine turboprops and regional jets (e.g., Beechcraft King Air 200, Embraer ERJ-145) exhibit the lowest total injuries.
2. **Risk Factors:** Severe weather (rain, fog, thunderstorms) and remote regions correlate with higher fatality rates.
3. **Trends:** Accident frequency peaked in the 1990s and declined with modern avionics; post-2000 aircraft show lower injury averages.

**Recommendations:**
- Prioritize acquisition of low-injury models and equip fleets with advanced weather-avoidance technology.
- Implement stricter weather-based dispatch policies and focus pilot training on adverse conditions.
- Deploy rugged, high-survivability aircraft to remote regions and modern jets on high-traffic routes.

---
*For detailed methodology, full code, and interactive dashboard, see the Jupyter Notebook and `clean_data/aviation_data_cleaned.csv` in this repository.*

