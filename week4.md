I found this amazing visualization [at](https://observablehq.com/@d3/calendar/2?intent=fork)

1. The data is retrieved from [link](https://finance.yahoo.com/quote/%5EDJI/history/?guccounter=1&guce_referrer=aHR0cHM6Ly9kMy5zdGF0aWMub2JzZXJ2YWJsZXVzZXJjb250ZW50LmNvbS8&guce_referrer_sig=AQAAADe_oli4OqrFuwuZSc0sSj2Ao7VNxIDriAwOgiWgikG1-nsvVlzI6BG71qPVqhb3WdBuhoUXdYgCPezqb-7G07efvFaMJHnrO20yxUmlmBd7eJQFbQdt0Y4xHLaN7--vTPkVHIYFb7LGsKVMb5DGGMLOMRMQj0WPzLoubTR0buuD)

2. Data is about stock prices of 'Dow Jones Industrial' when it was high, low, opened, and closed.

3. Visualization is from year 2000 to 2020 which is very similar to GitHub commit graphs.

4. Daily change is shown by colors where dark purple indicates up to -6% and dark green indicates up to +6%, and 0% indicated by white colors.

#Coding Part:

5. The code has an array of 5080 elements which stores objects having all data of datewise.
    ex- {
  Date: 2000-01-03
  Open: 11501.849609
  High: 11522.009766
  Low: 11305.69043
  Close: 11357.509766
  Adj Close: 11357.509766
  Volume: 169750000
}

6. The code defines various constants such as the width and height of the chart, formatting functions for values, and helper functions for time computation.

7. It computes the percent change in the closing value of the stock market data and defines a color scale based on this change.

8. The data is grouped by year, and a function is defined to draw thin white lines to separate each month.

9. For each year in the data:

    a. A group element is created and positioned.

    b. Text elements are appended to display the year and days of the week.

    c. Rectangles are appended to represent each day in the data. The fill color of each rectangle represents the percent change in the closing value of the stock.

    d. Title elements are added to provide tooltips displaying the date, percent change, and closing value of the stock.
