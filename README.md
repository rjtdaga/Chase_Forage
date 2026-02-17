# Chase_Forage
This repository contains the relevant files used to complete the JP Morgan Chase Quantitative Research Virtual Experience Program on Forage. The virtual experience consists of two sections:
1) Natural gas commodity contract price prediction:
   * The first step is given the price of natural gas commodity on month-ends over the span of 2020-2024, create a price prediction model that can predict the natural gas price at any date in the past or future.
   * The data over a year seems sinusoidal, with the mean increasing every year. Therefore, the price of natural gas is predicted for every month end using only that particular month's data over the years and predicting for the given year. The price is then predicted through interpolation within the year using a sinusoidal approximation.
   * A simpler approximation is to predict the price on the month ends before and after the given date. Then use linear interpolation within those two month ends to predict the price for the given date.
   * Upon developing this model, the next step is used to create a function to return the contract price, given an array of injection dates, withdrawal dates, cost of injection/withdrawal, storage costs as input.
2) Default prediction based on consumer data:
   * Given the consumer data of credit lines, loan amount, total debt, income, years employed and FICO score, predict whether any consumer given their details will default on the loan using feature engineering. 
