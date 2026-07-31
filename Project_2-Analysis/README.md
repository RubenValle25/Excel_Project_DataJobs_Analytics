# 📊 Data Science Job Market Analysis (Excel)

## 📌 Questions Analyzed

This project explores the 2023 data science job market by answering the following questions:

- 💼 Do more skills lead to higher salaries?
- 🌎 How do salaries compare across different regions?
- 🛠️ What are the most in-demand skills for data professionals?
- 💰 What is the median salary for the top 10 skills?

---

# 🧰 Excel Skills Used

This project was completed entirely in Microsoft Excel using the following tools:

- Power Query (ETL)
- PivotTables
- Pivot Charts
- Power Pivot
- DAX (Data Analysis Expressions)

---

# 📂 Dataset

The dataset contains real-world data science job postings from **2023**.

It includes information such as:

- Job titles
- Annual salaries
- Job locations
- Required skills

---

# 📈 Analysis

## 1. Do More Skills Lead to Higher Salaries?

### 🛠️ Excel Skill Used
**Power Query (ETL)**

### Extract

Using Power Query, I imported the original dataset and created two separate queries:

- **data_jobs_all** — Job posting information
- **data_job_skills** — Skills associated with each job ID

### Transform

The data was cleaned by:

- Changing data types
- Removing unnecessary columns
- Cleaning text values
- Removing extra whitespace

### Load

Both transformed queries were loaded into Excel for analysis.

### 📊 Insights

- There is a positive relationship between the number of requested skills and the median salary.
- Roles such as **Senior Data Engineer** and **Data Scientist** require more skills and offer significantly higher salaries.
- Positions requiring fewer specialized skills, such as **Business Analyst**, generally have lower salaries.

### 💡 Key Takeaway

Developing multiple technical skills can significantly improve earning potential in the data industry.

---

# 🌎 2. What Are the Salaries for Data Jobs in Different Regions?

### 🛠️ Excel Skills Used

- PivotTables
- DAX
- Power Pivot

### PivotTable

A PivotTable was created using the Power Pivot Data Model.

Configuration:

- **Rows:** `job_title_short`
- **Values:** `salary_year_avg`

### DAX Measures

Median salary for all jobs:

```excel
Median Salary :=
MEDIAN(data_jobs_all[salary_year_avg])
```

Median salary for United States jobs:

```excel
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)
```

### 📊 Insights

- Senior Data Engineers and Data Scientists have the highest median salaries both inside and outside the United States.
- The salary gap between US and international positions is largest for highly technical roles.

### 💡 Key Takeaway

Geographic location has a significant impact on salary, making location an important consideration during job searches and salary negotiations.

---

# 🛠️ 3. What Are the Top Skills of Data Professionals?

### 🛠️ Excel Skill Used

**Power Pivot**

### Data Model

A data model was created by linking:

- `data_jobs_all`
- `data_job_skills`

using the **job_id** field.

Power Pivot was then used to build relationships and create measures.

### 📊 Insights

- SQL and Python are the most requested technical skills.
- Cloud technologies such as AWS and Azure are becoming increasingly valuable.

### 💡 Key Takeaway

Mastering SQL, Python, and cloud technologies provides a strong competitive advantage in today's data job market.

---

# 💰 4. What Is the Pay for the Top 10 Skills?

### 🛠️ Excel Skill Used

**Pivot Charts**

### Visualization

A Combo PivotChart was created using:

- **Primary Axis:** Median Salary (Clustered Columns)
- **Secondary Axis:** Skill Likelihood (%) (Line with Markers)

Formatting improvements included:

- Custom chart title
- Axis titles
- Diamond markers
- Simplified chart styling

### 📊 Insights

- Python, SQL, and Oracle are associated with the highest median salaries.
- Microsoft Office skills (Word and PowerPoint) have the lowest salary impact and demand among technical positions.

### 💡 Key Takeaway

Investing time in learning technical programming and database skills provides substantially higher earning potential than general productivity software.

---

# 📌 Conclusion

This project demonstrates how Excel can be used as a powerful data analysis tool to explore real-world labor market trends.

Using **Power Query**, **Power Pivot**, **PivotTables**, **DAX**, and **Pivot Charts**, I analyzed thousands of job postings to identify:

- The relationship between skills and salary
- Regional salary differences
- The most valuable technical skills
- Salary trends across the most in-demand technologies

The analysis highlights that professionals who develop specialized technical skills—particularly **Python**, **SQL**, and **cloud technologies**—are more likely to qualify for higher-paying opportunities in the data industry.

---

# 🚀 Tools Used

- Microsoft Excel
- Power Query
- Power Pivot
- PivotTables
- Pivot Charts
- DAX

---

# 📁 Project Files

- 📄 Excel Workbook
- 📊 Dashboard
- 📈 Pivot Tables
- 📉 Charts
- 📂 Dataset
