# whale

Open source data analysis and manipulation tool including estimation of many different statistical models, as well as for conducting statistical tests, and statistical data exploration. It will be a fully typesafe Scala equivalent of Python its [numpy](https://numpy.org/doc/stable/index.html), [pandas](https://pandas.pydata.org), [scipy](https://www.scipy.org), [statsmodels](https://www.statsmodels.org/stable/index.html), and more. Special care will be taken in order to increase performance, minimalize overhead, and keep the API as close to its Python counterpart as possible whilst still remaining idiomatic Scala.

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
    * immutable
  * Series 
    * single column of DataFrame
    * single type parameter
    * optionally indexed
    * immutable
  * Vector
    * single column matrix (N x 1)
    * immutable
  * Matrix
    * typed operations (like Breeze)
    * backend agnostic 
      * support for multiple backends, with simple default implementation (Breeze, etc.)
    * linear algebra functionality (see [numpy.linalg](https://numpy.org/doc/stable/reference/routines.linalg.html))
    * immutable
 
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
    
### Implementation details
  * Require numeric types to match in order to allow arithmic operations. Like [typelevel/frameless](https://github.com/typelevel/frameless), make use of `.cast[Double]` in order to allow multiplication of an `Vector[Int]` with a `Vector[Double]`. 
