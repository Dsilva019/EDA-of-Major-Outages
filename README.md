# Exploratory Data Analysis of Major Outages
by Diego Silva (d1silva@ucsd.edu)



# Introduction
In this project, I studied prepared and cleaned a data set containing major outages reported by different states in the United States during January 2000-July 2016. In my analysis I wanted to investigate where and when do major outages tend to occur. This data set and analysis provides an understanding major outages patterns and how in the future they can be avoided to improve our electrical infrastructure.




# Cleaning and EDA

|   YEAR |   MONTH | U.S._STATE   | POSTAL.CODE   | NERC.REGION   | CLIMATE.REGION     |   ANOMALY.LEVEL | CLIMATE.CATEGORY   | CAUSE.CATEGORY     | CAUSE.CATEGORY.DETAIL   |   HURRICANE.NAMES |   OUTAGE.DURATION |   DEMAND.LOSS.MW |   CUSTOMERS.AFFECTED |   RES.PRICE |   COM.PRICE |   IND.PRICE |   TOTAL.PRICE |   RES.SALES |   COM.SALES |   IND.SALES |   TOTAL.SALES |   RES.PERCEN |   COM.PERCEN |   IND.PERCEN |   RES.CUSTOMERS |   COM.CUSTOMERS |   IND.CUSTOMERS |   TOTAL.CUSTOMERS |   RES.CUST.PCT |   COM.CUST.PCT |   IND.CUST.PCT |   PC.REALGSP.STATE |   PC.REALGSP.USA |   PC.REALGSP.REL |   PC.REALGSP.CHANGE |   UTIL.REALGSP |   TOTAL.REALGSP |   UTIL.CONTRI |   PI.UTIL.OFUSA |   POPULATION |   POPPCT_URBAN |   POPPCT_UC |   POPDEN_URBAN |   POPDEN_UC |   POPDEN_RURAL |   AREAPCT_URBAN |   AREAPCT_UC |   PCT_LAND |   PCT_WATER_TOT |   PCT_WATER_INLAND | OUTAGE.START        | OUTAGE.RESTORATION   |
|-------:|--------:|:-------------|:--------------|:--------------|:-------------------|----------------:|:-------------------|:-------------------|:------------------------|------------------:|------------------:|-----------------:|---------------------:|------------:|------------:|------------:|--------------:|------------:|------------:|------------:|--------------:|-------------:|-------------:|-------------:|----------------:|----------------:|----------------:|------------------:|---------------:|---------------:|---------------:|-------------------:|-----------------:|-----------------:|--------------------:|---------------:|----------------:|--------------:|----------------:|-------------:|---------------:|------------:|---------------:|------------:|---------------:|----------------:|-------------:|-----------:|----------------:|-------------------:|:--------------------|:---------------------|
|   2011 |       7 | Minnesota    | MN            | MRO           | East North Central |            -0.3 | normal             | severe weather     | nan                     |               nan |              3060 |              nan |                70000 |       11.6  |        9.18 |        6.81 |          9.28 | 2.33292e+06 | 2.11477e+06 | 2.11329e+06 |   6.56252e+06 |      35.5491 |      32.225  |      32.2024 |         2308736 |          276286 |           10673 |           2595696 |        88.9448 |        10.644  |       0.411181 |              51268 |            47586 |          1.07738 |                 1.6 |           4802 |          274182 |       1.75139 |             2.2 |      5348119 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2011-07-01 17:00:00 | 2011-07-03 20:00:00  |
|   2014 |       5 | Minnesota    | MN            | MRO           | East North Central |            -0.1 | normal             | intentional attack | vandalism               |               nan |                 1 |              nan |                  nan |       12.12 |        9.71 |        6.49 |          9.28 | 1.58699e+06 | 1.80776e+06 | 1.88793e+06 |   5.28423e+06 |      30.0325 |      34.2104 |      35.7276 |         2345860 |          284978 |            9898 |           2640737 |        88.8335 |        10.7916 |       0.37482  |              53499 |            49091 |          1.08979 |                 1.9 |           5226 |          291955 |       1.79    |             2.2 |      5457125 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2014-05-11 18:38:00 | 2014-05-11 18:39:00  |
|   2010 |      10 | Minnesota    | MN            | MRO           | East North Central |            -1.5 | cold               | severe weather     | heavy wind              |               nan |              3000 |              nan |                70000 |       10.87 |        8.19 |        6.07 |          8.15 | 1.46729e+06 | 1.80168e+06 | 1.9513e+06  |   5.22212e+06 |      28.0977 |      34.501  |      37.366  |         2300291 |          276463 |           10150 |           2586905 |        88.9206 |        10.687  |       0.392361 |              50447 |            47287 |          1.06683 |                 2.7 |           4571 |          267895 |       1.70627 |             2.1 |      5310903 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2010-10-26 20:00:00 | 2010-10-28 22:00:00  |
|   2012 |       6 | Minnesota    | MN            | MRO           | East North Central |            -0.1 | normal             | severe weather     | thunderstorm            |               nan |              2550 |              nan |                68200 |       11.79 |        9.25 |        6.71 |          9.19 | 1.85152e+06 | 1.94117e+06 | 1.99303e+06 |   5.78706e+06 |      31.9941 |      33.5433 |      34.4393 |         2317336 |          278466 |           11010 |           2606813 |        88.8954 |        10.6822 |       0.422355 |              51598 |            48156 |          1.07148 |                 0.6 |           5364 |          277627 |       1.93209 |             2.2 |      5380443 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2012-06-19 04:30:00 | 2012-06-20 23:00:00  |
|   2015 |       7 | Minnesota    | MN            | MRO           | East North Central |             1.2 | warm               | severe weather     | nan                     |               nan |              1740 |              250 |               250000 |       13.07 |       10.16 |        7.74 |         10.43 | 2.02888e+06 | 2.16161e+06 | 1.77794e+06 |   5.97034e+06 |      33.9826 |      36.2059 |      29.7795 |         2374674 |          289044 |            9812 |           2673531 |        88.8216 |        10.8113 |       0.367005 |              54431 |            49844 |          1.09203 |                 1.7 |           4873 |          292023 |       1.6687  |             2.2 |      5489594 |          73.27 |       15.28 |           2279 |      1700.5 |           18.2 |            2.14 |          0.6 |    91.5927 |         8.40733 |            5.47874 | 2015-07-18 02:00:00 | 2015-07-19 07:00:00  |

<iframe src="assets/num_outages.html" width=800 height=600 frameBorder=0></iframe>

<iframe src="assets/demandloss_duration.html" width=800 height=600 frameBorder=0></iframe>


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

|   YEAR |   CUSTOMERS AFFECTED Missing = False |   CUSTOMERS AFFECTED Missing = True |
|-------:|-------------------------------------:|------------------------------------:|
|   2000 |                           0.0192484  |                          0.0112867  |
|   2001 |                           0.00733272 |                          0.0158014  |
|   2002 |                           0.0146654  |                          0.00225734 |
|   2003 |                           0.0394134  |                          0.00677201 |
|   2004 |                           0.0586618  |                          0.0158014  |
|   2005 |                           0.0467461  |                          0.00902935 |
|   2006 |                           0.0531622  |                          0.020316   |
|   2007 |                           0.0375802  |                          0.03386    |

<iframe src="assets/year_missingness.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="assets/year_missingness_tvd_dist.html" width=800 height=600 frameBorder=0></iframe>


<iframe src="assets/kde_plot_real_vs_cust.html" width=800 height=600 frameBorder=0></iframe>

# Hypothesis Testing

| NERC.REGION   |     Fall |   Spring |   Summer |    Winter |
|:--------------|---------:|---------:|---------:|----------:|
| ECAR          | 0.235294 | 0.264706 | 0.411765 | 0.0882353 |
| FRCC          | 0.325581 | 0.186047 | 0.325581 | 0.162791  |
| FRCC, SERC    | 0        | 0        | 0        | 1         |
| HECO          | 0.666667 | 0        | 0.333333 | 0         |
| HI            | 1        | 0        | 0        | 0         |

<iframe src="assets/outage_dist_spp_overall.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="assets/emp_tvd_dist_spp_overall.html" width=800 height=600 frameBorder=0></iframe>
