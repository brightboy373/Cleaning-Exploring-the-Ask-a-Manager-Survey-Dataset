# Cleaning and Exploring the Ask a Manager Survey Dataset  
# Table of Contents  

1. [Project Overview](#project-overview)  
2. [Dataset Description](#dataset-description)
3. [Tools](#tools)
4. [Key Question(s) for Analysis](#_Key(S)-for-analysis)  
5. [Methods](#methods)    
6. [Insights](#insights)  
7. [Recommendations](#recommendations)  
8. [Visualizations](#visualizations)    
9. [Conclusion](#conclusion)

## Project Description: 
Using the dataset titled 'Ask a Manager Salary Survey 2021 (Responses),' I performed data transformation and exploratory analysis with Python. Additionally, I utilized Power BI for advanced visualization, uncovering insights on how salary varies across age groups, work experience, and industry.

## Dataset Description
The dataset, titled "Ask a Manager Salary Survey 2021 (Responses)," is a real-world collection of survey data featuring 17 variables focused on salaries and workplace demographics. Sourced from AskAManager.org, the data primarily reflects responses from the United States, with additional inputs from international participants.

+ 'Gender' tells us the gender of workers.
+ 'Industry' tells us the industry of the workers.
+ 'Age Groups' tells us the age group of the workers.
+ 'Work Year Experience' tells us the year of experince of the workers.
+ 'Location (Country, State, City)' tells us the location of workers.
+ 'Salary' tells us the Annual salary of workers.
+ 'Education' tells us the highest Education qualifications of workers.
+ 'Monetary compensation' tells us the bonuses or overtime in an average year.
+ 'Race' tells us the race of the workers.
+ 'Job Title' tells us the job title of the workers.
### Dataset
<a href= "https://github.com/brightboy373/Cleaning-Exploring-the-Ask-a-Manager-Survey-Dataset/blob/main/Ask%20A%20Manager%20Salary%20Survey%202021.csv">Ask a Manager Survey 2021(Respones)</a>

## Tools: 
+ Python, Jupyter notebook (Cleaning and exploratory analysis)
+ Libraries: Pandas, Numpy, matplotlib and, Seaborn.

+ Power BI (Data Visualization)

## Key Question(s) for Analysis:
+ How does age group influences salary?
+ Which industry pay the most?
+ Which Educational Qualification earns the most salary?
+ What is the most popular industry?
+ How does gender vary by educational qualification?
+ How do work year experience influences salary?

 ## Methods
### Data Wrangling:
+ Imported Libraries needed like  `seaborn`,  `pandas`,  `numpy`, and  `matplotlib`.
+ Handling Encoding Errors: The first hurdle was an encoding issue. I resolved it by using the latin-1 encoding to ensure proper reading of the data.
+ Renaming Irregular Columns: The column names were inconsistent, so I standardized them using Python’s  `rename()` function with a dictionary argument. Additionally, I applied the lower() function to make them lowercase and  `strip()` to remove trailing spaces.
+ Exploring Categories: Using  `value_counts()`, I examined the distribution of categories in variables like “Country” and “Job title.” This step helped me identify inconsistencies, such as duplicate entries (e.g., “United States”, “US”. “USA”, “UK”, “United Kingdom”, “United kinkdom”), and regroup them for clarity to the standard name.
+ Defined and handled the inconsistent data type assigned to my columns by assessing the data programmatically using the  `info()` function.
+ In the race column, I regrouped the column to multiracial, Biracial, and moniracial for easy readability. Categories with one race was named monoracial, Categories with two races was named Biracial, and categories with more than two races was renamed multiracial.
+ Changed the salary column from string to float using replace function to remove the commas. Then I converted all the salary to USD using the lambda function. Then I filled in null values with the mean before converting the data type from string to integer. I handled outlier in our salary column by calculating the interquartile range.
+ The monetary compensation, I converted it to USD using the current exchange rate, using lamba function. Then I also filled in null values with the mean before converting to integer.
+ Recategorized some rows in my work_year_exeperience column for easy understanding eg 41yearsormore to 41years+ using the  `replace` function.
+ I dropped unnecessary columns in my datafrom such as other_job_ context which was not needed for my analysis.

<a href= "https://github.com/brightboy373/Cleaning-and-Exploring-the-Ask-a-Manager-Survey-Dataset/blob/main/Survey%20data%20Analysis%20Project.ipynb">Data Cleaning and Exploratory Analysis</a>

### Dashboard and Visualization
After transforming my data with python, I created dashboard with Power BI to uncover insight into average salary by education, age group, work experience, and Top 5 industries by salary.

<img width="671" alt="Salary Trend dashboard" src="https://github.com/user-attachments/assets/921ea5c4-9de7-47e7-b90e-bf454f72cd7d" />

## Insights

+ The survey datasets highlight a clear relationship between salary, age group, and work experience. The 45-54 age group earns the highest average salary, reflecting their peak earning potential, while the under 18 age group has the lowest, likely due to limited work experience and entry-level roles. Similarly, work experience significantly impacts earnings, with those having 21-30 years of experience earning the most, followed by 31-40 years of experience. Interestingly, salary is likely to be influenced more by work experience than age. The slight decline in salary for the latter group may indicate that earnings begin to plateau or decrease as individuals approach retirement.

+ Individuals with Professional degrees have the highest average salaries, closely followed by those with PhDs, emphasizing the financial benefits of advanced education. In contrast, individuals with only a high school education earn the least on average, reflecting the influence of educational attainment on earning potential. This trend highlights the vital role of higher education in unlocking better-paying opportunities, highlighting its value in career advancement and income growth.

+ There is an imbalance in gender distribution in education levels, particularly in advanced degrees like PhDs and professional degrees, where men are more represented. However, women lead in the Master's degree category, suggesting their pursuit of higher education. The low representation of non-binary individuals and undisclosed gender groups across all education levels highlighting the need for inclusivity and opportunities for these groups to bridge educational gaps.

+ The science and technology sector offers the highest salary opportunities, making it the fastest growing industry in this era.

## Recommendation
+ Education and Salary: Individuals with higher educational qualifications, such as Professional degrees and PhDs, earn more on average. Encouraging and supporting individuals to pursue advanced education could improve earning potential. This is especially relevant for industries requiring specialized skills.

+ Work Experience and Salary: Salaries tend to peak between 21–30 years of work experience, suggesting the importance of consistent career progression and skill development. Employers should consider implementing mentorship and growth opportunities for employees to help them maximize their earning potential within this range.

+ Age and Salary: Salaries increase steadily across age groups, peaking around 45–54 years. Employers might consider leveraging the expertise of this group while also investing in younger employees to ensure a skilled workforce over time.

+ Industry Trends: The science and technology sector offers the highest salary opportunities, followed by education and NGOs. Individuals should be guided toward industries with higher earning potentials based on their skills and interests. Policymakers and educators might also emphasize STEM (Science, Technology, Engineering, and Math) education to prepare individuals for these lucrative fields.

+ Gender Representation: Efforts should be made to address gender gaps in high-paying industries and leadership roles to ensure equity and diversity. Programs to empower underrepresented groups to access better education and career opportunities would contribute to societal balance.

## Conclusion
This project involved a comprehensive exploration of the Ask a Manager Survey Dataset, focusing on cleaning, analyzing, and deriving actionable insights from the data. Through Exploratory Data Analysis (EDA), I uncovered key trends and patterns related to demographics, salary distributions, and job satisfaction across various industries, job titles, and experience levels.





