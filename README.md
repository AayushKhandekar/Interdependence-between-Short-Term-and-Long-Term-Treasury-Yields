# Interdependence between Short-Term and Long-Term Treasury Yields

### Overview

The objective of this project is to explore the relationship between short-term and long-term interest rates in the United States using historical data for 1-year and 10-year Treasury Yields. The goal is to understand how short-term rates affect long-term rates. We analyze each rate independently to understand how much of today's change in a rate can be explained by its own past values. We then analyze both the rates together to understand the influence of one rate on another.

### Models Used

#### ARIMA Models:

Applied ARIMA models to each rate independently to capture the internal time-dependent structure of yield changes.

The 1-year yield was best modeled as an AR(2) process.

The 10-year yield was best captured by an AR(3) process.These models revealed that both yield series show significant short-term memory and mean-reverting tendencies.

#### VAR (Vector Autoregression):

Used to examine the joint dynamics of 1-year and 10-year yield changes. The model showed that changes in the 10-year yield are significantly explained by past values of the 1-year yield, indicating short-term rates help predict movements in long-term rates.

#### SVAR (Structural VAR):

Imposed economic restrictions to isolate causal effects. Specifically, the model assumed that short-term rates can contemporaneously influence long-term rates but not vice versa. This allowed us to estimate the true structural impact of monetary policy shocks.

### Conclusions
1-year Treasury yields have a clear and significant influence on the 10-year Treasury yields but not the other way around. 

The estimated impact of a shock to the short-term rate on the long-term rate was approx 0.198.