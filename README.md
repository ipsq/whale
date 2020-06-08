# whale

Open source data analysis and manipulation tool including estimation of many different statistical models, as well as for conducting statistical tests, and statistical data exploration. It will be a fully typesafe Scala equivalent of Python's [pandas](https://pandas.pydata.org), [statsmodels](https://www.statsmodels.org/stable/index.html), and more. 

## Features
The following classes, models and functionality are planned to become part of this library. 

### Data
  * DataFrame
    * `abs`, `copy`, `corr`, `count`, `cov`, `divide`, `dot`, `drop`, `dropna`, `filter`, `filter`, `first`, `head`, `max`, `mean`, `median`, `min`, `mode`, `rank`, `std`, `tail`, `take`, `truncate`, `var`, and more
  * Series
  * Index
    * PeriodIndex
    * DatetimeIndex
    * TimedeltaIndex
    * MultiIndex
    * IntervalIndex
    * CategoricalIndex
    * RangeIndex
  * Window 
    * RollingWindow
    * ExpandingWindow
    * ExponentiallyWeightedMovingWindow
  * Resample
  * GroupBy
 
### Models
  * Time Series Analysis
    * AR
    * VAR
    * ARMA
    * ARIMA
    * SARIMAX
    * VARMAX
    * DynamicFactor
