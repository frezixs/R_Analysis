# R_Analysis

## Project Overview
This project uses R and some statistics, hypothesis testing and linear regression knowledge to analyze a series of datasets 
from the MechaCar industry.

## Linear Regression to Predict MPG
![image](https://user-images.githubusercontent.com/49871539/128645708-dc0bebc7-4171-4801-9029-d3f5fd2e62d6.png)

#### Question 1: Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
p-value represents the probability that each coefficient contributes a random amoumt of variance to the linear model 
with a significant level of 0.05, only vehicle_length and ground_clearance provide a non random amount of variance to the 
linear model of mpg. 

#### Question 2: Is the slope of the linear model considered to be zero? Why or why not?
The slope of the linear model is not considered to be zero. 
since our null hypothesis is that all slope is zero, however, the p-value of vehicle_length and ground_clearance 
is less than 0.05, so we reject the null hypothesis, therefore at least for vehicle_length and ground_clearance columns, 
the slope is not zero. 
The approximated linear model is 
mpg = 6.27 * vehicle_length - 3.41 * AWD + 3.55 * ground_clearance - 104

#### Question 3: Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The adjusted R-square is 0.6825, so this linear model is considered as effective. 

## Summary Statistics on Suspension Coils
#### total_summary 
![image](https://user-images.githubusercontent.com/49871539/128646179-82a1c7b4-4efb-4a32-8334-1744d13d327a.png)

#### lot_summary 
![image](https://user-images.githubusercontent.com/49871539/128646196-da3579e3-e83d-43f6-b6b0-8c723cf99011.png)

#### Question 1: The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
The design specs are respected for all manufacturing lots in total with a global variance of 62.3 psi.
On the lot level, Lot 1 and Lot 2 are into specs with respectively variances of 0.98 and 7.5 psi. 
The Lot 3 is out of specs with a variance of 170.3 psi.

## T-Tests on Suspension Coils
#### T-Test all manufacturing lots against the population mean
![image](https://user-images.githubusercontent.com/49871539/128646409-23b063f6-ea76-4ce7-921b-a8ac75308a8e.png)
Assuming our significance level is the common 0.05 percent, our p-value of 0.069 is above the significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we can state that the PSI across all manufacturing lots is statiscally similar to the population mean of 1498.78 psi.

#### T-Tests each manufacturing lot against the population mean
![image](https://user-images.githubusercontent.com/49871539/128646456-603d066e-1969-42b0-a90f-9a0ff9693b38.png)
![image](https://user-images.githubusercontent.com/49871539/128646459-c020c1f1-0e6b-4fc4-8b9e-0d5bbaf4781d.png)
![image](https://user-images.githubusercontent.com/49871539/128646462-b02fd8f1-0168-4bfd-afec-42b62a6afbe2.png)

For Lot 1: the p-value is below the significance level of 0.05 percent, so we can reject the null hypothesis and conclude that the PSI across the Lot 1 is statistically different from the population mean.

For Lot 2 and 3: both p-values are above the significance level, so we can conclude that the PSI for Lot2 and Lot3 are statistically similar to the population mean.

## Study Design: MechaCar vs Competition
To compare the performance of the MechaCar prototype against the vehicles from the competition, we will perform a statistical analysis based on the following metrics:

the "0 to 60 mph" time,
the braking distance,
the fuel economy (mpg),
the Power,
the safety rating.

In our case the null hypothesis would be: each performance metrics is statistically similar between the MechaCar prototype and all vehicle from the other manufacturers.

We would use a one-way ANOVA test. This test is used to compare the means of a continuous numerical variable across a number of groups.
So in this analysis we would compare the means for each metric across the different manufacturers.

To perform the test, we would need data of MechaCar vehicles and its competition, all gathered in a single dataframe where each metric is a column.











