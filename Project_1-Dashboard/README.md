# Excel Salary Dashboard

**Data Jobs Dataset**

The dataset used for this project contains real-world data science job information from 2023. The dataset provides a foundation for analyzing data using Excel. It includes detailed information on: **Job titles**, **Salaries**, **Locations**, **skills**
 
  <img width="800" height="333" alt="1_Salary_Dashboard_Final_Dashboard" src="https://github.com/user-attachments/assets/19b98363-3063-44c0-a9d5-ea185d542191" />
  
**Excel Skills Used**

The following Excel skills were utilized for analysis: 

-📉 Charts
 
-🧮 Formulas and Functions

-❎ Data Validation

**Dashboard Build**
## Charts

### Data Science Job Salaries - Bar Chart
<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/23aaa472-b495-4fa1-8de4-0910928f82e1" />


 **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
 
 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
 
 **Data Organization:** Sorted job titles by descending salary for improved readability.
 
 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
 
### Country Median Salaries - Map Chart
<img width="564" height="395" alt="1_Salary_Dashboard_Chart2" src="https://github.com/user-attachments/assets/f07dc0a1-6d73-4780-b937-b76981df0259" />

 **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
 
 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
 
 **Data Representation:** Plotted median salary for each country with available data.
 
 **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
 
 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.
 
## Formulas and Functions
 
### Median Salary by Job Titles
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
 
 **Array Formula:** Utilizes MEDIAN() function with nested IF() statement to analyze an array.
 
 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
 
 **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

### Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

 **Unique List Generation:** This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
 
 **Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

 Dashboard Implementation:

### Data Validation
 **Filtered List**
<img width="624" height="602" alt="1_Salary_Dashboard_Data_Validation" src="https://github.com/user-attachments/assets/4a8acace-c3d2-4894-8c5d-f1ff46d17e28" />


 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
 
-User input is restricted to predefined, validated schedule types

-Incorrect or inconsistent entries are prevented

-Overall usability of the dashboard is enhanced


### Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
