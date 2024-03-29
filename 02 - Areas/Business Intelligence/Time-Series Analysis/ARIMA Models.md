### [[Forecasting#^52b7e4|Exponential Smoothing]] vs. ARIMA


> [!HINT] Autocorrelation
> [[Basics#^9ff078|Correlation]] vs. [[Basics#^9ff078|Autocorrelation]] 


### Regression model
Used to predict value of dependent variable based on the value of at least one **independent variable**
Explain the impact of changes in a independent variable on the dependent variable

**Dependent var(Y):** The one we wish to explain
**Independent vars (X1, X2...Xk)** k vars used to explain Y

Relationship explained by linear function. Change in Y is caused by changes in (X1, X2 ... Xk )
![[Pasted image 20240204164013.png]]

### ARIMA (p,d,q)

> [!INFO] What is ARIMA?
> Numerical expression indicating how the observations of a target var are **statistically correlated with past observations of the same var**

- Most general class in forecasting which can be stationarized by transformations such as differencing and lagging
- Fine-tuned versions of random-walk models.

**Consists of:**
1. An **Autoregressive (AR)** component, seasonal or not
2. An **Moving Avarage (MA)** component, seasonal or not
3. The order of **Integration (I)** of the series

**Most common notion.**
$$
ARIMA(p,d,q) (P,D,Q)s
$$
– p is the number of autoregressive terms
– d is the number of non-seasonal differences
– q is the number of lagged forecast errors in the equation
– P is the number of seasonal autoregressive terms
– D is the number of seasonal differences
– Q is the number of seasonal lagged forecast errors in the equation
– s is the seasonal period (cycle frequency using R terminology)

#### Autoregressive part (AR):
We forecast the variable of interest using a linear combination of past values of the variable itself
**Autoregression** --> Regression of the variable against itself

**AR(p)** can be written as:
![[Pasted image 20240204164804.png]]
• 𝑦𝑡 = dependent variable
• 𝑦t, 𝑦t-1,…, 𝑦t-p= independent variables (i.e. lagged values of 𝑦𝑡 as predictors)
• phi1, phi2, …, phip = regression coefficients
• 𝜀!= error term (must be white noise)

![[Pasted image 20240204165108.png]]

#### Moving Average part (MA)
Moving average model uses **past forecast errors** in a regression-like model
**MA(q)** defined as:
![[Pasted image 20240204165616.png]]
--> A **moving average model** is used for forecasting future values while **moving average smoothing** is used for estimating the trend-cycle of past **values**
![[Pasted image 20240204165719.png]]

#### ARMA and ARIMA
![[Pasted image 20240204165746.png]]
To use ARMA the model must be stationary! If not, before estimating and ARMA model, we need to apply one or more differences --> Integration process **I(d) where d=number of differences needed to get stationary**

![[Pasted image 20240204165959.png]]

To estimate an ARIMA Model, **Maximum Likelihood Estimation (MLE)** is used.
MLE finds the values of the parameters which maximize the probability of obtaining the data we have observed -> For given values of (𝒑, 𝒅, 𝒒) (𝑷, 𝑫, 𝑸) (i.e. model order) the algorithm will try to
maximize the log likelihood when finding parameter estimates