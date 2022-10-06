# MechaCar_Statistical_Analysis

## Overview
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. An analysis was completed using R programming language to determine issues with AutosRUs' manufacturing.


## Resources
> * Languages: R
> * Tools: tidyverse, ggplot2, Rstudio, MS Excel
> * Data Sources: Suspension_Coil.csv, MechaCar_mpg.csv


## Linear Regression to Predict MPG
The MechaCar dataset of mpg was tested on 50 prototype cars. The MechaCar prototypes have multiple designs to identify ideal vehicle performance. Multiple metrics were collected for each vehicle and considered the the independent varibles in the dataset. These metrics are vehicle length, vehicle weight, spoiler angle, ground clearance and AWD. The dependent variable is mpg. A linear regression model was designed utilizing R language that predicts the mpg of MechaCar prototypes with several variables from the MechaCar_mpg.csv file.

![Summary of Linear Regression](Resources/Summary%20of%20Linear%20Regression%20Model.png)


### Results: 
> * The variables that provide a non-random amount of variance to the mpg values in the dataset are vehicle length and ground clearance.
> * The slope of the linear model would be considered as zero due to it being a incredibly small decimal.
> * The linear model predicts mpg of MechaCar prototypes effectively 71% of the time, as the R-squared value is 0.7149.



## Summary Statistics on Suspension Coils

In the MechaCar Suspension_Coil.csv dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.

## Manufacturing Lot Summary
Below is the summary statistics of all of the manufacturing lots. The mean is 1498.78 for this sample and the population mean was determined to be 1500.

![Manufacturing Lot Summary](Resources/Total%20Summary%20Suspension%20Coil.png)

### Summary by Manufacturing Lot Number
The means of the lot number are similar to the population mean and sample mean. 

![Summary by Manufacturing Lot Number](Resources/Summary%20by%20Manufacturing%20Lot%20Number.png)

### Results: 
> * The variance of the PSI for all manufacturing lots is 62.29356, which does not exceed the 100 pounds per square inch limit.
> * The variance for Lot 1 and Lot 2 meets the design specifications as their respective variance, falls within range. However, Lot 3 does not meet the design specifications as the variance is 170.2861224 and therefore exceeds the 100 pounds per square inch limit. As such, suspension coils from Lot 1 and Lot 2 should be used.


## T-Tests on Suspension Coils
T-tests were performed to determine if the PSI across all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. Confidence intervals or p-values can be utilized to determine whether results are statistically significant. Given that the confidence interval is 95%, the significance level is 0.05%. A confidence interval outlines the upper and lower limit for the mean.

### Suspension Coils Cumulative T-test
#![Commulative t-test](Resources/t-test%20for%20lots%20against%20psi.png)

### T-test  Lot 1
![Lot 1](Resources/t-test%20for%20lot%201.png)
### T-test  Lot 2
![Lot 2](Resources/t-test%20for%20lot%202.png)
### T-test  Lot 3
![Lot 3](Resources/t-test%20for%20lot%203.png)

### Results: 
> * Across all manufacturing lots, the PSI is not statistically different from the population mean of 1,500 pounds per square inch, as the p value of 0.06028 is higher than 0.05, which indicates strong evidence for maintaining the null hypothesis.
> * The PSI for manufacturing Lots 1 and 2 are not statistically different, as the respective p-values of 1 and 0.06072 are higher than 0.05. 
> * The PSI for Lot 3 is statistically different, as the p-value of 0.04168 is below 0.05, which indicates strong evidence for rejecting the null hypothesis.

## Study Design: MechaCar vs Competition
When comparing MechaCar to its competitor’s other metrics that could be of interest to a consumer could include cost, car color, city fuel efficiency, highway fuel efficiency, horsepower, maintenance cost, or safety rating.

> 1. What metric or metrics are you going to test?
The next metrics to test should be the safety rating, horsepower, and highway fuel efficiency, which address some safety concerns of consumers.

> 2. What is the null hypothesis or alternative hypothesis?
The null hypothesis is that the mean of the safety rating is zero. The alternative hypothesis is that the mean of the safety rating is not zero.

> 3. What statistical test would you use to test the hypothesis? And why?
Using a multiple linear regression statistical summary would show how the variables impact the safety ratings for MechaCar and their competitors.

> 4. What data is needed to run the statistical test?
A random sample of n > 30 for MechaCar and their competitor, would need to be collected including the safety ratings, highway fuel efficiency, and horsepower plus running the data through RStudio.
