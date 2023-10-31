# YorkRegion-CrimeForecast

## Task 1

In this task, we aim to forecast the average number of crimes expected to occur in the upcoming 30 days. To achieve this, we use multiple features:

1. **Historical Crime Data**: The number of crimes reported in the previous 30 days.
  
2. **External Features**: Various external indicators such as temperature, precipitation levels, and unemployment rates, among others, from the last 30 days.

3. **Time Features**: Periodic time features that capture seasonality and trends in the data.

By leveraging these features, we aim to build a predictive model that can accurately estimate the average number of crimes for the next 30 days.

### Data Preprocessing

Along with data of the crimes committed in York Region including date, district and Number of Crimes committed between 2021 and August of 2023, we use following dataset:


1. **Unemployment Rate**: Ontario monthly unemployment rate which we resample it daily.
  
2. **Weather Data**: Mean Temp (°C), Total Precipitation (mm) and Snow on Ground

3. **ICU Data**: Number of covid related patients in ICU in York Region.

4. **Holidays**: Holidays in Ontario.

#### Feature Engineeering

We further refine the dataset through feature engineering. Particularly:

  
1. **Weighted Moving Averages**: We create mutiple new features with taking weighted averges of different features of original dataset like number of crimes, mean temperature, log of precipitation, snow on ground, icu patients and unemployment rate over the last 30 days with differnt weights.
   
2. **Skewness Correction**: Some models are sensitive to skewness of features so we will correct it.
   
<div align="center">
<img  src="src/img/skewness.jpeg"  align = 'center' width="700">
</div>

4. **Feature Standardization**: We apply minmax scaler on fearues.

### Data Visualization

We visualize daily number of crimes aloan with some features. We also visualize correlation matrix between features and target value.


