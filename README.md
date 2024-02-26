## Online Ad-click Data Analysis Using Statistical Procedure 

### Problem Statement

Fred, a loyal friend, has opened a burger bistro in Brisbane but is facing slow business. To attract customers, he plans an online advertising campaign targeting residents every weekday from 11:00 a.m. to 1:00 p.m. with 3,000 ads, costing one cent each. The ad text promotes his tasty burgers and directs users to his site. Fred, displeased with the blue text, decides to experiment with 30 different colors over a month, distributing 3,000 ads evenly by color daily. The ad software tracks views and clicks, storing the data in a table.

Now, Fred seeks your help to interpret the results of his experiment. He wants to identify a color that significantly outperforms blue in attracting ad clicks. Despite being skilled at burgers, Fred lacks data analysis expertise, and he offers free burgers for a year if you assist him in analyzing and comparing daily clicks in the table.

### Dataset Description

The ad-click data is stored in a .csv file named colored_ad_click_table.csv, where columns are separated by commas. The first line contains column labels such as Color, Click Count: Day 1, View Count: Day 1, and similar labels for the other 19 days of the experiment. The Color column represents 30 possible text colors. Columns Click Count and View Count for each day tally the clicks and views of colored ads on that specific day. Fred expects daily views to be 100 for each color. The file structure is organized, providing data on clicks and views for all 30 colors over 20 days of Fred's experiment.

### Libraries used
- Numpy 1.25.2
- Pandas 1.5.3
- Seaborn 0.13.1
- Matplotlib 3.7.1

### Conclusion
In our analysis, we discovered that while most colors exhibited a significant deviation in ad-click percentages from blue, not all are practical for advertising purposes. Notably, black yielded the least p-value, emphasizing its suboptimal choice for clickability due to design considerations. Further investigation revealed that the mean click rate of black is significantly below the blue, suggesting that other colors with similar low p-values may share inferior click rates.

Among the colors with a mean higher than blue, such as Sapphire, Navy, Teal, Ultramarine, and Aquamarine, only Ultramarine displayed a p-value below 0.05. However, caution is warranted. Multiple comparison problems arise when conducting numerous experiments on the same dataset, leading us to employ Bonferroni Correction. Consequently, the statistically significant result for Ultramarine disappears.

Considering this, Fred's decision to swap Blue for Ultramarine remains inconclusive. A targeted experiment involving only the five promising colors could provide a more accurate assessment. By running a single experiment without the need for Bonferroni correction, Fred can determine whether Ultramarine outperforms blue, guiding his advertising strategy.

