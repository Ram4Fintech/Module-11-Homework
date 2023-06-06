***Module 11 Homework - Forecasting Net Prophet
**Mercado Libre - Financial Analysis and forecasting

**Google Colab: 
Firstly I created a file  in Google Colab and uplaoded my starter notebook into it. Thereafter the following steps were initiated:

** Step1: Finding unusual patterns in Hourly Google Search Traffic: 
After importing the necessary libraries and dependencies, I read the csv data file on hourly google search trends into a dataframe. Thereafter I sliced the data to the month of May 2020, the month in which the company released its annual financial resuts. The data is visualised in an hvplot. The result showed that the May 2020 google traffic was higher than the average for the whole year

**Step2:Identifying the traffic seasonality:
 In order to mine the google search traffic for seasonality, I grouped the search data to plot the average traffic in a working week - Monday to Friday. Then, using hv plot and heatmaps, I visualised the hour of the day and the day of the week traffic trends. the resulting heatmap is here: "[Image1.png]"
  By further groupong the data into week of the year, I could conclude that the search traffic did increases in the winter months of weeks 40 to 52. However the higher results than these were observed in weeks 4 and 6 which also were in the winter months

**Step 3: Search Traffic and stock prices:
For identifying the relationship between the google search trends and the company stock price trends, I had to first read the data from the csv file for the stock prices into a new dataframe. This data was then concaternated with the serach trends dataframe. This data was sliced into the soecific period of first half of 2020. This result was visualised in a shared hvplot showing the graphs for closing share prices and search trends. This is depicted here: "[Image2.png]" The result showed that though there were some positive corelationship between the two in Feb and Mar 2020, the spike in share prioces since May 2020 was not as a result of any appreciable spike in the search trends. Further analysis of the data showed that there is no marked corelation between stock volatility and the lagged search trends by one hour

**Step4: Creating Time Series model with Prophet: 
First, I reset the index in the serach trends data frame and labelled the two colums as ds and y as per Prophet's requirement. Thena  future dataframe was created based on 2000 nhours or 80 days. The data was visualised by a plot: "[Image3.png]" This image showed that the near term popularity of the company was actually going down. This data was further analysed into yhat, yhat_lower and yhat_upper to showcase the time of the day showing greatest popularity, the day of the week showing the most search traffic trend and the least search traffic in a year

**Step5: Optional:Forecast revenue using Time Series
After reading the historical sales data, I analysed the data graphically. thereafter I prepared the data for forecasting using Prophet. then I made predictions for the next quarter of the year by categorising the results into most likely, the best case and the worst case scenarios 