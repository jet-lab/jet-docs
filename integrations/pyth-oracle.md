# Pyth Oracle

**Website:** [https://pyth.network/](https://pyth.network/)



Jet uses Pyth network to source data for its onboarded assets. Jet also monitors an Pyth's [confidence interval](https://docs.pyth.network/how-pyth-works/price-aggregation) given for each asset. If the confidence in a quoted price drops, Jet will compare the current quoted price to the hourly EMA, and pause liquidations if the price divergence is > 5%.

