# stock-analysis

*This analysis report will discuss whether refactoring the existing stock analysis code has made it more efficient and viable so that it can accommodate larger data sets in the future.*

----


### Overview of project and background

This project will refactor existing code on behalf of Steve. His workbook currently analyses a small number of stocks and returns the performance of the stocks that he is interested in. He is looking to expand his data sets which his current workbook is not set up for.      

#### Purpose

The purpose of this project is to refactor the existing code on Steve's workbook to make it more scalable. His current workbook is set up to process a small number of stocks. It will not work well for thousands of stocks, as it will take longer and longer to run the script. Refactoring the code will allow him to potentially expand his datasets to include the entire stock market and cover more historical performance over the years as his requirements change.

#### Method

Prior to refactoring the code, a timer was set up to measure the speed of the code's run time for each year (2017 & 2018). We can then compare it to the performance of the refactored code to determine whether the script did run faster. The aim is to make the code run more efficiently and reduce the number of steps it takes to process the data. One way to do this is to reduce the number of loops in the code.


------
### Results

The results section will first compare the results of the stock performance between 2017 and 2018 and then compared the execution times between the original script vs the refactored the script.


#### Stock Performance analysis in 2017 vs 2018

When comparing the images below, we can see that in 2017 stocks performed considerable better than in 2018. With the exception of TERP, all the rest of the stocks had a positive return. DQ and SEDG stocks performed exceptionally well with a 199.4% and 184.5% return. In 2018, nearly all stocks had a negative return except ENPH and RUN. They were the only stocks to have positive returns in both 2017 and 2018.

2017                       |  2018
:-------------------------:|:-------------------------:
![Stock analysis results for 2017](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Stock%20Analysis%202017%20%20image.png)  |  ![stock analysis results 2018](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Stock%20Analysis%202018%20image.png)





| Year        | Original Time (Secs) |  Refactored Time (Secs) |
|:----     | :----:    |  :----:  |       
| 2017        |     1.2734  |     0.1914  |       
| 2018        | 1.5627      | 0.2148      |               



------

### Summary
