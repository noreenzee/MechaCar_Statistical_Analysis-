# MechaCar_Statistical_Analysis-
![image](https://user-images.githubusercontent.com/112978144/224794769-95c82720-0c76-4193-b11f-db271cd48323.png)

#- OverView
In this module, we apply our understanding of statistics and hypothesis testing to analyze a series of datasets from the automotive industry. Our analysis includes visualizations, statistical tests, and interpretation of the results. All of our statistical analysis and visualizations are written in the R programming language.

Throughout the module, we extract, transform, and load (ETL) data; visualize the data; and analyze the data using R. Additionally, we learned a variety of statistical tests, their real-world application in data science, and their implementation in R. The goal was to apply these statistical concepts beyond this module, to any dataset, using any programming language—including Python.
# Auto RUs
![image](https://user-images.githubusercontent.com/112978144/224795892-b88aaf47-a9c0-4434-a0cd-345bfd20225a.png)
# R
R is a programming language that has a variety of uses in data science. R has solidified itself in academia and industry as one of the go-to programming languages for statistical modelling and hypothesis testing. In recent years, R developers have extended R's capabilities to generate machine learning algorithms and other advanced models to ensure that R can be used in every stage of data analytics.
# Challenge Discription
In this challenge, we were assigned to  help Jeremy and the data analytics team do the following:

Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.
#- Part 1: Linear Regression to Predict MPG
The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using our knowledge of R, we designed a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file.

#- Deliverable 1 
#- Results
Results for following requirements are below
Create a new RScript by going to the File menu. Select "New File," followed by "RScript," or you can click the icon in the top-left corner of the RStudio window. Note that the icon looks like a white square with a plus sign in the top left corner.

Use the library() function to load the dplyr package.

Import and read in the MechaCar_mpg.csv file as a dataframe.
![image](https://user-images.githubusercontent.com/112978144/224799842-80705fc3-1bf3-4e93-aaf5-b046186835bc.png)


Perform linear regression using the lm() function. In the lm() function, pass in all six variables (i.e., columns), and add the dataframe you created in Step 4 as the data parameter.

Using the summary() function, determine the p-value and the r-squared value for the linear regression model.
![image](https://user-images.githubusercontent.com/112978144/224799304-541be6fc-70c5-4a03-878c-bb55a53400bf.png)
#- Written Summary
From the above output we can assume that:

The vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. That shows that, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. The vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance with the dataset.

The p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This shows that there is sufficient evidence to reject the null hypothesis, which further indcates that the slope of this linear model is not zero.

This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model does predict mpg of MechaCar prototypes effectively.

#_ Deliverable 2 Requirements
In deliverable 2 we were assigned to find following outcomes
#-Part 2: Create Visualizations for the Trip Analysis
The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using our knowledge of R, we created a summary statistics table to show:

The suspension coil’s PSI continuous variable across all manufacturing lots.

The following PSI metrics for each lot: mean, median, variance, and standard deviation..

In your MechaCarChallenge.RScript, import and read in the Suspension_Coil.csv file as a table.

Write an RScript that creates a total_summary dataframe using the summarize() function to get the mean, median, variance, and standard deviation of the suspension coil’s PSI column.

The total summary dataframe showing the mean, median, variance, and standard deviation
![image](https://user-images.githubusercontent.com/112978144/224802473-26877003-394c-4f33-891d-34897c5fc77d.png)

Write an RScript that creates a lot_summary dataframe using the group_by() and the summarize() functions to group each manufacturing lot by the mean, median, variance, and standard deviation of the suspension coil’s PSI column. 
![image](https://user-images.githubusercontent.com/112978144/224802897-1253900f-7798-48bc-8224-f663fdbed27c.png)

*- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

--Whilw looking at the whole population of the production lot, the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement.

![image](https://user-images.githubusercontent.com/112978144/224803688-2539fa6c-1b2d-475e-bfe3-98642dae3178.png)
 *- Lot 1 and Lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. However, it is Lot 3 that is showing much larger variance in performance and consistency, that is  170.29. It is Lot 3 that is causing the variance at the full lot level.
![image](https://user-images.githubusercontent.com/112978144/224804253-5719267e-8ac9-458f-a584-36b0ddd76e02.png)


#- Part 3: T-Tests on Suspension Coils
Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

Follow the instructions below to complete Part 3.

Technical Analysis
In your MechaCarChallenge.RScript, write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.



Next, write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

# Results

*- write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

![image](https://user-images.githubusercontent.com/112978144/224848179-7923d21d-ad7b-4e20-a6e2-ee0bb4712acc.png)

*- write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.
![image](https://user-images.githubusercontent.com/112978144/224848514-1646ce9e-f39e-4db8-a93e-2c2f6be49d8d.png)

*-From above screenshots we can see that the true mean of the sample is 1498.78, which is same as in the summary statistics above. With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis. we can say that the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.

Next looking at each individual lots:

*- Lot 1 sample actually has the true sample mean of 1500. With a p-Value of 1, we cannot reject the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500).
Lot 2 has the same outcome with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar.
However, Lot 3,  is a different scenario. Here the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the common significance level of 0.05. All staitical measures are indicating to reject the null hypothesis that this sample mean and the presumed population mean are not statistically different.

# Deliverable 4
## Study Design: MechaCar vs Competition
In your description, address the following questions:
Q-What metric or metrics are you going to test?
Collecting data for comparable models for the following metrics:

*_Safety Feature Rating: Independent Variable
*_Current Price vs purchased price (Selling): Dependent Variable
*_Engine (Electric, Hybrid, Gasoline etc): Independent Variable
*_Average Annual Cost of Maintenance: Independent Variable
*_MPG: Independent Variable


Q-What is the null hypothesis or alternative hypothesis?


*-Null Hypothesis
MechaCar is priced correctly based on its performance of key factors.
*-Alternative Hypothesis
MechaCar is NOT priced correctly based on performance of key factors.
Q-What statistical test would you use to test the hypothesis? And why?
A multiple linear regression is best option to be used to determine the factors that have the highest correlation with the list of the selling price.
Q-What data is needed to run the statistical test?
MechaCar Analysis- RUs




