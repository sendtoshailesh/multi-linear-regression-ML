# Bike Sharing Demand Prediction
> A multiple linear regression model to predict post-COVID bike sharing demand for BoomBikes, achieving 83% accuracy in demand prediction.

## Table of Contents
* [General Info](#general-information)
* [Key Findings](#key-findings)
* [Technical Details](#technical-details)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)

## General Information
- This project develops a multiple linear regression model to predict bike sharing demand based on various environmental and seasonal factors.
- BoomBikes, a US bike-sharing provider, faced significant revenue decline during COVID-19 and needs to understand post-pandemic demand patterns.
- The business problem focuses on:
  * Identifying significant variables affecting bike sharing demand
  * Understanding how well these variables explain demand variations
  * Preparing optimal business strategy for post-pandemic recovery
- The dataset contains daily bike rental records for 2018-2019 with 730 entries and features including:
  * Weather data (temperature, humidity, windspeed)
  * Seasonal information (season, month, year)
  * Holiday information
  * Working day status
  * Rental counts (casual, registered, total users)

## Key Findings
### Categorical Variables Analysis
- Season shows strong influence: Summer and Fall have highest demand
- Year-over-year growth: 23% increase from 2018 to 2019
- Weather conditions significantly impact rentals:
  * Clear weather increases rentals by 30%
  * Light rain/snow decreases rentals by 25%
  * Heavy rain/snow reduces demand by up to 50%
- Working days show more consistent rental patterns

### Numerical Variables Analysis
- Temperature has strongest correlation (0.62) with rentals
- Humidity shows moderate negative correlation
- Wind speed has minimal impact on rental demand

## Technical Details
### Data Preprocessing
- Handled categorical variables using dummy variables (drop_first=True)
- Scaled numerical features using MinMaxScaler
- Created derived features:
  * Temperature feel difference
  * Seasonal indicators
  * Monthly patterns

### Model Development
- Used multiple modeling approaches:
  * Linear Regression
  * Ridge Regression
  * Lasso Regression
- Final model achieves:
  * R-squared: 0.83
  * RMSE: [specific value]
- Validated assumptions through:
  * Residual analysis
  * Q-Q plots
  * Homoscedasticity checks

## Conclusions
1. Temperature is the strongest predictor:
   - Each unit increase correlates to 0.5 unit increase in rentals
   - Suggests focusing on weather-based pricing strategy

2. Strong year-over-year growth:
   - 23% increase indicates growing market acceptance
   - Positive indicator for post-pandemic recovery

3. Weather impact insights:
   - Clear weather boosts rentals by 30%
   - Opportunity for weather-based marketing and operations

4. Model Performance:
   - 83% variance explained by the model
   - Reliable tool for demand forecasting
   - Suitable for business planning

## Technologies Used
- pandas - version 1.5.3 (Data manipulation)
- numpy - version 1.24.3 (Numerical operations)
- matplotlib - version 3.7.1 (Visualization)
- seaborn - version 0.12.2 (Statistical visualization)
- scikit-learn - version 1.2.2 (Machine learning)
- statsmodels - version 0.13.5 (Statistical analysis)

## Acknowledgements
- Dataset provided by BoomBikes
- Analysis based on research by Fanaee-T, Hadi, and Gama, Joao (2013)
- Project completed as part of IITB-Upgrad Executive PG Programme

## Contact
Created by [Shailesh Mishra (sendtoshailesh@gmail.com)] - For questions about methodology, implementation, or insights.

## License
This project uses data from the research paper:
Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013)