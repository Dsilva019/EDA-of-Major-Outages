# Exploratory Data Analysis of Major Outages
by Diego Silva (d1silva@ucsd.edu)



# Introduction
In this project, I studied prepared and cleaned a data set containing major outages reported by different states in the United States during January 2000-July 2016. In my analysis I wanted to investigate where and when do major outages tend to occur. This data set and analysis provides an understanding major outages patterns and how in the future they can be avoided to improve our electrical infrastructure. Moving foward I will reference the data set as outages.




# Cleaning and EDA
In my data cleaning process I first looked at the raw data set to assess what steps needed to be done. I looked for any unnecessary rows and columns, checked the columns names, and anything else that looked out of the ordinary for a data set. In my specific case I noticed there were a couple of columns and rows that were unnecessary and the columns names were incorrect. So I dropped said columns, I set the columns to their proper respective names, and reset the index of the data frame. Lastly, I ensured the data types of the columns were best possible type that allowe me to properly analyze the data frame.

|   YEAR |   MONTH | U.S._STATE   | POSTAL.CODE   | NERC.REGION   | CLIMATE.REGION     |   ANOMALY.LEVEL | CLIMATE.CATEGORY   | CAUSE.CATEGORY     | CAUSE.CATEGORY.DETAIL   |   HURRICANE.NAMES |   OUTAGE.DURATION |   DEMAND.LOSS.MW |   CUSTOMERS.AFFECTED |   RES.PRICE |   COM.PRICE |   IND.PRICE |   TOTAL.PRICE |   RES.SALES |   COM.SALES |   IND.SALES |   TOTAL.SALES |   RES.PERCEN |   COM.PERCEN |   IND.PERCEN |   RES.CUSTOMERS |   COM.CUSTOMERS |   IND.CUSTOMERS |   TOTAL.CUSTOMERS |   RES.CUST.PCT |   COM.CUST.PCT |   IND.CUST.PCT |   PC.REALGSP.STATE |   PC.REALGSP.USA |   PC.REALGSP.REL |   PC.REALGSP.CHANGE |   UTIL.REALGSP |   TOTAL.REALGSP |   UTIL.CONTRI |   PI.UTIL.OFUSA |   POPULATION |   POPPCT_URBAN |   POPPCT_UC |   POPDEN_URBAN |   POPDEN_UC |   POPDEN_RURAL |   AREAPCT_URBAN |   AREAPCT_UC |   PCT_LAND |   PCT_WATER_TOT |   PCT_WATER_INLAND | OUTAGE.START        | OUTAGE.RESTORATION   |
|-------:|--------:|:-------------|:--------------|:--------------|:-------------------|----------------:|:-------------------|:-------------------|:------------------------|------------------:|------------------:|-----------------:|---------------------:|------------:|------------:|------------:|--------------:|------------:|------------:|------------:|--------------:|-------------:|-------------:|-------------:|----------------:|----------------:|----------------:|------------------:|---------------:|---------------:|---------------:|-------------------:|-----------------:|-----------------:|--------------------:|---------------:|----------------:|--------------:|----------------:|-------------:|---------------:|------------:|---------------:|------------:|---------------:|----------------:|-------------:|-----------:|----------------:|-------------------:|:--------------------|:---------------------|
|   2011 |       7 | Minnesota    | MN            | MRO           | East North Central |            -0.3 | normal             | severe weather     | nan                     |               nan |              3060 |              nan |                70000 |       11.6  |        9.18 |        6.81 |          9.28 | 2.33292e+06 | 2.11477e+06 | 2.11329e+06 |   6.56252e+06 |      35.5491 |      32.225  |      32.2024 |         2308736 |          276286 |           10673 |           2595696 |        88.9448 |        10.644  |       0.411181 |              51268 |            47586 |          1.07738 |                 1.6 |           4802 |          274182 |       1.75139 |             2.2 |      5348119 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2011-07-01 17:00:00 | 2011-07-03 20:00:00  |
|   2014 |       5 | Minnesota    | MN            | MRO           | East North Central |            -0.1 | normal             | intentional attack | vandalism               |               nan |                 1 |              nan |                  nan |       12.12 |        9.71 |        6.49 |          9.28 | 1.58699e+06 | 1.80776e+06 | 1.88793e+06 |   5.28423e+06 |      30.0325 |      34.2104 |      35.7276 |         2345860 |          284978 |            9898 |           2640737 |        88.8335 |        10.7916 |       0.37482  |              53499 |            49091 |          1.08979 |                 1.9 |           5226 |          291955 |       1.79    |             2.2 |      5457125 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2014-05-11 18:38:00 | 2014-05-11 18:39:00  |
|   2010 |      10 | Minnesota    | MN            | MRO           | East North Central |            -1.5 | cold               | severe weather     | heavy wind              |               nan |              3000 |              nan |                70000 |       10.87 |        8.19 |        6.07 |          8.15 | 1.46729e+06 | 1.80168e+06 | 1.9513e+06  |   5.22212e+06 |      28.0977 |      34.501  |      37.366  |         2300291 |          276463 |           10150 |           2586905 |        88.9206 |        10.687  |       0.392361 |              50447 |            47287 |          1.06683 |                 2.7 |           4571 |          267895 |       1.70627 |             2.1 |      5310903 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2010-10-26 20:00:00 | 2010-10-28 22:00:00  |
|   2012 |       6 | Minnesota    | MN            | MRO           | East North Central |            -0.1 | normal             | severe weather     | thunderstorm            |               nan |              2550 |              nan |                68200 |       11.79 |        9.25 |        6.71 |          9.19 | 1.85152e+06 | 1.94117e+06 | 1.99303e+06 |   5.78706e+06 |      31.9941 |      33.5433 |      34.4393 |         2317336 |          278466 |           11010 |           2606813 |        88.8954 |        10.6822 |       0.422355 |              51598 |            48156 |          1.07148 |                 0.6 |           5364 |          277627 |       1.93209 |             2.2 |      5380443 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2012-06-19 04:30:00 | 2012-06-20 23:00:00  |
|   2015 |       7 | Minnesota    | MN            | MRO           | East North Central |             1.2 | warm               | severe weather     | nan                     |               nan |              1740 |              250 |               250000 |       13.07 |       10.16 |        7.74 |         10.43 | 2.02888e+06 | 2.16161e+06 | 1.77794e+06 |   5.97034e+06 |      33.9826 |      36.2059 |      29.7795 |         2374674 |          289044 |            9812 |           2673531 |        88.8216 |        10.8113 |       0.367005 |              54431 |            49844 |          1.09203 |                 1.7 |           4873 |          292023 |       1.6687  |             2.2 |      5489594 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2015-07-18 02:00:00 | 2015-07-19 07:00:00  |

The bar plot below presents the count of outages that occured in each U.S state. One interesting note is that the California seems to have a significantly higher count outages compared to the rest of the states, even though it is not the biggest state by land area.

<iframe src="assets/num_outages.html" width=800 height=600 frameBorder=0></iframe>

The scatter plot below presents the relationship between the OUTAGE DURATION and DEMAND LOSS MW columns of Outages. The plot suggests that short Outage Duration times results in a higher Demand Loss (MW) and longer Outage Duration times results in a lower Demand Loss (MW).

<iframe src="assets/demandloss_duration.html" width=800 height=600 frameBorder=0></iframe>

This table shows gives a break down of Outage CATEGORY CAUSE for each state, showing which Outage CATEGORY CAUSE is the most and least common among each state. Also gives a general idea how severe the problem of outages is in each state.

| U.S._STATE           |   equipment failure |   fuel supply emergency |   intentional attack |   islanding |   public appeal |   severe weather |   system operability disruption |
|:---------------------|--------------------:|------------------------:|---------------------:|------------:|----------------:|-----------------:|--------------------------------:|
| Alabama              |                   0 |                       0 |                    1 |           0 |               0 |                5 |                               0 |
| Alaska               |                   1 |                       0 |                    0 |           0 |               0 |                0 |                               0 |
| Arizona              |                   4 |                       0 |                   18 |           0 |               0 |                4 |                               2 |
| Arkansas             |                   1 |                       0 |                    6 |           1 |               7 |               10 |                               0 |
| California           |                  21 |                      17 |                   24 |          28 |               9 |               70 |                              41 |
| Colorado             |                   0 |                       1 |                    5 |           1 |               0 |                4 |                               4 |
| Connecticut          |                   0 |                       0 |                    8 |           0 |               0 |               10 |                               0 |
| Delaware             |                   1 |                       0 |                   37 |           0 |               0 |                2 |                               1 |
| District of Columbia |                   1 |                       0 |                    0 |           0 |               0 |                9 |                               0 |
| Florida              |                   4 |                       0 |                    2 |           0 |               3 |               26 |                              10 |


# Assessment of Missingness
## NMAR Analysis:
In the Outages data frame, the 'CAUTEGORY.CAUSE.DETAIL' column is supposed to give a specific reason for the 'CATEGORY.CAUSE' of the outage. This column could be NMAR because the reason why a value would be missing can be due to negligence of the person logging the data because they may have felt the specific reason may not be significant enough or if an investigation was not done. This column would be MAR if another column provided information whether an investigation was done to figure out the specific cause of the outage.

## Missingness Dependency:
I wanted to find out a column in which the missingness of 'CUSTOMERS.AFFECTED' was dependent on and a column in which its missingness was not dependent on. For this investigation I chose the 'YEAR' and 'PC.REALGSP.CHANGE' columns to test the missingness dependency of these columns.

For my test of the missingness dependency on the 'YEAR' column, I first created a distribrution plot as seen below. This plot shows the distribution of 'YEAR' by missingness of 'CUSTOMERS.AFFECTED'. To investiage whether the differences in the distributions were significant, I decided to perform a permutation test.

<iframe src="assets/year_missingness.html" width=800 height=600 frameBorder=0></iframe>


 My null hypothesis, the distribution of 'YEAR' when 'CUSTOMERS' is missing is the same as the distribution of 'YEAR' when 'CUSTOMERS.AFFECTED' is not missing. My alternative hypothesis, The distribution of 'YEAR' when 'CUSTOMERS' is missing is not the same as the distribution of 'YEAR' when 'CUSTOMERS.AFFECTED' is not missing. I decided to use the total variation distance (tvd) as my test statistic, the observed tvd value I saw was 0.306. Additionally, I chose a significance level of 0.05 as a cut off for my p-value, since a p-value smaller than 0.05 indicates a strong evidence against my null hypothesis. The plot below shows the results of my permuation test. It displays the emperical distribution of the generated TVDs under the null. The green line shows the observed value. The p-value I calculated was essentially 0.

<iframe src="assets/year_missingness_tvd_dist.html" width=800 height=600 frameBorder=0></iframe>

In conclusion, we reject the null, since my p-value, 0, is smaller than the 0.05 significance level. There is strong enough evidence to suggest the distribution of 'YEAR' when 'CUSTOMERS.AFFECTED' is missing is not the same as the distribution of 'YEAR' when 'CUSTOMERS.AFFECTED' is not missing. As a result, we conclude that the CUSTOMERS.AFFECTED column is dependent on the 'YEAR' column.

For my test of the missingness dependency on the 'PC.REALGSP.CHANGE' column, I first created a kernal density plot as seen below. This plot shows the kernel density of 'PC.REALGSP.CHANGE' by missingness of 'CUSTOMERS.AFFECTED'. Since the difference of means of the plots was 0.0577, which tells us the means of the two distributions are similar. But as seen in the plot the shapes look different. As a result, I decided to test whether the differences in shape were significant or not by using the Kolmogorov-Smirnov (ks) test statistic as my test statistic for this permutation test. My Null Hypothesis, the shape of the distribution of 'PC.REALGSP.CHANGE' when 'CUSTOMERS.AFFECTED' is missing is the same as the shape of the distribution of 'PC.REALGSP.CHANGE' when 'CUSTOMERS.AFFECTED' is not missing. My alternative hypothesis , the shape of the distribution of 'PC.REALGSP.CHANGE' when 'CUSTOMERS.AFFECTED' is missing is not the same as the shape of the distribution of 'PC.REALGSP.CHANGE' when 'CUSTOMERS.AFFECTED' is not missing. Additionally, I chose a significance level of 0.05 as a cut off for my p-value, since a p-value smaller than 0.05 indicates a strong evidence against my null hypothesis.

<iframe src="assets/kde_plot_real_vs_cust.html" width=800 height=600 frameBorder=0></iframe>

After performing the permutation test with the ks as my test statistic, I got a p-value of 0.279.

Since the p-value is greater than the 0.05 significance level, we fail to reject the null. There is not enough evidence to suggest that the shape of the distribution of 'PC.REALGSP.CHANGE' when 'CUSTOMERS.AFFECTED' is missing is not the same as the shape of the distribution of 'PC.REALGSP.CHANGE' when 'CUSTOMERS.AFFECTED' is not missing.

## Overall Conclusion:
In my missingness dependency investigation, I concluded that the missingness of the 'CUSTOMERS.AFFECTED' column is dependent on the 'YEAR' but the same can be said for the 'PC.REALGSP.CHANGE'.

# Hypothesis Testing
To answer my main question I decided to compare the distributions of the outages in each season of the SPP Region and the Overall NERC Region distribution of outages in each season. The table below displays said distributions.

| NERC.REGION   |     Fall |   Spring |   Summer |    Winter |
|:--------------|---------:|---------:|---------:|----------:|
| ECAR          | 0.235294 | 0.264706 | 0.411765 | 0.0882353 |
| FRCC          | 0.325581 | 0.186047 | 0.325581 | 0.162791  |
| FRCC, SERC    | 0        | 0        | 0        | 1         |
| HECO          | 0.666667 | 0        | 0.333333 | 0         |
| HI            | 1        | 0        | 0        | 0         |

The chart below displays the distributions of the outages in each season in the SPP Region and the Overall NERC Region distribution of outages in each season. I noticed that there does seem to be a difference between the distributions but to test whether the differences are significant or not I decided to perform a hypothesis test. Like my previous tests, I chose a significance level of 0.05 as a cut off for my p-value, since a p-value smaller than 0.05 indicates a strong evidence against my null hypothesis.

<iframe src="assets/outage_dist_spp_overall.html" width=800 height=600 frameBorder=0></iframe>

My null hypothesis, there is not a difference between the season distributions between the SPP Region and the overall distribution of the seasons in the NERC Regions. My alternative hypothesis, there is a difference between the season distributions between the SPP Region and the overall distribution of the seasons in the NERC Regions. For my hypothesis I will use total variation distance, since I am a comparing the distributions of outages in each seasons which are categorical distributions. My observed tvd was, 0.123.

After performing my hypothesis, I plotted my results in the plot below. The plot displays the empirical distributions of the generated TVDs under the null. The green line in the plot represents my observed tvd. Additionally, my calculated p-value was 0. Which can be seen in the graph since there are essentially no tvds generated in the hypothesis test under the null that were equal to or greater than my observed.

<iframe src="assets/emp_tvd_dist_spp_overall.html" width=800 height=600 frameBorder=0></iframe>

In conclusion, the probability that the observed TVD came from the distribution of TVDs under that the assumption that null is true is essentially 0. Additionally, my p-value was smaller than the 0.05 significance level, we reject the null. There is strong enough evidence to suggest that the distribution of outages for each season in the SPP Region is different from the distribution of outages for each season for  Region.
