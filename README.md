## 📝 A. Analyzing Customer Churn in Power BI
### I. Case Study Description
For subscription-based businesses, reducing customer churn is a top priority. In this Power BI case study, you'll investigate a dataset from an example telecom company called Databel and analyze their churn rates. Analyzing churn doesn’t just mean knowing what the churn rate is: it’s also about figuring out why customers are churning at the rate they are, and how to reduce churn. You'll answer these questions by creating measures and calculated columns, while simultaneously creating eye-catching report pages.

### II. Dataset
#### Customer Status

| Field          | Description                                      |
| -------------- | ------------------------------------------------ |
| Customer ID    | The unique ID that identifies a customer         |
| Churn Label    | Contains "Yes" or "No" to indicate churn status   |
| Churn Reason   | The reason why the customer ended the contract    |
| Churn Category | Groups multiple churn reasons for analysis       |

#### Demographics

| Field        | Description                                       |
| ------------ | ------------------------------------------------- |
| Gender       | The gender of the customer (Male/Female/Prefer not to say) |
| Under 30     | Indicates if the customer is under 30 (Yes/No)    |
| Senior       | Indicates if the customer is 65 or above (Yes/No) |
| Age          | The age of the customer                            |

#### Contract Information

| Field                  | Description                                          |
| ---------------------  | ---------------------------------------------------- |
| Contract Type          | Contains "Month-to-Month", "One Year" or "Two Year"  |
| Payment Method         | Preferred payment method of the customer             |
| State                  | The code of the state where the customer lives       |
| Phone Number           | Phone number of the customer                         |
| Group                  | Indicates if the customer is part of a group contract (Yes/No) |
| Number of Customers in Group | Number of customers part of the group          |

#### Subscription Types & Charges

| Field                     | Description                                           |
| ------------------------- | ----------------------------------------------------- |
| Account Length            | The number of months the customer has been with Databel |
| Local Calls               | Amount of local (within the US) calls from the customer |
| Intl Calls                | Amount of international (outside the US) calls from the customer |
| Intl Mins                 | The number of minutes spent calling internationally. Intl Active: Indicates if the customer called internationally with a "Yes" or "No" |
| Intl Plan                 | Indicates if the customer has a premium plan to call internationally for free with "Yes" or "No. This premium is reflected in the amount of the monthly charge. |
| Extra Intl Charges        | Contains the extra charges for international calls for customers who are not on an international plan |
| Customer Service Calls    | The number of calls made to customer service           |
| Avg Monthly GB Download   | Contains the average monthly download volume in gigabytes |
| Unlimited Data Plan       | Indicates if the customer has free unlimited download capacity with "Yes" or "No". This premium is reflected in the amount of the monthly charge |
| Extra Data Charges        | Contains the extra charges for data downloads for customers who are not on an unlimited plan |
| Monthly Charges           | Average of all Monthly Charges to the customer         |
| Total Charges             | Sum of all monthly charges                             |

### III. Data analysis flow in Power BI
#### 1. Data Check
+ Check for duplicate or missing values
+ Do a sense check with other internal data sources
#### 2. Explore Data
+ Ask yourself the right questions
+ Build your first visualizations
#### 3. Analyze & Visualize Data
+ Choose the right visualization to convey a message
+ Perform more advanced analysis
#### 4. Dashboarding
+ Combine visualizations in one or more dashboards
#### 5. Communicate Insights
+ Communicate your insights to stakeholders
### IV. The Problem
#### 1. Solving customer churn
+ A fictitious dataset about churn from a Telecom provider (Databel)
+ Your task: discover why customers are churning
#### 2. Defining churn
The churn rate, also known as the rate of attrition or customer churn, is the rate at which customers stop doing business with an entity.
+ Leaky bucket problem
+ Keeping customers is easier than getting new customers
+ Reducing churn is a priority for many companies

### V. Insights discovered so far
#### 1. The churn rate for Databel is ~27%.
#### 2. ~45% of the reasons why customers churn is related to competitors.
#### 3. The churn rate in California is abnormally high (>60%).

## 📝 B. HR Analytics in Power BI
### I. Case Study Description
In this Power BI case study, you will be exploring a dataset for a fictitious software company called Atlas Labs. This course focuses on helping you import, analyze and visualize Human Resources data in Power BI. Building on your existing knowledge of the platform, you'll learn how to effectively work with Power BI using example data.

You’ll carry out exploratory data analysis and will use DAX to help build powerful visualizations. You’ll finish your analysis by diving deeper into attrition and what factors impact attrition. This analysis will help the organization determine what action they will need to take to retain more employees.

We’ll finalize the case study by making design changes to our report that provides a clean, branded design.

### II. Dataset
#### Performance

| Field                               | Description                                                | Datatype |
| ----------------------------------- | ---------------------------------------------------------- | -------- |
| PerformanceID                       | A unique ID that identifies an individual performance review | text     |
| EmployeeID                          | A unique ID that identifies an employee, connects to DimEmployee | text     |
| ReviewDate                          | Date an employee’s review took place                         | date     |
| EnvironmentSatisfaction             | Rating for employees' satisfaction with their environment, connects to DimSatisfiedLevel | number   |
| JobSatisfaction                     | Rating for employees' satisfaction with their job role, connects to DimSatisfiedLevel | number   |
| RelationshipSatisfaction            | Rating for employees' satisfaction with their relationships at work, connects to DimSatisfiedLevel | number   |
| WorkLifeBalance                     | Rating for employees' satisfaction with their work-life balance, connects to DimSatisfiedLevel | number   |
| SelfRating                          | Rating for employees' performance based on their own view, connects to DimRatingLevel | number   |
| ManagerRating                       | Rating for employees' performance based on their manager’s view, connects to DimRatingLevel | number   |
| TrainingOpportunitiesWithinYear     | Number of training opportunities offered in the last 12 months | number   |
| TrainingOpportunitiesTaken           | Number of training opportunities taken                       | number   |

#### Employee

| Field                   | Description                                                | Datatype |
| ----------------------- | ---------------------------------------------------------- | -------- |
| EmployeeID              | A unique ID that identifies an employee                     | text     |
| FirstName               | First name of an employee                                   | text     |
| LastName                | Last name of an employee                                    | text     |
| Gender                  | Self-defined employee gender identity                       | text     |
| Age                     | Current age of an employee                                  | number   |
| BusinessTravel          | Frequency of business travel: Frequent Traveller, Some Travel, and No Travel | text     |
| Department              | Department an employee works in: Technology, HR, and Sales  | text     |
| DistanceFromHome        | Kilometer distance between an employee’s home and their office | number   |
| State                   | State where the employee lives                              | text     |
| Ethnicity               | Self-defined employee ethnicity                             | text     |
| Education               | Education level for employees, connects to DimEducationLevel | number   |
| EducationField          | Employee field of study                                     | text     |
| Job Role                | Current/latest employee job role                             | text     |
| MaritalStatus           | Current/latest employee marital status                      | text     |
| Salary                  | Current/latest employee salary                               | number   |
| StockOptionLevel        | The banding level for stock options that the employee has    | number   |
| Overtime                | "Yes" or "No" to indicate whether an employee is expected to work overtime in their role | text     |
| HireDate                | Date the employee joined the company                         | date     |
| Attrition               | "Yes" or "No" to indicate whether an employee has left the organization | text     |
| YearsAtCompany          | Number of years since the employee joined the organization   | number   |
| YearsInMostRecentRole   | Number of years the employee has been in their most recent role | number   |
| YearsSinceLastPromotion | Number of years since the employee last got promoted         | number   |
| YearsWithCurrManager    | Number of years the employee has been with their current manager | number   |

#### Satisfied Level

| Field                               | Description                                                | Datatype |
| ----------------------------------- | ---------------------------------------------------------- | -------- |
| SatisfactionID                      | A unique ID that connects to EnvironmentSatisfaction, JobSatisfaction, RelationshipSatisfaction, and Work-Life Balance in FactPerformanceRating | text     |
| SatisfactionLevel                   | Provides meaning to the satisfaction level: Very Satisfied, Satisfied, Neutral, Dissatisfied, and Very Dissatisfied | number   |
| SatisfactionText                    | Text representation of the satisfaction level               | text     |

#### Rating Level

| Field                               | Description                                                | Datatype |
| ----------------------------------- | ---------------------------------------------------------- | -------- |
| RatingID                            | A unique ID that connects to SelfRating and ManagerRating in FactPerformanceRating | text     |
| RatingLevel                         | Provides meaning to the rating level: Above and Beyond, Exceeds Expectation, Meets Expectation, Needs Improvement, and Unacceptable | number   |
| RatingText                          | Text representation of the rating level                      | text     |

#### Education Level

| Field                               | Description                                                | Datatype |
| ----------------------------------- | ---------------------------------------------------------- | -------- |
| EducationLevelID                    | A unique ID that connects to Education in DimEmployee      | text     |
| EducationLevel                      | Provides meaning to the education level: Doctorate, Masters, Bachelors, High School, and No Formal Qualifications | number   |
| EducationText                       | Text representation of the education level                 | text     |



### III. Case study goals
+ Primary goal: Monitor key HR metrics on employees
+ Secondary goal: Understand what factors impact attrition

### IV. Key insights uncovered
#### 1. Atlas Labs has employed over 1,470 people.
#### 2. Atlas Labs currently employs over 1,200 people.
#### 3. The largest department by far is Technology.
#### 4. The attrition rate for employees leaving the organization is 16%
#### 5. Majority of employees are between 20-29 years old.
#### 6. Currently, Atlas Labs employ 2.7% more women than men.
#### 7. Non-binary make up 8.5% of total employees.
#### 8. White have the highest average salary
#### 9. 'Mixed or multiple ethnic groups' have one of the lowest average salaries.


