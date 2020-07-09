# Financial Plan; Summary Report

The following budget analysis is based off of financial data sourced through Plaid APIs. The financial transaction data is retrieved from the most recent 90 days starting July 8th 2020.

## Budget Anaysis 


Below is an transaction table over the most recent 90 days sourced from the account followed by the previous years gross income, currently monthyl income and projected yearly income. Below the table is a pie chart visualizing the distribution of transactions from the expense table.


| Category       | Total Amount |
|----------------|--------------|
| Food and Drink | \\$3,317.19    |
| Payments       | \\$6,310.50    |
| Recreation     | \\$235.50      |
| Shops          | \\$1,500.00    |
| Transfers      | \\$20,537.34   |
| Travel         | \\$35.19       |
|---|---|
| Previous Years Gross Income | \\$7,285.00 |
| Currently Monthly Income    | \\$500.00   |
| Projected Yearly Income     | \\$7,389.00 |


![Expenses Pie Chart]
(spending_category_chart.png)


According to the expense pie chart, the client has the greatest amount of transactions in the Transfer and Payment categories. If we assume both these categories are transactions of either account transfer debits/credits or income credits, we can assume that the largest actual expenses category is Food and Drink.

The total monthly expenses sum to $10,645.24 per month; please note that this total number includes transaction of debits and credits of Payments and Transfers.

![Total Monthly Expenses]
(total_monthly_expenses.png "Total Monthly Expenses")

##Retirement Planning

Using an Alpaca API we are able to fetch and analyze one year of closing prices for stocks SPDR S&P 500 ETF Trust (SPY) and iShares Core U.S. Aggregate Bond ETF (AGG). The closing prices begin on 2019-01-01 and conclude on 2019-12-31. The average daily return for SPY, rounded up to two decimal places is is 0.21%; while AGG is 0.78%. 

Below is a graph of a Monte Carlo simulation run 500 times on a portfolio containing AGG and SPY stock. A Monte Carlo simulation generates random variables which enables us to assess risk and various potential outcomes of a predetermined system; these variables are modelled on the basis of probability distributions. This portfolio has a 60/40 Stock/Bond allocation which then generates a 30 year simulation of daily returns.

![Simulated Retirement Portfolio]
(monte_carlo_simulation_forecast.png)

Below, there are two tables; one represents expected cumulative returns for 30 years at the 10th, 50th, and 90th percentile. The other table shows a scenario of an initial investment of $20,000 with expected returns at the 10th, 50th and 90th percentile over the course of 20 years.  

|Type of Return|Years|Percentile|Output|
|---|---|---|---|
|Expected cumulative portfolio return | 30 years | 10th percentile | 39.66
|Expected cumulative portfolio return | 30 years | 50th percentile | 59.11
|Expected cumulative portfolio return | 30 years | 90th percentile | 82.74


|Type of Return|Initial Investment|Percentile|Return|
|---|---|---|---|
|Expected portfolio return | \\$20,000 | 10th percentile | \\$224,824.93.
|Expected portfolio return | \\$20,000 | 50th percentile | \\$302,677.06
|Expected portfolio return | \\$20,000 | 90th percentile | \\$406,248.55


According to the graph below, there is probable reason to believe that the ending return mean lies between these two red bounds of 10.72 and 22.38 since 95% of the time confidence intervals contain the true mean.

![90% Confidence Interval for Ending Returns](90_CL_ending_returns.png "90% Confidence Interval for Ending Returns")