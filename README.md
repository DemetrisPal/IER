# title: What is the effect of lockdown in 2020 on students who moved out for studies, regarding the calories burnt each day, an observational study.

This project aims to study the behavior of students of Erasmus University Rotterdam before and during lockdown. A questionnaire was used to collect information about the activity of the students as well as the Omron device which measures calories and steps per day. A statistical test gave an insight on the data as how significant the change of the activity of the students was from the year 2019 to 2020. The main focus of the study was on the part of students who moved out during their studies and they were living alone or with other students.

## Getting Started

These instructions will give you a copy of the project up and running on
your local machine for development and testing purposes.


### Installing

You just need a working software of Microsoft excel and the .xlsx file provided in the github link.

## Running/Reproducing the tests

The statistical test used is unpaired T-test for two independent groups. There is not any steps to follow to get the results as they are ready to use in the .xlsl file provided. Below I provide the steps I used to make this file.

PROCEDURE
	step1: Open the "Demetris Palochis.xlsx" file and go to the "Data used" sheet.
	step2: In a new column use the function SUM to calculate the total amount of calories burnt by each student during the period of 7 days. To do that enter in the first row of your new column "=SUM(" , then select the appropriate cells of the participant of the first row, type ")" and press ENTER. Then hover over the new value you calculated, at the bottom right of the cell until the small cross appears. Drag and drop that cross downwards until all of the data are selected.
	step3: Now calculate the average calories per day. In a similar way as in step2, go to the first row and divide the SUM by 7 (type: =[@[Sum of calories]]/7). Then apply that formula to all of the rows.
	step4: Calculate the mean for 2019 and for 2020. Use the filters on the first row of the grid to make an ascending order in the year column. Then, below the column with the average calories per day, use the function AVERAGE() to calculate a mean value for 2019 and 2020 by selecting the corresponding cells of the same column.
	step5: In a similar manner as in step4, calculate the standard deviation for each year. Use the function STDEV.S() .
	step6:  Proceed with the T-test. In the excel file the test was carried out in the "T test" sheet. You can do it in the same sheet. First use the function count to find the number of samples per year (count). Then substract 1 by each number to find the degrees of freedom per year (df).
	step7: Calculate the sum of squares for each year (SS1 and SS2). Multiply the square of standard deviation with the degrees of freedom for each year.
	step8: Calculate the square overall standard deviation (sp^2), this gives one value for both years.  This is equal to the sum of SS1 and SS2 over the sum of standard deviations ((SS1 + SS2)/(SD1+SD2)).
	step9: The calculate the T-value. T-value is equal to the difference of the mean values over the squareroot of (sp^2/n1 + sp^2/n2), where sp^2 is the square overall standard deviation and n1, n2 are the number of sample for 2019 and 2020 respectively.
	step10: Calculate the P-value. Use the function T.DIST.2T(x1 ; x2). In the place of x1 use the absolute value of T-value and in the place of x2 use the total number of degrees of freedom which is the sum of df1 and df2.

ADDITIONAL: Calculate and plot the normal distribution for 2019 and 2020 separately. For each set of values of mean calories burnt, use the function NORM.DIST(x1 ; x2 ; x3 ; FALSE). For x1 use the value of mean calories per day at each row, for x2 use the mean value of the corresponding year, x3 use the corresponding standrad deviation and finally add the value FALSE. This function should be used at each row of the data but the mean value and standard deviation should be for the correct year (2019 or 2020). The plot in a scatter graph the average calories per day versus the normalised value. You should produce two separate graphs of a bell-shaped curve. To make a tidy curve use the filtes on the top to make the normalised value ascending from low to high values. You can see the graphs at the last two sheets of the excel file.

### Style test

In this study I used the software Microsoft Excel version 2104. I chose this software as it was the first time I was doing a statistical test and at the same time Excel provides with very useful and easy fucntions to perform the test correctly. Besides, the study was simple and a Python/Matlab code was not providing a better result. In most cases, with big datasets a code in Python, Matlab or any other language is written, as it is more efficient and professional.

## Authors

Demetris Palochis
email: dpalochis@student.tudelft.nl
