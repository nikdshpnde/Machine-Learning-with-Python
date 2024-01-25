# Machine-Learning-with-Python
The goal is to build a machine learning model using the weekly deaths dataset to accurately predict total deaths by cause at a state level from 2014-2019. Predicting deaths by cause will provide actionable insights to guide public health policy.

India is hosting the ICC World Cup 2023, but one match has drawn attention for a different reason: **poor air quality index (AQI)** in Delhi. The capital city experiences poor AQI during every winter season, and this year was no exception. A match between Bangladesh and Sri Lanka held in Delhi raised eyebrows again for the high air pollution levels. Similarly, New York City experienced alarming air quality levels this year due to wildfires in Canada.

As a data-driven Business Analyst, I decided to focus on the various medical causes of deaths in the United States. Instead of analyzing trends, patterns, and visualizations, I built a machine learning model to predict deaths caused by diseases such as **diabetes mellitus, Alzheimer's disease, chronic lower respiratory diseases, and cerebrovascular diseases**.

The [dataset](https://data.cdc.gov/NCHS/Weekly-Counts-of-Deaths-by-State-and-Select-Causes/3yf8-kanr) contains counts of deaths by the week the deaths occurred, by state of occurrence, and by select causes of death between 2014 and 2019.

The machine learning model built using Random Forest shows **99% accuracy** is predicting deaths caused by various issues. 


**Objective:**

The goal is to build a machine learning model using the weekly deaths dataset to accurately predict total deaths by cause at a state level from 2014-2019. Predicting deaths by cause will provide actionable insights to guide public health policy.

**Data Overview:**

The dataset covers 6 years of weekly death counts for 50 states, Washington DC and the US from 2014-2019. It includes 13 variables like jurisdiction, year, week, and deaths by 10 causes.

The dataset contains weekly death counts by state and cause from 2014-2019. After initial cleaning, it contains:
1. 50 states + Washington DC and USA totals
2. 13 variables: jurisdiction, year, week, and deaths by 10 causes
3. 6 years of data from 2014-2019
4. 1,872 total observations

**Preprocessing:**

Several preprocessing steps are taken to wrangle the raw data into a format suitable for modeling.

Derived an aggregated yearly deaths feature by summing weekly deaths per state and year. This created a consistent prediction target variable.

Merged yearly deaths with population data and calculated a deaths per 100K population feature. This normalized deaths across states for comparison.

Encoded categorical features like jurisdiction and sorted the data. This formatted predictors appropriately.

**Exploratory Analysis:**

1. Analyzing the preprocessed data provides insights to guide model development:

2. California has the highest total deaths from 2014-2019 at 4.17 million. Its large population of 39.5 million contributes to the leading death count.

3. Smaller states like West Virginia have lower total deaths but higher mortality rates. West Virginia's 1.82 million population suffers 3,120 deaths per 100K people - far above the national average.

4. The US has a mortality rate of 2,239 per 100K population. This is lower than the national statewide average of 2,276 per 100K, likely due to younger national demographics.

**Model Development:**

1. A Random Forest Regressor model is selected for its ability to capture nonlinear relationships in the data.

2. The model is trained on 80% of preprocessed data and tested on 20%. It achieves a high R-squared score of 0.9930, indicating it captures over 99% of variance in the test data.

3. A Decision Tree model is also tested but only achieves an R-squared of 0.9847. Thus, the Random Forest model is preferred.

**Recommendations:**

The Random Forest model shows strong performance predicting causes of death. It could provide state health agencies actionable insights like:

Predicting high diabetes death rates based on population obesity levels to target diabetes prevention programs.

Forecasting increasing cardiovascular deaths due to aging populations to allocate more cardiology resources.

Projecting rising cancer deaths due to environmental factors to focus research on carcinogen exposure.


**Future Scope:**

For production use, continued model monitoring, retraining on new data, and adding socioeconomic features could further improve accuracy. 
