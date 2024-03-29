A TS is stationary when its properties do not depend on the time at which the series is observed
**--> A time series with a trend or seasonality is not stationary**

Other props of stationarity:
– the values oscillate frequently around the mean, independently from time
– the variance of the fluctuations remains constant across time
– the autocorrelation structure is constant over time and no periodic fluctuations exist
![[Pasted image 20240203213331.png]]

Typical examples of non-stationaries: All series that exhibit a deterministic trend or the so called **Random walk**

The [[ACF-Plot]] is also useful for identifing non-stationary ts.
--> for a stationary time series, the ACF will drop to zero (i.e. within confidence bounds) relatively quickly, while the ACF of non-stationary data decreases slowly
Macht Sinn, weil bei einem Datensatz ohne deterministische Erklärung, wie soll da ein Zusammenhang zwischen den Beobachtungen bestehen?
![[Pasted image 20240203213703.png]]

### Differencing
One way to make a ts stationary by computing differences between consecutive observations.
- This helps to stabilize the mean of a ts by removing changes in the level of a ts and so eliminating a trend (or seasonality if a specific differencing order is used)
- The Order of Integration for a Time Series, denoted I(d), reports the minimum number of differences (d) required to obtain a stationary series (note: I(0) --> means the series is stationary!)
- Transformations such as logarithms can help to stabilize the variance of a time series
![[Pasted image 20240203214008.png]]
![[Pasted image 20240203214035.png]]

> [!WARNING] Mehrfache Differenzierung
> Manchmal kann es vorkommen, dass eine Differenzierung nicht ausreicht, um die TS stationär zu machen. In dem Fall einfach nochmal differenzieren

**Seasonal difference:** Difference between observation and corresponding observation of previous (seasonal) cycle

$$
y_{t}^{'} = y_{t} - y_{t-F}
$$

Where F is the (seasonal) cycle frequency
-> The seasonal differencing removes strong and stable seasonality pattern (and transform into a white noise the so called “seasonal random walk”, i.e. $y_{t} = y_{t-F} + \varepsilon _{t}$)

**Consider that**
- Sometimes it’s needed to apply both “simple” first differencing and seasonal differencing in order to obtain a stationary series
- It makes no difference which is done first—the result will be the same
- However, if the data have a strong seasonal pattern, it’s recommended that seasonal differencing be done first because sometimes the resulting series will be stationary and there will be no need for a further nonseasonal differencing