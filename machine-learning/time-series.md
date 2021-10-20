# Key Terms  
**Trend**  
A long-term increase or decrease in the data is referred to as a trend. It is not necessarily linear. It is the underlying pattern in the data over time.  

**Seasonal**  
When a series is influenced by seasonal factors i.e. quarter of the year, month or days of a week seasonality exists in the series. It is always of a fixed and known period. E.g. – A sudden rise in sales during Christmas, etc.

**Cyclic**  
When data exhibit rises and falls that are not of the fixed period we call it a cyclic pattern. For e.g. – duration of these fluctuations is usually of at least 2 years.  

**Stationarity**  
Achieved by:
1. Differencing  
2. Log or square-root to stabilize non-constant variance  
3. Curve-fitting (kernel)  

# Time Domain
## Auto-Regressive Integrated Model Average  
A linear regression model is constructed including the specified number and type of terms, and the data is prepared by a degree of differencing in order to make it stationary, i.e. to remove trend and seasonal structures that negatively affect the regression model. 
### Assumptions  
- Stationary data: properties of series does not depend on actual time captured  
- Univariate

### Parameters  
**p**: Number of lag observations (lag order)  
**d**: number of times raw observations are differenced  
**q**: size of moving average window  
- Should be used for short-term forecasts **only**  

Number of lags determined by autocorrelation analysis which examines serial dependence  
Cylic behaviour of series found by spectral analysis to describe how variatoin in a time series may be accounted for by cyclic components  
Trend estimation and decomposition performed for seasonl adjustment

# Frequency Domain 