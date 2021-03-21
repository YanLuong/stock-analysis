# Stock Analysis - VBA Challenge

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



#### Results of original script vs refactored

* *Please refer to the end of the report for the actual screenshots that correspond to the execution times seen in the results table below.*

Looking at the performance results in the table below, we can see that after refactoring the code that there was an improvement in the overall execution times. Roughly a full second was shaved off the execution time for both years.

| Year        | Original Time (Secs) |  Refactored Time (Secs) |
|:----     | :----:    |  :----:  |       
| 2017        |     1.2734  |     0.1914  |       
| 2018        | 1.5627      | 0.2148      |               



------

### Summary

Overall, there are advantages of refactoring. In this case, the number of loops we ran were reduced. In the original script, there were nested **for** loops where it ran within a loop. After refactoring, there were less iterations and for loops. In the original code (left screenshot image below), we can see that there is a nested **for j** loop within the **for i**. That meant that once the first **for i** loop is run, it would then move on to the **for j** loop. Once the **j loop** had finished iterating, it would go back to the **for i** loop and then repeat the **for j** loop. This loop would finally finish when the **for i** iterates to 11. By then the **for j** would have run 12 times within the **for i** loop. There was alot of unnecessary repetition. In the refactored script (right image below), the equivalent loop is not nested thus it will run once and as it iterates through the rows, the values are placed in the arrays by tickerIndex. Based on this project we can conclude that refactoring improved the performance and made the code more efficient. One of the drawbacks of refactoring, is that the process is very time consuming and may limit new development. However, i do believe that the advantages outweight the disadvantages as the demand or requirements change, a well designed and maintained code improves the longevity as well as provide a solid foundation for future upgrades.

Original                       | Refactored
:-------------------------:|:-------------------------:
![original code](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Screen%20Shot%202021-03-21%20at%201.02.52%20am.png)  |  ![refactored code](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Screen%20Shot%202021-03-21%20at%201.03.04%20am.png)



-----

### Screenshots

Execution time of the original script for 2017 (image 1)

![Original script 2017](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Original%20Run%20Time%202017.png)

***

Execution time of the original script for 2018 (image 2)

![Original script 2018](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Original%20Run%20Time%202018.png)

***

Execution time of the refactored script for 2017 (image 3)

![Refactored script 2017](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/VBA_Challenge_2017.png)

***

Execution time of the refactored script for 2018 (image 4)

![Refactored script 2018](https://github.com/YanLuong/stock-analysis/blob/main/vba_Challenge/Resources/Refactored%20Run%20Time%202018.png)










