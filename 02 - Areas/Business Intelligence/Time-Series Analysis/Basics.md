### Why Time Series Analysis?
To enhance comprehension and predictions on any quantitative variable of interest (i.e. sales, sensors' measurements etc.)
--> Forecasting

**What is time series data?**
One single object (sales) observed over *multiple equally-spaced time periods*

> [!NOTE] Definition TSA
> A time series is a collection of observations made sequentially through time, whose dynamics is often characterized by short/long period fluctuations (seasonality and cycles) and/or long period direction (trend)
> 
> Such observations may be denoted by 𝒀𝟏 , 𝒀𝟐, 𝒀𝟑,… 𝒀𝒕,… , 𝒀𝑻 since data are usually collected at discrete points in time


![[Pasted image 20240203181709.png]]

#### Main objectives 
1. Summary description 
2. Interpretation of series features (seasonality, trend, etc.)
3. Forecasting (prediction)
4. Hypothesis testing and Simulation (Scenarios)

#### What else?
- Demand prediction
- Price prediction
- Anomaly detection

### Main Elements of Time Series Properties
![[Pasted image 20240203183010.png]]
**Trend:** Exists when there is a long-term increase or decrease in the data
**Cycle:** Oscillatory component which is repeated after a certain amount of time
**Residual:** The residual/error component is everything that is not considered in previous components. It is assumed to be the sum of a set of random factors not relevant for describing the dynamics of the series --> White noise

**Correlation:** Measures amount of relationship between two variables
**Autocorrelation:** Measures the linear relationship between lagged values of ts. r1 measures the relationship between yt and yt-1, r2 measures relationship between yt and yt-2 ^9ff078