**Step 1: Find Unusual Patterns in Hourly Google Search Traffic**

The data science manager asks if the Google search traffic for the company links to any financial events at the company. Or, does the search traffic data just present random noise? To answer this question, pick out any unusual patterns in the Google search data for the company, and connect them to the corporate financial events.

Completed the following steps:

1. Read the search data into a DataFrame, and then slice the data to just the month of May 2020. (During this month, MercadoLibre released its quarterly financial results.) Visualize the results. Do any unusual patterns exist?
2. Calculated the total search traffic for the month, and then compare the value to the monthly median across all months.

**Step 2: Mine the Search Traffic Data for Seasonality**

Marketing realizes that they can use the hourly search data, too. If they can track and predict interest in the company and its platform for any time of day, they can focus their marketing efforts around the times that have the most traffic. This will get a greater return on investment (ROI) from their marketing budget.

To that end, you want to mine the search traffic data for predictable seasonal patterns of interest in the company. To do so, complete the following steps:

1. Grouped the hourly search data to plot the average traffic by the hour of day. Does the search traffic peak at a particular time of day or is it relatively consistent?
2. Grouped the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday). Does the search traffic get busiest on any particular day of the week?
3. Grouped the hourly search data to plot the average traffic by the week of the year. Does the search traffic tend to increase during the winter holiday period (weeks 40 through 52)?

**Step 3: Relate the Search Traffic to Stock Price Patterns**

You mention your work on the search traffic data during a meeting with people in the finance group at the company. They want to know if any relationship between the search data and the company stock price exists, and they ask if you can investigate.

Completed the following steps:

1. Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.
2. Marketed events emerged during the year of 2020 that many companies found difficult. But, after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms. Slice the data to just the first half of 2020 (*2020-01* to *2020-06* in the DataFrame), and then plot the data. Do both time series indicate a common trend that’s consistent with this narrative?
3. Created a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Create two additional columns:
    * “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility
    * “Hourly Stock Return”, which holds the percent change of the company's stock price on an hourly basis

**Step 4: Create a Time Series Model with Prophet**

Produced a time series model that analyzes and forecasts patterns in the hourly search data. To do so, completed the following steps:

1. Set up the Google search data for a Prophet forecasting model.
2. After estimating the model, plot the forecast. How's the near-term forecast for the popularity of MercadoLibre?
3. Plot the individual time series components of the model to answer the following questions in the space provided in the starter file:
    * What time of day exhibits the greatest popularity?
    * Which day of the week gets the most search traffic?
    * What's the lowest point for search traffic in the calendar year?
