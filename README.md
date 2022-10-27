# MechaCar_Statistical_Analysis

## Overview
In this analysis, I used R to explore MechaCar production data in order to troubleshoot issues that are blocking AutosRUs' manufacturing process.

## Results
Linear Regression to Predict MPG
I performed multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.


## total_summary

I then wrote an RScript that creates a lot_summary dataframe using the group_by() and the summarize() functions to group each manufacturing lot by the mean, median, variance, and standard deviation of the suspension coil’s PSI column.

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.

Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
It meets this specification for lots in total, however, Lot 3 individually does not. The variance of the suspension coils in Lot 3 exceeds 100 pounds per square inch. Its variance is 170 pounds per square inch. Lot 3's mean and median are also slightly smaller, and its standard deviation is larger than that of Lots 1 and 2.

T-Tests on Suspension Coils
In this deliverable, I performed t-tests to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch. I wrote RScripts using the t.test() function.

The following shows the summary of the t-tests:

t_test_total.png

This p-value for all is 0.5578, which is above above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis.

The three individual t-tests for each lot:


The sample means for lots 1 and 2 are 1500 and 1500.2 respectively, which matches the population mean of 1500. The p-values for lots 1 and 2 are 1.00 and 0.61, which are both above the significance level. These two lots are statisatically similar to the population.

On the other hand, Lot 3 yielded a slightly different sample mean of 1492 and a p-value of 0.04, which is less than the significance level of 0.05. For this case specifically, there is sufficient evidence to reject the null hypothesis and state that the two means are statistically different.

Production lot 3 may need a deeper examination in order to resolve the differences in suspension coils.

Study Design: MechaCar vs Competition
For the next part of this project, I designed a study to quantify how the MechaCar performs against the competition. I considered different metrics that would be of interest to a consumer: cost, city or highway fuel efficiency, horse power, maintenance cost, and safety rating.

What metric or metrics are you going to test?
I would test city and highway fuel efficiency and maintenance cost.

What is the null hypothesis or alternative hypothesis?
The null hypothesis would be: MechaCar has the same fuel efficiencies as competitors in the same class. The alternative hypothesis is that the fuel efficiencies are not all the same for each car in the class.

What statistical test would you use to test the hypothesis? And why?
I would use two-sample t-test because the success metrics are numerical (city and highway fuel efficiency) and the sample size is large. There are a number of other cars from different makers that are currently on the market to which we can compare the MechaCar.

What data is needed to run the statistical test?
In order to run the statistical test, the data needed includes the city fuel efficiency (city and highway mpgs), and maintenance cost (totals) for each car model. Maintenance cost data needed would include the cost for any repairs and other services needed. For current/next year newer models, there may not be as much data since these models most likely will not have needed much maintenance work performed.

It would be interesting to see how MechaCar compares to other cars in fuel efficiency and maintenance cost.
