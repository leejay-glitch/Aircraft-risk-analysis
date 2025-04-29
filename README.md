# Aircraft-risk-analysis
Analyzing aviation accident data from 1962 to 2023 to recommend low-risk aircraft models and operational strategies for safer business investments.

## Overview
This project explores historical aviation accident data to identify aircraft makes and models with the lowest risk profiles, assess conditions under which accidents occur, and provide actionable recommendations for the airline business.

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
   ![Total injuries and uninjured cases across all accidents](https://github.com/user-attachments/assets/fffbc912-3c79-4ec3-822d-972f2d8bbddd)

3. **Top 10 Aircraft Models by Total Injuries**  
   ![Top 10 aircraft models by injury severity](https://github.com/user-attachments/assets/0bc5a94a-8047-407f-981e-9f0d7afa1140)

4. **Accident and Injury Trends Over Time**  
  
  ![yearly trends accidents and injuries](https://github.com/user-attachments/assets/bd2bfa8b-907b-4484-8af8-0e949d7b6628)

> Visuals correspond to the figures in the Jupyter Notebook and presentation slides.
>
> Below you can find an interactive dashboard with other visuals generated
> https://public.tableau.com/views/AircraftRiskanalysisworkbook1/Generaloverview?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Conclusion
**Key Findings:**
1. **Safest Models:** Multi-engine turboprops and regional jets (e.g., Beechcraft King Air 200, Embraer ERJ-145) exhibit the lowest total injuries.
2. **Risk Factors:** Severe weather (rain, fog, thunderstorms) and remote regions correlate with higher fatality rates.
3. **Trends:** Accident frequency peaked in the 1990s and declined with modern avionics; post-2000 aircraft show lower injury averages.

**Recommendations:**
- Prioritize acquiring low-injury models and equip planes with advanced weather-avoidance technology.
- Implement stricter weather-based dispatch policies and focus pilot training on adverse conditions.
- Deploy aircraft with greater survival measures to remote regions and modern jets on high-traffic routes.

---
*For detailed methodology, full code, and interactive dashboard, see the Jupyter Notebook and  in this repository.*

