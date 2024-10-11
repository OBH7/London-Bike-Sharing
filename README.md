# Bike Usage and Weather Analysis Visualization Project

## Overview
This project analyzes the relationship between weather conditions and bike usage in London using data visualization tools in Tableau. The primary objective is to explore how various weather factors like temperature, humidity, and wind speed affect the number of bike rides over different periods.

## Data
- **Data Source**: The dataset used in this project is too large to include directly in this repository.
  - You can download the data from [Data Source Link](https://www.kaggle.com/datasets/hmavrodiev/london-bike-sharing-dataset?resource=download).
  - The dataset contains fields such as:
    - `timestamp`: Date and time of each record.
    - `cnt`: Number of bike rides during the recorded hour.
    - `t1`: Actual temperature (in Celsius).
    - `hum`: Humidity percentage.
    - `wind_speed`: Wind speed in meters per second.
    - `weather_code`: Coded weather information (e.g., clear, rainy, foggy).
    - `is_holiday`: Binary indicator (1 for holidays, 0 otherwise).
    - `is_weekend`: Binary indicator (1 for weekends, 0 otherwise).
    - `season`: Season of the year (encoded as 1 = winter, 2 = spring, etc.).

## Tableau Public Link
You can view the interactive Tableau visualizations directly on Tableau Public through the following link:

[View the Bike Usage and Weather Analysis Dashboard on Tableau Public](https://public.tableau.com/your_dashboard_link_here)

## Visualizations
The Tableau dashboard includes the following visualizations:
1. **Time Series Analysis**:
   - Visualizes the total number of bike rides over time.
   - Includes a date filter for selecting specific periods.
2. **Weather Impact on Bike Usage**:
   - Scatter plots showing the relationship between bike usage (`cnt`) and weather factors like `t1` (temperature), `hum` (humidity), and `wind_speed`.
   - Each scatter plot includes trend lines to highlight the relationship.
3. **Daily and Weekly Trends**:
   - Time series charts aggregated to daily and weekly levels, showing the moving averages of bike rides.
   - Analysis of seasonal trends in bike usage.

## Calculated Fields
The following calculated fields were used to aggregate and analyze data in Tableau:

1. **Sum of Bike Rides per Day**
   - Calculates the total number of bike rides for each day:
     ```tableau
     { FIXED DATE([timestamp]): SUM([cnt]) }
     ```

2. **Average Temperature per Day**
   - Calculates the average temperature for each day:
     ```tableau
     { FIXED DATE([timestamp]): AVG([t1]) }
     ```

3. **Average Humidity per Day**
   - Calculates the average humidity for each day:
     ```tableau
     { FIXED DATE([timestamp]): AVG([hum]) }
     ```

4. **Average Wind Speed per Day**
   - Calculates the average wind speed for each day:
     ```tableau
     { FIXED DATE([timestamp]): AVG([wind_speed]) }
     ```

## Insights
The analysis revealed the following insights:
- **Temperature**: Bike usage tends to increase with moderate temperatures but decreases in extremely cold or hot conditions, indicating that riders prefer comfortable weather for biking.
- **Humidity**: Higher humidity levels are correlated with a slight reduction in bike usage. This could be due to the discomfort caused by high humidity levels while riding.
- **Wind Speed**: Wind speed shows a weak negative correlation with bike rides, likely due to difficult riding conditions when the wind speed is high.
- **Seasonality**: Bike usage is higher in spring and summer compared to winter, which aligns with typical outdoor activity patterns.
- **Weekends and Holidays**: Higher bike usage is observed on weekends and holidays, suggesting that many users ride for leisure during non-working days.

## Prerequisites
- **Tableau Public Account**: A Tableau Public account is required if you want to interact with the dashboard.
- **Internet Access**: Since the dashboard is hosted on Tableau Public, users need internet access to view it.

## How to Use the Project
1. **View the Dashboard**:
   - Click the [link to the Tableau Public dashboard](https://public.tableau.com/shared/9K6PCNN56?:display_count=n&:origin=viz_share_link)
   - Explore the interactive visualizations, use filters to focus on specific periods, and observe how weather conditions affect bike usage.

## Acknowledgments
- Special thanks to the open data source for providing the London bike usage data.
- This project was inspired by the goal of understanding how environmental factors impact transportation habits.

## License
This project is licensed under the MIT License. See the `LICENSE.md` file for details.
