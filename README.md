# Cleaning-Exploring-the-Ask-a-Manager-Survey-Dataset
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

## Project Description: 
Using the dataset titled 'Ask a Manager Salary Survey 2021 (Responses),' I performed data transformation and exploratory analysis with Python. Additionally, I utilized Power BI for advanced visualization, uncovering insights on how salary varies across age groups, work experience, and industry.

## Tools: 
+ Python (Cleaning and exploratory analysis)

+ Power BI (Data Visualization)

# Key Question(S) for Analysis:
+ How does age group influences salary?
+ Which industry pay the most?
+ Which Educational Qualification earns the most salary?
+ What is the most popular industry?
+ Which Country gives the most monetary_bonuses?
+ How does gender influences salary?
+ How do factors like race and education level correlate with salary?
+ How salaries compare for the same role in different location?
+ How do work year experience influences salary?
+ Which country has more work year experience?


## Data Wrangling:
+ Handling Encoding Errors: The first hurdle was an encoding issue. I resolved it by using the latin-1 encoding to ensure proper reading of the data.
+ Renaming Irregular Columns: The column names were inconsistent, so I standardized them using Python’s rename() function with a dictionary argument. Additionally, I applied the lower() function to make them lowercase and strip() to remove trailing spaces.
+ Exploring Categories: Using value_counts(), I examined the distribution of categories in variables like “Country” and “Job title.” This step helped me identify inconsistencies, such as duplicate entries (e.g., “United States”, “US”. “USA”, “UK”, “United Kingdom”, “United kinkdom”), and regroup them for clarity to the standard name.
+ In the race column, I regrouped the colum to multiracial and moni racial for east readability.
+ I changed the salary column from string to float using replace function to remove the commas. Then I converted all the salary to USD. Then I filled in null values before converting to integer.
+ The monetary compensation, I converted it to USD using the current exchange rate, using lamba function.
+ I recategorized my work_year_exeperience column for easy understanding eg 41yearsormore to 41years+.
+ I dropped unnecessary columns such as other_job_ context which was not needed for my analysis.
