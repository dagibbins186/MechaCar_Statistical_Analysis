# Context
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called for a review of the production data. The goal is to generate insights that may help the manufacturing team via:
\
\
-a multiple linear regression analysis that identifies which variables in the dataset predict the mpg of MechaCar prototypes
\
-a set of summary statistics about the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
\
-a group of t-tests to determine if the manufacturing lots are statistically different from the mean population
\
\
Finally, Auto RU is asking for a statistical study to compare MechaCar vehicles against the vehicles from other manufacturers. Once the production troubles are fixed, it's time to take MechaCar to market! To be successful, Auto RU needs to know about its strengths and competition.

# Linear Regression to Predict MPG
This analysis examines variables of vehicle length, vehicle weight, spoiler angle, ground clearance, all wheel drive (AWD) and miles per gallon (mpg). It uses R to design a linear model that predicts the mpg of MechaCar prototypes. An R^2 of .7149 indicates that the model explains 71% of mpg predictions. The p-value of 5.35e-11 also suggests the results are not due to chance. The vehicle length and ground clearance statistically impact mpg. Conversely, vehicle weight, spoiler angle, and AWD produce only random variance. 


# Summary Statistics on Suspension Coils
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI). Together, all manufacturing lots meet these design specifications. The variance is 62.30.
\
\
!["Total_Summary_DataFrame.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/Total_Summary_DataFrame.PNG)
\
\
On average, the PSI is 1499, and the median is 1500. The mean and median are almost the same, showing the data is evenly distributed. However, a break down into the three types of lots reveals another picture. Lot 3 does not meet the PSI-requirement. Lot 1 and lot 2 produce variance within the limits.
\
\
!["Lot_Summary_DataFrame.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/Lot_Summary_DataFrame.PNG)
\
\
Lot 3 has a variance of 170 PSI. Its data appears far more spread out than Lot 1 or Lot 2, which have variances of .98 and 7.47 respectively. Lot 1 and Lot 2's small variances advise that their data points tend to be very close to the mean, and to each other. On the other hand, Lot 3's variance exceeds the 100 PSI threshold, and disproportionately affects the total lot's variance of 62.30. 


# Comparison of Manufacturing Lots to the Population
A T-Test looks all the manufacturing lots' and each of the manufacturing lot's mean PSI relative to the total population's PSI. The total population's mean is 1500 PSI while the mean of all manufacturing lots is 1499. With a P-Value of .06, these means all lots are statistically similar to the total population. The same is true for Lot 1 and Lot 2. When the manufacturing lots are broken apart, Lot 1 and Lot 2's means of 1500.2 and 1500.00 predictably vary insignificantly from the total population's mean of 1500. Only Lot 3 shows a statistically significant difference of means. On average, Lot 3's PSI is 1496. This generates a P-value of .04 when it's compared to the total population.

# Study Design: MechaCar vs Competition
**Problem Statement**
\
MechaCar faces a competitive market. To sell its product, MechaCar needs to formalize its value proposition, and identify how it compares to competitors. 
\
**Metrics**
\
Road Test (Independent variable)
\
Reliability (Independent variable)
\
Owner Satisfaction (Dependent variable)
\
Safety (Independent variable)
\
**Hypothesis**
\
Alternate Hypothesis: Road test, reliability and safety predict owner satisfaction.
Null Hypothesis: Road test, reliability and safety do not predict owner satisfaction.
\
**Statistical Test**
\
Multiple linear regression (MLR), also known simply as multiple regression, is a statistical technique that uses several explanatory variables to predict the outcome of a response variable. First, it is recommended that MechaCar determine if the variables (Road Test, Reliability and Safety) predicts owner satisfaction or not. With this information, MechaCar can see what customers value. Then, with a T-Test, MechaCar can establish difference between itself and a competitor by these variables. If there is a significant difference between MechaCar and a competitiors, then MechaCar can effectively market its differentiation by what customer's want.
\
# Appendix
## Modeling for Linear Regression to Predict MPG
!["Variables-Coefficients-MPG.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/Variables-Coefficients-MPG.PNG)
!["Coefficients_Intercepts_MPG.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/Coefficients_Intercepts_MPG.PNG)
!["F-Statistic-MPG.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/F-Statistic-MPG.PNG)


## Modeling for Summary Statistics on Suspension Coils
!["Read_Suspension_Coil_CSV.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/Read_Suspension_Coil_CSV.PNG)
!["Total_Summary_Lot_Summary_Code.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/Total_Summary_Lot_Summary_Code.PNG)


## Modeling for T-Test and Comparisons between Manufacturing Lots/ the Population**
!["T-Test.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/T-Test.PNG)
!["T_TestLot3.PNG"](https://github.com/dagibbins186/MechaCar_Statistical_Analysis/blob/main/Images/T_TestLot3.PNG)
