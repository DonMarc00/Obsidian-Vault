in this chart you can read the linear correlation index between the values in t and all the possible lags (t-1, t-2, …, t-k);
![[Pasted image 20240203212916.png]]The ACF plot shows the autocorrelations which measure the linear relationship between 𝑦! and 𝑦!"# for
different values of k but consider that:
• if 𝑦t and 𝑦t-1 are correlated, then 𝑦t-1 and 𝑦t-2 must also be correlated
• But then 𝑦t and 𝑦t-2 might be correlated, simply because they are both connected to 𝑦t-1

-> The Partial Autocorrelation Function (PACF) consider the linear relationship between 𝑦t and 𝑦t-k after removing the effects of other time lags 1, 2, 3,…, 𝑘 − 1