### What?
Exists when a series is influenced by seasonal factors (month, quarter, day of week, time of day etc.) --> Is always of a fixed and known period

### Additive seasonality
The dynamics of the components are independents from each other. A increase in trend doesn't imply and increase in the magnitude of seasonal dips
The difference of the trend and the raw data is roughly constant in similar periods of time
![[Pasted image 20240203183519.png]]
### Multiplicative seasonality
Amplitude of the seasonality increase/decrease with an increasing/decreasing trend --> Components are not independent from each other
When the variation in the seasonal pattern (or the variation around the trend-cycle) appears to be
proportional to the level of the time series, then a multiplicative model is more appropriate
![[Pasted image 20240203183911.png]]

### Frequency
Depending on the data granularity and time of seasonality that wants to be modeled, it is important to consider the right seasonal frequency
**Frequency:** How many observations you have for every seasonal cycle.

**Problem:** For observations smaller than a week, there is the problem that smaller data might have bigger seasonality wrapped around it
i.e. hourly data can have a daily seasonality (frequency=24) and a weekly seasonality (frequency=24*7=168)
![[Pasted image 20240203184345.png]]