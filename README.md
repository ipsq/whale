# whale

Open source data analysis and manipulation tool including estimation of many different statistical models, as well as for conducting statistical tests, and statistical data exploration. It will be a fully typesafe Scala equivalent of Python its [pandas](https://pandas.pydata.org), [statsmodels](https://www.statsmodels.org/stable/index.html), and more. Special care will be taken in order to increase performance, minimalize overhead, and keep the API as close to its Python counterpart as possible.

## Features
The following classes, models and functionality are planned to become part of this library. 

### Classes
  * DataFrame
    * fully typed by using tuples and case classes (see [typelevel/frameless](https://github.com/typelevel/frameless))
    * backend agnostic 
      * support for multiple backends, with simple default implementation (Apache Spark, etc.)
    * lazy computations
    * aggregate functionality
      * GroupBy
      * Window
        * RollingWindow
        * ExpandingWindow
        * ExponentiallyWeightedMovingWindow
    * optionally indexed
      * SeqIndex (simple list based indexing)
      * PeriodIndex
      * DatetimeIndex
      * TimedeltaIndex
      * MultiIndex
      * IntervalIndex
      * CategoricalIndex
      * RangeIndex
  * Series 
    * single column of DataFrame
    * single type parameter
    * optionally indexed
  * Vector
    * single column matrix (N x 1)
  * Matrix
    * typed operations (like Breeze)
    * backend agnostic 
      * support for multiple backends, with simple default implementation (Breeze, etc.)
    * linear algebra functionality (see [numpy.linalg](https://numpy.org/doc/stable/reference/routines.linalg.html))
 
### Models
  * Regression analysis
    * OLS
    * WLS
    * GLS
  * Time-series analysis
    * AR
    * VAR
    * ARMA
    * ARIMA
    * SARIMAX
    * VARMAX
