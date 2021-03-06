
# PyCitySchools_Challenge


## Overview of PyCityShcools Challenge
The goal of this challenge was to analyze the standardized testing results from a large number of schools state-wide. The test results covered both Math and Reading from 9th to 12th grade and the purpose of this analysis was to see how removing test results from Thomas High School's 9th grade class affect the overall results we obtained from the assignment in Module 4 ( see 
![A test image](Images\Screenshot 1 .png)
In Module 4 we found the overall passing percentage of the students and determine whether there is any correlation with the budget per student.
Deliverable 1: Replace Thomas High School's 9th-grade reading and math scores with Nan.
We used the loc method to select all the reading and math scores from the ninth grade at Thomas High School. Inside the loc method a comparison operator was used to retrieve all the rows with Thomas High School, logical and comparison operators were used to retrieve all the rows with the "reading_score" and "math_score" column. The reading and math score for the ninth graders in Thomas High School are replaced with Nans. The code and table can be seen below.


![test](./Images/Screenshot_1.png)

![test](./Images/Screenshot_2.png)

![test](./Images/Screenshot_3.png)

![test](./Images/Screenshot_4.png)


## Deliverable 2: 
Repeat the School District Analysis
In this section, we reanalyzed the following metrics after excluding the 9th-graders test results:
* The District summary
* The school summary
* The top 5 and bottom 5 performing schools, based on the overall passing rate
* The average reading score for each grade level from each school
* The average math score for each grade level from each school
* The scores by school spending per student, by school size and by school type
________________________________________
### The District summary
Recalculated total student count by subtracting the number of ninth-grade students in Thomas High School from the total student count, then recalculated the passing math and passing reading percentages and overall passing percentage.
Using the new student total and recalculated math, reading and overall passing percentage.
 I created a new data frame and formatted the values accordingly as seen below :
 
![test](./Images/Screenshot_5.png)

![test](./Images/Screenshot_6.png)

![test](./Images/Screenshot_7.png)

![test](./Images/Screenshot_8.png)

![test](./Images/Screenshot_9.png)

![test](./Images/Screenshot_10.png)

![test](./Images/Screenshot_11.png)

![test](./Images/Screenshot_12.png)

![test](./Images/Screenshot_13.png)

![test](./Images/Screenshot_14.png)

![test](./Images/Screenshot_15.png)

![test](./Images/Screenshot_16.png)

![test](./Images/Screenshot_17.png)

 
### The school summary
Using the same methods from previous examples I created a data frame, including the data metrics: School Type, total students, total school budget, per student budget, average math score, average reading score, passing math percentage, passing reading percentage and overall passing percentage. I formatted the school budget and per student budget to include the dollar sign and set the values to show to the hundreds place. You can see the data in the screenshot.  
 
 ### The top 5 and bottom 5 performing schools, based on the overall passing rate
![test](./Images/Screenshot_18.png)
To find the top 5 and bottom 5 performing schools, I recalculated the passing math percentage, passing reading percentage and overall passing percentage of Thomas High School and entered the new data into the school summary data frame.
After calculating the total number of students in 10th, 11th, and 12th grade I calculated the number of those students who passed math and reading.
* Total number of students in 10th - 12th grade: 1174
* 	Passing reading: 1139
* 	Passing math: 1094

Next, I calculated the percentage of 10th to 12th graders who passed reading, math and the overall passing percentage by excluding the 9th grades data as seen below 

Next to calculate the top 5 and bottom 5 I replaced the new data from Thomas High School in the per_school_summary_df by using the loc function and used ascending=False.head(5) to find the top five schools and ascending=True.head(5) to find the bottom five schools.
### The Average math score and reading for each grade level from each school
I calculated the average math and reading score for each grade level with the new total student count and by creating a series of scores by grade level. 


![test](./Images/Screenshot_19.png)

![test](./Images/Screenshot_20.png)

![test](./Images/Screenshot_21.png)
### Results Based on School Spend
![test](./Images/Screenshot_22.png)

![test](./Images/Screenshot_23.png)

### Results Based on Student Spend
![test](./Images/Screenshot_24.png)

![test](./Images/Screenshot_25.png)

![test](./Images/Screenshot_26.png)

### Results Based on School Size
![test](./Images/Screenshot_27.png)
### Results Based on School Type
![test](./Images/Screenshot_28.png)
## Results
### How is the district summary affected?
* Original Data to After data clean up: Average Math Score 79.0 to 78.9, Average Reading Score stayed the same, % Passing Math went from 75 to 74, % passing reading went from 86 to 85, % Overall Passing 64 to 65 How is the school summary affected?
*Thomas High School overall passing percent went from 90.95% down to 65.08% after removing 9th grades testing results. Going from placing 2nd to 8th How does replacing the ninth graders math and reading scores affect Thomas High Schools performance relative to the other schools?
* Thomas High School % passing math went from 93.27% down to 66.91% and their % passing reading went from 97.31% (which was 2nd best among all other schools) down to 69.66% How does replacing the ninth-grade scores affect the following?
* Math and reading score by grade: Math grade for 9th graders went from 80.34% down to 80.12% and reading did not change much. (?)
* Scores by school spending: Thomas High school was in the $630 to $644 spending range and was one of four high schools in that range, their % passing math was higher than the average prior to omitting the 9th grade test results and so reduced the averages for schools in that range when the test results dropped from 90.95% down to 65.08%
* Scores by school type: Thomas High school, as it is a charter school, negatively affected the passing math percentage and passing reading percentage
* % Passing math went from 73% down to 67%
* % Passing reading went from 84% down to 77%
* % Overall went from 63% down to 56%
* Scores by school size:
* Thomas High School is in the 1000 to 2000 range
* % Passing math went from 94% down to 88%
* % Passing reading went from 97% down to 91%
* % Overall went from 91% down to 85%
## Summary
Overall, replacing all of Thomas High Schools 9th grade math and reading test results with NaN has negatively affected several data points; Thomas High Schools rankings for the overall percentage of passing students dropped from 2nd best to 8th worst. In addition, their malpractice negatively affected the ratings for charter schools and school sizes in the range of 1000 to 2000 kids.